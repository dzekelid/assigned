---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Assign Private Ip Addresses
  version: 1.0.0
  description: Assigns one or more secondary private IP addresses to the specified
    network interface.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AssignIpv6Addresses:
    get:
      summary: Assign Ipv6 Addresses
      description: Assigns one or more IPv6 addresses to the specified network interface.
      operationId: assignipv6addresses
      x-api-path-slug: actionassignipv6addresses-get
      parameters:
      - in: query
        name: AllowReassignment
        description: Indicates whether to allow an IP address that is already assigned
          to another network interface or instance to be reassigned to the specified
          network interface
        type: string
      - in: query
        name: NetworkInterfaceId
        description: The ID of the network interface
        type: string
      - in: query
        name: PrivateIpAddress.N
        description: One or more IP addresses to be assigned as a secondary private
          IP address to the network interface
        type: string
      - in: query
        name: SecondaryPrivateIpAddressCount
        description: The number of secondary IP addresses to assign to the network
          interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - IP Address
  /?Action=AssignPrivateIpAddresses:
    get:
      summary: Assign Private Ip Addresses
      description: Assigns one or more secondary private IP addresses to the specified
        network interface.
      operationId: assignprivateipaddresses
      x-api-path-slug: actionassignprivateipaddresses-get
      parameters:
      - in: query
        name: DeviceIndex
        description: The index of the device for the network interface attachment
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: NetworkInterfaceId
        description: The ID of the network interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - IP Address
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