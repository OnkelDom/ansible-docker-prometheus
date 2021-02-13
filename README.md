# Ansible Docker Prometheus (untestst)

Playbook to deploy basics and Docker containers with Ansible

Included:
 * nativ - node-exporter
 * nativ - docker host setup
 * docker - prometheus
 * docker - alertmanager
 * docker - grafana
 * docker - blackbox-exporter

 Prepare:

 First of all, clone the following Repos:
 ```
git clone https://github.com/OnkelDom/ansible-docker-prometheus.git
git submodule add git@github.com:OnkelDom/ansible-role-docker.git ansible-docker-prometheus/roles/
git submodule add git@github.com:OnkelDom/ansible-role-node-exporter.git ansible-docker-prometheus/roles/
 ```

 Edit the variables in playbooks/all.yml
 
 Edit the configuration files if needed:
  * files/alertmanager.yml # Alertmanager config file
  * files/prometheus.yml # Prometheus config file
  * files/prometheus-alertrules.yml # Prometheus Alertrules config file
  * files/blackbox-exporter-file-sd.json # Prometheus Job for Blackbox-Exporter file service disvocery
  * files/blackbox-exporter.yml # Blackbox-Exporter config file
  