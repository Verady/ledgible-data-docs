# ledgible-data-docs

## Client Routes
The following guide explains the routes available to Ledgible OAuth clients for interaction with the Ledgible API, including required query parameters and URL formats.
|Route Format     |Description          
|--------------------|--------------------
|`/request/[exchangeName]?userId=xxxxxxxxxxxx` <br /><br /> *Example*: 'https://data.ledgible.io/request/kraken?userId=xxxxxxxxxxxx'<br /><br /> **Query Parameters**: <br /> - Unique user identifier (required)|Opens request flow for a given exchange, prompts user to acknowledge data-handling requirements and proceed to respective credential-entry or OAuth flow.
|`/auth/[exchangeName]` <br /><br /> *Example*: 'https://data.ledgible.io/request/kraken?userId=xxxxxxxxxxxx'<br /><br /> **Query Parameters**: *N/A*|Allows entry of specific API credentials for the user for the respective exchange.
|`/auth/[exchangeName]/callback?code=xxxxxxxxxxxx&redirect_uri=xxxxxxxxxxxxx` <br /><br /> *Example*: 'https://data.ledgible.io/auth/coinbase/callback?code=xxxxxxxxxxxx&redirect_uri=xxxxxxxxxxxxx'<br /><br /> **Query Parameters**: *N/A*|Callback route for the respective OAuth exchange authentication flow. Accepts required OAuth parameters from exchange OAuth redirect.
|`/update/[exchangeName]` <br /><br /> *Example*: 'https://data.ledgible.io/update/kraken?userId=xxxxxxxxxxxx&exchange_id=xxxxxxxxxxx'<br /><br /> **Query Parameters**: <br /> - Unique user identifier <br /> - Unique exchange identifier |Allows an existing user with an existing exchange to update existing API credentials or re-auth through the exchange's OAuth flow to re-establish access based on matching exchange/uses IDs.


## Collection for Insomnia / Postman

https://github.com/Verady/ledgible-data-docs/blob/main/Insomnia_Ledgible-Data.json
