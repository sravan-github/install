root@ansible-instance-12:/home/gcpuser/install# ansible-vault decrypt in_var.yml --vault-password-file file.yml
Decryption successful
root@ansible-instance-12:/home/gcpuser/install# ansible-playbook -i hosts install.yml

PLAY [localhost] ********************************************************************************************************************************************

TASK [include_vars] *****************************************************************************************************************************************
ok: [localhost]

TASK [Installing {{ packages }} on {{ hostname }}] **********************************************************************************************************
ok: [localhost] => (item=[u'wget', u'net-tools', u'git', u'maven', u'openjdk-11-jdk'])

PLAY RECAP **************************************************************************************************************************************************
localhost                  : ok=2    changed=0    unreachable=0    failed=0
