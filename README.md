# Tada Membership API Official
This repository only show API Official for TADA ( Not Full API )

# List
Host : https://api-int.gift.id/

| Path        | Response           | Request           |
| ------------- |:-------------:|:-------------:|
| /v1/users/otp/request | JSON | POST |
| /v1/users/otp/register | JSON | POST |
| /v1/users/profile | JSON | PATCH |
| /v1/users/profile | JSON | GET |
| /v2/users/cards/list | JSON | GET |
| /v2/users/vouchers/list | JSON | POST |

#

```http
POST /v1/users/otp/request HTTP/2
Host: api-int.gift.id
Auth: basic
Authorization: Basic GENERATED_AUTHORIZATION
X-Vnd-App-Platform: Android
X-Vnd-App-Name: TADA Wallet
X-Vnd-App-Version: 4.21
X-Vnd-App-Use-Decimal: true
X-Vnd-App-Device-Name: G011A
X-Vnd-App-Device-Id: 4ed1763be207e431
X-Vnd-Build-Code: 1BMN2AQFJ4U541T4-411
Content-Type: application/json; charset=utf-8
Content-Length: 95
Accept-Encoding: gzip, deflate
User-Agent: okhttp/4.9.2

{"phone_number":"YOUR_PHONE_NUMBER","country":"ID","sessId":"4ed1763be207e431","senderType":"sms"}
```
```http
HTTP/2 200 OK
Date: Thu, 30 Dec 2021 05:24:08 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 112
Access-Control-Allow-Origin: *
Vary: Accept-Encoding
Cf-Cache-Status: DYNAMIC
Expect-Ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
Server: cloudflare
Cf-Ray: 6c58d710cfa648fa-SIN
Alt-Svc: h3=":443"; ma=86400, h3-29=":443"; ma=86400, h3-28=":443"; ma=86400, h3-27=":443"; ma=86400

{"success":true,"secret":"ITVZ2T9UNTGMNAXSVM61TBYBCNTYEBYK","isNewUser":true,"remainingTime":45,"elapsedTime":4}
```
#
```http
POST /v1/users/otp/register HTTP/2
Host: api-int.gift.id
Auth: basic
Authorization: Basic GENERATED_AUTHORIZATION
X-Vnd-App-Platform: Android
X-Vnd-App-Name: TADA Wallet
X-Vnd-App-Version: 4.21
X-Vnd-App-Use-Decimal: true
X-Vnd-App-Device-Name: G011A
X-Vnd-App-Device-Id: 4ed1763be207e431
X-Vnd-Build-Code: 1BMN2AQFJ4U541T4-411
Content-Type: application/json; charset=utf-8
Content-Length: 141
Accept-Encoding: gzip, deflate
User-Agent: okhttp/4.9.2

{"phone_number":"YOUR_PHONE_NUMBER","otp_token":"425067","country":"ID","sessId":"4ed1763be207e431","secret":"ITVZ2T9UNTGMNAXSVM61TBYBCNTYEBYK"}
```
```http
HTTP/2 200 OK
Date: Thu, 30 Dec 2021 05:25:22 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 447
Access-Control-Allow-Origin: *
Cache-Control: no-store
Pragma: no-cache
Vary: Accept-Encoding
Cf-Cache-Status: DYNAMIC
Expect-Ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
Server: cloudflare
Cf-Ray: 6c58d8de099d4a95-SIN
Alt-Svc: h3=":443"; ma=86400, h3-29=":443"; ma=86400, h3-28=":443"; ma=86400, h3-27=":443"; ma=86400

{"access_token":"THIS_ACCESS_TOKEN","expired_at":"2022-12-30T05:25:22.646Z","expires_in":31535999,"user":{"id":5318395,"name":null,"phone":"YOUR_PHONE_NUMBER","email":null,"imageUrl":null},"token_type":"Bearer"}
```
```http
GET /v1/users/profile HTTP/2
Host: api-int.gift.id
Auth: bearer
Authorization: Bearer THIS_ACCESS_TOKEN
Content-Type: application/json
X-Vnd-App-Platform: Android
X-Vnd-App-Name: TADA Wallet
X-Vnd-App-Version: 4.21
X-Vnd-App-Use-Decimal: true
X-Vnd-App-Device-Name: G011A
X-Vnd-App-Device-Id: 4ed1763be207e431
X-Vnd-Build-Code: 1BMN2AQFJ4U541T4-411
Accept-Encoding: gzip, deflate
User-Agent: okhttp/4.9.2
```
```http
Output Response Profile ^
```
```http
POST /v2/users/cards/list HTTP/2
Host: api-int.gift.id
Auth: bearer
Authorization: Bearer THIS_ACCESS_TOKEN
X-Vnd-App-Platform: Android
X-Vnd-App-Name: TADA Wallet
X-Vnd-App-Version: 4.21
X-Vnd-App-Use-Decimal: true
X-Vnd-App-Device-Name: G011A
X-Vnd-App-Device-Id: 4ed1763be207e431
X-Vnd-Build-Code: 1BMN2AQFJ4U541T4-411
Content-Type: application/json; charset=utf-8
Content-Length: 40
Accept-Encoding: gzip, deflate
User-Agent: okhttp/4.9.2

{"archived":false,"page":1,"perPage":45}
```
```http
PATCH /v1/users/profile HTTP/2
Host: api-int.gift.id
Auth: bearer
Authorization: Bearer THIS_ACCESS_TOKEN
X-Vnd-App-Platform: Android
X-Vnd-App-Name: TADA Wallet
X-Vnd-App-Version: 4.21
X-Vnd-App-Use-Decimal: true
X-Vnd-App-Device-Name: G011A
X-Vnd-App-Device-Id: 4ed1763be207e431
X-Vnd-Build-Code: 1BMN2AQFJ4U541T4-411
Content-Type: application/json; charset=utf-8
Content-Length: 111
Accept-Encoding: gzip, deflate
User-Agent: okhttp/4.9.2

{"name":"Noruayda","email":"noruadaya@gmail.com","birthday":"1995-12-31","phone":"YOUR_PHONE_NUMBER","sex":"Male"}
```
```http
HTTP/2 200 OK
Date: Thu, 30 Dec 2021 05:25:54 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 353
Access-Control-Allow-Origin: *
Vary: Accept-Encoding
Cf-Cache-Status: DYNAMIC
Expect-Ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
Server: cloudflare
Cf-Ray: 6c58d9a3a92f4c4d-SIN
Alt-Svc: h3=":443"; ma=86400, h3-29=":443"; ma=86400, h3-28=":443"; ma=86400, h3-27=":443"; ma=86400

{"id":5318395,"name":"Noruayda","email":"noruadaya@gmail.com","phone":"YOUR_PHONE_NUMBER","sex":"Male","birthday":"1995-12-31T00:00:00.000Z","occupation":null,"city":null,"address":null,"confirmedAt":"2021-12-30T05:25:22.353Z","imageUrl":null,"Language":"en","CountryCode":"ID","createdAt":"2021-12-30T05:24:08.532Z","updatedAt":"2021-12-30T05:25:54.268Z"}
```
```http
POST /v2/users/vouchers/list HTTP/2
Host: api-int.gift.id
Auth: bearer
Authorization: Bearer THIS_ACCESS_TOKEN
X-Vnd-App-Platform: Android
X-Vnd-App-Name: TADA Wallet
X-Vnd-App-Version: 4.21
X-Vnd-App-Use-Decimal: true
X-Vnd-App-Device-Name: G011A
X-Vnd-App-Device-Id: 4ed1763be207e431
X-Vnd-Build-Code: 1BMN2AQFJ4U541T4-411
Content-Type: application/json; charset=utf-8
Content-Length: 40
Accept-Encoding: gzip, deflate
User-Agent: okhttp/4.9.2

{"archived":false,"page":1,"perPage":45}
```