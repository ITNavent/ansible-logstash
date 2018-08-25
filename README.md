# Ansible Logstash

Rol para instalar Logstash

## Configuración default
(ver logstash.yml.j2)
[https://www.elastic.co/guide/en/logstash/current/logstash-settings-file.html](https://www.elastic.co/guide/en/logstash/current/logstash-settings-file.html)

```yml
logstash_version: 6.4.0

logstash_xms: 1g
logstash_xmx: 1g

logstash_conf_pipeline_id: main
logstash_conf_pipeline_workers: 2
logstash_conf_pipeline_batch_size: 125
logstash_conf_pipeline_batch_delay: 50
logstash_conf_pipeline_unsafe_shutdown: false
logstash_conf_config_test_and_exit: false
logstash_conf_config_reload_automatic: false
logstash_conf_config_reload_interval: 3s
logstash_conf_config_debug: false
logstash_conf_config_support_escapes: false
logstash_conf_queue_type: memory
logstash_conf_queue_page_capacity: 64mb
logstash_conf_queue_max_events: 0
logstash_conf_queue_max_bytes: 1024mb
logstash_conf_queue_checkpoint_acks: 1024
logstash_conf_queue_checkpoint_writes: 1024
logstash_conf_queue_drain: false
logstash_conf_dead_letter_queue_enable: false
logstash_conf_dead_letter_queue_max_bytes: 1024mb
logstash_conf_http_host: 127.0.0.1
logstash_conf_http_port: 9600
logstash_conf_log_level: info
logstash_conf_log_format: plain
```