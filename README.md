# ssh-access
Grant/Revoke SSH access to a group of instances to a user

#python -c 'import crypt; print(crypt.crypt("dev@somesh123", "$6$random_salt"))'
$6$random_salt$zl.Ziyu.VDOkSJsGF7z5MBymYVVXiz1Nl52n81QbMNxhqx5spc1M4I6HV2.P8ZdeOkFWblZ5d5liKQCyJintZ0


# Use below given command to add new user and grant SSH access
ansible-playbook -i inventory/hosts -l dev-machine -e "operation=grant" site.yml -u somesh -k -K


# Use below given command to revoke SSH access from a user
ansible-playbook -i inventory/hosts -l dev-machine -e "operation=revoke" site.yml -u somesh -k -K
