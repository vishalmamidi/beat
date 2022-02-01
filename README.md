# off metrics

logging.metrics.enabled: false

- type: tcp
  max_message_size: 10MiB
  host: "localhost:9000"
  

## http 

filebeat.inputs:
- type: http_endpoint
  enabled: true
  listen_address: 192.168.1.1
  listen_port: 8080
  response_code: 200
  response_body: '{"message": "success"}'
  url: "/"
  prefix: "json"
  content_type: ""
