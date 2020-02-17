# Ansible Role: Installs Spacewalk package management system

Installs Spacewalk client.

[![Build Status](https://travis-ci.org/KAMI911/ansible-role-spcewalk.svg?branch=master)](https://travis-ci.org/KAMI911/ansible-role-spacewalk-client)

## Table of Contents

1. [Requirements][Requirements]
2. [Installation][Installation]
3. [Role Variables][Role Variables]
4. [Dependencies][Dependencies]
5. [Example Playbook][Example Playbook]
6. [Licensing][Licensing]
7. [Author Information][Author Information]
8. [Support][Support]
9. [Contributing][Contributing]
10. [Donation][Donation]

## Requirements

None.

## Role Variables

    spacewalk_client_manage_service: true



    spacewalk_client_service_enabled: true



    spacewalk_client_service_status: 'restarted'  # Possible values are: reloaded, restarted, started, stopped



    force_spacewalk_client_install: false



    spacewalk_client_installer_force_download: true



    spacewalk_client_installer_force_overwrite: true



    spacewalk_client_installer_keep: true



    spacewalk_client_installer_local: false  # The true means try to copy from Ansible's local files folder



    spacewalk_client_cert_url: http://spw.example.com/pub/rhn-org-trusted-ssl-cert-1.0-1.noarch.rpm



    spacewalk_client_server_url: http://spw.example.com/XMLRPC



    spacewalk_client_ca_cert_path: /usr/share/rhn/RHN-ORG-TRUSTED-SSL-CERT



    spacewalk_client_activation_key: ACTIVATION-KEY



    spacewalk_client_download_validate_certs: 'yes'

This variable sometimes does not get set and shouldn't be relied on.

    spacewalk_client_ansible_distribution_major_version: '{{ ansible_distribution_major_version|int }}'



    spacewalk_client_el6_url: http://yum.spacewalkproject.org/2.6-client/RHEL/6/x86_64/spacewalk-client-repo-2.6-0.el6.noarch.rpm



    spacewalk_client_el7_url: https://copr-be.cloud.fedoraproject.org/results/%40spacewalkproject/spacewalk-2.9-client/epel-7-x86_64/00911911-spacewalk-repo/spacewalk-client-repo-2.9-4.el7.noarch.rpm



    spacewalk_client_proxy_yum_url:



    spacewalk_client_proxy_yum_username:



    spacewalk_client_proxy_yum_password:



    spacewalk_client_proxy_remove_after: true



    spacewalk_client_install_dir: /opt/



    spacewalk_client_dir_mode: '0770'



    spacewalk_client_file_mode: '0660'



    spacewalk_client_root_user: 'root'



    spacewalk_client_root_group: 'root'



    spacewalk_client_download_dir: '{{ spacewalk_client_install_dir }}/tmp'



    spacewalk_client_service_name: osad



    spacewalk_client_installed: false



## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - spacewalk-client

## Licensing

The Spacewalk Ansible Role application and documantations are licensed under the terms of
the MIT / BSD, you will find a copy of this license in the
[LICENSE](LICENSE) file included in the source package.

## Author Information

This role was created in 2019 by Kálmán Szalai - KAMI

## Support

If you have any question, do not hesitate and drop me a line.
If you found a bug, or have a feature request, you can [fill an issue](https://github.com/KAMI911/ansible-role-spacewalk-client/issues).

### Using as a submudule of an AWX playbook

#### Add as a submodule

```
git submodule add --force git@github.com:KAMI911/ansible-role-spacewalk-client.git roles/spacewalk-client
```

#### Update as sumodule

Update only this submodule

```
git submodule update --remote roles/spacewalk-client/
```

Update all submodules:

```
git submodule foreach git pull origin master
```

## Contributing

There are many ways to contribute to ansible-role-spacewalk-client -- whether it be sending patches,
testing, reporting bugs, or reviewing and updating the documentation. Every
contribution is appreciated!

Please continue reading in the [contributing chapter](CONTRIBUTING.md).

### Fork me on Github

https://github.com/KAMI911/ansible-role-spacewalk-client

Add a new remote `upstream` with this repository as value.

```
git remote add upstream https://github.com/KAMI911/ansible-role-spacewalk-client.git
```

You can pull updates to your fork's master branch:

```
git fetch --all
git pull upstream HEAD
```

## Donation

If you find this useful, please consider a donation:

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RLQZ58B26XSLA)

<!-- TOC URLs -->
[Requirements]: #requirements
[Installation]: #installation
[Role Variables]: #role_variables
[Dependencies]: #dependencies
[Example Playbook]: #example_playbook
[Licensing]: #licensing
[Author Information]: #author_information
[Support]: #support
[Contributing]: #contributing
[Donation]: #donation
