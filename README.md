# CRYT-Pay
Accept CRYT Payments on your Website/Store with easy integration.

----
## What is it? ##

  - CRIT-Pay allows you to accept payments in KRIT on your website, with a few lines of code and in extreme security.
  
----
## What is needed? ##

  - A few minutes to understand how to integrate it, no registration, no data or passphrase, all automated and adaptable to your website.
  
  ----
## Let's Begin ##

  - First step: A simple HTML form that focuses on CRYT Pay, setting the required parameters. (paymentform.html)
  - Important: Order_id and Custom are the 2 parameters required and also necessary to identify the order on your website, they must not be the same and should preferably be generated at random. They are the 2 parameters that identify the order even when requesting the status of an order by calling the callback from CRYT-Pay.
  - Once the form is created by setting the parameters, perhaps taking them from your database which logs the requests and then verifies that the payment has been completed or not, the user sends the form, CRYT Pay creates the order and directs the user to the payment page on https://pay.crytrex.com/pay_web.html?id="UNIQUE_ID "where" id "is created by the server and is unique.

On this page the user has the QR code, the CRYT address (set in the form) The total with the exchange of the moment, the unencrypted message to be attached, and other information such as ORDER_ID WEBSITE and the amount in the currency chosen in the form.

Once the user sends the payment, exact CRYT with "NOT CRYPTED" message, the system detects the transaction, updates the payment status and redirects the user to the success page previously set in the form.

Through the callback "https://pay.crytrex.com/order_details_ipn.php?order_id=**ORDERID**&custom=**CUSTOM**" you can check verify and update the status of an order with the combination ORDER_ID and CUSTOM and proceed by updating the payment information on your website.

status = 0 *ORDER NOT PAID

status = 1 *ORDER COMPLETED


IPN endpoint url return a JSON with all details, included the Transaction id from CRYT Blockchain.

And the payment system is complete.

CRYT Pay works in a simple, fast, anonymous and integrable way in a few minutes.
  
  ----
  
Supported Currency with Live Exchange Rates:

| USD | EUR | GBP | JPY | CAD | AUD | HKD | RUB | ISK | PHP | DKK | HUF | CZK | RON | SEK | IDR | INR | BRL | THB | CHF | MYR | BGN | NOK | NZD | MXN | SGD | ILS | KRW | PLN | 
