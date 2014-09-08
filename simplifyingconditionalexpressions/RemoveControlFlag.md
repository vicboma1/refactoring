#Remove Control Flag

###Si tenemos una variable que actúa como un indicador de control para una serie de expresiones booleanas, 
###Utiliza un break o devuelva su valor directamente :

```
  public void checkSecurity(String[] people) {
        boolean found = false;
        for (int i = 0; i < people.length; i++) {
            if (! found) {
               if (people[i].equals ("Don")){
                 sendAlert();
                 break;
               }
               if (people[i].equals ("John")){
                 sendAlert();
                 break;
               }
            }
        }
    }
```
![](http://www.iconki.com/icons/Software-Applications/32x32-Applications-Basics/arrow_down_blue.png)

```
    public void checkSecurity(String[] people) {
         for (int i = 0; i < people.length; i++) {
             if (people[i].equals ("Don")){
                sendAlert();
                break;
             }
             if (people[i].equals ("John")){
                sendAlert();
                break;
             }
         }
     }
```
