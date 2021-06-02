## Cookie Based Issues

1. Cookies Attributes </br>
  * Check all cookie attributes are set properly.
  
2. Cross Site Scripting
  * Check for XSS if the application is reflected cookie value in the response.
  
3. SQL Injection
  * 
4.  If the cookies are using some access defining parameter such as "user_id"
  * Change the value of these parameter in order to check if you can access other user's data.
  
5. Check for guessable or weak cookie

6.  Try accessing a protected resource by removing cookies.
  * If the resource is accessible via GET Request, try for Direct Request (Forceful Browsing) with unauthenticated user.
  
7. Denial of Service - Cookie Bomb
  * Forcing the server to process cookies larger than the restricted cookie size defined by the server may cause Denial of Service Attack.
  * Read: https://blog.innerht.ml/tag/cookie-bomb/
  
8. Parameter Pollution
  * Assume that the cookies utilize a parameter called "user_id=" to retrieve some data.
  * Attacker, add an additional "user_id=" parameter value to the cookie with victim's user ID. Like: "user_id=attacker&user_id=victim" 
  * Three things can happen here:
    - The application may retrieve data of Victim User. 
    - The Application may retrieve data of both Attacker & Victim User.
    - The Application is not vulnerable and doesn't return anything.

9. Mass Assignment 
  * Similar to the Parameter Pollution, However, in this, Attacker tried to Inject multiple User ID in same user_id parameter.

10. Insecure Deserialization
   * If cookies are using Serialized Objects, try performing Insecure Deserialization Checks.
  
