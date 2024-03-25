# NETOPIA Payments module for Magento 2.4.X (composer-installable)

## Options
* Card payment
* mobilPay WALLET

## Installation
1. Add custom 'vcs' type composer repository.
2. Run composer require netopia/netcard:"dev-master"

** See original repository for more info.

## Verification
By run the following command you can make sure, if this module is installed successfully on your Magento Proiect
* <code>php bin/magento module:status</code>

## After installation
Recommended to firstly, go to Admin panel & fill the necessary data
<code><your_magento_admin>->Stores->Configuration->Sales->Payment Methods->Netopia Payments</code>

* #### Configuration
    * **Base configuration** : To enable / disable the payment method, switch to Live or Sandbox, ....
    * **Certificate Configuration** : To uploade / remove the public & private keys for Live & Sandbox
    * **Custom configuration** : To set order status regarding the payment status, recommanded to use Defulte one 
    * **mobilPay WALLET Configuration** : To set mobilPay WALLET setting
    * **Conditions / Agreements** : To declare the agreements with NETOPIA Payments and send the agreement to NETOPIA Payments.
        * before send the agreements, make sure you already uploaded the keys & save the setting & agreements.
        
    Note : The fileds are not complited from configuration section, will set by default value, 

## Where Keys / Certificates are located
The Public & Private Keys for Live and Sandbox are located in <your_magento_root>/app/code/Netopia/Netcard/etc/certificates
* make sure you have right ownership & permition
### Other general usefull note
If in any case you update/upgrade your Magento Module & not see the changes, so maybe is cached.
You can using such command like this <code>php bin/magento ca:cl</code> to clean the cache or
Using such command <code>bin/magento setup:di:compile</code> to compile or regenerate your modules.
Sometime remove the contents of actual cache folders such as <code>MagentoRoot/var/cache/</code> | <code>MagentoRoot/var/page_cache/</code> | <code>MagentoRoot/generated/code</code> is helping too

##### Good to know
* To get the module compatible with previous versions of Magento, using the other branches of this GitHub repository. for ex. for Magento Version 2.3.X we can get the module by run git command like : **git clone --single-branch --branch V2.3 https://github.com/mobilpay/Magento.git**

NETOPIA Payments development team try to keep compatibility of the Magento module with latest version of Magento, in order to helping you to implamenting your ecomerce website faster.

## Tested up to : 
Magento : **2.4.6**

PHP : **8.2.8**

Openssl : **3.0**
