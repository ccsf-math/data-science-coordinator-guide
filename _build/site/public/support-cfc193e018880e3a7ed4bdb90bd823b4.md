# Support

## Responsibility
The Data Science coordinator organizes specific tutoring opportunities for MATH 108 students. Since MATH 108 is such a new course, we usually need to provide additional support for our tutors and establish alternative tutoring opportunities in order to provide a similar level of tutoring for our MATH 108 students that the rest of our students in the Department experience.

## Contacts
- Charles Hutchins: chutchin@ccsf.edu
- Kseniya Usovich: k_usovich@berkeley.edu
- Sean Morris: sean.smorris@berkeley.edu

## Overview
We believe that a key feature of Berkeley's success with DATA 8 was the extensive support system for their students. Every since the beginning of MATH 108, we've tried to build up a support network for the course. 

### Math Lab Tutors

### Data Ambassadors
Through a Learning Grant, we have supported remote tutoring and mentoring via our **Data Ambassadors** program. The program originally featured UC Berkeley students pursuing degrees in Data Science, many of whom were former community college students. These ambassadors provided virtual homework help and mentorship.

Over time, we have expanded the program to include CCSF students as ambassadors and extended participation to students from **Laney College** and **Berkeley City College**.

**Kseniya** has served as the primary organizer of the program. She helps hire ambassadors at Berkeley and coordinates their availability with the needs of each participating college. The **Data Science Coordinator** works with Kseniya to set the mentoring and tutoring schedule, ensure ambassadors have access to relevant materials and sample solutions, and share this information with students, faculty, and staff at CCSF.


## Onboarding Process for Support Staff

To ensure support staff (e.g., Data Ambassadors or Math Lab Tutors) are fully equipped to assist with MATH 108, follow the steps below:

---

### 1. Confirm Access Requirements

Ensure that each support staff member has:

- A GitHub account
- Access to our [JupyterHub](https://your-hub-url)
- Access to the appropriate `materials-xxXX-staff` GitHub repository
- Membership in the relevant GitHub Team:
  - [Data Ambassadors](https://github.com/orgs/ccsf-math-108/teams/data-ambassadors)
  - [Math Lab Tutors](https://github.com/orgs/ccsf-math-108/teams/math-lab-tutors)

> _Purpose: This gives them access to materials, sample solutions, and relevant team discussions._

---

### 2. Google Account Setup

If the staff member **does not** have a `@mail.ccsf.edu` Google account:

- Collect their preferred **Google-based email address** (e.g., a `@berkeley.edu` or `@gmail.com` address)
- Send that email address to **Sean** so it can be added for login access

> _Note: Berkeley-affiliated emails work as they are associated with Google accounts._

---

### 3. GitHub Authentication on JupyterHub

To enable GitHub-based authentication on the JupyterHub:

1. **Invite** the staff member (by GitHub username) to the `ccsf-math-108` GitHub organization  
   - Add them to the appropriate team (typically **Data Ambassadors**)
2. Have them [open a terminal](https://jupyterlab.readthedocs.io/en/latest/user/terminal.html) in the JupyterHub
3. In the terminal, type:
   ```bash
   gh auth login
