#Replace Method with Method Object

###Cuando tengamos un método muy grande, convertirlo el cuerpo en una clase.
###De manera que todas las variables locales se convierten en campos de ese objeto. 
```
//Class Account

int gamma (int inputVal, int quantity, int yearToDate) {
    int importantValue1 = (inputVal * quantity) + delta();
    int importantValue2 = (inputVal * yearToDate) + 100;
    if ((yearToDate - importantValue1) > 100)
        importantValue2 -= 20;
    int importantValue3 = importantValue2 * 7;
    // and so on...
    return importantValue3 - 2 * importantValue1;
}

```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
  //class Gamma...
    private final Account account;
    private int inputVal;
    private int quantity;
    private int yearToDate;
    private int importantValue1;
    private int importantValue2;
    private int importantValue3;
    
    Gamma (Account source, int inputValArg, int quantityArg, int yearToDateArg) {
        this.account = source;
        inputVal = inputValArg;
        quantity = quantityArg;
        yearToDate = yearToDateArg;
    }
    
    Integer compute () {
        importantValue1 = (inputVal * quantity) + _account.delta();
        importantValue2 = (inputVal * yearToDate) + 100;
        if ((yearToDate - importantValue1) > 100)
            importantValue2 -= 20;
        int importantValue3 = importantValue2 * 7;
        // and so on...
        return importantValue3 - 2 * importantValue1;
    }
    
    ...
     
    Integer gamma (Integer inputVal, Integer quantity, Integer yearToDate) {
        return new Gamma(this, inputVal, quantity, yearToDate).compute();
    }
    
}
```