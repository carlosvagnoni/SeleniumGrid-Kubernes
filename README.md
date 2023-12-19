# SeleniumGrid-Kubernetes

This repository contains Kubernetes deployment files to set up a Selenium Grid cluster using Kubernetes.

The configurations in this repository facilitate the creation of a Selenium Grid setup consisting of a hub and various browser nodes (Chrome, Firefox, and Edge). This setup enables efficient parallel test execution and browser compatibility testing.

## Docker Images Used

This project utilizes the following Docker images:

- [Selenium Grid Hub](https://hub.docker.com/r/selenium/hub): This image serves as the hub for Selenium Grid, enabling the remote execution of WebDriver tests in collaboration with Selenium Grid nodes.

- [Selenium Grid Node with Chrome](https://hub.docker.com/r/selenium/node-chrome): This image provides a Selenium Grid node with Chrome support. When paired with the Selenium Grid Hub, it facilitates the execution of WebDriver tests in environments specifically equipped with the Chrome browser.

- [Selenium Grid Node with Edge](https://hub.docker.com/r/selenium/node-edge): Similar to the previous node, this image offers a Selenium Grid node tailored for Edge support. It works alongside the Selenium Grid Hub to execute WebDriver tests remotely in Microsoft Edge environments.

- [Selenium Grid Node with Firefox](https://hub.docker.com/r/selenium/node-firefox): Another node image compatible with Selenium Grid, designed for Firefox support. When combined with the Selenium Grid Hub, it enables the remote execution of WebDriver tests in environments utilizing the Firefox browser.

## Usage

1. Ensure you have a Kubernetes cluster set up.
2. Deploy these configuration files using `kubectl create -f <filename>` to create the Selenium Grid components for the first time.
3. Verify the deployment using `kubectl get pods/services` or access the Minikube Dashboard by running `minikube dashboard` in your terminal.
4. Run the following command `minikube service selenium-hub-svc --url`. This command specifically fetches the URL of the `selenium-hub-svc` service from Minikube, enabling easy access to the Selenium Hub. Users can use this URL to configure their testing frameworks or any other services to interact with the Selenium Hub within the Minikube cluster.

## Configuration

Each deployment file (`selenium-hub-deployment.yaml`, `selenium-node-chrome-deployment.yaml`, etc.) contains detailed configurations for the respective components. Customize these configurations as per your requirements.

## Contributing

Feel free to contribute by opening issues, providing suggestions, or submitting pull requests.