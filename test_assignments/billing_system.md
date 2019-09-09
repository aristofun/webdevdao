## RoR: billing system

**Requirements** 

Please build us a new billing system. We sell a widget in 3 different ways: 

1. Direct sale for $100 per item. 

2. Affiliates who resell our widget based on a tiered billing system. They pay us based on how many widgets they sell total.

    * They sell 0-500 widgets in a month, $60 per widget.  
    * They sell 501-1000 widgets in a month, $50 per widget.  
    * They sell 1001+ widgets in a month, $40 per widget.  

    We have the following Affiliates: 
    * A Company: Sells the widget for $75/ea.  
    * Another Company: Sells the widget for $65/ea.  
    * Even More Company: Sells the widget for $80/ea.  

3. Resellers who resell our widget based on a flat billing system. They pay us $50 per widget.

We have the following Resellers: 
* Resell This: Sells the widget for $75 
* Sell More Things: Sells the widget for $85 

All three groups can receive orders for this service. An order includes a quantity of widgets ordered, a method used, and an amount paid.

Build a class that generates 100 randomized orders for one month. These orders should be randomly assigned to each of the 6 possible types of sale and should be for a random number of widgets between 1 and 100. Build a service object that we can use to generate billing reports.

This library needs to generate the following reports: 
* Total amount we should bill each Affiliate and Reseller.  
* Profit earned by each Affiliate and Reseller.  
* Total revenue for the company from all sales: Affiliate, Reseller and Direct. 

**Additional information**

This object needs to have a simple and documented interface that we can easily integrate with our existing systems. For the purposes of the test, a persistence layer is not required. Also, testing is very important to our team so please provide some basic unit tests (Rspec or Minitest preferred).