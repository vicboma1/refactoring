#Split Temporary Variable

###Hacer una variable temporal independiente para cada asignación :

```
double temp = 2 * (height + width);
System.out.println (temp);
temp = height * width;
System.out.println (temp);

```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
final double perimeter = 2 * (height + width);
System.out.println (perimeter);
final double area = height * width;
System.out.println (area);

```