# CI/CD Pipeline Report for the Flutter Application

## Pipeline Environment

The CI/CD pipeline for our Flutter application is designed to operate in a highly scalable and efficient cloud-based environment. The key components of our infrastructure and environment include:

Operating Systems: The pipeline is configured to run on ubuntu-latest as the operating system. This choice offers a stable and widely supported environment for building and testing our Flutter application.

Cloud Services: The pipeline is hosted on GitHub, utilizing GitHub Actions for continuous integration and deployment tasks. This provides a seamless integration with our source code repository, allowing for automated builds and deployments upon code pushes.

Network Configurations: Our pipeline operates within GitHub's secure cloud environment, ensuring that all data transfers and operations are conducted securely and efficiently across all stages of the CI/CD process.

## Pipeline Tools

GitHub Actions: Chosen for its deep integration with GitHub repositories, GitHub Actions enables us to automate our workflows directly from our source code. This tool supports a wide range of CI/CD operations, from code checkout to deployment, making it an ideal choice for our pipeline.

Flutter Action: A custom GitHub Action (subosito/flutter-action@v2) that sets up a Flutter environment. This tool simplifies the process of installing Flutter and ensures that we are using a consistent version of Flutter across all builds.

peaceiris/actions-gh-pages: Utilized for deploying our Flutter web application to GitHub Pages. This action automates the deployment process, making it easy to publish our application's web version directly from our CI/CD pipeline.

## Features, Strengths, and Limitations

GitHub Actions offers a wide range of pre-built actions and integrations, making it highly versatile for different CI/CD scenarios. However, it is inherently tied to GitHub, limiting its use to projects hosted on this platform.
Flutter Action provides a quick setup for Flutter environments, which is crucial for our Flutter-based application. Its limitation is that it is a third-party action, relying on external maintenance and updates.
peaceiris/actions-gh-pages simplifies the deployment process to GitHub Pages, but its use is specific to GitHub Pages hosting and may not be suitable for other platforms.

## Automation Process

Code Checkout: Utilizing actions/checkout@v4 to clone the latest version of the source code into the runner's environment.

Flutter Environment Setup: Setting up the Flutter environment using subosito/flutter-action@v2 with the stable channel. This ensures that our application is built using a stable and consistent Flutter version.

Dependency Installation: Running `flutter pub get` within the ./FlutterDemoApp directory to install all necessary dependencies for the Flutter application.

Running Tests: Executing `flutter test` to run unit tests and ensure that all components of the application function correctly.

Building the Application: Compiling the application into a web format using `flutter build web`, preparing it for deployment.

Deployment: Using peaceiris/actions-gh-pages@v3 to deploy the built web application to GitHub Pages. This step automates the process of updating our web application whenever changes are pushed to the repository.

