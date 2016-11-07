# Rethinkdb v. 2.3.5


### Work the multi index based on the field tags

```Javascript
  // Create
  r.db("Awr").table("y").indexCreate("tags", {multi:true})
  
  // Get records by multi index
  r.db("Awr").table("y").getAll("sp","kt","aa", {index:"tags"}) 
  
  // Get records by multi index with table
  r.db("Awr").table("w").eqJoin("id", r.db("Awr").table("y"),  {index: "tags"}).zip()
    
```

### Update by index
```Javascript
   r.db("System").table("Corporation")
   .getAll("A00ff17e6f25031c463acece7a7917042460BIBI", {index:"ID"})
   .update({CORP:"Bi"})
 ```
  
### Update multi field
```Javascript
  r.db("Awr").table("y")
 .get("e5b370c1-8ce3-4a18-be29-fb13cc8f5984")
 .update({ "title": [ "P12", "p22"],   "content":[ "ct", "ct", "ctf", "ca", "czz"],  "tags": [ "kt", "lt", "vt", "aa", "zz"]})
```
