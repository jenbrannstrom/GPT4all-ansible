# GPT4all-ansible
Ansible script to set up [GPT4ALL](https://github.com/nomic-ai/gpt4all) on an AWS Virtual Private Cloud
## Pre-requisites:
### 1. an AWS account, and create an IAM user for CLI (download the CSV of the access key & secret)
### 2. a Spot.io account, for spot instances on AWS at cheaper rates

3. ansible cli installed on your own machine:
```sudo apt install ansible```

4. install
```ansible-galaxy collection install amazon.aws```
and
```ansible-galaxy collection install community.aws```

5. install botocore
```pip install boto3 botocore```

6. install 
```sudo apt-get install jq```

7. install
```pip install awscli``` (make sure it is updated to latest version)

8. Before running the ansible script, you need to set the access & secret that you downloaded in CSV from AWS in the keys file

