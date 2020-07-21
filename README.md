# read_log_files
Program to read and print web logs

<b>LogEntry</b> - Class that has five private variables, a constructor, five get methods to access the private fields, and a toString method for printing out a LogEntry. Contains the following methods:
* <b>LogEntry</b> - constructor method that initializes the following private variables:
  * *ipAddress* - String to contain the ip address.
  * *accessTime* - Date object to contain the time of access.
  * *request* - String to contain the request.
  * *statusCode* - Integer to contain the status code.
  * *bytesReturned* - Integer to contain the bytes returned.
* <b>getIpAddress</b> - returns the *ipAddress* as a String.
* <b>getAccessTime</b> - returns the *accessTime* as a Date object.
* <b>getRequest</b> - returns the *request* as a String.
* <b>getStatusCode</b> - returns the *statusCode* as an Integer.
* <b>getByesReturned</b> - returns the *bytesReturned* as an Integer.

<b>LogAnalyzer</b> - constructor initializes records to an empty ArrayList. Contains the following methods:
* <b>readFile</b> - creates a FileResource and to iterate over all the lines in the file. For each line, creates a LogEntry and store it in the records ArrayList. 
* <b>printAllHigherThanNum</b> - has one integer parameter num. This method examines all the web log entries in records and print those LogEntrys that have a status code greater than num.
* <b>uniqueIPVisitsOnDay</b> - has one String parameter named someday in the format “MMM DD” where MMM is the first three characters of the month name with the first letter capitalized and the others in lowercase, and DD is the day in two digits (examples are “Dec 05” and “Apr 22”). This method accesses the web logs in records and returns an ArrayList of Strings of unique IP addresses that had access on the given day.
  * For example, consider that d is a Date. String str = d.toString(); allows you to now use a String representation of the date.) Be sure to test your program with code in the Tester class. Using the file weblog-short_log you should see that the call to uniqueIPVisitsOnDay(“Sep 14”) returns an ArrayList of 2 items and uniqueIPVisitsOnDay(“Sep 30”) returns an ArrayList of 3 items.
* <b>countUniqueIPs</b> - returns an integer representing the number of unique IP addresses. It assumes that the instance variable records already has its ArrayList of Strings read in from a file, and accesses records in computing this value. 
* <b>countUniqueIPsInRange</b> - has two integer parameters named low and high. This method returns the number of unique IP addresses in records that have a status code in the range from low to high, inclusive.
  * For example, using the file short-test_log, the call countUniqueIPsInRange(200,299) returns 4, as there are four unique IP addresses that have a status code from 200 to 299. The call countUniqueIPsInRange(300,399) returns 2. In this case, note that there are three entries in the file that have a status code in the 300 range, but two of them have the same IP address.

<b>WebLogParser</b> - class with <b>ParseEntry</b> helper method.

<b>Tester</b> - Class to test the program.

Links to exercises:
* https://www.coursera.org/learn/java-programming-arrays-lists-data/supplement/cAl9o/programming-exercise-reading-log-files
* https://www.coursera.org/learn/java-programming-arrays-lists-data/supplement/xGjL5/programming-exercise-finding-unique-ip-addresses
* https://www.coursera.org/learn/java-programming-arrays-lists-data/supplement/ygOPU/programming-exercise-counting-website-visits
