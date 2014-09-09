#Move Field

###Cuando tengamos dos clases compuestas, intentar mover los atributos a las clases que más los usen :

```

 public class Account {
   private AccountType _type;
   private double _interestRate;
 
   double interestForAmount_days (double amount, int days) {
       return _interestRate * amount * days / 365;
   }
 }
 
 public class AccountType {
    private double _interestRate;
  
    void setInterestRate (double arg) {
        _interestRate = arg;
    }
  
    double getInterestRate () {
        return _interestRate;
    }
 }
 
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
  public class Account {
    private AccountType type;
      
    double interestForAmount_days (double amount, int days) {
        return type.getInterestRate() * amount * days / 365;
    }
    
  }
     
```


