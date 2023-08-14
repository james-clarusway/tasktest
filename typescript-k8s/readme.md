# Deploying Typescript-Node-Starter Application With Minikube

# Minikube Installation (for windows)

** Open the Powershell as administrator and paste this command **

New-Item -Path 'c:\' -Name 'minikube' -ItemType Directory -Force
Invoke-WebRequest -OutFile 'c:\minikube\minikube.exe' -Uri 'https://github.com/kubernetes/minikube/releases/latest/download/minikube-windows-amd64.exe' -UseBasicParsing

** Add the minikube.exe binary to your PATH. **

$oldPath = [Environment]::GetEnvironmentVariable('Path', [EnvironmentVariableTarget]::Machine)
if ($oldPath.Split(';') -inotcontains 'C:\minikube'){
  [Environment]::SetEnvironmentVariable('Path', $('{0};C:\minikube' -f $oldPath), [EnvironmentVariableTarget]::Machine)
}

** Start your cluster ** 

minikube start


# Create Your Working Folder 

mkdir typescript-k8s && cd typescript-k8s


# Copy the Contents of the typescript-test Folder we Prepared Before and Put them in typescript-k8s


# Create Docker Image From Your Dockerfile

** go to the typescript-ks8/Typescript-Node-Starter folder **

docker build -t typescript .




