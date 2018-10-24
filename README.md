# Generate-Collection-Code
Guide for Generating Collection Code using our API

This method is used to Generate collection code to Receive Payments

HTTP Method: POST


# Resource Url

https://cofredpayaccess.com/api/v1/collections

# Headers

See our Guide for how to setup Header https://github.com/cofred/Header-Authentication

# Authentication Headers Example

merchant_id: VF9CMTY3WURPZUpJdkNnVWJWRXE=   // Base64 Encoded

secret_code: I8AtLUljNqcdS4F76OVy2Zf1bJvGwsP95rE

terminal_id: YINCU

access_token: dUp4dEtybVg0Ump4MEFT  // Base64 Encoded

timestamp: 1505628722


# Request Parameters

Field	M/O	Length	Format	Description

Amount	M		Numeric	Transaction Amount 

Reference	M		Alpha Numeric	Merchant Reference ID

Callback url	M		Url	Callback url to get Response after user makes the payment.


# Callback Code Response

A HTTP response code 200 is sent back for a success

# Response Parameters

Field	Description

responseCode	Response Code

CollectionCode	Unique Transaction reference generated by Cofred

MerchantReference	Date and Time of Transaction

Qr Imageurl	Response Message which will return Transaction success message

ResponseMessage	Response Message which will return Transaction success message


# Sample Response

200

{
"responseCode":"200",
"CollectionCode":139497170178,
"MerchantReference":"5656565656",
"qr_imageurl":"https://cofred.com/secure/assets/qr_image/139497170178.png",
"responseMessage":"Payment Code Generated Successfully!"
}

# Communication

Requests will be sent over the REST protocol using POST Method.
