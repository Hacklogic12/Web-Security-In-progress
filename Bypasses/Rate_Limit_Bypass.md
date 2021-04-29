## **Methods to Bypass Rate Limit**

### Limit Bypass Functionality- OTP, Coupon code, Feedback Form, Login, Singup, Comments etc.
***

1. **Using Request-ID**
  ```
  If the application is using the different **Request-ID** in each request then intercept the request, copy the request id in the *.txt* file and drop the request. Likewise,       prepare a list of request ids. Now, using the intruder, load the file and perform the attack.
  ```
2. **Using Burp Extension**
   * https://github.com/TheKingOfDuck/burpFakeIP/blob/master/fakeIP.py
   * https://portswigger.net/bappstore/3a656c1be14148c6bf95642af42eb854 (Random-IP-Address)
  ```
  Note- Using IP-Rotate burp extension, each request will go through AWS API gateway endpoiints in each region changing source IP on each request to the target.
  https://rhinosecuritylabs.com/aws/bypassing-ip-based-blocking-aws/
  ```
 
3. **Using Different Parameter**
   - POST /api/v1/login
   - POST /api/v1/Login 
   - POST /api/v1/singup
   - POST /api/v1/sign-up
   - POST /api/v1/Sign-up
   
4. **Use the following request-header** 
```
  - X-Originating-IP: 127.0.0.1
  - X-Forwarded-For: 127.0.0.1
  - X-Remote-IP: 127.0.0.1
  - X-Remote-Addr: 127.0.0.1
 ```
 > ***Tip-1*** Try with X-Forwarded-For: IP 2x times instead of one time. </br>
 > ***Tip-2*** Sometimes, it is showing 10 request per account, then can bypass it by using different IP after 10 attempts. Use X-Forwarded-For: 192.168.0.101

5. Using **null byte** and **CRLF**  
   - %00, %0d%0a, %20, %0, %09, %0c
   
6. Changing **user-agents**   
