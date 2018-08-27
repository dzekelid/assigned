swagger: "2.0"
x-collection-name: Instructure
x-complete: 1
info:
  title: Instructure Canvas Utility APIs
  description: canvas-lms-includes-a-rest-api-for-accessing-and-modifying-data-externally-from-the-main-application-in-your-own-programs-and-scripts--
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /group_categories/{group_category_id}/assign_unassigned_members:
    post:
      summary: Assign unassigned members
      description: Assign unassigned members.
      operationId: assign-unassigned-members
      x-api-path-slug: group-categoriesgroup-category-idassign-unassigned-members-post
      parameters:
      - in: query
        name: sync
        description: The assigning is done asynchronously by default
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
      - Assign
      - Unassigned
      - Members