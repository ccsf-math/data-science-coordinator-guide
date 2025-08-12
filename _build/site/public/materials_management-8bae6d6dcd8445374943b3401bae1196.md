---
title: Materials Management (Editing)
---

For context, this page is assuming that you are working with our JupyterHub. With a few modifications, this guide will support working offline from your own computer. Additionally, this guide will reference the Fall 2025. Make appropriate updates for other semesters.

---

## Clone Repositories

For the semester you are working on, you want to make sure that you have a clone of the `materials`, `materials-fa25-staff`, and `materials-fa25` repositories. 

Assuming that you are working from the root directory of our hub, you should have the following structure:

```{code-block} text
/
├── materials/
├── materials-fa25-staff/
└── materials-fa25/
```

If any of these folders are missing (e.g. `materials-fa25`), you can create them with the contents from GitHub by running the following in a terminal:

``` bash
git clone https://github.com/ccsf-math-108/materials-fa25.git
```

--- 

## Pull First

Before you begin making changes, first you want to pull content from GitHub so you have the most update to date version of the materials. You'll need to do this for each repository. That means you should navigate to each folder and run the `git pull` command. For example, if you want to modify content in `materials`, then you'll run the following in a terminal:

``` bash
cd ~/materials
git pull
```

---

## Working with Jupyter Notebooks

---

### Editing a Notebook
As an editor, you should only edit the main notebooks found in the [`materials` repository]. Never edit the `autograder` or `student` version, since this will likely cause issues.

1. Open or create the notebook you want to edit in the [`materials` repository].
1. Make the changes you want to make.
1. Shutdown the notebook's kernel.
1. Save the notebook.
1. Run the `generate_dist_files` script.
1. Stage the content you want to commit to GitHub.
1. Create the commit with an update message.
1. Push the commit to GitHub.

---

#### Common Example

If you edited the file `~/materials/lec/lec01/lec01.ipynb` and you want to share your edits of the content in `~/materials/lec/lec01` back to GitHub, then you would run the following in a terminal:

``` bash
git pull
git add ~/materials/lec/lec01/*
git commit -m "A note about your changes"
git push
```
    
---

#### Distributing Content to Other Repositories
The `generate_dist_files` script creates the `autograder` and `student` versions of each notebook and stores them in the `materials/dist` folder.

``` mermaid
flowchart TD;
    A["Main Notebook"] --> B([generate_dist_files])
    B --> C["Autograder version of notebook"]
    B --> D["Student version of notebook"]
```

