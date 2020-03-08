# nullmailer

[![Build Status](https://cloud.drone.io/api/badges/rolehippie/nullmailer/status.svg)](https://cloud.drone.io/rolehippie/nullmailer)

Ansible role to configure nullmailer

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

## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
