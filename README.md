This is a container enviorment that allows the user to run flutter applications.
In order to run this containerized enviorment you will need to complete some steps
1. You will need to have the application Docker Desktop installed.
2. You will also need to install Flutter for on your machine to utilize this container. YOU DO NOT NEED TO INSTALL THE SDK. That is taken care of in the container.
3. Make sure when running this container with your flutter app, that you run Docker and create your own container.
4. To run your flutter app using this container, use the command flutter run -d web-server into your terminal
5. If you encounter issues when inputting this command  use the command FLUTTER PUB UPGRADE(no caps) in the terminal. If this issue is encountered, you will need to input this command everytime the container is rebuilt


NOTE:
Make sure that When you install your flutter app that it is on the your path on your machine.
