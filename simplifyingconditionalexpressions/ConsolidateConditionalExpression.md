#Consolidate Conditional Expression

###Si tenemos una secuencia de pruebas condicionales con el mismo resultado, combinarlas en una sola expresión condicional y extraerlo :

```
 double disabilityAmount() {
       if (_seniority < 2) return 0;
       if (_monthsDisabled > 12) return 0;
       if (_isPartTime) return 0;
       // compute the disability amount
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
  double disabilityAmount() {
       if (isNotEligibleForDisability()) return 0;
       // compute the disability amount
       ...
   }

   boolean isNotEligibleForDisability() {
       return ((_seniority < 2) || (_monthsDisabled > 12) || (_isPartTime));
   }
```


