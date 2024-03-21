# Autograding with GitHub

This document contains step-by-step instructions on creating a system for quick feedback on assignments for CSSSKL 143. Any questions related to implementing, altering, or managing this system, or any feedback on how to improve the system or this guide, should be sent to Cameron Kline-Sharpe (cklinesh@uw.edu) and Dr. Johnny Lin (jwblin@uw.edu).

An FAQ is also available for this guide.

## 0. System Flow
The general workflow for this system is as follows:
* Before assigning the homework, set up the GitHub repositories for your students.
  * Create repositories with the supplied workflows (step 1 below)
  * Edit the supplied tests and skeleton code files to suit your assignment (step 2 below)
* Students will submit their assignments (step 3 below)
* You and/or any graders will look over the test results and the code to see which tests failed and why. You can also make comments directly in the code.

The goal of this system is to make grading work both easier and faster. If you have any suggestions on how to improve the system, let us know!

## 1. Tutorial for Instructors

This tutorial will show you how to set up autograded assignments using two example repositories found in the [fatgoose-uwb](https://github.com/fatgoose-uwb) organization. 

This guide uses code found in the “fatgoose-uwb” organization. You will need to clone the “sprint-base-1” and “sprint-meta” repositories. You will eventually want to create your own set of repositories, so it may be worthwhile to create a GitHub organization for your grading to make organization of your GitHub easier. A tutorial for starting a new organization can be found here.

## Cloning the repositories

1. Create a new public repository in your GitHub organization called "sprint-meta".

2. Bare clone the sprint-base-meta repository from fatgoose-uwb.

   ```bash
   git clone --bare https://github.com/fatgoose-uwb/spring-base-meta.git
   ```

3. Navigate into the repository.

   ```bash
   cd sprint-base-meta.git/
   ```

4. Mirror the local files to your new repository in your organization.

   ```bash
   git push --mirror YOUR_REPOSITORY
   ```

5. Delete the local copy of the fatgoose-uwb repository.

   ```bash
   cd ..
   rm -rf sprint-base-1.git/
   ```

6. Repeat this process for the sprint-base-1 repository in [fatgoose-uwb](https://github.com/fatgoose-uwb).
7. Clone your new repositories.

   ```bash
   git clone https://github.com/YOUR_ORGANIZATION/sprint-meta.git
   git clone https://github.com/YOUR_ORGANIZATION/sprint-1.git
   ```
8. Edit the backref.cfg configuration file under `sprint-1/.github/workflows`. Replace `fatgoose-uwb` with the name of your GitHub organization, and replace `sprint-base-meta` and `sprint-base-1` with the names of your repositories.
9. You may also wish to set a protection on your main branch so that students cannot alter it. This can be done by [setting access permissions](https://docs.github.com/en/organizations/managing-access-to-your-organizations-project-boards/project-board-permissions-for-an-organization) to your organization, or by [adding protections to your main branch](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches).

## Editing and testing the assignment

To change the due date for sprint-1, edit the sp1.md file under `sprint-meta/dates`, then push to your sprint-meta repository.

To modify the sprint-1 assignment, edit the problem files and test files in sprint-1/src/ and then push to your repository. You (probably) will not need to edit pom.xml or any workflow files to have your tests run automatically. 

To test your system, create a solution for your assignment that will pass all of your tests. Then follow the tutorial for students ("student-tutorial.md") in this folder to submit your work. Also, try making code that fails a test (add a new file, or fail a unit test, etc.). See what happens then. If you have followed the directions above and your tests are failing, check out the FAQ.

## Grading the submissions

Your students will submit the links to their pull requests in Canvas. The pull request page on GitHub will show whether the checks have passed or failed. If checks failed, the page will look something like this:

img

To learn more about which tests failed, click **Details**.

To view the student's code, click **Files changed.** To annotate the code, hover over a line and click the blue plus sign.

When you are finished, assign the submission a grade in Canvas.

## Acknowledgements
Thanks to Dr. Peng Du for setting up this auto-testing system. Thanks also to Dr. Johnny Lin and Dr. Yusuf Pisan for their work in coordinating this process.
