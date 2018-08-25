---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Assign guarantor to a tenant and vice versa
  version: 1.0.0
  description: Assign guarantor to a tenant and vice versa.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/todo/assignleadstoowningnegotiators:
    put:
      summary: Assign InboundLead Todos to the owning Negotiators of the property.
      description: Assign inboundlead todos to the owning negotiators of the property..
      operationId: DefaultToDo_AssignLeadsToOwningNegotiatorsBytoDoId
      x-api-path-slug: apitodoassignleadstoowningnegotiators-put
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: toDoId
      responses:
        200:
          description: OK
      tags:
      - Assign
      - InboundLead
      - Todos
      - To
      - Owning
      - Negotiators
      - Of
      - Property
  /api/todo/assigntasktonegotiator:
    put:
      summary: Assign a task to a negotiator by its Id.
      description: Assign a task to a negotiator by its id..
      operationId: DefaultToDo_AssignTaskToNegotiatorBytaskIdBynegotiatorId
      x-api-path-slug: apitodoassigntasktonegotiator-put
      parameters:
      - in: query
        name: negotiatorId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: taskId
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Task
      - To
      - Negotiator
      - By
      - Its
      - Id
  /api/todo/assignleadstopredefinedteams:
    put:
      summary: Assign InboundLead Todos to the predefined neg teams. e.g. Sales Valuers,
        Sales Viewings, Lettings Viewings etc etc
      description: Assign inboundlead todos to the predefined neg teams. e.g. sales
        valuers, sales viewings, lettings viewings etc etc.
      operationId: DefaultToDo_AssignLeadsToPredefinedTeamsBytoDoId
      x-api-path-slug: apitodoassignleadstopredefinedteams-put
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: toDoId
      responses:
        200:
          description: OK
      tags:
      - Assign
      - InboundLead
      - Todos
      - To
      - Predefined
      - Neg
      - Teams
      - ""
      - E
      - G
      - ""
      - Sales
      - Valuers
      - ""
      - Sales
      - Viewings
      - ""
      - Lettings
      - Viewings
      - Etc
      - Etc
  /api/todo/assignleadsforspecifiednegs:
    put:
      summary: Assign InboundLead Todos to all the specified Negs using round-robin
        assignement.
      description: Assign inboundlead todos to all the specified negs using round-robin
        assignement..
      operationId: DefaultToDo_AssignLeadsForSpecifiedNegsByassignPropertyLeadsCommandDataContract
      x-api-path-slug: apitodoassignleadsforspecifiednegs-put
      parameters:
      - in: body
        name: assignPropertyLeadsCommandDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Assign
      - InboundLead
      - Todos
      - To
      - ""
      - Specified
      - Negs
      - Using
      - Round-robin
      - Assignement
  /api/progression/lettings/assignguarantortotenant:
    post:
      summary: Assign guarantor to a tenant and vice versa
      description: Assign guarantor to a tenant and vice versa.
      operationId: LettingsProgression_AssignGuarantorToTenantByidBydataContract
      x-api-path-slug: apiprogressionlettingsassignguarantortotenant-post
      parameters:
      - in: body
        name: dataContract
        description: The data contract
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: id
        description: The id of the tenant role
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Guarantor
      - To
      - Tenant
      - Vice
      - Versa
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