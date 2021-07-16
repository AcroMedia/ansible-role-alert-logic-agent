# ansible-role-alert-logic-agent

![.github/workflows/molecule.yml](https://github.com/AcroMedia/ansible-role-alert-logic-agent/workflows/.github/workflows/molecule.yml/badge.svg)

Install the Alert Logic threat manager / log manager agent to your EC2 app nodes running in an Amazon VPC.

## Requirements

- OS: Ubuntu
- Alert Logic IDS appliance running in your VPC
- Your playbook must gather facts

## Role Variables

- `alert_logic_agent_deb_source`: See defaults/main.yml
- `alert_logic_agent_state`: Can be one of `present` (the default) or `absent`.

## AMIs

AMI ids will probably get out dated time to time. Will have to add new one once it does.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  gather_facts: true
  become: true
  roles:
    - name: Install the alert logic agent
      role: acromedia.alert-logic-agent
```

## License

GPLv3

## Author Information

[Acro Media Inc](https://www.acromedia.com/)
