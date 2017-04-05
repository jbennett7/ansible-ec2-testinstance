# ansible-ec2-testinstance

- to be used as a role.
- place aws key information in vars directory.

```
ansible-vault edit vars/aws_access.yml
ec2_username: 'user'
ec2_access_key: 'KEYKEY'
ec2_secret_key: 'secretSECRET'
ec2_console_login_link: 'https://11111112.signin.aws.amazon.com/console'
```

```
echo "aws_access_key_password" > .aws_access.pwd
```

- this role can be tested after previous has been set up:
```
ansible-playbook -i inventory test_e2instances.yml --vault-password-file=.aws_access.pwd --tags test
```
