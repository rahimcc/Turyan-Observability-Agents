# vm-agents


```
vm-observability-agents
├── vm-agent-base/                     # shared across every vm-agent, regardless of app
│   ├── alloy-base.river               # log shipping + prometheus.exporter.unix/cadvisor
│   ├── docker-compose.base.yml        
│   └── README.md
│
└── vm-agents/
    └── airflow-vm/                    # app-specific overlay for Airflow
        ├── alloy-airflow.river        # imports base, adds statsd_exporter component/job
        ├── mapping.yml                # statsd -> prometheus metric mapping
        ├── docker-compose.override.yml
        └── README.md  
```
