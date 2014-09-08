#Consolidate Duplicate Conditional Fragments

###Si el mismo fragmento de código se encuentra en todas las ramas de una expresión condicional. Extraer a fuera la expresión.
```
  if (isSpecialDeal()) {
           total = price * 0.95;
           send();
       }
       else {
           total = price * 0.98;
           send();
       }
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
   if (isSpecialDeal())
          total = price * 0.95;
      else
          total = price * 0.98;
      send();
```


