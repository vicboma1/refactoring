#Introduce Assertion

###Una sección de código asume algo sobre el estado del programa, debemos hacer el supuesto explícito con una afirmación : 

```
   if (date.before (SUMMER_START) || date.after(SUMMER_END))
           charge = quantity * _winterRate + _winterServiceCharge;
       else charge = quantity * _summerRate;
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
 double getExpenseLimit() {
       Assert.isTrue (_expenseLimit != NULL_EXPENSE || _primaryProject != null);
       return (_expenseLimit != NULL_EXPENSE) ?
           _expenseLimit:
           _primaryProject.getMemberExpenseLimit();
   }
```


