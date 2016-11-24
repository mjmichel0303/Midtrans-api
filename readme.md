
Midtrans Payment API Postman Collection
=====================================

Midtrans&nbsp; :heart: Postman!

## Description

This repository contains [Postman](https://www.getpostman.com) collection for various payment API call to [Midtrans](https://midtrans.com) Payment API.

API covered:
* [SNAP API](http://snap-docs.midtrans.com)
* [Core API](http://api-docs.midtrans.com)

## Usage Instruction

1. Download and open [Postman](https://www.getpostman.com)
2. [Register to Midtrans](https://dashboard.midtrans.com/register)
3.  Import:
 - Use this link: https://www.getpostman.com/collections/b25a3fcfb9f0afc1f348 , or
 - Clone or [download](/archive/master.zip) this repository, then import postman collections from `MidtransPaymentAPI.postman_collection` file.
4. [Login](http://dashboard.midtrans.com) to Midtrans, switch to **Sandbox**, go to menu `Settings > Access Keys`. Copy your **Server Key**
5. In Postman, open **Midtrans Payment API** then choose one request you want to try, click on `Authorization` tab (beside Headers tab)
6. Select **Type** as `Basic Auth`, fill **Username** with your **Server Key** (looks like this `VT-server-xxxxxx`). Leave **Password** field blank, click **Update Request**
7. Now you can `save` then click `send` the request. You will get server response.

> ![Authorization Config](https://cloud.githubusercontent.com/assets/13027142/20592019/1e6ab9ec-b25e-11e6-9285-c68fef6c538c.png)


## SNAP Token Usage Example

If you are testing `Snap transaction token request` you will get response like:
```
{ "token": "bffb82ff-f8bb-4651-86b0-0c2316b77c0a" }
```
To use that token, you can open file `snap-opener/index.html` in your web browser to preview the SNAP payment page.
- Tips: you can also append snap token like this in url `../snap-opener/index.html?snap_token=bffb82ff-f8bb-4651-86b0-0c2316b77c0a&is_production=false`

You can also edit file `snap/index.html` and insert your own token to the HTML, then open in web browser.
- All implementation in this example are pure HTML & Javascript so you don't need to have any server running.

## Production Mode

All endpoint used in this postman collection is for `sandbox transaction`, to switch to `production` change endpoint URL from:

`https://api.sandbox.midtrans.com/../..`

to

`https://api.midtrans.com/../..`

(Just remove the `sandbox.` from url)

## Troubleshooting

If you get error
```
{
  "error_messages": [
    "Access denied due to unauthorized transaction, please check client or server key",
    "Visit https://snap-docs.midtrans.com/#request-headers for more details"
  ]
}
```
- Please make sure you do step 4-7 properly like instructed in **Usage Instruction** section.
- Please make sure you are using correct **Server Key** (Serverkey for sandbox & production are different).

### Get Help

* [Midtrans&nbsp;](https://www.midtrans.com)
* [Midtrans registration](https://dashboard.midtrans.com/register)
* [SNAP documentation](http://snap-docs.midtrans.com)
* [Core API documentation](http://api-docs.midtrans.com)
* Can't find answer you looking for? email to [support@midtrans.com](mailto:support@midtrans.com)
