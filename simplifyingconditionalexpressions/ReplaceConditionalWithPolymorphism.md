#Replace Conditional with Polymorphism

###Si tiene un condicional que determina un comportamiento diferente en función del tipo de un objeto, desplaza cada 
###expresion condicional a un método abstracto de una subclase :

```
   public double getSpeed() {
        switch (_type) {
            case EUROPEAN:
               return getBaseSpeed();
            case AFRICAN:
               return getBaseSpeed() - getLoadFactor() * _numberOfCoconuts;
            case NORWEGIAN_BLUE:
               return (_isNailed) ? 0 : getBaseSpeed(_voltage);
        }
        throw new RuntimeException ("Should be unreachable");
    }
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
  class Employee...
      int payAmount() {
          switch (getType()) {
              case EmployeeType.ENGINEER:
                 return _monthlySalary;
              case EmployeeType.SALESMAN:
                 return _monthlySalary + _commission;
              case EmployeeType.MANAGER:
                 return _monthlySalary + _bonus;
              default:
                 throw new RuntimeException("Incorrect Employee");
          }
      }
      
    int getType() {
      return _type.getTypeCode();
    }
    
    private EmployeeType _type;
  
    abstract class EmployeeType...
      abstract int getTypeCode();
    
    class Engineer extends EmployeeType...
      int getTypeCode() {
          return Employee.ENGINEER;
      }
    
    ... and other subclasses

    
     class EmployeeType...
        int payAmount(Employee emp) {
            switch (getTypeCode()) {
                case ENGINEER:
                   return emp.getMonthlySalary();
                case SALESMAN:
                   return emp.getMonthlySalary() + emp.getCommission();
                case MANAGER:
                   return emp.getMonthlySalary() + emp.getBonus();
                default:
                   throw new RuntimeException("Incorrect Employee");
            }
        }
        
     ...
        
      class Employee...
        int payAmount() {
            return _type.payAmount(this);
        }
        
      class Engineer...
        int payAmount(Employee emp) {
            return emp.getMonthlySalary();
        }
        
        ...
        
      class EmployeeType...
          int payAmount(Employee emp) {
              switch (getTypeCode()) {
                  case ENGINEER:
                     throw new RuntimeException ("Should be being overridden");
                  case SALESMAN:
                     return emp.getMonthlySalary() + emp.getCommission();
                  case MANAGER:
                     return emp.getMonthlySalary() + emp.getBonus();
                  default:
                     throw new RuntimeException("Incorrect Employee");
              }
          }
          
       class Salesman...
          int payAmount(Employee emp) {
              return emp.getMonthlySalary() + emp.getCommission();
          }
      
        class Manager...
          int payAmount(Employee emp) {
              return emp.getMonthlySalary() + emp.getBonus();
          }
      
      ...
      
        class EmployeeType...
          abstract int payAmount(Employee emp);    
```
