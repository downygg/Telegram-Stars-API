
# Telegram Stars API

This repository provides an API to facilitate users in purchasing Telegram Stars. Telegram Stars are a feature that allows users to support content creators on the Telegram platform. With this API, users can easily and quickly make purchases of Stars.


# Key Features
- **Ton Wallet Generator:** Provide to create Ton Wallet as Payment Method
- **Recipient Check:** Provide to check available Telegram User as recipient.
- **Price Check:** Provide to check price for stars quantity.
- **Stars Purchase:** Perform Stars purchases using TON Wallet payment methods.

# Main Endpoints
- **API ENDPOINT :** http://139.99.39.26:6555/api

## Ton Wallet Generator

- **GET** ``/ton/generate``
```
Response : {
    "mnemonic" : <object>,
    "non_bounceableaddress: <string>,
    "bounceableaddress: <string>
}
``` 

## Recipient Check
- **GET** ``/stars/check/:useraname``
```
Response : {
    "recipient" : <string>,
    "name": <string>
}
```

## Price Check
- **GET** ``/stars/price/:quantity``
```
Response : {
    "stars": <string>,
    "tonvalue": <string>,
    "usdvalue": <string>
}
```

## Stars Purchase
- **POST** ``/stars/pay``
```
Parameter : {
    "qty" : <string>,
    "username": <string>,
    "mnemonic": <object>
}

Response : {
    "ok": <object>,
    "ref": <string>
}
```
# 
