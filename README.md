# Ansible Role: Supervisor

This role will assume the setup of [supervisord](http://supervisord.org/).

As noted in [ATTRIBUTION](ATTRIBUTION), It is based on https://github.com/ElaoInfra/ansible-role-supervisor

## Requirements

None.

## Dependencies

None.

## Configuration example

```yaml
roles:
- role: ansible-role-supervisor
  supervisor_configs_exclusive: true
  supervisor_configs:
    - file:     foo.conf
      template: program_base.conf.j2
      config:
        -  nginx:
            command: "/usr/sbin/nginx"
            process_name: "/usr/sbin/nginx"
        -  nginx2:
            command: "/usr/sbin/nginx"
            process_name: "/usr/sbin/nginx"
    - file:     bar.conf
      template: program_base.conf.j2
      config:
        -  nginx3:
            command: "/usr/sbin/nginx"
            process_name: "/usr/sbin/nginx"
        -  nginx4:
            command: "/usr/sbin/nginx"
            process_name: "/usr/sbin/nginx"
```

# License

MIT

# Author information

* ReactiveOps **[reactiveops.com](https://www.fairwinds.com/)**
* ELAO [**(http://www.elao.com/)**](http://www.elao.com)
