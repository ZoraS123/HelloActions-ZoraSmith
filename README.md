# HelloActions-ZoraSmith

## Project Overview

This project demonstrates how to use GitHub Actions to
automatically and manually run a Python Hello World program.

The Python program reads an environment variable called
WHO_TO_GREET and prints a personalized greeting.

## Workflow Triggers

The GitHub Actions workflow uses two triggers:

- **Push:** Automatically runs the workflow when changes
  are pushed to the main branch.
- **Workflow Dispatch:** Allows the workflow to be
  started manually from the GitHub Actions tab.

## Workflow Job

The workflow contains one job named `hello-python`.

This job runs on a GitHub-hosted Ubuntu Linux runner
using `ubuntu-latest`.

The runner provides the environment where the workflow
steps execute.

## Workflow Steps

The workflow performs three main steps:

1. **Checkout:** Uses `actions/checkout@v4` to make
   the repository files available on the runner.

2. **Set Up Python:** Uses `actions/setup-python@v5`
   to configure Python 3.11 on the runner.

3. **Run Python Program:** Sets the `WHO_TO_GREET`
   environment variable and executes `python hello.py`.

The program prints a greeting and a message confirming
that it is running inside GitHub Actions.

## Testing and Verification

I tested the GitHub Actions workflow using both
automatic and manual execution.

### Automatic Run

The workflow ran successfully after I committed
`hello.yml` to the main branch.

### Manual Run

I manually triggered the workflow using the
Run workflow button in the GitHub Actions tab.

Both successful runs used the same workflow.

### Verified Output

The automatic run produced:

```text
Hello GitHub Actions Student!
This program is running inside GitHub Actions.
```

The output confirms that the Python program
successfully read the environment variable
and executed on the GitHub-hosted runner.

## GitHub Actions Concepts

### Compiling vs. Running

Compiling translates source code into a form that can
be executed by a computer. Running means executing
the program's instructions.

Python does not require a separate compilation command
for this lab. The workflow prepares Python and runs
the program using `python hello.py`.

### Workflow vs. Job vs. Step

- **Workflow:** The complete automation defined
  in `hello.yml`.
- **Job:** A group of steps executed on a runner.
  This workflow has one job called `hello-python`.
- **Step:** An individual action or command within
  a job, such as checking out the repository,
  setting up Python, or running the program.

### Viewing Program Output

The program output is available in the GitHub
repository under Actions. Select a workflow run,
open the job, and expand the Run the Python
program step to view its logs.

## AI Assistance Disclosure

I used ChatGPT to explain YAML syntax, troubleshoot the
workflow, and organize the README documentation.

I created and configured the GitHub repository,
committed the workflow, and tested the automatic
and manual workflow runs myself.

I reviewed the explanations to better understand
how the workflow, jobs, steps, and triggers work.
