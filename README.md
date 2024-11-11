# mlflow-operation

## For Dagshub:

```
import dagshub
dagshub.init(repo_owner='ashokk.bangaru', repo_name='mlflow-operation', mlflow=True)

```

## MLflow on AWS:
1. Login on AWS console
2. Create IAM  user with Admin access (attach privacy policies and add a security key)
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket (mlflowbuck)
5. Create EC2 machine (Ubuntu) and add Security groups 5000 port


## Run the following commands on EC2 machine:
```
sudo apt update

sudo apt install python3-pip

sudo apt install pipenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell

aws configure

mlflow server -h 0.0.0.0 --default-artifact-root s3://xxxxxx

#set uri in your  loacl terminal and in the code:

$env:MLFLOW_TRACKING_URI = ""
$env:MLFLOW_TRACKING_URI
set MLFLOW_TRACKING_URI=

```
