# ansible-role-filebeats

Example vars:

```
install_filebeat: present

filebeat:
    filebeat:
      prospectors:
        -
          paths:
            - /var/log/syslog
          input_type: log
          document_type: syslog
      registry_file: /var/lib/filebeat/registry
    output:
      logstash:
        hosts: ["localhost:5044"]
    logging:
      files:
        rotateeverybytes: 10485760 # = 10MB
```
