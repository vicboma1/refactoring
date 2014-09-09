#Move Method

###Cuando tengamos dos clases compuestas, intentar mover los metedos a las clases más débiles.

```
  public class Account {
  
   private AccountType _type;
   private int _daysOverdrawn;
   
   double overdraftCharge() {
        if (type.isPremium()) {
            double result = 10;
            if (daysOverdrawn > 7) result += (daysOverdrawn - 7) * 0.85;
            return result;
        }
        else return daysOverdrawn * 1.75;
    }
  
   double bankCharge() {
        double result = 4.5;
        if (daysOverdrawn > 0) result += overdraftCharge();
        return result;
    }
  }
  
  public class AccountType {
     double overdraftCharge(int daysOverdrawn) {
         if (isPremium()) {
             double result = 10;
             if (daysOverdrawn > 7) result += (daysOverdrawn - 7) * 0.85;
             return result;
         }
         else return daysOverdrawn * 1.75;
     }
  }
   
 
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
 public class Account { 
    double bankCharge() {
        double result = 4.5;
        if (_daysOverdrawn > 0) result += _type.overdraftCharge(_daysOverdrawn);
        return result;
    }
  }
  
  public class AccountType {
     double overdraftCharge(Account account) {
         if (isPremium()) {
             double result = 10;
             if (account.getDaysOverdrawn() > 7)
                result += (account.getDaysOverdrawn() - 7) * 0.85;
             return result;
         }
         else return account.getDaysOverdrawn() * 1.75;
     }
     
```


