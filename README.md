win-baseline
=========

Ansible role to setup OS baseline on windows

```
  - Setup Hostname
  - Set TimeZone
  - Disable Shutdown Button
  - Configure RDP
  - Windows Updates

```


Role Variables
--------------

```
# General Settings
timezone: Arabian Standard Time
shutdown_button_disable: true

# Windows update
win_updates: true
win_updates_category_names: ['CriticalUpdates', 'SecurityUpdates', 'UpdateRollups']
win_updates_reboot: true

# Remote Desktop Service
remote_desktop_enabled: true
remote_desktop_minencryptionLevel: '3'
remote_desktop_port: 3389
remote_desktop_securitylayer: '1'
remote_desktop_group: 'Administrators'
remote_desktop_members: []
bastion_host_ip: 192.168.122.1 #Bastion Host / RDP Source IP / Network 

```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
  - hosts: win
    gather_facts: no 
    roles:
      - role: win-baseline
```
License
-------

MIT

Author Information
------------------

Muhammed Iqbal <iquzart@hotmail.com>
