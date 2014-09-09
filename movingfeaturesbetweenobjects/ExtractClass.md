#Extract Class

###Simplificar una clase con la información semánticamente necesaria y componerla 
###con otra clase que tenga la información adicional :

```
 public class Person {
 
      private String name;
      private String officeAreaCode;
      private String officeNumber;
      
      public String getName() {
          return name;
      }
      public String getTelephoneNumber() {
          return ("(" + officeAreaCode + ") " + officeNumber);
      }
      String getOfficeAreaCode() {
          return officeAreaCode;
      }
      void setOfficeAreaCode(String arg) {
          officeAreaCode = arg;
      }
      String getOfficeNumber() {
          return officeNumber;
      }
      void setOfficeNumber(String arg) {
          officeNumber = arg;
      }
 
 }
 
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

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
      public TelephoneNumber getOfficeTelephone() {
          return officeTelephone;
      }
 
     
  }
      
   public class TelephoneNumber {
   
      private String number;
      private String areaCode;
   
      public String getTelephoneNumber() {
          return ("(" + areaCode + ") " + _number);
      }
      public String getAreaCode() {
          return areaCode;
      }
      public void setAreaCode(String arg) {
          areaCode = arg;
      }
      public String getNumber() {
          return number;
      }
      public void setNumber(String arg) {
          number = arg;
      }
   }
   
´´´


