#Decompense Conditional

###Cuando tengamos declaraciones condicionales muy compactas, desacoplarlas en metodos externos : 

```
   if (date.before (SUMMER_START) || date.after(SUMMER_END))
           charge = quantity * _winterRate + _winterServiceCharge;
       else charge = quantity * _summerRate;
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
    if (notSummer(date))
            charge = winterCharge(quantity);
        else charge = summerCharge (quantity);
  
    private boolean notSummer(Date date) {
        return date.before (SUMMER_START) || date.after(SUMMER_END);
    }
  
    private double summerCharge(int quantity) {
        return quantity * _summerRate;
    }
  
    private double winterCharge(int quantity) {
        return quantity * _winterRate + _winterServiceCharge;
    }
```


