|HTTP Request or Response|HTTP Header|Data type|Purpose|Example|GET|POST|PUT|DELETE|
|---|---|---|---|---|---|---|---|---|
|Request|NZRIS-org-nz-Request-Id|String|API Consumer generated unique transaction ID Provides NZRIS and the API consumer with a “tracking identifier”, which is useful to trace and troubleshoot transactions that have failed This is also used on a POST operation to prevent a transaction from accidentally being replayed|NZRIS-org-nz-Request-Id: C65A1C5A-8F74-4E0B-BA06-16CB47358D85|O|O|O|O|
|Request|Authorization|String|Contains the OAuth token in the format “Authorization: Bearer <token>”|Authorization: Bearer 456789ab-fedc-2345-6543-abcfeda543987|M|M|M|M|
|Request|Accept|String|The NZRIS data provider API will only return responses in JSON format If no Accept header is provided, JSON will be returned anyway If any other format is requested, the PPSR API will return a “406: Not acceptable” response|Accept: application/json|O|O|O|O|
|Request|Content-Type|String|The New PPSR API will only accept JSON requests and will return responses in JSON format If no Content-type header is requested, JSON will be returned anyway If any other format is requested, the PPSR API will return a “406: Not acceptable” response|Content-type: application/json|N/A|M|M|N/A|
|Request|Host|String|Domain name of the NZRIS API gateway hosting the NZRIS data provider API|Host: api.NZRIS.org,nz|M|M|M|M|
|Response|Date|Date|Date/time the response was generated (in Greenwich mean time)|Date: Wed, 18 Nov 2015 21:14:52 GMT|M|M|M|M|
|Response|Service-Version|Version number|Confirm which version (major number only) of the API the response is compliant with|Service-Version: v1 |M|M|M|M|
|Response|Last-Modified|Date|Date/time the returned resource was last updated (in Greenwich mean time)|Last-Modified: Wed, 18 Nov 2015 21:14:52 GMT|M|M|M|M|
|Response|Content-Location|String|Contains a URI of the resource (not provided when a collection is returned)|Content-Location: /services/v1/companies-office/ppsr/financing-statements/FH04R729A8ND9224|C|M|M|M|
|Response|Content-Type|String constant|The structure of the response payload (where one is returned).  The New API will always return JSON|Content-Type: application/json|M|M|M|M|
|Response|NZRIS-org-nz-Request-Id|String|As described in the Request section above.  Only if supplied by consumer in the request.  The same ID is returned to the consumer so that the response can be paired with the request sent (confirmation)|NZRIS-org-nz-Request-Id: C65A1C5A-8F74-4E0B-BA06-16CB47358D85|C|C|C|C|
|Response|NZRIS-org-nz-Correlation-Id |String|NZRIS generated unique ID for the response.|NZRIS-org-nz-Correlation-Id: 514dbf50-4475-4e4d-86ee-e2001f158026|O|M|M|M|
|Response|Cache-Control|String|For reference data API only.  Indicates how long the response can be used / relied upon|Cache-Control: private,max-age=14400,must-revalidate |C|N/A|N/A|N/A|
|Response|Cache-Control|String constant|For all transactional APIs (excluding reference data), the response should not be cached.  Consumers should always GET a fresh copy of the expected resource (confirming ETag) before any PUT operation|Cache-Control: No-cache|C|M|M|N/A|
