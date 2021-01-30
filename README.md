<p align="center">
  <a href="https://github.com/sbmallik/github-actions-test"><img alt="GitHub Actions status" src="https://github.com/sbmallik/github-actions-test/workflows/container2/badge.svg"></a>
</p>

# Github Actions Test

***

## Test Framework

This repository contains the code to test the Github Actions. The code uses YML configuration files to represent each workflow. Logically these files can interface with any type of code base like NodeJS, Python, Ruby or Java.

### Pre-requisites

* A Bourne-compatible shell, like bash or zsh
* [Git](http://gitscm.com/)
* [Node 10.15+](http://nodejs.org/)

### Setup

Clone this GIT repository to the local machine as follows:

```bash
git clone git@github.com:sbmallik/github-actions-test.git
cd github-actions-test
```

Next, it is necessary to create a new repository in github, to accommodate the workflow files.
Later, this can be pushed to the above repository associated with the individual github account with the following commands:

```bash
git add -A
git commit -m "Initial commit."
git remote add origin git@github.com:<github-username>/github-actions-test.git
git push -u origin master
```

### Environment variables used

The only environment variables used are the standard ones provided by github actions. In addition the following ones are used for test and demonstration purpose:

1. `ACTIONS_RUNNER_DEBUG` - Used to control the debug logs in the runner level
1. `ACTIOND_STEP_DEBUg` - Same purpose, but for step level
1. `WF_SECRET` - Example of secret implementation provided by github settings

All these variables are configured with the github user account.

### Running Tests

The test execution process is currently triggered by push action in the repository. So the test execution is expeted at the time of repository creation in the `Actions` tab. An individual workflow can be re-run from the web interface.

### Filtering tests

Individual filtering of workflow files isn't available, however it is possible to disable a workflow file from the web-interface of the `Actions` tab.
