## Mass Assignment
***
1. **Description**

```
Software frameworks sometime allow developers to automatically bind HTTP request parameters into program code variables or objects to make using that framework easier on developers. This can sometimes cause harm.

Attackers can sometimes use this methodology to create new parameters that the developer never intended which in turn creates or overwrites new variable or objects in program code that was not intended. This is called a Mass Assignment vulnerability.
Many frameworks provide convenient mass-assignment functionality. This lets developers inject an entire set of user-entered data from a form directly into an object or database.
```
2. **Example/Exploitation**
```
- Guess the sensitive parameter field and can use in add user or edit user functionality.
- Guess an idea of internal variables used in object using API Docs or other.
- E.g. There is a parameter "isAdmin" to know about user. Take the advantage of this variable and add it into "adduser" and "password update". Make the user as admin.
- Guess: isadmin, is_admin, is_Admin, is_administrator, is_Administrator, is_admin_user, is_admin_account etc.
```
3. **Mitigation**
```
- The developer should change the code to either explicitly assign the attributes for the allowed fields, or use a whitelisting function provided by the framework.
  def signup
  # Explicit assignment:

  @user = User.create(
    email: params[:user][:email],
    password: params[:user][:password]
  )

  # or whitelisting:

  @user = User.create(
    params.require(:user).permit(:email, :password)
  )
end
```
4. **References**
