[![Build Status](https://travis-ci.org/singleplatform-eng/ansible-role-awslogs.svg?branch=master)](https://travis-ci.org/singleplatform-eng/ansible-role-awslogs)

ansible-role-awslogs
=========

Ansible role for installing and configuring the CloudWatch Logs Agent

https://galaxy.ansible.com/singleplatform-eng/awslogs/

Role Variables
--------------

- `awslogs_config`: list of log files to monitor

    Example:
    
        awslogs_config:
          - file: /var/log/syslog
            datetime_format: "%b %d %H:%M:%S"
            log_group_name: syslog

- `awslogs_http_proxy`: The HTTP proxy to use (if any)

- `awslogs_https_proxy`: The HTTPS proxy to use (if any)

Example Playbook
----------------

    - hosts: all
      become: yes
      roles:
          - ansible-role-awslogs

Author Information
------------------

[SinglePlatform Engineering](http://engineering.singleplatform.com/)

License
-------

BSD 3-Clause
