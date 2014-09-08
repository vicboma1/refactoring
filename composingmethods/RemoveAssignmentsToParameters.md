#Remove Assignments To Parameters

###Cuando el código se asigne a un parámetro, utiliza una variable temporal en su lugar :

```
Integer discount (int inputVal, int quantity, int yearToDate) {
    if (inputVal > 50) inputVal -= 2;
    ...
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
Integer discount (Integer inputVal, Integer quantity, Integer yearToDate) {
    int result = inputVal;
    if (inputVal > 50) result -= 2;
    ...
}
```