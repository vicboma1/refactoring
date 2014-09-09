#Remove Middle Man

###Cuando una clase es demasiado simple, llamamos al delegado directamente. 

```
  public class Person {
     Department department;	
     public Person getManager() {
         return department.getManager();
  
  public  class Department {
     private Person manager;
     public Department (Person manager) {
         manager = manager;
     }
 
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
 class Person {
 
 ...
 
    public Department getDepartment() {
        return _department;
    }
  }
  
  manager = john.getDepartment().getManager();
   
´´´


