# Postman collection
**What is a Postman collection?**

It is a series of prepared requests using the different paths presented in the specification. Using this, you will be able to test the configuration of your server.
There are more details regarding each different request inside the collection, which you can explore using the Postman app.
## Usage
We encourage you to import the Postman collection to the Postman desktop app where you will find all the available functionalities. 
 1. Download the [Postman app](https://dl.pstmn.io/download/latest/win64).
 2. Install it.
 3. Import the files inside the Postman folder.
 
![How to use postman](https://github.com/outpaycelab/outpayce-connect-api/blob/51eb2fbfe2de5ad467d3e36758d37503be3c9f1d/assets/animation-postman.gif)

## Content
Using this tool you will be able to test the different requests and scenarios while connected to your server. Once all the requests are working you can send us the report with the results.
### Environment
You must complete the environment file with information related to your server and the type of payment to be tested, this can be done using the Postman app or editing the file. There are some example values that you can change.
### Credit Card scenarios
These are the use cases that you will find inside the CC collection:
* Authorization
  * Standard use cases
    - Authorization with required parameters
    - Authorization with merchant and acquirer data
    - Authorization with cardholder data
    - Authorization with travel data
  * External 3DS data use cases
    - Authorization for AMEX with 3DS
    - Authorization for VISA with 3DS
    - Authorization for MASTERCARD with 3DS
* Reversal
  - Reversal simple request
  - Reversal with extra parameters
* Capture  
  - Capture simple request 
  - Capture merchant/acquirer
* Refund 
  - Refund simple request 
  - Full Refund merchant/acquirer

### Alternative Payment Methods scenarios
These are the use cases that you will find inside the APM collection:
* Authorization - 1 Step
  * Positive cases
    - 202 Successfully accepted Standard use case
    - 202 Successfully accepted Simple use case

  * Error cases
    - 400 INVALID INPUT PARAM(S) - PLEASE ADJUST REQUEST
    - 400 MISSING REQUIRED INPUT PARAM(S) - PLEASE ADJUST REQUEST
    - 500 INTERNAL PROCESSING ERROR
    - 400 INVALID FORMAT

* Inquiry/Resumption
  * Positive cases
    - 201 Successfully created Standard use case
    - 201 Successfully created Simple use case
  * Error cases
    - 409 PAYMENT TRANSACTION EXPIRED
    - 502 TIMEOUT ERROR UNKNOWN
    - 424 AUTHORISATION DENIED INSUFFICIENT FUNDS

* Webhooks
  * Authorization 
    - Successful Authorization
    - Authorization Pending
    - Authorization denial

  * Refund 
    - Refund success
    - Refund failure
    - refund denial

* Refund
  * Positive cases
    - 201 Successfully created case
  * Error cases
    - 409 PAYMENT TRANSACTION EXPIRED
    - 424 PAYMENT DECLINED
    - 500 SYSTEM UNAVAILABLE
  
You will have more information regarding the different scenarios and variables inside each collection. 
