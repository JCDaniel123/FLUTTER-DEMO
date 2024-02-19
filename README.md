This is a container environment that allows the user to run flutter applications.
In order to run this containerized environment you will need to complete some steps
1. You will need to have the application Docker Desktop installed.
2. Make sure that you have Visual Studio Code installed on your machine. This container runs on VS code.
3. You will also need to install Flutter on your machine to utilize this container. YOU DO NOT NEED TO INSTALL THE SDK. That is taken care of in the container.
4. Make sure when running this container with your flutter app, that you run Docker and create your own container.
5. To run your flutter app using this container, use the command flutter run -d web-server into your terminal
6. If you encounter issues when inputting this command  use the command "flutter pub upgrade" in the terminal. If this issue is encountered, you will need to input this command every time the container is rebuilt


NOTE:
Make sure that when you install your flutter app that it is on the your path on your machine.
