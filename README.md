# nullmailer

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/nullmailer) [![Build Status](https://img.shields.io/drone/build/rolehippie/nullmailer/master?logo=drone)](https://cloud.drone.io/rolehippie/nullmailer) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/nullmailer)](https://github.com/rolehippie/nullmailer/blob/master/LICENSE) 

Ansible role to install and configure nullmailer relay MTA. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [nullmailer_adminaddr](#nullmailer_adminaddr)
  * [nullmailer_defaultdomain](#nullmailer_defaultdomain)
  * [nullmailer_host](#nullmailer_host)
  * [nullmailer_password](#nullmailer_password)
  * [nullmailer_port](#nullmailer_port)
  * [nullmailer_ssl](#nullmailer_ssl)
  * [nullmailer_tls](#nullmailer_tls)
  * [nullmailer_username](#nullmailer_username)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### nullmailer_adminaddr

Admin address as default sender

#### Default value

```YAML
nullmailer_adminaddr: root
```

### nullmailer_defaultdomain

Default domain used for nullmailer

#### Default value

```YAML
nullmailer_defaultdomain: '{{ ansible_fqdn }}'
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

### nullmailer_ssl

Enable SSL for remote connection

#### Default value

```YAML
nullmailer_ssl: true
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

## Dependencies

* None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
