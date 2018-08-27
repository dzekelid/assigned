swagger: "2.0"
x-collection-name: SendGrid
x-complete: 1
info:
  title: SendGrid
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