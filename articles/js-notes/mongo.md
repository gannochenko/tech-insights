# Mongo

* Update
    * `save`
    * `update`
    * `updateMany`
    * Two ways of updating
        * `.update()` by filter
        * get, check data consistency and then `.save()`
* Delete
    * `findByIdAndRemove`
    * `deleteMany`

Two ways to store nested objects:
* Normalized - by reference
* De-normalized - embed the document
* Hybrid

## ObjectId

24-char string

Bytes:
* 0-3 - timestamp
* 4-6 - machine id
* 7-8 - process id
* 9-11 - counter

Advantages of that kind of id over and auto-increment field:
* it is highly scalable
* you can have several instances and you don't need to synchronize their autoincrement field
