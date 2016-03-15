# amazon-mws-orders
Amazon Marketplace Web Service Orders PHP Client Library - Version 2013-09-01
=================================================

Installation
------------

Install [Composer](http://getcomposer.org/) and add amazon-mws-orders to your `composer.json`:

    composer require aivanouski/amazon-mws-orders

Version
-------

Current version is `MWSOrdersPHPClientLibrary-2013-09-01._V293335039_`.

Installation
----------
Add the reference into your composer.json : 

    "aivanouski/amazon-mws-orders": "dev-master"
	composer update

Use in controller :

 $config = array (
   'ServiceURL' => $serviceUrl,
   'ProxyHost' => null,
   'ProxyPort' => -1,
   'ProxyUsername' => null,
   'ProxyPassword' => null,
   'MaxErrorRetry' => 3,
 );

 $service = new \MarketplaceWebServiceOrders_Client(
        AWS_ACCESS_KEY_ID,
        AWS_SECRET_ACCESS_KEY,
        APPLICATION_NAME,
        APPLICATION_VERSION,
        $config);
		
 $request = new \MarketplaceWebServiceOrders_Model_ListOrdersRequest();
 $request->setSellerId(MERCHANT_ID);
 
 $response = $service->ListOrders($request);