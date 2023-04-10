# GPT4all-ansible
Ansible script to set up [GPT4ALL](https://github.com/nomic-ai/gpt4all) on an AWS Virtual Private Cloud
## Pre-requisites:
1. an AWS account, with an IAM user for CLI (download the CSV of eth access key & secret)
2. a Spot.io account, for spot instances on AWS at cheaper rates
3. ansible cli installed on your own machine
4. before running the ansible script, you need to set the access & secret from AWS:
```export AWS_ACCESS_KEY_ID='YOUR AWS ACCESS KEY'``` AND
```export AWS_SECRET_ACCESS_KEY='YOUR AWS SECRET'```

