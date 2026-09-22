# vm-agents

observability/
  vm-agent-base/          # shared: alloy logs, node_exporter, cadvisor
    alloy-base.river
    docker-compose.base.yml
  vm-agents/
    airflow-vm/
      alloy-airflow.river      # imports/extends base + adds statsd bits
      mapping.yml
      docker-compose.override.yml
