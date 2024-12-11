# myges-documentation
Documentation for the MyGES API

## Authenticate a user and get a token
GET https://authentication.kordis.fr/oauth/authorize?response_type=token&client_id=skolae-app
### Headers
Authorization : Basic {credentials}

*Convert a string with the value <b>username:password</b> to Base64 to get the appropriate value of {credentials}

You should get a redirect address, the value query parameter <b>access_token</b> of the redirection address (comreseaugesskolae:/oauth2redirect#) is the token you need to use. In the documentation the token will be called {token}, you will need to replace {token} with your own token value.

## Use the token to get and modify user informations

All endpoints listed require an Autorization header with the value :

bearer {token}

### GET https://api.kordis.fr/me/profile

### GET https://api.kordis.fr/me/agenda?start={startTime}&end={endTime}

startTime: the start time in milliseconds since the Unix Epoch

endTime : the end time in milliseconds since the Unix Epoch

### GET https://api.kordis.fr/me/news/banners

### GET https://api.kordis.fr/me/news?page={page}

### GET https://api.kordis.fr/me/{year}/grades

### GET https://api.kordis.fr/me/{year}/absences

### GET https://api.kordis.fr/me/{year}/teachers

### GET https://api.kordis.fr/me/{year}/classes

### GET https://api.kordis.fr/me/classes/{classeId}/students

### GET https://api.kordis.fr/me/students/{studentId}

