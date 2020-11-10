# Jenkins Main Deployment

In order to play with installing Jenkins on K8s you should have a K8s cluster where to play, on development I use minikube and Virtualbox as the driver, you can use any driver you want.

## Installation

### Build the Jenkins Docker Image

```bash
docker build -t yosoyvilla/jenkins-main:lts .
```
notice that I'm using my username to tag the image, you can use any tag you want.

### Start the minikube cluster

```bash
minikube start --vm-driver=virtualbox --apiserver-ips 127.0.0.1 --apiserver-name localhost
```

## How does it works?

WIP

## Usage

```bash
kubectl apply -f .
```

## Notes

- Keep in mind that I'm using `/tmp/` as my persistent storage, you should change that if you want to run it on a server o keep your configuration

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
