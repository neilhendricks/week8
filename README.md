# week8

Green Site <br/>
Attack 1: XSS on Green
Go to Contact Us section and give feedback
  Type any username and a fake email, and in the feedback section, inject code
  Input javascript code: <SCRIPT>alert('XSS attack')</SCRIPT>
  Submit the feedback  
 When you log in and click on the feedback page, the alert will pop up

Attack 2: Username Enumeration on Green
When logging in, if you use a correct username but an incorrect password, it will produce bold text saying unsuccessful login.
If you use an incorrect username and an incorrect passwoard, the result unsuccessful login text will not be bold.

Bonus Objective XSS on Green
Similar to the previous XSS attack on Green, just use the following line of code to send the user to any link
<SCRIPT>windows.location.assign('https://www.hofstra.edu/home/index.html')</SCRIPT> <br/>
<br/>

Blue Site <br/>
Attack 1: SQL injection
Go to Find a Salesperson
Click on a Salesperson
In the URL, https://35.225.211.56/blue/public/salesperson.php?id=4%27OR%271%27%3D%271
You can see the Salesperson's ID. In the example above, id=4
The id value can now be replaced with something else, such as SQL code ' OR SLEEP(3)=0--'

Attack 2: Session Hijacking
The session id can be found using burp
The session id can then be manipulated to acess the users session


Red Site<br/>
Attack 1: CSRF on Red
Similar to XSS attack on Green site. Submit a malicious script on the feeback section. 

Attack 2: IDOR
In the Salesperson section, the id of each salesperson is in the URL.
The id value can be changed the find users that should not be found. 

