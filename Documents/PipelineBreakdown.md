# Introduction
Continuous Integration and Continuous Deployment (CI/CD) pipelines are fundamental to modern software development. They enable developers to integrate changes to their projects more frequently and reliably. This report details the CI/CD pipeline for my Flutter web application, highlighting the automation of building, testing, and deploying phases.

## DevContainer Environment
The development environment is containerized using Docker, which provides a consistent and isolated setting regardless of the local machine setup. This fixes the "it works on my machine issue. The devcontainer.json configures the Docker container specifically for Flutter development by using a premade image hosted by the Microsoft Container Registry that uses a basic docker image, "Ubuntu," that includes some standard tools for setting up dev environments. This ensures that dependencies and SDKs needed for a Flutter app to run are available on any machine that uses this container, saving time, effort, and headaches. For this app, the dev container is being used to make changes to the application or any other changes quickly without risk.

## Source Code Version Control Tools
Git serves as the version control system for this app project. It helps manage the changes to the source code and enables multiple developers to work simultaneously. Even though currently there are not numerous developers working on this app, having the setup for a possible future team is important. Git is being used since it blends easily with VS code, allowing for changes to easily be committed to the local repository and staged to be quickly pushed to the remote repository hosted on GitHub. These quick pushes trigger the Github actions pipeline, which helps with consistent feedback when making changes.

## CI/CD Pipeline Environment
The .github/workflows/main.yml file configures the CI/CD pipeline using GitHub Actions. The workflow is triggered to run on every push to the repository. Github Actions is being used here for its simplicity and its connection to GitHub pages, which the application is being deployed to.

## CI/CD Tools
GitHub Actions is the CI/CD tool of choice for this application, automating the build `flutter run -d web-server` command and `flutter test'command, as well as the deployment processes. It is configured to deploy the Flutter web application to GitHub Pages upon a successful build.
## Deployment Environment
The application is deployed to GitHub Pages, a hosting service provided by GitHub. It is an ideal platform for hosting static web pages generated from the Flutter build process in general. It was very useful for this project because of how easily github pages meshes with the Github repository. And since the entire version control revolves around Github, I thought that it would be more logical to keep everything relative to each other in a streamlined manner.

## Flutter Web Application
The application is a default Flutter demo clicker app, showcasing basic functionality and serving as a template for further development. It features a button feature that can be clicked by the user. It features a counter functions as well that counts the amount of times the user clicks the button. The app also has a music feature as well as a basic background ui. It is tested and deployed via the GitHub Actions pipeline.
## Conclusion
Throughout the project, the CI/CD pipeline has proven to be a valuable asset, automating tedious tasks and easily adding and removing features. While challenges arose in configuring the pipeline to handle Flutter's specific requirements, these were overcome, leaving room for future improvements, such as adding more complex testing and deployment strategies as well as possibly adding future configurations to the main yml file to not deploy the application on every push. But overall, this pipeline and continuous integration setup will be a strong foundation for future Flutter app projects.