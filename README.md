Ansible Resolv
==============
Based on: [ypsman/ansible-resolv](https://github.com/ypsman/ansible-resolv)

[![Build Status](https://travis-ci.org/esolitos/ansible-resolv.svg?branch=master)](https://travis-ci.org/esolitos/ansible-resolv)

Handles the `/etc/resolv.conf` configuration: DNS Nameserver and Domain.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: ypsman.resolv
          resolv_dns_domain: 'mydomain.org'
          resolv_searchpath: ['mydomain.local', 'mydomain.org']
          resolv_options:
            - 'rotate'
            - 'timeout:2'
          resolv_dns_server:
            - 8.8.8.8
            - 8.8.4.4
