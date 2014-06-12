---
title: Pathwright API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>

includes:
  - errors

search: true
---

# API Reference


**Note:** This API reference is very preliminary. The calls shown below
are subject to frequent change, and are here for early adopters to start
experimenting with.

# Gift subscriptions

Gift subscriptions are used to give someone a free subscription to a school
for a period of time. The recipient need not be a current user, and the
gift subscription can be converted to a paid subscription by the user at
any time.

## Create gift subscription code

```shell
curl "https://api.pathwright.com/api/public/subscription/gift-code/"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 1,
  "subscription_plan": 123,
  "gift_duration": 1,
  "recipient_email": "someone@somewhere.com",
  "recipient_first_name": "Some",
  "recipient_last_name": "Person",
  "gift_code": "ABCD123456"
}

```

This endpoint is used to create a single gift subscription code, which may
be sent to a recipient. Said recipient doesn't have to be a current Pathwright
user.

### HTTP Request

`POST https://api.pathwright.com/api/public/subscription/gift-code/`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
subscription_plan | yes | The ID of the subscription plan to gift.
gift_duration | yes | The number of months the subscription is for.
recipient_email | no | If known, the email of the recipient.
recipient_first_name | no | If known, the recipient's first name.
recipient_last_name | no | If known, the recipient's first name.

