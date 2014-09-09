#Inline Class

###Cuando una clase no aporta solvencia, eliminarla y añadir sus atributos a otras.

```
 public class Person {
 
     private String name;
     private TelephoneNumber officeTelephone = new TelephoneNumber();
  
     public String getName() {
         return name;
     }
     public String getTelephoneNumber(){
         return officeTelephone.getTelephoneNumber();
     }
     TelephoneNumber getOfficeTelephone() {
         return officeTelephone;
     }
  
   }
   
   public class TelephoneNumber {
   
    private String number;
    private String areaCode;
        
     public String getTelephoneNumber() {
         return ("(" + areaCode + ") " + number);
     }
     String getAreaCode() {
         return areaCode;
     }
     void setAreaCode(String arg) {
         areaCode = arg;
     }
     String getNumber() {
         return number;
     }
     void setNumber(String arg) {
         number = arg;
     }
   }
 
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
public class Person {

       String getAreaCode() {
           return officeTelephone.getAreaCode();
       }
       void setAreaCode(String arg) {
           officeTelephone.setAreaCode(arg);
       }
       String getNumber() {
           return officeTelephone.getNumber();
       }
       void setNumber(String arg) {
           officeTelephone.setNumber(arg);
       }
   }
   
     Person martin = new Person();
     martin.setAreaCode ("781");
   
´´´


