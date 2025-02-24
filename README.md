# ECS ( elastic container service )

`Create Docker based Container using AWS`


### Step-1 :-

Go to IAM  --->  Create user = ecs-class

Policy =  Admiministrator access policy

Generate Access-key & Secret Access-key

### Step-2 :-

Go to ECR   ---->  Create Repository 

Visibility settings = private

Repository name = ecs-repo

### Step-3 :-

Open Terminal ( ubuntu instance )

Connect your instance

sudo su -

apt update

#### To install the AWS CLI, run the following commands.


```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

#### To check awscli install or not

```
aws --version
```


apt install git docker.io -y

### Step-4 :-

Configure AWS Cli  = aws configure

( mention access-key & secret access-key )

git clone https://github.com/itscloudevops/aws-ecs-proj.git 

cd  < repo-name >

ls

` if you want to create docker image then go to ecr `
Go to ECR

- Copy & paste Log-in command
    
- Build your Docker image 

- After the build completes, tag your image

- Push this image to your newly created AWS repository ( ECR )

### Step-5 :-

Go to ECS   --->  Create Cluster

Name of Cluster = my-ecs-cluster

Infrastructure  = AWS Fargate (serverless)

Task definitions  ---->   Create new task definition

Task definition family = ecs-demo-task ( name )

Container details

- NAME = my-ecs-container

- Image URI = go to ecr and copy-paste image url

- create


Go to Task definition   ---->   Click on Deploy   ----->  Create Service

Service name = myservice

Create


### Step-6 :-

Copy and paste Container Public-ip on Browser 🌏⛳🚀✌️



===============================END==============================
