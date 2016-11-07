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
  
  
