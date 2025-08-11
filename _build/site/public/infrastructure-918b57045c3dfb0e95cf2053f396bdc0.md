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

### Authentication Flow
```mermaid
flowchart TD
    A[User accesses JupyterHub] --> B[Redirect to CI Login]
    B --> C[User selects Google as Identity Provider]
    C --> D[Redirect to Google Login]
    D --> E[User logs in with Google]
    E --> F[Google returns OAuth token to CI Login]
    F --> G[CI Login returns assertion to JupyterHub]
    G --> H[JupyterHub authenticates user]
    H --> I[Spawn user server]
    I --> J[User lands on JupyterHub interface]
    J --> K[User interacts with JupyterHub]
    
    subgraph Google Services
        E
        F
    end

    subgraph CI Login
        C
        D
        G
    end

    subgraph JupyterHub
        B
        H
        I
        J
        K
    end
```

### `nbgitpuller` Link Flow

```mermaid
flowchart TD;
    A[User clicks nbgitpuller link] --> B[nbgitpuller parses URL and identifies repo]
    B --> C[nbgitpuller fetches repository content from GitHub]
    C --> D[nbgitpuller pulls files into user's Jupyter environment]

    subgraph GitHub
        C
    end

    subgraph Canvas/Website
        A
    end

    subgraph JupyterHub
        B
        D
    end

```