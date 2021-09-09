# Development process

An agile methodology based on [Kanban workflow](https://en.wikipedia.org/wiki/Kanban_(development)) 
is used in P2P models to produce software. A customized version of the Kanban board
is implemented through Github's [project board feature](https://docs.github.com/en/issues/organizing-your-work-with-project-boards/managing-project-boards/about-project-boards). 
An image of a basic kanban is depicted below.

![img_board](https://docs.github.com/assets/images/help/projects/project-board-basic-kanban-template.png)

The starting points of the process are the definition of milestones and the creation 
of issues (i.e., bugs, todos, feature requests). Issues are created using the 
issue tracking tool available on repositories. It is encouraged to describe issues 
at the maximum possible level of detail, providing backtrace messages of exceptions 
and instructions to reproduce the error in case of bugs or any supporting material 
in the case of new features (see below for the guide to create an issue). To be 
tracked by the management tool, issues should be assigned to one defined
milestone and project.

After creating issues, the team prioritizes the work to be done by moving the
issues to the **`ToDo`** stage in the workflow process. Branches
should be created to isolated the development work, so the developer should create 
a branch from the **`develop branch`** for each issue she is working on. After 
completing the work, a pull request should be created indicating the team about 
changes desired to be included in the develop branch (see below for the guide
to link pull requests to issues). The issue is then moved to the **`Testing`** 
stage in the workflow. After the proposed solution has been tested exhaustively, 
the branch containing the solution is merged into **`develop`**, and the issue is 
moved to the **`Done`** stage.

Issues are included in milestones, and milestones are organized in springs. When
springs are finished, the **`develop branch`** is merged into the **`main branch`**.
A new production-ready release is generated from the **`main branch`** (see below 
on creating releases).

## Interested guidelines

- [Create an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-issues/creating-an-issue)
- [Work with branches](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches)
- [Create a pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
- [Link pull requests to issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-issues/linking-a-pull-request-to-an-issue)
- [Create release](https://docs.github.com/en/github/administering-a-repository/releasing-projects-on-github/managing-releases-in-a-repository#creating-a-release)
