### WITTY FLOW SMS PIP PACKAGE

#### Step 1: Install The Package Via Pip

#### Via Pip
```python
 pip install witty-flow-sms
```

### Step 2: Initialize

```python
#IMPORT 
from witty_flow_sms import WittyFlowSms

APP_ID = XXXXXXXXXXXX
APP_SECRET = XXXXXXXX
client = WittyFlowSms(APP_ID, APP_SECRET)
```
### Usage

### Send Text Message
```javascript
  // SEND SMS
  // sendMessage Takes 3 Params (phone, sender, message)
  // sender => string should not be more than 14 characters
  // phone => string should take the 0244XXXXXX format
  // message => string should not me more than 180 characters
  res = client.send_sms('0507565349', 'Possitech', 'Test Message')

  // OnSuccess Response
  {
    "status": "success",
    "code": 2020,
    "message": "Accpeted for delivery",
    "data": {
        "status": "accepted",
        "message_id": "ebb04f7f-147f-4d17-877b-8dd8af4ed2fe",
        "message": "New message",
        "date_created": "2020-08-24T00:17:09.000000Z",
        "direction": "MT",
        "from": "Ghana",
        "to": "233541348180",
        "type": "plain",
        "message_segments": 1,
        "cost": "0.03",
        "service_rate": "0.030000",
        "callback_url": null
    }
}

```

### Send Flash Message
```javascript
  // SEND SMS
  // sendMessage Takes 3 Params (phone, sender, message)
  // sender => string should not be more than 14 characters
  // phone => string should take the 0244XXXXXX format
  // message => string should not me more than 180 characters
  res = client.send_sms('0507565349', 'Possitech', 'Test Message')

  // OnSuccess Response
  {
    "status": "success",
    "code": 2020,
    "message": "Accpeted for delivery",
    "data": {
        "status": "accepted",
        "message_id": "ebb04f7f-147f-4d17-877b-8dd8af4ed2fe",
        "message": "New message",
        "date_created": "2020-08-24T00:17:09.000000Z",
        "direction": "MT",
        "from": "Ghana",
        "to": "233541348180",
        "type": "plain",
        "message_segments": 0,
        "cost": "0.03",
        "service_rate": "0.030000",
        "callback_url": null
    }
}
```

### Get Sms Status
```javascript
  // Get Sms Status
  // getSmsStatus Takes 1 Param (message_id)
  // message_id => string
  res = client.check_sms_status('21776c6f-3c84-40c0-b0a5-14c3b0c6f514')

  // OnSuccess Response
  {
    "status": "success",
    "code": 2000,
    "message": "Message retrieved",
    "data": {
        "message_id": "21776c6f-3c84-40c0-b0a5-14c3b0c6f514",
        "status": "delivered",
        "message": "New message",
        "date": "2020-08-23T23:54:04.000000Z",
        "readable_date": "Sun August 23, 2020 11:54:04 PM",
        "direction": "MT",
        "type": "1",
        "sender": "Ghana",
        "recipient": "233541348180",
        "message_segments": 1,
        "cost": "0.03",
        "rate": "0.030000",
        "billing": "charged"
    }
}
```


### Get Account Balance
```javascript
  res = client.get_account_balance()
  // OnSuccess Response
  {
    "status": "success",
    "code": 2000,
    "message": "Balance Retrieved",
    "data": {
        "balance": "19.19",
        "currency": "GHS"
    }
}
```
