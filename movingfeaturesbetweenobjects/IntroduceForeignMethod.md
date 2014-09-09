#Introduce Foreign Method

###Cuando tengamoss un dominio de clases inmutables y necesitemos añadir un método, crear una clase auxiliar por composición para llamar a esa clase :

```
  Date newStart = new Date (previousEnd.getYear(),
        previousEnd.getMonth(), previousEnd.getDate() + 1);
   
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
    Date newStart = nextDay(previousEnd);
 
    private static Date nextDay(Date arg) {
        return new Date (arg.getYear(),arg.getMonth(), arg.getDate() + 1);
    }
   
```


