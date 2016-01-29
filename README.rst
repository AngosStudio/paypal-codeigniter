######
Notice
######

Our `standard class library <https://github.com/angelleye/paypal-php-library>`_ is more closely maintained and is now compatible with Composer which allows you to autoload the library and make it available in CodeIgniter.

We will still maintain this library as necessary, but if it may be beneficial to you to use the standard class with Composer.

************
Introduction
************

This PHP class library for PayPal makes it easy to integrate nearly every PayPal API they provide.

All of the web services included in PayPal's NVP documentation are included, as well as Adaptive Accounts, 
Adaptive Payments, Permissions, Invoicing, PayFlow, and more.

*******************
Server Requirements
*******************

-  PHP version 5.2.4 or newer.
-  CodeIgniter 2.0+

************
Installation
************

Merge the /application directory into your CodeIgniter /application directory.

Open /application/config/paypal-sample.php and adjust the value with your own Sandbox and Production API credentials.  Then save-as paypal.php.

There are detailed comments inside the config file to help you fill it out correctly.

****************************
How to Make PayPal API Calls
****************************

Open /application/controllers/paypal/controllername.php depending on which PayPal API you're going to be using. 

Example:  If we want to make a call to the RefundTransaction API we open payments_pro.php and then seek out the Refund_transaction() function. 

Each controller file includes functions with PHP arrays for every parameter available to that particular API. Simply fill in the array parameters with your own dynamic (or static) data. This data may come from...

- Session Variables
- PHP Variables
- Database Recordsets
- Static Values
- Etc.

When you run the function you will get a $PayPalResult array that consists of all the response parameters from PayPal, original request parameters sent to PayPal, and raw request/response info for troubleshooting.

If errors occur they will be available in $PayPalResult['ERRORS'].

*******
Samples
*******

The Payments Pro controller has two methods ready for demo purposes after you update your config file.

- Do_direct_payment_demo()
- Get_balance()

The Adaptive Payments controller has one sample ready for demo.

- Convert_currency()

The PayFlow controller has one sample ready for demo.

- Process_transaction_demo()

*********
Resources
*********

-  `PayPal Name-Value Pair API Developer Guide <https://cms.paypal.com/cms_content/US/en_US/files/developer/PP_NVPAPI_DeveloperGuide.pdf>`_
-  `Adaptive Accounts Developer Guide <https://cms.paypal.com/cms_content/US/en_US/files/developer/PP_AdaptiveAccounts.pdf>`_
-  `Adaptive Payments Developer Guide <https://cms.paypal.com/cms_content/US/en_US/files/developer/PP_AdaptivePayments.pdf>`_
-  `Express Checkout Integration Guide <https://cms.paypal.com/cms_content/US/en_US/files/developer/PP_ExpressCheckout_IntegrationGuide.pdf>`_
-  `Invoice Service API Guide <https://cms.paypal.com/cms_content/US/en_US/files/developer/PP_InvoicingAPIGuide.pdf>`_
-  `Mass Payments User Guide <https://cms.paypal.com/cms_content/US/en_US/files/developer/PP_MassPayment_Guide.pdf>`_
-  `PayPal Merchant Setup and Administration Guide <https://www.x.com/developers/paypal/development-and-integration-guides#msa>`_
-  `PayPal Payments Pro Documentation <https://www.x.com/developers/paypal/development-and-integration-guides#wpp>`_
-  `PayPal Recurring Billing / Recurring Payments Guide <https://www.x.com/developers/paypal/development-and-integration-guides#recurring>`_
