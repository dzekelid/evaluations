---
swagger: "2.0"
x-collection-name: AWS Machine Learning
x-complete: 0
info:
  title: AWS Machine Learning API Get Evaluation
  version: 1.0.0
  description: Returns an Evaluation that includes metadata as well as the current
    status of the Evaluation.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateEvaluation:
    get:
      summary: Create Evaluation
      description: Creates a new Evaluation of an MLModel.
      operationId: createEvaluation
      x-api-path-slug: actioncreateevaluation-get
      parameters:
      - in: query
        name: EvaluationDataSourceId
        description: The ID of the DataSource for the evaluation
        type: string
      - in: query
        name: EvaluationId
        description: A user-supplied ID that uniquely identifies the Evaluation
        type: string
      - in: query
        name: EvaluationName
        description: A user-supplied name or description of the Evaluation
        type: string
      - in: query
        name: MLModelId
        description: The ID of the MLModel to evaluate
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Evaluations
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
  /?Action=DescribeEvaluations:
    get:
      summary: Describe Evaluations
      description: Returns a list of DescribeEvaluations that match the search criteria
        in the request.
      operationId: describeEvaluations
      x-api-path-slug: actiondescribeevaluations-get
      parameters:
      - in: query
        name: EQ
        description: The equal to operator
        type: string
      - in: query
        name: FilterVariable
        description: 'Use one of the following variable to filter a list of Evaluation
          objects:'
        type: string
      - in: query
        name: GE
        description: The greater than or equal to operator
        type: string
      - in: query
        name: GT
        description: The greater than operator
        type: string
      - in: query
        name: LE
        description: The less than or equal to operator
        type: string
      - in: query
        name: Limit
        description: The maximum number of Evaluation to include in the result
        type: string
      - in: query
        name: LT
        description: The less than operator
        type: string
      - in: query
        name: NE
        description: The not equal to operator
        type: string
      - in: query
        name: NextToken
        description: The ID of the page in the paginated results
        type: string
      - in: query
        name: Prefix
        description: A string that is found at the beginning of a variable, such as
          Name or Id
        type: string
      - in: query
        name: SortOrder
        description: A two-value parameter that determines the sequence of the resulting
          list of Evaluation
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Evaluations
  /?Action=GetEvaluation:
    get:
      summary: Get Evaluation
      description: Returns an Evaluation that includes metadata as well as the current
        status of the Evaluation.
      operationId: getEvaluation
      x-api-path-slug: actiongetevaluation-get
      parameters:
      - in: query
        name: EvaluationId
        description: The ID of the Evaluation to retrieve
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Evaluations
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