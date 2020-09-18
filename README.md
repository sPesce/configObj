# Javascript Fetch Config Object Helper
*creates a config object for fetching to a json api backend with optional inclusion of bearer token*

## Example Usage:
- Post a new user to `/users/`:<br/>
`fetch(<usersURL>,configObj("POST",false,<newUserObject>));`
- Get a user from `/find_user/` from the token in the header:<br/> 
`fetch(<usersURL>,configObj("GET",true);`
- Patch a user to `/users/` to update it, assuming that the user is found on backend through the token in the header: <br/>
`fetch(<usersURL>,configObj("PATCH",true,<updatedUserObject>));`

## Example rails backend for above fetches
### Routes:
