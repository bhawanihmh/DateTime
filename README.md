# DateTime
SELECT TO_CHAR( SYSDATE, "MM-dd-yyy HH:mm:ss" ) FROM dual;

# Java
``
SimpleDateFormat sdf = new SimpleDateFormat("dd-MM-yyyy hh:mm:ss"); 
String dateInString = "22-01-2015 10:20:56"; 
Date date = sdf.parse(dateInString);
  LocalDate localDate = date.toInstant().atZone(ZoneId.systemDefault()).toLocalDate();
  int year = localDate.getYear(); 
  System.out.println("year = " + year);
  int month = localDate.getMonthValue();
  String monthStr = month < 10 ? ("0"+month) : ""+month;
System.out.println("monthStr = " + monthStr);
int dayOfMonth = localDate.getDayOfMonth();
String dayOfMonthStr = dayOfMonth < 10 ? ("0"+dayOfMonth) : ""+dayOfMonth; 
System.out.println("dayOfMonthStr = " + dayOfMonthStr);
int hours = date.getHours();
String hoursStr = hours < 10 ? ("0"+hours) : ""+hours; 
System.out.println("hoursStr = " + hoursStr);
int minutes = date.getMinutes();
String minutesStr = minutes < 10 ? ("0"+minutes) : ""+minutes; 
System.out.println("minutesStr = " + minutesStr);
int seconds = date.getSeconds();
String secondsStr = seconds < 10 ? ("0"+seconds) : ""+seconds; 
System.out.println("secondsStr = " + secondsStr);
``
