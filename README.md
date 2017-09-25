# Ansible Logstash

Rol para instalar Logstash

## Configuración default
(ver logstash.yml.j2)

```yml
logstash_group: logstash
logstash_user: logstash
logstash_install_dir: /opt/logstash
logstash_version: 5.2.0
logstash_pipeline_files: []

# Node identity
logstash_node_name: ""

# Data path
logstash_path_data: "{{ logstash_install_dir }}/data"

# Pipeline settings
logstash_pipeline_workers: "{{ ansible_processor_vcpus }}"
logstash_pipeline_output_workers: 1
logstash_pipeline_batch_size: 125
logstash_pipeline_batch_delay: 5
logstash_pipeline_unsafe_shutdown: false

# Pipeline configuration settings
logstash_path_config: "{{ logstash_install_dir }}/config"
logstash_config_string: ""
logstash_config_test_and_exit: false
logstash_config_reload_automatic: false
logstash_config_reload_interval: 3
logstash_config_debug: false

# Queuing Settings
logstash_queue_type: memory
logstash_path_queue: "{{ logstash_path_data }}/queue"
logstash_queue_page_capacity: 250mb
logstash_queue_max_events: 0
logstash_queue_max_bytes: 1024mb
logstash_queue_checkpoint_acks: 1024
logstash_queue_checkpoint_writes: 1024
logstash_queue_checkpoint_interval: 1000

# Metrics Settings
logstash_http_host: "127.0.0.1"
logstash_http_port: "9600-9700"

# Debugging Settings
logstash_log_level: info
logstash_path_logs: "{{ logstash_install_dir }}/logs"

# Other settings
logstash_path_plugins: []
```

## Creacion de pipelines
Crear los archivos ```.conf``` con la configuracion de
los pipelines y utilizar la variable ```logstash_pipeline_files```
para incluirlos.