# GPT4all-ansible
Ansible script to set up [GPT4ALL](https://github.com/nomic-ai/gpt4all) on an AWS Virtual Private Cloud
The steps to set up a Private cloud on AWS work. The steps to install GPT4ALL is in progress.

## Pre-requisites:
### - an AWS account, and create an IAM user for CLI (download the CSV of the access key & secret)
### - a Spot.io account, for spot instances on AWS at cheaper rates

Steps
- ansible cli installed on your own machine:
```sudo apt install ansible```

- install
```ansible-galaxy collection install amazon.aws community.aws```

- install botocore
```pip install boto3 botocore```

- install 
```sudo apt-get install jq```

- install
```pip install awscli``` (make sure it is updated to latest version)

- Before running the ansible script, you need to set the access & secret that you downloaded in CSV from AWS in the keys file

