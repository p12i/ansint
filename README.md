# ansint
Ansible inventory helper

``ansint`` is a console tool providing functionality to:
- creating basic skeleton of ansible workspace
- creating basic skeleton of ansible roles
- adding hosts to inventory
- adding grops to inventory
- adding vairables to group and hosts
- adding hosts to groups
- listing hosts, groups and vars

# Examples
- creating workspace in current directory 

  ```ansint init```
- creating workspace in provided directory

  ``` ansint init directory ```
- creating role skeleton under ```roles``` directory

   ``` ansint role webserver ```
- creating role skeleton under provided directory directory

   ``` ansint role webserver -p playbook/roles```
- adding host to inventory

   ``` ansint -I inventory host web01 -i 10.0.0.1 -g werbservers -g atlanta -e port:8080 -e url:http://localhost/```
- adding group to inventory

   ``` ansint -I inventory group database -N -n db01 -n db02```

- adding viariable to host or group

   ``` ansint -I inventory host -A web01  -e foo1:bar -e foo2:bar2```

- listing hosts with variables

   ``` ansint -I inventory list hosts -d ```

- listing hosts in given group

   ``` ansint -I inventory list groups -d grp1```
