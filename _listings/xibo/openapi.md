---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 1
info:
  title: Xibo API
  description: xibo-cms-api
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
  /campaign/layout/assign/{campaignId}:
    post:
      summary: Assign Layouts
      description: Assign Layouts to a Campaign
      operationId: campaignAssignLayout
      x-api-path-slug: campaignlayoutassigncampaignid-post
      parameters:
      - in: path
        name: campaignId
        description: The Campaign ID
      - in: formData
        name: layoutId
        description: Array of Layout ID/Display Orders to Assign
      - in: formData
        name: unassignLayoutId
        description: Array of Layout ID/Display Orders to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Layouts
  /displaygroup/{displayGroupId}/display/assign:
    post:
      summary: Assign one or more Displays to a Display Group
      description: Adds the provided Displays to the Display Group
      operationId: displayGroupDisplayAssign
      x-api-path-slug: displaygroupdisplaygroupiddisplayassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: displayId
        description: The Display Ids to assign
      - in: formData
        name: unassignDisplayId
        description: An optional array of Display IDs to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Displays
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/displayGroup/assign:
    post:
      summary: Assign one or more DisplayGroups to a Display Group
      description: Adds the provided DisplayGroups to the Display Group
      operationId: displayGroupDisplayGroupAssign
      x-api-path-slug: displaygroupdisplaygroupiddisplaygroupassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: displayGroupId
        description: The displayGroup Ids to assign
      - in: formData
        name: unassignDisplayGroupId
        description: An optional array of displayGroup IDs to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - DisplayGroups
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/media/assign:
    post:
      summary: Assign one or more Media items to a Display Group
      description: Adds the provided Media to the Display Group
      operationId: displayGroupMediaAssign
      x-api-path-slug: displaygroupdisplaygroupidmediaassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: mediaId
        description: The Media Ids to assign
      - in: formData
        name: unassignMediaId
        description: Optional array of Media Id to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Media
      - Items
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/layout/assign:
    post:
      summary: Assign one or more Layouts items to a Display Group
      description: Adds the provided Layouts to the Display Group
      operationId: displayGroupLayoutsAssign
      x-api-path-slug: displaygroupdisplaygroupidlayoutassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: layoutId
        description: The Layouts Ids to assign
      - in: formData
        name: unassignLayoutId
        description: Optional array of Layouts Id to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Layouts
      - Items
      - To
      - Display
      - Group
  /playlist/library/assign/{playlistId}:
    post:
      summary: Assign Library Items
      description: Assign Media from the Library to this Playlist
      operationId: playlistLibraryAssign
      x-api-path-slug: playlistlibraryassignplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Optional duration for all Media in this assignment to use on
          the Widget
      - in: formData
        name: media
        description: Array of Media IDs to assign
      - in: path
        name: playlistId
        description: The Playlist ID to assign to
      - in: formData
        name: useDuration
        description: Optional flag indicating whether to enable the useDuration field
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Library
      - Items
---