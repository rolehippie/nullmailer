# nullmailer

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/nullmailer)
[![General Workflow](https://github.com/rolehippie/nullmailer/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/nullmailer/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/nullmailer/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/nullmailer/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/nullmailer/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/nullmailer/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/nullmailer)](https://github.com/rolehippie/nullmailer/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.nullmailer-blue)](https://galaxy.ansible.com/rolehippie/nullmailer)

Ansible role to install and configure nullmailer relay MTA.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [nullmailer_adminaddr](#nullmailer_adminaddr)
  - [nullmailer_allmailfrom](#nullmailer_allmailfrom)
  - [nullmailer_auth_login](#nullmailer_auth_login)
  - [nullmailer_default_aliases](#nullmailer_default_aliases)
  - [nullmailer_defaultdomain](#nullmailer_defaultdomain)
  - [nullmailer_enabled](#nullmailer_enabled)
  - [nullmailer_extra_aliases](#nullmailer_extra_aliases)
  - [nullmailer_host](#nullmailer_host)
  - [nullmailer_password](#nullmailer_password)
  - [nullmailer_port](#nullmailer_port)
  - [nullmailer_sendmail_overwrite](#nullmailer_sendmail_overwrite)
  - [nullmailer_ssl](#nullmailer_ssl)
  - [nullmailer_tls](#nullmailer_tls)
  - [nullmailer_username](#nullmailer_username)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### nullmailer_adminaddr

Admin address as default sender

#### Default value

```YAML
nullmailer_adminaddr: root
```

### nullmailer_allmailfrom

Define an address that's always used as sender

#### Default value

```YAML
nullmailer_allmailfrom:
```

### nullmailer_auth_login

Force SMTP "AUTH LOGIN" mode instead of auto-detecting.

#### Default value

```YAML
nullmailer_auth_login: false
```

### nullmailer_default_aliases

List of default mail aliases

#### Default value

```YAML
nullmailer_default_aliases:
  - alias: mailer-daemon
    recipient: postmaster
  - alias: postmaster
    recipient: root
  - alias: nobody
    recipient: root
  - alias: hostmaster
    recipient: root
  - alias: usenet
    recipient: root
  - alias: news
    recipient: root
  - alias: webmaster
    recipient: root
  - alias: www
    recipient: root
  - alias: ftp
    recipient: root
  - alias: abuse
    recipient: root
  - alias: noc
    recipient: root
  - alias: security
    recipient: root
```

#### Example usage

```YAML
nullmailer_default_aliases:
  - alias: root
    recipient: user1@example.com
  - alias: postmaster
    recipients:
      - user1@example.com
      - user2@example.com
      - user3@example.com
```

### nullmailer_defaultdomain

Default domain used for nullmailer

#### Default value

```YAML
nullmailer_defaultdomain: '{{ ansible_fqdn }}'
```

### nullmailer_enabled

Enable nullmailer installation optionally

#### Default value

```YAML
nullmailer_enabled: true
```

### nullmailer_extra_aliases

List of extra mail aliases

#### Default value

```YAML
nullmailer_extra_aliases: []
```

#### Example usage

```YAML
nullmailer_extra_aliases:
  - alias: root
    recipient: user1@example.com
  - alias: postmaster
    recipients:
      - user1@example.com
      - user2@example.com
      - user3@example.com
```

### nullmailer_host

Host for remote connection

#### Default value

```YAML
nullmailer_host:
```

### nullmailer_password

Password for remote connection

#### Default value

```YAML
nullmailer_password:
```

### nullmailer_port

Port for remote connection

#### Default value

```YAML
nullmailer_port:
```

### nullmailer_sendmail_overwrite

Enforce a sendmail wrapper for old versions

#### Default value

```YAML
nullmailer_sendmail_overwrite: "{{ (false if nullmailer_allmailfrom is none else true)
  and ansible_distribution_version is version('16.04', '<=') }}"
```

### nullmailer_ssl

Enable SSL for remote connection

#### Default value

```YAML
nullmailer_ssl: false
```

### nullmailer_tls

Enable STARTTLS for remote connection

#### Default value

```YAML
nullmailer_tls: false
```

### nullmailer_username

Username for remote connection

#### Default value

```YAML
nullmailer_username:
```

## Discovered Tags

**_nullmailer_**

## Dependencies

- [community.general](https://github.com/ansible-collections/community.general)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
