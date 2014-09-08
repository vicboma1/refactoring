#Extract Method

###Agrupar fragmentos de código en métodos propios :

```
public String toString (Integer age) {
    System.out.println();
    System.out.println ("name:" + name);
    System.out.println ("age" + age);
}
```

![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
public String toString(Integer age) {
    toStringSpace();
    toStringDetails(age);
}
 
public String toStringDetails(Integer age) {
    System.out.println ("name:" + name);
    System.out.println ("age" + age);
}

public String toStringSpace(){
    System.out.println();
}
```


