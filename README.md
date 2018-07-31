Role Name
=========

ClamAV is an open source antivirus engine for detecting trojans, viruses,
malware & other malicious threats.

Requirements
------------

* Ubuntu server 18.04


Role Variables
--------------

- clam_msg     
- clam_from    
- clam_to      
- clam_options 
- clam_include 
- clam_exclude

Dependencies
------------

- Postfix

Example Playbook
----------------

    - hosts: servers
      vars:
        # ClamAV settings
        clam_msg     : 'ClamAV found {{ ansible_hostname }}'
        clam_from    : 'clamav@example.net'
        clam_to      : 'example@example.net'
        clam_options : '-ri'
        clam_include : '/home /opt'
        clam_exclude : '/tmp'

      roles:
         - sec-clamav

License
-------

GPLv3

Author Information
------------------

E: lrutten@bitfinity.nl
I: https://www.bitfinity.nl
