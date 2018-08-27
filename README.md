# MIBCloud 3rdparty Getting started

## API reference
### Rest
#### Overview
URIs relative to https://a.prota.space/v1, unless otherwise noted

###### Authorization

Need to request with an access token. it is presented in https://console.microbot.is.

Example:

* curl
```http
$ curl '{REST_API_URL}' -i -H 'Authorization Bearer: {access_token}'
```

###### Request

Only supports a json format.

###### Response

Return value type is a json format.

#### APIs
##### Users
###### Gets a user's data by email.
HTTP Request

```http
GET https://a.prota.space/v1/users/{email}
```

Parameters

* Path paramters

| Parameter name | value | description |
| --- | --- | --- |
| email | string | User's email address registered in the MIBcloud |

Request body

* Do not supply a request body with this method.

Response

* Type: application/json

| key | value | description |
| --- | --- | --- |
| id | string | The ID for user registered in the MIBcloud |
| email | string | User's email address registered in the MIBcloud |
| language | string | Default language code of user |
| account_ids | string list | The IDs associated with user |

Example

* cURL

```http
$ curl 'https://a.prota.space/v1/users/{email}' -i -H 'Authorization Bearer: {access_token}'
```

##### Products
###### Gets gadgets data of a product by product id
HTTP Request

```http
GET https://a.prota.space/v1/products/{product_id}/gadgets
```

Parameters

* Path paramters

| Parameter name | value | description |
| --- | --- | --- |
| product_id | string | Product ID to get gadgets |

Request body

* Do not supply a request body with this method.

Response

* Type: application/json

| key | value | description |
| --- | --- | --- |
| id | string | The ID for user registered in the MIBcloud |
| mac | string | User's email address registered in the MIBcloud |
| name | string | Default language code of user |
| kind | string | The IDs associated with user |
| firmware_version | string | The IDs associated with user |
| sdk_version | string | The IDs associated with user |
| model_number | string | The IDs associated with user |
| model_name | string | The IDs associated with user |
| hub_id | string | The IDs associated with user |
| account_id | string | The IDs associated with user |
| user_id | string | The IDs associated with user |
| status | string | The IDs associated with user |
| rssi | string | The IDs associated with user |
| battery | string | The IDs associated with user |

Example

* cURL

```http
$ curl 'https://a.prota.space/v1/products/{product_id}/gadgets' -i -H 'Authorization Bearer: {access_token}'
```

##### Gadgets
