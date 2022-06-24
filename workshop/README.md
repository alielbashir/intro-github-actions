# Get started with GitHub Actions

## Goals

In this workshop, you will learn how to build a Continuous Integration (CI) workflow in GitHub actions for a Python project

| **Goal**                      | Create a CI workflow with GitHub Actions                                    |
| ----------------------------- | --------------------------------------------------------------------- |
| **What will you learn**       | The basics of creating a GitHub Actions workflow that runs on code changes|
| **What you'll need**          | [Python](https://www.python.org/downloads/), [Visual Studio Code](https://code.visualstudio.com/download) and a [GitHub account](https://github.com/signup) |
| **Duration**                  | 1 Hour |
| **Microsoft Cloud Topics taught**                 | GitHub Actions |
| **Slides** | [Powerpoint](slides.pptx) 
                         
## Video

Embed your Train the Trainer video here. Instructions on how to create a great video experience is [available on this page](../video-guidance.md).

## Pre-Learning
- [Create and manage projects in Python](https://docs.microsoft.com/en-us/learn/modules/python-create-manage-projects/)
- [Build continuous integration (CI) workflows by using GitHub Actions](https://docs.microsoft.com/en-us/learn/modules/github-actions-ci/)

## Prerequisites

- [Python](https://www.python.org/downloads/)
- [Visual Studio Code](https://code.visualstudio.com/download)
- [Git](https://git-scm.com/download)

## What students will learn

<!-- *In this area, describe the scenario and intended solution, paraphrasing what is in the module or creating a brief description here*

Example: Have you ever wanted to visit a museum virtually or explore its collections right from your home computer? In this workshop, use an API, or Application Programming Interface, to learn more about a museum collection. -->

In this workshop, you will build a Continuous Integration workflow for a Python project using GitHub Actions. The final workflow will:

1. Check code syntax
2. Run automated tests
everytime a new commit is pushed to the project.

By the end of this workshop you will be able to:
1. Setup a GitHub Actions workflow
2. Configure automated linting and testing in the workflow
3. Debug workflow logs to identify problems and fix them

## Milestone 1 - Setup a GitHub Repository

Let's begin by forking the sample repository, so we can make changes upon it.

1. Login to your GitHub account

2. Fork the sample repository into your own account https://github.com/alielbashir/python-calculator

3. Clone the forked repo into your PC and authenticate GitHub in VSCode #TODO add image



## Milestone 2 - Setup a Python project

Now we need to set up a Python project on our local machine, for which we will create our CI workflow.

1. Open the project in VSCode
![image](https://user-images.githubusercontent.com/53450844/168304812-15adfdb3-910f-4f66-bace-1e6e18ae5641.png)
After opening the project you should open a new terminal to run commands using VSCode's integrated terminal
![image](https://user-images.githubusercontent.com/53450844/168305239-9c7084cf-2c15-42d5-b55b-7099eaea5eba.png)
![image](https://user-images.githubusercontent.com/53450844/168305326-2ec5af48-7426-453d-9a80-f0734fa4248d.png)

2. Install pytest and flake8 using this command
```
py -m pip install pytest flake8
```
3. Run tests using pytest on the terminal
![image](https://user-images.githubusercontent.com/53450844/168305834-14728299-046c-4e81-8ee9-89d456c9b4ea.png)
```
py -m pytest
```
The command should run and show you that all the tests passed

4. Lint using flake8
![image](https://user-images.githubusercontent.com/53450844/168306766-687b6f8a-f31a-436b-853a-c767f476ded4.png)
```
py -m flake8
```
If you see no output don't worry, that means the code has no syntax issues :)

5. Push to GitHub
```
git push
```

## Milestone 3 - Create the GitHub Actions workflow

1. Navigate to the GitHub Actions page on your forked repo
2. Click "configure" on the suggested Python Application workflow
3. Commit the new file into the remote repo
4. Refresh the repo's homepage and confirm the workflow runs successfully
5. Pull the changes into your local repo


## Milestone 4 - Push changes to GitHub

1. Add a new calculate square area function and write it's test
```py
# calculator.py
def calculate_square_area(width):
    return width * 2 
```
```py
# test_main.py
def test_calculate_square_area():
    assert calculate_square_area(10) == 100
```

2. Commit and push the change to GitHub
```
git push
```


## Milestone 5 - Review workflow and make changes so it passes

The workflow run failed! Looks like there's an error we need to debug

1. Open the workflow details page
2. Click on the failing action
3. Inspect the logs to find the cause of the workflow failure
4. Fix the cause locally and push the change you made
5. Wait and confirm the workflow passes


## Quiz or Code Challenge


## Next steps


[AZ-400: Implement CI with Azure Pipelines and GitHub Actions](https://docs.microsoft.com/en-us/learn/paths/az-400-implement-ci-azure-pipelines-github-actions/)

[Build and deploy applications to Azure by using GitHub Actions](https://docs.microsoft.com/en-us/learn/modules/github-actions-cd/)

## Practice

Now that you know how to build a CI workflow for Python, you can apply this knowledge to create a CI workflow for projects with any other language. Can you set up a CI workflow for past projects? Can you modify this workflow to run on different branches? 

## Feedback

Be sure to give [feedback about this workshop](https://forms.office.com/r/MdhJWMZthR)!

[Code of Conduct](../CODE_OF_CONDUCT.md)

