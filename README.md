# Ansible
A simple Ansible playbook to launch ec2 instances and run commands on them.

## Instrcutions
  - Create `.env` with the necessary environment variables (see example below)
  - Run the commands provided below
  - Add ssh keys to `keys/` folder
  - To run commands on your newly created servers, modify the `inventory` file accordingly

Commands:
```
docker-compose run --name station station

sudo apt-get install ansible
pip install boto

ansible-playbook playbooks/ec2.yml
ansible-playbook -i inventory playbooks/run.yml -vvvv
ansible-playbook -i inventory playbooks/hadoop.yml -vvvv
```

Example `.env` file:
```
AWS_ACCESS_KEY=xxxxxxxxxxxxxxxxxxxx
AWS_SECRET_KEY=xxxxxxxxxxxxxxxxxx/xxxxx/xxxxxxxxxxx/xxx

VPC_SUBNET_ID=subnet-xxxxxxxx
```
