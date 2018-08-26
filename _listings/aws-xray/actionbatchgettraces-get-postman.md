{
  "info": {
    "name": "AWS X-Ray API Batch Get Traces",
    "_postman_id": "0924625d-a355-4091-819b-6d62cfa56e7d",
    "description": "Retrieves a list of traces specified by ID.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Traces",
      "item": [
        {
          "id": "5f2577be-3779-496d-a1d9-0afd2483b962",
          "name": "batchGetTraces",
          "request": {
            "url": "http://example.com/api/?Action=BatchGetTraces?NextToken=NextToken&TraceIds=TraceIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves a list of traces specified by ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a60244f1-a219-433a-97fe-968cf7eeac2f"
            }
          ]
        }
      ]
    }
  ]
}