---
title: GitHub (Editing)
---

[GitHub](https://github.com/) is a web-based platform for hosting files in repositories, collaborating on projects, and tracking changes over time. It uses Git, an open-source version control system, to manage and record those changes.

We use GitHub to organize course materials, manage user access, facilitate conversations, and track issues for all content and contributors associated with our courses and programs. This resource contains what you need to know about how we use GitHub.

If you don't already have a GitHub account you’d like to use, you'll need to create one by [signing up](https://github.com/signup).

---

## Organizations

[Organizations](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations) are shared accounts where we can collaborate across many projects at once. Our organizations are:

- [ccsf-math](https://github.com/orgs/ccsf-math): For all non-course-specific projects under the Mathematics Department
- [ccsf-math-108](https://github.com/orgs/ccsf-math-108): For all MATH 108 materials and staff

---

## Repositories

[Repositories](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories) contain all of the code, files, and each file’s revision history. We can discuss and manage our work within the repository. There are several repositories within our organizations; here are the main repositories for **Fall 2025**:

- [ccsf-math/jupyterhub](https://github.com/ccsf-math/jupyterhub/): Public repository containing the configuration files for the CCSF JupyterHub
- [ccsf-math-108/materials](https://github.com/ccsf-math-108/materials): Private repository for all MATH 108 materials
- [ccsf-math-108/materials-fa25-staff](https://github.com/ccsf-math-108/materials-fa25-staff): Private repository for sharing all MATH 108 materials and conversations with relevant individuals for Fall 2025
- [ccsf-math-108/materials-fa25](https://github.com/ccsf-math-108/materials-fa25): Public repository for sharing all MATH 108 materials and conversations for Fall 2025

The content within the `materials-fa25-staff` and `materials-fa25` repositories is derived from the `materials` repository.

---

## Projects

We use [GitHub Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects) to organize the release and development of course materials each semester and to host conversations about updates, clarifications, and issues.

---

### Project Setup Workflow

Before the start of the semester:

1. Create a [new project](https://github.com/orgs/ccsf-math-108/projects) using the naming scheme "`SEMESTER` `YEAR` Materials" (e.g., "Fall 2025 Materials"). This project will host all the items for the semester, and we can limit the view of the items and details based on the role of the individuals in the organization. This allows those with full access to see all items and conversations, while limiting the view for those who don’t have or need full access.
1. Add the `Milestone` and `Repository` [fields](https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields) to the project.
1. Create a single select field called `Module` with an field option for each Module in Canvas (e.g. `Week 01: September 1 - September 7`) and an field option called `No Module`.
1. Create a single select field called `Status` with the field options `Pending`, `Editing`, `Reviewing`, and `Ready`.
1. Create a single select field called `Released to Student GitHub` with the field options `True`, `False`, and `Not Relevant`.
1. Create a single select field called `Item` with the field options `Lecture`, `Discussion Worksheet`, `Lab`, `Homework`, `Project`, `Exam`, `Practice Exam`, `Survey`, `Reference Material`, `Guided Learning Activity`, `Textbook Quiz`, `Textbook Content`, `Overview Page`, `Issue`.
1. [Rename the project layout view](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/managing-your-views#renaming-a-saved-view) to **Weekly Release**.
1. Save the project layout view.
1. Add an issue to the project for each item from the course materials. (e.g. Create the `Lecture 01: Introduction` issue.) For each issue:
    1. Assign the issue to the relevant field options for `Milestone`, `Module`, `Item`, and `Released to Student GitHub`.
    1. For the field `Status`, assign the issue the option of `Pending`.
    1. If possible, assign the issue an `Assignees` option.
1. [Group the items](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/customizing-the-table-layout#grouping-by-field-values) by `Milestone`.
1. Create [Milestones](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/about-milestones) within each relevant repository. These milestones allow us to group related items so we can focus on what needs to be done for the upcoming release of materials.  
   *Example:* Create a milestone called **Week 01 Release** with a due date of August 15, 2025, in the `materials-fa25-staff` repository.