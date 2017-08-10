jimwitte.mongodb
==============
Install mongodb for Ubuntu 16.04. Optionally disable "transparent huge pages".

Details
-------
The script for disabling tranparent huge pages is installed as a systemd service, runs when system is started.
mongodb is also installed as a systemd service.

Requirements
------------
systemd: installs systemd service units
tested with Ubuntu 16.04 and mongodb 3.4, ansible 2.3.1

Role Variables
--------------
Default role variables and values:

```
mongodb_db_path: "/srv/data/mongodb"
mongodb_log_path: "/var/log/mongodb/mongod.log"
mongodb_configure_thp: "true"
mongodb_bind_ip: "127.0.0.1"
mongodb_port: "27017"
mongodb_version: "3.4"
mongodb_disable_thp_script_path: "/usr/local/bin"
```

Example Playbook
----------------
    - hosts: servers
      roles:
         - {role: jimwitte.mongodb}

License
-------
BSD

Author Information
------------------
Jim Witte
jim@thunderingbison.com
