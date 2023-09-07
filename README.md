# grafana_agent

Install Grafana Agent on Linux.

**What is Grafana Agent**:  
Grafana Agent is a vendor-neutral, batteries-included telemetry collector developed by Grafana Labs.
It is designed to be flexible, performant, and compatible with multiple ecosystems such as Prometheus and OpenTelemetry.

## Requirements

None.

## Role Variables

All the variables are listed and documented inside the [defaults directory](./defaults/main.yml),
but there's a list of main variables:

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `grafana_agent_variant` | `static` | Choose the Grafana Agent flavour to install |
| `grafana_agent_config_local_path` | `""` | Local path to the Grafana Agent configuration file to upload to the remove host |

## Dependencies

None.

## Example Playbook

```yaml
- name: Install Grafana Agent
  become: true
  hosts: all
  vars:
    grafana_agent_variant: "flow"
    grafana_agent_config_local_path: "{{ playbook_dir }}/files/config.river"
  roles:
    - grafana_agent
```

## License

MIT

## Author Information
FedericoAntoniazzi ([website](https://federicoantoniazzi.dev))
