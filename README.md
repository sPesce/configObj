# Javascript Fetch Config Object Helper
*creates a config object for fetching to a json api backend with optional inclusion of bearer token*

## Usage:
`configObj(method,authenticate,data)`
#### Input:
- **method:string**: http method (ex: "GET", "PATCH", "POST" ... etc.)
- **authenticate:boolean**: should config object include a bearer token in the header for authentication?
- **data:object**: the payload being sent as *body* in config object *JSON.stringify() is used in the function*
### Output:
- A config object used as the optional second parameter in a fetch method call


## Example Usage:
#### setup:
`const USERS_URL = 'localhost:3000/'`
`const FIND_USER_URL = 'localhost:3000/find_user'`
`const user = {phone_number: "5552221919"}`
#### examples:
- Post a new user:<br/>
`fetch(USERS_URL,configObj("POST",false,user));`
- Get a user from the token in the header:<br/> 
`fetch(FIND_USER_URL,configObj("GET",true);`
- Patch a user to `/users/` to update it, assuming that the user is found on backend through the token in the header: <br/>
`fetch(USERS_URL,configObj("PATCH",true,user));`

