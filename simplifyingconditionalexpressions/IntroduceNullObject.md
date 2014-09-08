#Introduce Null Object

###Si se compara un objecto con un valor nulo, crear un valor nulo para comparar dicho objecto :

```
 if (customer == null) plan = BillingPlan.basic();
           else plan = customer.getPlan();
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
  class NullCustomer { ... }

  interface Nullable {
     boolean isNull();
   }
 
  class Customer implements Nullable ..
   
  class Customer...
     static Customer newNull() {
         return new NullCustomer();
     }
       
  if (customer == Customer.newNull) plan = BillingPlan.basic()
      else plan = customer.getPlan();
      ...
      
```
