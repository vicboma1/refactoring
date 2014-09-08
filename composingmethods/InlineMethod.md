#Inline Method

###Si el cuerpo del método es tan claro como su nombre, agruparlo todo en el mismo método :

```
int getRating() {
  return (moreThanFiveLateDeliveries()) ? 2 : 1;
}

boolean moreThanFiveLateDeliveries() {
  return _numberOfLateDeliveries > 5;
}

```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
int getRating() {
  return (_numberOfLateDeliveries > 5) ? 2 : 1;
}
```