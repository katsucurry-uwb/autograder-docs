## 3. Setting up a tutorial for students

Along with the assignment, a step-by-step guide for students on how to submit their answers to the auto-testing system, created by Dr. Peng Du, has been provided; see the student-instructions.md file (in the Google Drive folder). You will probably need to tailor the tutorial to fit with your teaching style; to help with that, Sections 2.1 - 2.3 are an example step-by-step tutorial with screenshots. Feel free to use (or not use) any of the material below in your version of the student guide.

We also recommend walking through the tutorial in class and/or providing a video tutorial.

*Info for students below*

<img width="60%" alt="image" src="">


1. Got to the GitHub repository for your coding assignment.
2. **Fork the repository.** Click **Fork**, then click **Create fork**. This creates a personal copy of the code for you.

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/f7c95fcfb94d1949c99059bf7b82c355918fea30/images/fork.png">


3. **Enable GitHub workflows.** In your repository, click **Actions**, then click the green button. This will enable automatic testing for your submissions.
4. **Clone the repository to your machine.** In IntelliJ, select **File > New > Project from Version Control...** from the menu bar. You may be asked to log into GitHub.
5. **Create a new branch.** In Git, branches are used to contain work on some repository until that work is complete and ready to be merged with the main “trunk” of the repository. In IntelliJ, select **Git > New Branch...** from the menu bar. Name your branch "work", then click **Create**.
#### 6. Complete the assignment.

Be sure to read the full assignment text before you start to code. Also take a look at the comments left for you in the programming files inside src. Do not modify any code outside the src repository.

#### 7. Test your code.

To test your code, open the test files under src/test/java, then click the green Play button in the gutter to the left of the test method. To run all tests, right-click on the src/test/java folder in the **Project** tool window and select **Run 'All Tests'**. You can find more instructions on running tests in IntelliJ [here](https://www.jetbrains.com/help/idea/performing-tests.html#run-with-options).

#### 8. Commit and push your changes.

You will commit (“collect all the changes together”) and push (“send those changes to the online repository”). Instructions for pushing with Intellij can be found [here](https://www.jetbrains.com/help/idea/commit-and-push-changes.html). More general guides can be found [here](https://docs.github.com/en/get-started/using-git/about-git). You should do this regularly, so that you can be sure your work is saved securely in multiple places.

3.3 Submit assignment

3.3.1 Create a pull request

Once you have pushed your last changes, you will need to create a new pull request from your “work” branch to your main branch. Do NOT create a pull request to the instructors repository. Once you have pushed changes to the online repository, you should see a notification like the one below (indicated with the purple arrow). You may need to navigate to the “main” branch to see this popup. If the notice does not appear, you can manually create a pull request; see more information about that process here, but check the “main” branch first. You can do this by clicking the branch selection button (indicated in red below) and selecting the main branch. Once you click the “compare and pull request button”, you will need to change some settings in your pull request, so don’t just press “create pull request” right away. Do NOT make any changes or a PR after the deadline, as the “late assignment” check will fail.

img


Once you have pressed the “compare and pull request button”, you will be brought to the screen below. Before you create a pull request, you will need to change the destination of the request. Do this by pressing the button indicated below and selecting your fork of the repository’s main branch (base: main).

img

At this point, you should add a title (and comment, if needed) to your pull request.

img

Once all that is done, you can create the pull request. Once the pull request is created, GitHub will begin to test your submission automatically. This process may take a moment, so don’t immediately step away from your assignment once you have created the request.

3.3.2 Examine the test results.

Once the automatic checks have been completed, GitHub will let you know if all the tests have passed or not. Passing tests will look like this:

img

If you see the above, you are probably good to go, but make sure to double check that you have finished with your assignment.

Failing Checks will look like this:

img

To see the details of which checks failed, I can press the “details” link, as shown below:

img

You can see that I failed the unit tests. I can see which tests I failed by expanding that section and scrolling to the failed tests. This may take a bit of scrolling, but don’t give up!

3.3.3 Submit to Canvas
Once you have submitted your pull request, you should submit the URL of your pull request to canvas. Just navigate to the main page of the pull request (which you can find through the “pull requests” tab next to “code” and “actions”), and copy that page’s URL.