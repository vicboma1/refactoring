#Hide Delegate

###Cuando llamamos a una clase delegada, creamos métodos para ocultar el delegado :

```
 public class Person {
    Department department;
 
    public Department getDepartment() {
        return department;
    }
    public void setDepartment(Department arg) {
        department = arg;
    }
  }
     
  public class Department {
    private String chargeCode;
    private Person manager;
 
    public Department (Person manager) {
        manager = manager;
    }
 
    public Person getManager() {
        return manager;
    }
 }
   
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
  ...
  
  public Person getManager() {
       return _department.getManager();
  }
  
  ...

   manager = john.getManager();
   
´´´


