# ledgible-data-docs

## Client Routes
The following guide explains the routes available to Ledgible OAuth clients for interaction with the Ledgible API, including required query parameters and URL formats.
|Route Format     |Description          
|--------------------|--------------------
|`/request/[exchangeName]?user_id=xxxxxx&redirect_uri=xxxxxx&client_id=xxxxxx`<br/><br/> *Example*: https://data-sandbox.ledgible.io/request/kraken?user_id=abc123&redirect_uri=https%3A%2F%2Fmydomain.com%2Fcallback&client_id=xxxxxx<br/><br/> **Required Query Parameters**: <br/> ***redirect_uri*** - encoded callback URI for the client making the request, must match OAuth profile<br />***client_id*** - client ID associated with the client making the request<br/><br/>**Optional Query Parameters**<br/>***entity_name*** - optional display name for the entity making the request for access, to be displayed on OAuth pages, otherwise defaults to generic text|Opens request flow for a given exchange, prompts user to acknowledge data-handling requirements and proceed to respective credential-entry or OAuth flow.
|`/auth/[exchangeName]/update?user_id=xxxxxx&token=xxxxxx&data_source_id=xxxxxx`<br/><br/> *Example*: https://data-sandbox.ledgible.io/auth/kraken/update?user_id=abc123&token=ushDYwhad7d7999shdesjaa&data_source_id=373c4c01-b9b7-43a2-b0e5-e524927b627a<br/><br/> **Required Query Parameters**: <br/>***token*** - valid OAuth access token provided by Ledgible<br />***data_source_id*** - Ledgible system identifier for the specific data source to be updated<br/><br/>**Optional Query Parameters**<br/>*None*|Opens update flow for an existing data source tied to a specific user. If api-based, will ask user to input updated credentials. For OAuth exchanges, it will immediately trigger an OAuth flow to update the user's stored credentials.


## Collection for Insomnia / Postman

https://github.com/Verady/ledgible-data-docs/blob/main/Insomnia_Ledgible-Data.json


## Oauth Client Flow
![OAuth Client Flow - Create Exchange](https://user-images.githubusercontent.com/664512/122285966-bc6be980-cec5-11eb-9fea-10d6d6bc0723.png)

