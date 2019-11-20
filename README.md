# Ansible Role: New Relic PHP Agent

[![Ansible Role](https://img.shields.io/badge/role-blackstar257.newrelic--php-blue.svg)](https://galaxy.ansible.com/blackstar257/newrelic-php/)
[![Build Status](https://travis-ci.org/blackstar257/ansible-newrelic-php.svg?branch=master)](https://travis-ci.org/blackstar257/ansible-newrelic-php)

This ansible role installs and configures the New Relic PHP Agent on RHEL/CentOS, Debian & Ubuntu based systems.

## Requirements

This role requires Ansible 2.4 or higher.

## Role Variables

| Name                                                    | Default                                 | Description |
| ------------------------------------------------------- | --------------------------------------- | ----------- |
| newrelic_config_path                                    | "/etc/php.d"                            |             |
| newrelic_agent_extension                                | "newrelic.so"                           |             |
| newrelic_agent_enabled                                  | "true"                                  |             |
| newrelic_license_key                                    | false                                   |             |
| newrelic_agent_logfile                                  | "/var/log/newrelic/php_agent.log"       |             |
| newrelic_agent_loglevel                                 | info                                    |             |
| newrelic_agent_high_security                            | false                                   |             |
| newrelic_agent_appname                                  | "PHP Application"                       |             |
| newrelic_agent_daemon_logfile                           | "/var/log/newrelic/newrelic-daemon.log" |             |
| newrelic_agent_daemon_loglevel                          | info                                    |             |
| newrelic_agent_daemon_port                              | "/tmp/.newrelic.sock"                   |             |
| newrelic_agent_daemon_ssl                               | true                                    |             |
| newrelic_agent_daemon_ssl_ca_bundle                     | false                                   |             |
| newrelic_agent_daemon_ssl_ca_path                       | false                                   |             |
| newrelic_agent_daemon_proxy                             | false                                   |             |
| newrelic_agent_daemon_pidfile                           | false                                   |             |
| newrelic_agent_daemon_location                          | "/usr/bin/newrelic-daemon"              |             |
| newrelic_agent_daemon_collector_host                    | "collector.newrelic.com"                |             |
| newrelic_agent_daemon_dont_launch                       | 0                                       |             |
| newrelic_agent_error_collector_enabled                  | true                                    |             |
| newrelic_agent_error_collector_record_database_errors   | false                                   |             |
| newrelic_agent_error_collector_prioritize_api_errors    | false                                   |             |
| newrelic_agent_browser_monitoring_auto_instrument       | true                                    |             |
| newrelic_agent_transaction_tracer_enabled               | true                                    |             |
| newrelic_agent_transaction_tracer_threshold             | "apdex_f"                               |             |
| newrelic_agent_transaction_tracer_detail                | 1                                       |             |
| newrelic_agent_transaction_tracer_slow_sql              | true                                    |             |
| newrelic_agent_transaction_tracer_stack_trace_threshold | 500                                     |             |
| newrelic_agent_transaction_tracer_explain_enabled       | true                                    |             |
| newrelic_agent_transaction_tracer_explain_threshold     | 500                                     |             |
| newrelic_agent_transaction_tracer_record_sql            | "obfuscated"                            |             |
| newrelic_agent_transaction_tracer_custom                | false                                   |             |
| newrelic_agent_framework                                | false                                   |             |
| newrelic_agent_webtransaction_name_remove_trailing_path | false                                   |             |
| newrelic_agent_webtransaction_name_functions            | false                                   |             |
| newrelic_agent_webtransaction_name_files                | false                                   |             |
| newrelic_agent_daemon_auditlog                          | false                                   |             |
| newrelic_agent_transaction_events_enabled               | true                                    |             |
| newrelic_agent_attributes_enabled                       | true                                    |             |
| newrelic_agent_transaction_events_attributes_enabled    | true                                    |             |
| newrelic_agent_transaction_tracer_attributes_enabled    | true                                    |             |
| newrelic_agent_error_collector_attributes_enabled       | true                                    |             |
| newrelic_agent_browser_monitoring_attributes_enabled    | false                                   |             |
| newrelic_agent_attributes_include                       | false                                   |             |
| newrelic_agent_attributes_exclude                       | false                                   |             |
| newrelic_agent_transaction_events_attributes_include    | false                                   |             |
| newrelic_agent_transaction_events_attributes_exclude    | false                                   |             |
| newrelic_agent_transaction_tracer_attributes_include    | false                                   |             |
| newrelic_agent_transaction_tracer_attributes_exclude    | false                                   |             |
| newrelic_agent_error_collector_attributes_include       | false                                   |             |
| newrelic_agent_error_collector_attributes_exclude       | false                                   |             |
| newrelic_agent_browser_monitoring_attributes_include    | false                                   |             |
| newrelic_agent_browser_monitoring_attributes_exclude    | false                                   |             |
| newrelic_agent_feature_flag                             | false                                   |             |
| newrelic_agent_custom_insights_events_enabled           | true                                    |             |
| newrelic_agent_labels                                   | false                                   |             |
| newrelic_agent_synthetics_enabled                       | true                                    |             |

## Dependencies

blackstar257.newrelic

## Example Playbook

Configure NewRelic agent with defaults.

```yaml
- hosts: all
  roles:
    - {
        role: blackstar257.newrelic-php,
        newrelic_license_key: 0123456789012345678901234567890123456789,
      }
```

## License

BSD

## Author Information

Original Owner Norman Leutner
Forked by blackstar257
