# [Plugin Handle](https://github.com/annihilatoratm/prestashop-doc/tree/main?tab=readme-ov-file#prestashop-16-module-for-payneteasy-payment-gateway)
# [User registration](https://github.com/annihilatoratm/opencart-doc/blob/main/doc-eng.md#user-registration)
# [Payment Flow](https://github.com/annihilatoratm/opencart-doc/blob/main/doc-eng.md#payment-flow-1)

## Plugin for OpenCart 1.x for pay by PaynetEasy

### Requirements

* PHP 5.3 - 5.5
* [Curl extension](http://php.net/manual/en/book.curl.php)
* [OpenCart](http://www.opencart.com/index.php?route=download/download) 1.x (плагин тестировался с версией 1.5)

### Functionality

[merchant PaynetEasy API](http://wiki.payneteasy.com/index.php/PnE:Merchant_API).
- [ ] [Sale Transactions](http://wiki.payneteasy.com/index.php/PnE:Sale_Transactions)
- [ ] [Preauth/Capture Transactions](http://wiki.payneteasy.com/index.php/PnE:Preauth/Capture_Transactions)
- [ ] [Transfer Transactions](http://wiki.payneteasy.com/index.php/PnE:Transfer_Transactions)
- [ ] [Return Transactions](http://wiki.payneteasy.com/index.php/PnE:Return_Transactions)
- [ ] [Recurrent Transactions](http://wiki.payneteasy.com/index.php/PnE:Recurrent_Transactions)
- [x] [Payment Form Integration](http://wiki.payneteasy.com/index.php/PnE:Payment_Form_integration)
- [ ] [Buy Now Button integration](http://wiki.payneteasy.com/index.php/PnE:Buy_Now_Button_integration)
- [ ] [eCheck integration](http://wiki.payneteasy.com/index.php/PnE:eCheck_integration)
- [ ] [Western Union Integration](http://wiki.payneteasy.com/index.php/PnE:Western_Union_Integration)
- [ ] [Bitcoin Integration](http://wiki.payneteasy.com/index.php/PnE:Bitcoin_integration)
- [ ] [Loan Integration](http://wiki.payneteasy.com/index.php/PnE:Loan_integration)
- [ ] [Qiwi Integration](http://wiki.payneteasy.com/index.php/PnE:Qiwi_integration)
- [ ] [Merchant Callbacks](http://wiki.payneteasy.com/index.php/PnE:Merchant_Callbacks)

### <a name="get_package"></a> Получение пакета с плагином

#### Package buil
1. [Install the composer](http://getcomposer.org/doc/00-intro.md)
2. Clone the repository with the plugin: `composer create-project payneteasy/php-plugin-opencart --stability=dev --prefer-dist`
3. Go to the plugin directory: `cd php-plugin-opencart`
4. Compose the plugin into the archive: `composer archive --format=zip`

### Installation

1. [Get package](#get_package)
2. Unarchive the package into the OpenCart root directory

### Configuration and deletion

#### Plugin configuration

1. Open OpenCart administration panel
2. Go to payment modules section
    1. Choose "Extensions" section
    2. Choose "Payments"

    ![go to payment modules](img/go_to_payment_modules.png)
2. Installing of PaynetEasy module
    1. Choose the module and press "Install" button

    ![install module](img/install_module.png)
3. Switch to configuration mode

    ![go to edit form](img/go_to_edit_form.png)
4. Edit mode
    1. Fill the form
    2. Save

    ![edit config](img/edit_config.png)


#### Plugin deletion

##### Delete the plugin from admin panel

1. Go to OpenCart admin panel
2. Go to payment modules section
    1. Choose "Extensions" section
    2. Choose "Payments"

    ![go to payment modules](img/go_to_payment_modules.png)
3. Delete the module
    1. Choose the module and press "Uninstall" (стрелка #1)

    ![remove module](img/remove_module.png)

##### Delete module's files for complete deletion

* `admin/controller/payment/payneteasy_form.php`
* `admin/language/english/payment/payneteasy_form.php`
* `admin/model/payment/payneteasy_form.php`
* `admin/view/image/payment/payneteasy.png`
* `admin/view/template/payment/payneteasy_form.php`
* `catalog/controller/payment/payneteasy_form.php`
* `catalog/language/english/payment/payneteasy_form.php`
* `catalog/model/payment/payneteasy_form.php`
* `catalog/view/theme/default/template/payment/payneteasy_form_checkout.php`
* `catalog/view/theme/default/template/payment/payneteasy_form_error.php`
* `vendor/composer/`
* `vendor/payneteasy/`
* `vendor/autoload.php`

  ## User registration
  
  1. Click on *My Account* button at the top of the main panel. In the drop-down menu select **Register** option and follow to the User Registration page.

  <img src="/images/opencart-register-1.png" width=60% height=60%>

  2. On the **Register Account** page please fill all necessary Personal details, Password, aggree to the Privacy Policy and click *Continue* button.

  <img src="/images/opencart-register-2.png" width=60% height=60%> <img src="/images/opencart-register-3.png" width=60% height=60%>


  ## Payment Flow

  1. Go to the needed section of products (e.g. Phones & PDAs). Choose an item and press on *Add to Cart* button.

  <img src="/images/opencart-1-upd.png" width=60% height=60%> <img src="/images/opencart-2.png" width=60% height=60%> <img src="/images/opencart-3.png" width=60% height=60%>
  
  2. Once the item is added to the cart, the pop-up with success message will be displayed. Press on *Shopping cart* button and choose *View cart* option to see all items added to the cart or *Checkout* to go to Checkout page directly.

  <img src="/images/opencart-4.png" width=60% height=60%> <img src="/images/opencart-5.png" width=60% height=60%> <img src="/images/opencart-6.png" width=60% height=60%>
  
  3. On the **Checkout** page all required *Shipping Address* parameters must be filled. Also *Shipping Method* and *Payment Method* have to be set. On the **Payment method options** pop-up screen choose **Payment system PaynetEasy** payment method. Once all required parameters were set, click on *Place Order* button.

  <img src="/images/opencart-7.png" width=60% height=60%> <img src="/images/opencart-9.png" width=60% height=60%>
  <img src="/images/opencart-8-2.png" width=60% height=60%> <img src="/images/opencart-10.png" width=60% height=60%>
  <img src="/images/opencart-11.png" width=60% height=60%>

  4. On **Payneteasy Payment Form** all Creadit Card information must be set. Once done, press on *Process payment* button. Wait for finish of the payment. 

  <img src="/images/opencart-12.png" width=60% height=60%>
  <img src="/images/opencart-13.png" width=60% height=60%>
  <img src="/images/opencart-14.png" width=60% height=60%>
