{
  "info": {
    "name": "AWS X-Ray API Get Trace Summaries",
    "_postman_id": "44490081-89da-48e4-8f14-d55f1bbaefc5",
    "description": "Retrieves IDs and metadata for traces available for a specified time frame using an\n      optional filter.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Traces",
      "item": [
        {
          "id": "6bcbb243-b3cd-45ad-816e-ab645f4d5a99",
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
              "id": "8d0b8452-69cc-4c31-afad-9499ea400da5"
            }
          ]
        }
      ]
    },
    {
      "name": "Service Graph",
      "item": [
        {
          "id": "f3951f05-6051-4cd2-90c8-2c31d9dc7033",
          "name": "getServiceGraph",
          "request": {
            "url": "http://example.com/api/?Action=GetServiceGraph?EndTime=EndTime&NextToken=NextToken&StartTime=StartTime",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves a document that describes services that process incoming requests, and\n      downstream services that they call as a result."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e8cd99c-d007-46f0-97ae-e35946578b16"
            }
          ]
        }
      ]
    },
    {
      "name": "Trace Graph",
      "item": [
        {
          "id": "0cae9512-7c13-46f2-a44b-b38dad92468d",
          "name": "getTraceGraph",
          "request": {
            "url": "http://example.com/api/?Action=GetTraceGraph?NextToken=NextToken&TraceIds=TraceIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves a service graph for one or more specific trace IDs."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9e385cce-0c77-43f7-8efb-108f1c3b5880"
            }
          ]
        }
      ]
    },
    {
      "name": "Trace Summaries",
      "item": [
        {
          "id": "cb27b765-e8d2-49a5-8347-119351fc74f3",
          "name": "getTraceSummaries",
          "request": {
            "url": "http://example.com/api/?Action=GetTraceSummaries?EndTime=EndTime&FilterExpression=FilterExpression&NextToken=NextToken&Sampling=Sampling&StartTime=StartTime",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves IDs and metadata for traces available for a specified time frame using an\n      optional filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be59ccd0-0f2a-4a3d-8e1d-d8b6bd614cd7"
            }
          ]
        }
      ]
    }
  ]
}