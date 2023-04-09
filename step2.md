### via Console attach an (elastic) ip address
### Create file: "check_security_group_rules.sh" 
### replace "YOUR_INSTANCE_ID_HERE"

  ```INSTANCE_ID="YOUR_INSTANCE_ID_HERE" # Replace with your instance ID```

   ```SG_ID=$(aws ec2 describe-instances --instance-ids $INSTANCE_ID --query 'Reservations[].Instances[].SecurityGroups[].GroupId' --output text)```

    a```ws ec2 describe-security-groups --group-ids $SG_ID --query 'SecurityGroups[].IpPermissions[]' --output json```


### save it in the same DIR adn run that file using :
### make the script executable by:


```chmod +x check_security_group_rules.sh```

### Then


```./check_security_group_rules.sh```


### Get the deets, then run:

```aws ec2 authorize-security-group-ingress --group-id sg-"YOUR SECURITY GROUP ID HERE" --protocol tcp --port 22 --cidr "YOUR_IP_ADDRESS/32" ```


### Once SSH is open you can 

```ssh -i /path/to/your/private_key.pem ec2-user@<YOUR IP ADDRESS> ```

### Then install python

```python3 --version```

### Find the path to the installed Python interpreter using the which command:
```which python3```

# Note the path to the Python interpreter, exit the SSH session, and update your part2.yml file with the correct path:
eg: 
``[ec2-user@ip-10-0-1-243 ~]$ which python3
/usr/bin/python3```

### Now proceed to part 2, by running:

```ansible-playbook -i hosts.ini part2.yml```

