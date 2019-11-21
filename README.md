# Ansible Role: New Relic PHP Agent

[![Ansible Role](https://img.shields.io/badge/role-blackstar257.newrelic-blue.svg)](https://galaxy.ansible.com/blackstar257/newrelic/)
[![Build Status](https://travis-ci.org/blackstar257/ansible-newrelic.svg?branch=master)](https://travis-ci.org/blackstar257/ansible-newrelic)

This ansible role installs and configures the New Relic PHP Agent on RHEL/CentOS, Debian & Ubuntu based systems.

## Requirements

This role requires Ansible 2.4 or higher.

## Role Variables

| Name                                                            | Default                                 | Description |
| --------------------------------------------------------------- | --------------------------------------- | ----------- |
| newrelic_config_path                                            | "/etc/php.d"                            | description |
| newrelic_agent_extension                                        | "newrelic.so"                           | description |
| newrelic_agent_enabled                                          | true                                    | description |
| newrelic_license_key                                            | "REPLACE_WITH_REAL_KEY"                 | description |
| newrelic_agent_logfile                                          | "/var/log/newrelic/php_agent.log"       | description |
| newrelic_agent_loglevel                                         | "info"                                  | description |
| newrelic_agent_high_security                                    | false                                   | description |
| newrelic_agent_appname                                          | "PHP Application"                       | description |
| newrelic_agent_process_host_display_name                        | ""                                      | description |
| newrelic_agent_daemon_logfile                                   | "/var/log/newrelic/newrelic-daemon.log" | description |
| newrelic_agent_daemon_loglevel                                  | "info"                                  | description |
| newrelic_agent_daemon_address                                   | /tmp/.newrelic.sock                     | description |
| newrelic_agent_daemon_ssl_ca_bundle                             | ""                                      | description |
| newrelic_agent_daemon_ssl_ca_path                               | ""                                      | description |
| newrelic_agent_daemon_proxy                                     | ""                                      | description |
| newrelic_agent_daemon_pidfile                                   | ""                                      | description |
| newrelic_agent_daemon_location                                  | /usr/bin/newrelic-daemon                | description |
| newrelic_agent_daemon_collector_host                            | ""                                      | description |
| newrelic_agent_daemon_dont_launch                               | 0                                       | description |
| newrelic_agent_daemon_utilization_detect_aws                    | true                                    | description |
| newrelic_agent_daemon_utilization_detect_azure                  | true                                    | description |
| newrelic_agent_daemon_utilization_detect_gcp                    | true                                    | description |
| newrelic_agent_daemon_utilization_detect_pcf                    | true                                    | description |
| newrelic_agent_daemon_utilization_detect_docker                 | true                                    | description |
| newrelic_agent_daemon_app_timeout                               | 10m                                     | description |
| newrelic_agent_daemon_app_connect_timeout                       | 0                                       | description |
| newrelic_agent_error_collector_enabled                          | true                                    | description |
| newrelic_agent_error_collector_ignore_user_exception_handler    | false                                   | description |
| newrelic_agent_error_collector_ignore_exceptions                | ""                                      | description |
| newrelic_agent_error_collector_ignore_errors                    | ""                                      | description |
| newrelic_agent_error_collector_record_database_errors           | false                                   | description |
| newrelic_agent_error_collector_prioritize_api_errors            | false                                   | description |
| newrelic_agent_browser_monitoring_auto_instrument               | true                                    | description |
| newrelic_agent_transaction_tracer_enabled                       | true                                    | description |
| newrelic_agent_transaction_tracer_threshold                     | apdex_f                                 | description |
| newrelic_agent_transaction_tracer_detail                        | 1                                       | description |
| newrelic_agent_transaction_tracer_slow_sql                      | true                                    | description |
| newrelic_agent_transaction_tracer_stack_trace_threshold         | 500                                     | description |
| newrelic_agent_transaction_tracer_explain_enabled               | true                                    | description |
| newrelic_agent_transaction_tracer_explain_threshold             | 500                                     | description |
| newrelic_agent_transaction_tracer_record_sql                    | obfuscated                              | description |
| newrelic_agent_transaction_tracer_custom                        | ""                                      | description |
| newrelic_agent_transaction_tracer_internal_functions_enabled    | false                                   | description |
| newrelic_agent_framework                                        | ""                                      | description |
| newrelic_agent_webtransaction_name_remove_trailing_path         | false                                   | description |
| newrelic_agent_webtransaction_name_functions                    | ""                                      | description |
| newrelic_agent_webtransaction_name_files                        | ""                                      | description |
| newrelic_agent_daemon_auditlog                                  | ""                                      | description |
| newrelic_agent_transaction_events_enabled                       | true                                    | description |
| newrelic_agent_attributes_enabled                               | true                                    | description |
| newrelic_agent_transaction_events_attributes_enabled            | true                                    | description |
| newrelic_agent_transaction_tracer_attributes_enabled            | true                                    | description |
| newrelic_agent_error_collector_attributes_enabled               | true                                    | description |
| newrelic_agent_browser_monitoring_attributes_enabled            | false                                   | description |
| newrelic_agent_attributes_include                               | ""                                      | description |
| newrelic_agent_attributes_exclude                               | ""                                      | description |
| newrelic_agent_transaction_events_attributes_include            | ""                                      | description |
| newrelic_agent_transaction_events_attributes_exclude            | ""                                      | description |
| newrelic_agent_transaction_tracer_attributes_include            | ""                                      | description |
| newrelic_agent_transaction_tracer_attributes_exclude            | ""                                      | description |
| newrelic_agent_error_collector_attributes_include               | ""                                      | description |
| newrelic_agent_error_collector_attributes_exclude               | ""                                      | description |
| newrelic_agent_browser_monitoring_attributes_include            | ""                                      | description |
| newrelic_agent_browser_monitoring_attributes_exclude            | ""                                      | description |
| newrelic_agent_feature_flag                                     | ""                                      | description |
| newrelic_agent_custom_insights_events_enabled                   | true                                    | description |
| newrelic_agent_labels                                           | ""                                      | description |
| newrelic_agent_synthetics_enabled                               | true                                    | description |
| newrelic_agent_cross_application_tracer_enabled                 | true                                    | description |
| newrelic_agent_distributed_tracing_enabled                      | false                                   | description |
| newrelic_agent_span_events_enabled                              | true                                    | description |
| newrelic_agent_transaction_tracer_gather_input_queries          | true                                    | description |
| newrelic_agent_error_collector_capture_events                   | true                                    | description |
| newrelic_agent_guzzle_enabled                                   | true                                    | description |
| newrelic_agent_phpunit_events_enabled                           | false                                   | description |
| newrelic_agent_datastore_tracer_instance_reporting_enabled      | true                                    | description |
| newrelic_agent_datastore_tracer_database_name_reporting_enabled | true                                    | description |
| newrelic_agent_security_policies_token                          | ""                                      | description |

## Dependencies

None

## Example Playbook

Configure NewRelic agent with defaults.

```yaml
- hosts: all
  roles:
    - {
        role: blackstar257.newrelic,
        newrelic_license_key: 0123456789012345678901234567890123456789,
      }
```

## License

BSD

## Author Information

Original Owner Norman Leutner
Forked by blackstar257
