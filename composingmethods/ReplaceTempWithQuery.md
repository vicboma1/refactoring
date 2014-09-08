#Replace Temp with Query

###Extraer la expresión en un método.
###Sustituir todas las referencias en una llamada a un nuevo método para que se pueda utilizar en otros métodos. :

```
double basePrice = _quantity * _itemPrice;
if (basePrice > 1000)
    return basePrice * 0.95;
else
    return basePrice * 0.98;
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
if (basePrice() > 1000)
    return basePrice() * 0.95;
else
    return basePrice() * 0.98;
...

Double basePrice() {
    return _quantity * _itemPrice;
}

```
