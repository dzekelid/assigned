---
swagger: "2.0"
x-collection-name: SendGrid
x-complete: 0
info:
  title: SendGrid Get Ips Assigned
  description: |-
    **This endpoint allows you to retrieve only assigned IP addresses.**

    A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ips/assigned:
    get:
      summary: Get Ips Assigned
      description: |-
        **This endpoint allows you to retrieve only assigned IP addresses.**

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: ips.assigned.get
      x-api-path-slug: ipsassigned-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Assigned
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---