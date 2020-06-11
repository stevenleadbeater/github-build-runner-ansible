# github-build-runner-ansible
A script to set your self hosted build runner up for use with github actions

## Setup and Usage
You will need to go to your repository / organisation settings and click "actions" and "Add Runner" under the "Self-hosted runners" section. The token you get in the subsequent page is time limited and single use. You can then use it as follows:
 
```bash
ansible-playbook ../.ansible/deploy.yml --private-key="REPLACE_THIS_WITH_YOUR_SSH_PRIVATE_KEY" -i {}, -v -u ubuntu -e "token=REPLACE_THIS_WITH_YOUR_TOKEN"
```
