## Mass Assignment
***
1. **Description**

```
Software frameworks sometime allow developers to automatically bind HTTP request parameters into program code variables or objects to make using that framework easier on developers. This can sometimes cause harm.

Attackers can sometimes use this methodology to create new parameters that the developer never intended which in turn creates or overwrites new variable or objects in program code that was not intended. This is called a Mass Assignment vulnerability.
```
2. **Example/Exploitation**
```
- Guess the sensitive parameter field and can use in add user or edit user functionality.
- Guess an idea of internal variables used in object using API Docs or other.
- E.g. There is a parameter **"isAdmin"** to know about user. Take the advantage of this variable and add it into **adduser** and **password update**. Make the user as admin
```
3. **Mitigation**
