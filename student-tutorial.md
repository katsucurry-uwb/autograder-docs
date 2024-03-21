## GitHub Homework Tutorial

This tutorial will show you how to download, complete, and submit your programming assignment through GitHub.
It assumes that you are using IntelliJ IDEA.

#### 1. **Fork the repository.**

Go to the GitHub repository for your coding assignment. Click **Fork**, then click **Create fork**. This creates a personal copy of the code for you.

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/4ec68de4220334ad7d3c3f1ff8df96303cd07283/images/fork.png">

#### 2. **Enable GitHub workflows.**

In your repository, click **Actions**, then click the green button. This will enable automatic testing for your submissions.

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/48e3c2342cfa5603fe4f6efc01ea4cd7ef9acf7f/images/actions.png">

#### 3. **Clone the repository to your machine.**

In IntelliJ, select **File > New > Project from Version Control** from the menu bar. You may be asked to log into GitHub or provide a [token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token).

#### 4. **Create a new branch.**

In Git, branches are used to contain work on some repository until that work is complete and ready to be merged with the main “trunk” of the repository. In IntelliJ, select **Git > New Branch...** from the menu bar. Name your branch "work", then click **Create**.

#### 5. Complete the assignment.

Be sure to read the full assignment text before you start to code. Also take a look at the comments left for you in the programming files inside src. Do not modify any code outside the src repository.

#### 7. Test your code.

To test your code, open the test files under src/test/java, then click the green Play button in the gutter to the left of the test method. To run all tests, right-click on the src/test/java folder in the **Project** tool window and select **Run 'All Tests'**. You can find more instructions on running tests in IntelliJ [here](https://www.jetbrains.com/help/idea/performing-tests.html#run-with-options).

#### 8. Commit and push your changes.

Next, you should commit (“collect all the changes together”) and push (“send those changes to the online repository”). In IntelliJ, select **Git > Commit** from the menu bar. Add a commit message, then click **Commit and Push**. More instructions for pushing with Intellij can be found [here](https://www.jetbrains.com/help/idea/commit-and-push-changes.html). More general guides can be found [here](https://docs.github.com/en/get-started/using-git/about-git). You should do this regularly, so that you can be sure your work is saved securely in multiple places.

#### 9. Create a pull request.

Once you have pushed your last changes, you will need to create a new pull request from your “work” branch to your main branch. Do NOT create a pull request to the instructors repository. Once you have pushed changes to the online repository, you should see a notification like the one below (indicated with the purple arrow). You may need to navigate to the “main” branch to see this popup. If the notice does not appear, you can manually create a pull request; see more information about that process here, but check the “main” branch first. You can do this by clicking the branch selection button (indicated in red below) and selecting the main branch. Once you click the “compare and pull request button”, you will need to change some settings in your pull request, so don’t just press “create pull request” right away. Do NOT make any changes or a PR after the deadline, as the “late assignment” check will fail.

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/5074cedf47c5aaa58241b257cc5ef12b6b621d40/images/compare-and-pull-request.png">

Once you have pressed the “compare and pull request button”, you will be brought to the screen below. Before you create a pull request, you will need to change the destination of the request. Do this by pressing the button indicated below and selecting your fork of the repository’s main branch (base: main).

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/5074cedf47c5aaa58241b257cc5ef12b6b621d40/images/change-destination.png">

At this point, you should add a title (and comment, if needed) to your pull request.

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/5074cedf47c5aaa58241b257cc5ef12b6b621d40/images/pull-request-comment.png">

Once all that is done, you can create the pull request. Once the pull request is created, GitHub will begin to test your submission automatically. This process may take a moment, so don’t immediately step away from your assignment once you have created the request.

#### Examine the test results.

Once the automatic checks have been completed, GitHub will let you know if all the tests have passed or not. Passing tests will look like this:

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/5074cedf47c5aaa58241b257cc5ef12b6b621d40/images/test-results-student.png">

If you see the above, you are probably good to go, but make sure to double-check that you have finished with your assignment.

Failing Checks will look like this:

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/5074cedf47c5aaa58241b257cc5ef12b6b621d40/images/failed-test-student.png">

To see the details of which checks failed, I can press the “details” link, as shown below:

<img width="60%" alt="image" src="https://github.com/katsucurry-uwb/autograder-docs/blob/5074cedf47c5aaa58241b257cc5ef12b6b621d40/images/view-details-student.png">

You can see that I failed the unit tests. I can see which tests I failed by expanding that section and scrolling to the failed tests. This may take a bit of scrolling, but don’t give up!

#### Submit to Canvas
Once you have submitted your pull request, you should submit the URL of your pull request to canvas. Just navigate to the main page of the pull request (which you can find through the “pull requests” tab next to “code” and “actions”), and copy that page’s URL.