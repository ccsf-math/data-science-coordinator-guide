# Infrastructure

## Responsibility
The Data Science coordinator maintains the technology needed to run MATH 108.

## Overview
MATH 108 utilizes various applications from the [Project Jupyter](https://www.jupyter.org) community to provide students with interactive notebooks for lectures and assignments. The Data Science coordinator should work with {term}`Sean Morris` and {term}`Shawn Wiggins` to make sure the JupyterHub is set up before the start of the semester and continue to be in communication with them about updates and issues.

## MATH 108 Technology

```mermaid
sequenceDiagram
    participant User
    participant JupyterHub
    participant GoogleAuth
    participant UserServer
    participant GitHub
    participant nbgitpuller

    User->>JupyterHub: Access JupyterHub URL
    JupyterHub->>GoogleAuth: Redirect for login
    GoogleAuth-->>User: Google Login Page
    User->>GoogleAuth: Submit credentials
    GoogleAuth-->>JupyterHub: Return OAuth token
    JupyterHub->>User: Authenticated, spawn server
    JupyterHub->>UserServer: Start single-user server
    User-->>UserServer: Redirected to notebook interface

    Note over User, UserServer: Authenticated & environment ready

    User->>UserServer: Click nbgitpuller link
    UserServer->>nbgitpuller: Parse link and GitHub repo info
    nbgitpuller->>GitHub: Fetch specified content
    GitHub-->>nbgitpuller: Return notebook files
    nbgitpuller->>UserServer: Pull notebooks into user dir
    UserServer-->>User: Notebooks ready
```

```mermaid
flowchart TD
    A[User clicks nbgitpuller link] --> B[Redirect to User's Server]
    B --> C[nbgitpuller parses URL params]
    C --> D[Clones or pulls from GitHub repo]
    D --> E[Copies/syncs files to user's working directory]
    E --> F[Opens target notebook or path]

```