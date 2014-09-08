#Replace Nested Conditional with Guard Clauses

###Un método tiene un comportamiento condicional que no tiene claro el camino normal de ejecución. Utiliza cláusulas 
###de guardia para todos los casos especiales.

```
  public double getPayAmount() {
      double result;
      if (_isDead) result = deadAmount();
      else {
          if (_isSeparated) result = separatedAmount();
          else {
              if (_isRetired) result = retiredAmount();
              else result = normalPayAmount();
          };
      }
    return result;
    };
    
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
public double getPayAmount() {
     if (_isDead) return deadAmount();
     if (_isSeparated) return separatedAmount();
     if (_isRetired) return retiredAmount();
     return normalPayAmount();
   }; 
```
