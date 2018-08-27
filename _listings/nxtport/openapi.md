swagger: "2.0"
x-collection-name: NxtPort
x-complete: 1
info:
  title: Portcall+ API (sandbox)
  description: portplus-api
  version: 1.0.0
host: api-sb.nxtport.eu
basePath: /PortCallPlus/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/pickup_rights/{id}/assign:
    put:
      summary: Assign
      description: Assign the PickupRight to a truck driver.
      operationId: putApiV1PickupRightsAssign
      x-api-path-slug: apiv1pickup-rightsidassign-put
      parameters:
      - in: query
        name: api_token
        description: authentication token of user making the request
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: id of the PickupRight as reported by List PickupRights
      responses:
        200:
          description: OK
      tags:
      - Assign
  /api/v1/pickup_rights/{id}/revoke_assignment:
    put:
      summary: Revoke Assignment
      description: Revoke the current PickupRight assignment. This must be used in
        case you did an assign of a PickupRight to a driver and you want to cancel
        this. This action is only possible as long as the PickupRight is not exercised.
      operationId: putApiV1PickupRightsRevokeAssignment
      x-api-path-slug: apiv1pickup-rightsidrevoke-assignment-put
      parameters:
      - in: query
        name: api_token
        description: authentication token of user making the request
      - in: path
        name: id
        description: id of the PickupRight as reported by List PickupRights
      responses:
        200:
          description: OK
      tags:
      - Revoke
      - Assignment