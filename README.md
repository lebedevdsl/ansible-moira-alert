lebedevdsl.moira-alert
=========



Requirements
------------

Path to packages needed

Role Variables
--------------

Naming: 
``` <namespace>_<component>_variable ```

Most of them are selfexplanatory. Refer to moira documentation https://moira.readthedocs.io/en/latest/installation/configuration.html.  Defaults listed as in template.

```
moira_web_package: moira-web
moira_cache_package: moira-cache
moira_notifier_package: moira-notifier
moira_worker_package: moira-worker

moira_redis_host: localhost
moira_redis_port: 6379

moira_graphite_host: 'localhost'
moira_graphite_prefix: 'moira'
moira_graphite_interval: 60

moira_cache_log_file: '/var/log/moira/cache/cache.log'
moira_cache_listen: ':2003'
moira_cache_retentions: '/etc/moira/storage-schemas.conf'
moira_cache_pidfile: '/var/run/moira/moira-cache.pid'

moira_worker_log_dir: '/var/log/moira/worker'
moira_worker_log_level: 'info'

moira_api_port: 8081
moira_api_listen: '127.0.0.1'

moira_checker_nodata_interval: 60
moira_checker_check_interval: 5
moira_checker_metrics_ttl: 3600
moira_checker_stop_checking_interval: 30

moira_web_uri: 'http://localhost'

moira_notifier_log_file: '/var/log/moira/notifier/notifier.log'
moira_notifier_log_level: 'debug'
moira_notifier_log_color: 'true'
moira_notifier_sender_timeout: '10s0ms'
moira_notifier_resending_timeout: '24:00'

moira_sender_mail_smtp_host: 'smtp.example.com'
moira_sender_mail_smtp_port: 25
moira_sender_mail_smtp_pass: ''
moira_sender_mail_smtp_user: ''
moira_sender_mail_mail_from: 'moira@gmail.com'
moira_sender_mail_insecure_tls: 'false'

```


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: lebedevdsl.moira-alert, become: yes }

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
