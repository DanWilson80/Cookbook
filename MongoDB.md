MongoDB
======
  
Index
------
[MongoDB Terminal Commands](#MongoDB \Terminal \Commands)

MongoDB Terminal Commands
------

* **show dbs** - shows all DB's  
* **use [db name]** - use DB, will create the DB if it doesn't exist    
* **show collections** - show collections inside current DB  
* **db.createCollection('collectionName')** - create a new collection  
* **db.[collection].drop()** - delete collection  
* **db.[collection].insert({ name: "Dan", age: "39" })** - inserts new entry to collection  
* **db.[collection].find()** - lists collection objects  
* **db.[collection].find().pretty()** - lists objects neatly  
* **db.[collection].remove({ name: "Dan", age: "39" })** - deletes object from collection  
* **db.[collection].remove({})** - deletes the contents of a collection but leaves the collection existing empty within the DB * **db.[collection].update({"_id": ObjectId("number")}, {$set:{"author": ObjectId("number")}});** - updates the id and in this case sets the author to be whatever user id we enter so we can cahnge records from the terminal inside MongoDB   
* **db.drop.dataBase()** - delete DB's  

  
* **Add new user with cURL:**   
```
curl -d "username="ian2&password=password" -X POST http://localhost:3000/register
```  
* *This will POST a new "username": "ian2", "password": "password" to the http://localhost:3000/register ROUTE*  
* **If we had a *reviews* collection and wanted to update the *author*(if we had one setup in our models) we would use the following command from terminal while running `./mongod` and `mongo`:  
  
**Update review author:**  
```
db.reviews.update({"_id": ObjectId("5bb28ac8fcd2647d7c0c0446")}, {$set: {"author": ObjectId("5bc521c0b142b6d7f7523406")}});
```  
*This example takes a review "_id" and changes it's "author" to the "user id" that we take from the "users" collection to allow manual alteration of the collections from the terminal within MongoDB*  
  
[Index](#Index)  
  

  
  
