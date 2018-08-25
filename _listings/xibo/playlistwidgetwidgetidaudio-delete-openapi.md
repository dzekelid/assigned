---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Delete assigned audio widget
  description: Delete assigned audio widget from specified widget ID
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /playlist/widget/{widgetId}/audio:
    delete:
      summary: Delete assigned audio widget
      description: Delete assigned audio widget from specified widget ID
      operationId: WidgetAudioDelete
      x-api-path-slug: playlistwidgetwidgetidaudio-delete
      parameters:
      - in: path
        name: widgetId
        description: Id of a widget from which you want to delete the audio from
      responses:
        200:
          description: OK
      tags:
      - Assigned
      - Audio
      - Widget
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