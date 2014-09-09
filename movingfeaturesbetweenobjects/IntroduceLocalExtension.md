#Introduce Local Extension

###Cuando tengamos un dominio de clases inmutables y necesitemos añadir un método, crear una clase auxiliar por composición para llamar a esa clase :

```
   public class MfDateSub extends Date {
   
     public MfDateSub (String dateString) {
             super (dateString);
       }

     private static Date nextDay(Date arg) {
         return new Date (arg.getYear(),arg.getMonth(), arg.getDate() + 1);
        }
   }
   
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
public class MfDateSub extends Date {

     public MfDateSub (Date arg) {
         super (arg.getTime());
     }
  
      private Date nextDay() {
          return new Date (getYear(),getMonth(), getDate() + 1);
    }
 }
 
```


