---
title: GitHub (Editing)
---

[GitHub](https://github.com/) is a web-based platform for hosting files in repositories, collaborating on projects, and tracking changes over time. It uses Git, an open-source version control system, to manage and record those changes.

We use GitHub to organize course materials, manage user access, facilitate conversations, and track issues for all content and contributors associated with our courses and programs. This resource contains what you need to know about how we use GitHub.

If you don't already have a GitHub account you’d like to use, you'll need to create one by [signing up](https://github.com/signup).

---

## Organizations

[Organizations](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations) are shared accounts where we can collaborate across many projects at once. Our organizations are:

- [ccsf-math](https://github.com/orgs/ccsf-math): For all non-course-specific projects under the Mathematics Department.
- [ccsf-math-108](https://github.com/orgs/ccsf-math-108): For all MATH 108 materials and staff.

---

## Repositories

[Repositories](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories) contain all of the code, files, and each file’s revision history. We can discuss and manage our work within the repository. Here are the main repositories for **Fall 2025**:

- [ccsf-math/jupyterhub](https://github.com/ccsf-math/jupyterhub/): Public repository containing the configuration files for the CCSF JupyterHub.
- [ccsf-math-108/materials](https://github.com/ccsf-math-108/materials): Private repository for all MATH 108 materials. This repository should be limited to instructors and editors.
- [ccsf-math-108/materials-fa25-staff](https://github.com/ccsf-math-108/materials-fa25-staff): Private repository for sharing all MATH 108 materials and conversations with relevant individuals for Fall 2025.
- [ccsf-math-108/materials-fa25](https://github.com/ccsf-math-108/materials-fa25): Public repository for sharing all MATH 108 materials and conversations for Fall 2025.

The content within the `materials-fa25-staff` and `materials-fa25` repositories is derived from the `materials` repository.

---

## Projects

We use [GitHub Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects) to organize the release and development of course materials each semester and to host conversations about updates, clarifications, and issues.

**Note:** GitHub Project visibility depends on repository permissions. A person who does not have access to a private repository cannot see its linked issues in the Project, even if the Project itself is visible to them.

---

### Initial Project Setup

1. **Create the semester project**  
   - Go to [ccsf-math-108 Projects](https://github.com/orgs/ccsf-math-108/projects) and create a project named "`SEMESTER` `YEAR` Materials" (e.g., "Fall 2025 Materials").
   - This project will hold all items for the semester.  
   - Adjust visibility so full-access members can see everything, while others only see what their repository permissions allow.

2. **Add fields**  
   Create the following single-select fields in the Project:  
   - **Milestone** (linked to GitHub Milestones)  
   - **Module** – one option per Canvas module (e.g., `Week 01: September 1 - September 7`) plus `No Module`  
   - **Status** – `Pending`, `Editing`, `Reviewing`, `Ready`  
   - **Released to Student GitHub** – `True`, `False`, `Not Relevant`  
   - **Item** – `Lecture`, `Discussion Worksheet`, `Lab`, `Homework`, `Project`, `Exam`, `Practice Exam`, `Survey`, `Reference Material`, `Guided Learning Activity`, `Textbook Quiz`, `Textbook Content`, `Overview Page`, `Issue`

3. **Group and customize views**  
   - Group items by **Milestone**.  
   - Rename the primary layout view to **Weekly Release** and save it.

4. **Create milestones**  
   - In each relevant repository, create milestones for each release.  
   - Example: **Week 01 Release** due August 15, 2025, in `materials-fa25-staff`.

5. **Add issues for all course items**  
   - Each item should be an issue in the repository where its source files live (private if needed).  
   - Assign appropriate `Milestone`, `Module`, `Item`, `Released to Student GitHub`, and set `Status` to `Pending`.  
   - Add an `Assignees` value if known.  
   - In the issue body, link to development, sample solution, and student versions and note changes needed before review.

---

### Ongoing Maintenance

1. **Editing** – When starting work on an item, set `Status` to `Editing`.
2. **Reviewing** – Once ready for review, set `Status` to `Reviewing`.
3. **Change requests** – If revisions are requested, document them in the issue, then set `Status` back to `Editing`.
4. **Commit references** – When pushing edits, reference the issue in the commit message or comment.
5. **Final approval** – After faculty/staff approve changes, set `Status` to `Ready`. 
