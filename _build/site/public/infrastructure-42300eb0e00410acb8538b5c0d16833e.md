# Infrastructure

## Responsibility
The Data Science coordinator maintains the technology needed to run MATH 108.

## Overview
We utilize various technologies to provide students, faculty, and staff with interactive notebooks for lectures and assignments. A [JupyterHub](https://jupyter.org/hub), hosted by [Cloudbank](https://www.cloudbank.org/) and [2i2c](https://2i2c.org/), is the central piece of our technology that is used for authenticating users, synchronizing course materials, 


The Data Science coordinator should work with {term}`Sean Morris` and {term}`Shawn Wiggins` to make sure the JupyterHub is set up before the start of the semester and continue to be in communication with them about updates and issues.

## MATH 108 Technology

### Authentication Flow
```mermaid
flowchart TD
    A[User accesses JupyterHub] --> B[Redirect to CILogon]
    B --> C[User selects Google as Identity Provider]
    C --> D[Redirect to Google Login]
    D --> E[User logs in with Google]
    E --> F[Google returns OAuth token to CILogon]
    F --> G[CILogon returns assertion to JupyterHub]
    G --> H[JupyterHub authenticates user]
    H --> I[Spawn user server]
    I --> J[User lands on JupyterHub interface]
    J --> K[User interacts with JupyterHub]
    
    subgraph Google Services
        E
        F
    end

    subgraph CILogon
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