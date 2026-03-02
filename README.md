# Instructions to Deploy and Create App
Clone the repository:
```
git clone https://github.com/H0RAC3Z/SOFE3980U-Lab3-Part1
```

Get to the maven prj:
```
cd SOFE3980U-Lab3-Part1/BinaryCalculatorWebapp
```

Build:
```
mvn package
```

Build image to repo: 
```
docker build -t us-central1-docker.pkg.dev/project-e3d98e07-b588-4684-81a/sofe3980u/binarycalculator .
```

Push image:
```
docker push us-central1-docker.pkg.dev/project-e3d98e07-b588-4684-81a/sofe3980u/binarycalculator
```

Move to .yaml files
```
cd kubernetes/
```

Deploy using .yaml:
```
kubectl create -f deploy.yaml
```

Create service using .yaml:
```
kubectl create -f service.yaml
```

Verify deployment and service:
```
kubectl get deployment
```
```
kubectl get services
```

Wait for external IP then run at external IP:
```
http://<external-ip>:8080
```
