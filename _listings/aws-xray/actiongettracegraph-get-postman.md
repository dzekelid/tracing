{
  "info": {
    "name": "AWS X-Ray API Get Trace Graph",
    "_postman_id": "dd062329-7298-4b9f-8d07-f886beb42059",
    "description": "Retrieves a service graph for one or more specific trace IDs.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Traces",
      "item": [
        {
          "id": "b04e1fa5-9f79-42c0-9992-84dc2183410e",
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
              "id": "3e0c302e-8ec9-4427-b98d-8b7a0d2694ba"
            }
          ]
        }
      ]
    },
    {
      "name": "Service Graph",
      "item": [
        {
          "id": "acbe0a7d-7f6b-4dfc-860b-2d1cbd63a790",
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
              "id": "ddfc5147-7436-4f11-a33c-ca1405326aec"
            }
          ]
        }
      ]
    },
    {
      "name": "Trace Graph",
      "item": [
        {
          "id": "d298c759-1d5f-4b99-b6f1-80266fb8781f",
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
              "id": "e7c574b0-fdc5-4c05-a781-4506c92fdc66"
            }
          ]
        }
      ]
    }
  ]
}