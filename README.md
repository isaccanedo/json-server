# json-server
Demo of the JSON server for fake JSON data

We can use this url: http://jsonplaceholder.typicode.com/

OR... make this server to do locally.

Following tutorial video: https://www.youtube.com/watch?v=1zkgdLZEdwM

### Basic install start

* `npm init` (use a nam other than json-server or it won;t work)
* `D:\WEBDEV\demos\json-server>npm install --save json-server`

### Basic install start

* Now we need to make a script to start the json server
* We can start the server with: `json-server --watch db.json`
* Let's make this an npm scripts
* In scripts in package.json in json:server
* `"json:server":"json-server --watch db.json"`

### Make data file

* Next we have to create our data file - call it db.json
* This is going to be a basic json file
* Get the starter data from http://jsonplaceholder.typicode.com/users
* Add fake data
* Let's say you have users and companies - you can add a companyId to correlate



### Start server

* Start server:  `npm run json:server`

* Should get a result like:
```

 Loading db.json
 Done

 Resources
 http://localhost:3000/users
 http://localhost:3000/companies

 Home
 http://localhost:3000

 Type s + enter at any time to create a snapshot of the database
 Watching...

```


### Different routes available

* GET ALL USERS
http://localhost:3000/users

* GET SINGLE USER
http://localhost:3000/users/1

* GET ALL COMPANIES
http://localhost:3000/companies

* GET SINGLE COMPANY
http://localhost:3000/companies/1

* GET ALL USERS OF A COMPANY
http://localhost:3000/companies/1/users

* FILTER COMPANIES BY NAME
http://localhost:3000/companies?name=Microsoft
http://localhost:3000/companies?name=Microsoft&name=Apple

* PAGINATION & LIMIT
http://localhost:3000/companies?_page=1&_limit=2

* SORTING
http://localhost:3000/companies?_sort=name&_order=asc

* USERS AGE RANGE
http://localhost:3000/users?age_gte=30
http://localhost:3000/users?age_gte=30&age_lte=40

* FULL TEXT SEARCH
http://localhost:3000/users?q=Leanne


### Add User - Postman in Chrome

* We're going to add a user in Postman - this is something you cannot do with the remote version.

* POST: http://localhost:3000/users
* Go into Headers (if not there, hit + on tabs) and specify Content-Type is application/json
* In Body (raw data): curly braces and data

Example:

```
{
	  "name": "Chris Scott",
      "username": "C3333",
      "age": "42",
      "email": "Chadada_McDermott@dana.io",
      "companyId":"2"
}
```


* Hits SEND, should get info back with new Id
* Check: http://localhost:3000/users


### Delete User - Postman in Chrome

* Switch to Delete
* http://localhost:3000/users/11


### Patch User - Postman in Chrome
* Start same as Add user but for Patch
* Go into Headers (if not there, hit + on tabs) and specify Content-Type is application/json
* In Body (raw data): curly braces and data
* PATCH: http://localhost:3000/users/1
```
{
	"username":"Cs1900"
}
```







.
