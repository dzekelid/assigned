---
swagger: "2.0"
x-collection-name: AWS Machine Learning
x-complete: 1
info:
  title: AWS Machine Learning API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteBatchPrediction:
    get:
      summary: Delete Batch Prediction
      description: Assigns the DELETED status to a BatchPrediction, rendering it unusable.
      operationId: deleteBatchPrediction
      x-api-path-slug: actiondeletebatchprediction-get
      parameters:
      - in: query
        name: BatchPredictionId
        description: A user-supplied ID that uniquely identifies the BatchPrediction
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Batches
  /?Action=DeleteDataSource:
    get:
      summary: Delete Data Source
      description: Assigns the DELETED status to a DataSource, rendering it unusable.
      operationId: deleteDataSource
      x-api-path-slug: actiondeletedatasource-get
      parameters:
      - in: query
        name: DataSourceId
        description: A user-supplied ID that uniquely identifies the DataSource
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Data Sources
  /?Action=DeleteEvaluation:
    get:
      summary: Delete Evaluation
      description: Assigns the DELETED status to an Evaluation, rendering it unusable.
      operationId: deleteEvaluation
      x-api-path-slug: actiondeleteevaluation-get
      parameters:
      - in: query
        name: EvaluationId
        description: A user-supplied ID that uniquely identifies the Evaluation to
          delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Evaluations
  /?Action=DeleteMLModel:
    get:
      summary: Delete M L Model
      description: Assigns the DELETED status to an MLModel, rendering it unusable.
      operationId: deleteMLModel
      x-api-path-slug: actiondeletemlmodel-get
      parameters:
      - in: query
        name: MLModelId
        description: A user-supplied ID that uniquely identifies the MLModel
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Models
---