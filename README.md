# Automated Monitoring Setup with Grafana, Prometheus, and Ansible

## How to Run the Ansible Playbook:

1. Make sure Ansible is installed on your control node.
2. Ensure SSH connectivity to the target monitoring servers.
3. Update the `monitoring.yml` playbook with the appropriate hosts and variables.


4. Run the playbook using the following command:

$ ansible-playbook monitoring.yml -b -u node --ask-become-pass



## Structure of the Ansible Playbook:

- The playbook installs Prometheus and Grafana packages using the `apt` module.
- Configuration files for Prometheus and Grafana are copied using the `template` module.
- Service handlers ensure services are restarted when configuration changes occur.

## Accessing the Grafana Dashboard:

1. Open a web browser and navigate to `http://<grafana_server_ip>:3000`.
2. Log in with the default credentials (username: admin, password: admin).
3. Configure Prometheus as a data source in Grafana.
4. Import the provided Grafana dashboard JSON file for visualization.

## Code Comments:

- Comments are added in the Ansible playbook to explain each task's purpose and usage.
- Configuration file templates include placeholders for dynamic values.

