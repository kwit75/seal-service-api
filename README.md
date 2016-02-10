#### POST /seal-service/{accountId}/sign-item

Initiates the signing process for an item

* `accountId` - The account id

##### Body
```
{
    "itemId": "1234567", 
    "itemDescription": "Cykel säljes",
    "pNo": "19760726-0259"
}
```

##### Response

204 NO_CONTENT - Returned if the request succeeds and the caller can instruct the end user to lauunch the Bank ID application.
4xx-5xx - Returned if the request failed for any reason.

---

#### POST /handle-signing-response

Callback for signing response 

##### Body
```
{
    "result": "SIGN_OK",
    "itemId": "1234567",
    "idkToken": "LCa0a2j/xo/5m0U8HTBBNBNCLXBkg7+g+YpeiGJm564=",
    "pNo": "19760726-0259"
}
```

