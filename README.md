# Jenkins Pipeline

This Jenkins pipeline automates the process of checking out code from a Git repository, building the project, running unit tests, ensuring quality, and deploying the project. It also includes post-build steps to notify the team of the success or failure of the pipeline.

## Pipeline Stages

1. **Git-Checkout**
   - Checks out the code from a specified Git repository.

2. **Build**
   - Builds the checked-out project by running a build script.

3. **Unit-Test**
   - Runs unit tests on the project using a testing script.

4. **Quality**
   - Performs quality assurance checks on the project using a quality assurance script.

5. **Deploy**
   - Deploys the project using a deployment script.

## Post-Build Actions

- **Always**: This block will always run, regardless of the result of the pipeline.
- **Success**: This block will run if the pipeline completes successfully.
- **Failure**: This block will run if the pipeline fails.

## Notes

- Ensure that the scripts (`Build.sh`, `Unit.sh`, `Quality.sh`, `Deploy.sh`) are executable before running the pipeline.
- If the scripts do not have execution permissions, you may need to run `chmod +x` on them to allow execution.

