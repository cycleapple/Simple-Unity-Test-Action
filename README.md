# Simple Unity Test GitHub Action

## Description:

The "Simple Unity Test" is a GitHub Action that allows you to run Unity Play Mode and Editor Mode tests on your Unity projects. It
automates the process of executing tests, capturing the test results, and uploading them as artifacts. Is designed for windows self-hosted runner.

## Features:

- Supports running Unity Play Mode tests.
- Supports running Unity Editor Mode tests.
- Captures test results and logs for both Play Mode and Editor Mode tests.
- Uploads the test results as artifacts, making it easy to access and analyze the test outcomes.

## Usage:

To use the "Simple Unity Test" GitHub Action in your workflow, you need to specify the full path to the Unity executable as an input.
Here's an example workflow that demonstrates how to integrate the action into your project:

```yaml
name: Unity Test Workflow

on:
  push:
    branches:
      - main

jobs:
  test:
    name: Run Unity Tests
    runs-on: ubuntu-latest
    steps:
      - name: Run Simple Unity Test
        uses: cycleapple/Simple-Unity-Test-Action@v1
        with:
          unityPath: '/path/to/unity/executable'

      # Additional steps to deploy, build, or perform other actions based on test results
```

## Inputs:

- `unityPath` (required): The full path to the Unity executable. This input specifies where the Unity engine is located on the runner's
  machine.


## License:

This GitHub Action is provided under the [MIT License](https://opensource.org/licenses/MIT). Feel free to modify and use it in your
projects as per the terms of the license.