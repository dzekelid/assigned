swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/project/{projectKeyOrId}/permissionscheme:
    get:
      summary: Get assigned permission scheme
      description: |-
        Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.getAssignedPermissionScheme_ge
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assigned
      - Permission
      - Scheme
    put:
      summary: Assign permission scheme
      description: |-
        Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.assignPermissionScheme_put
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Permission
      - Scheme
  /api/2/issue/{issueIdOrKey}/assignee:
    put:
      summary: Assign issue
      description: Assigns the issue to the user. Use this resource to assign issues
        for the users having "Assign Issue" permission, and not having the "Edit Issue"
        permission. If `name` body parameter is set to "-1" then automatic issue assignee
        is used. A `name` set to `null` will remove the assignee.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.assignIssue_put
      x-api-path-slug: api2issueissueidorkeyassignee-put
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to be updated
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Issue
  /api/2/mypermissions:
    get:
      summary: Get my permissions
      description: |-
        Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

        If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

        If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

        If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

        The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

        Global permissions work in the same way regardless of the scope.
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getMyPermissions_get
      x-api-path-slug: api2mypermissions-get
      parameters:
      - in: query
        name: issueId
        description: Id of the issue to scope returned permissions for
      - in: query
        name: issueKey
        description: Key of the issue to scope returned permissions for
      - in: query
        name: permissions
        description: A comma separated list of permission keys to check
      - in: query
        name: projectId
        description: Id of project to scope returned permissions for
      - in: query
        name: projectKey
        description: Key of project to scope returned permissions for
      responses:
        200:
          description: OK
      tags:
      - My
      - Permissions
  /api/2/notificationscheme:
    get:
      summary: Get notification schemes paginated
      description: |-
        Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) list of [notification schemes](https://confluence.atlassian.com/x/8YdKLg) in order by display name.

        ### About notification schemes

        A notification scheme is a list of events and recipients who will receive notifications for those events. The list is contained within the `notificationSchemeEvents` object and contains pairs of `events` and `notifications`:

        *   `event` Identifies the type of event. The events can be [Jira system events](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-eventsEvents) or [custom events](https://confluence.atlassian.com/x/AIlKLg).
        *   `notifications` Identifies the [recipients](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-recipientsRecipients) of notifications for each event. Recipients can be any of the following types:

        *   `CurrentAssignee`
        *   `Reporter`
        *   `CurrentUser`
        *   `ProjectLead`
        *   `ComponentLead`
        *   `User` (the `parameter` is the user key)
        *   `Group` (the `parameter` is the group name)
        *   `ProjectRole` (the `parameter` is the project role ID)
        *   `EmailAddress`
        *   `AllWatchers`
        *   `UserCustomField` (the `parameter` is the ID of the custom field)
        *   `GroupCustomField`(the `parameter` is the ID of the custom field)

        _Note that you should allow for events without recipients to appear in responses._

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with a notification scheme for it to be returned.
      operationId: com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationSchemes_get
      x-api-path-slug: api2notificationscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Schemes
      - Paginated