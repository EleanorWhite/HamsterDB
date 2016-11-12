# HamsterDB
New Database Structure

## Initial Notes:
### TODO:
* Memory Loader
* Interpreter
* Define file form/ syntax

### Node Types:
* field
* relationship

### Functions:
* insert
    * fields
    * relationships
* remove
* path
* degrees of separation
* alter
    * change fields
    * add/remove relationships 

## Design and Possibly Pseudocode:
### The Database Class

* We write an interpreter in shell script that can generate types.
* This then creates header and implementation files with all the types.
* The Database class should have a friend class called Node.
* The types should inherit from the Node class.
* What data types would the Node class have?
* Would we have to use templated functions that can work with various subclasses of the node class?

```
Node has a string datamember that is the primary key
Node has a list of Relationship objects
  Relationship objects each contain a tag
  Relationship objects each contain a list of objects that this object has this relationship to
Node has a function that adds relationships
  Should be a simple matter
Node has a function that finds relationships
  Should also be a simple matter
Node has a function that finds what relationship this object has to something else
Node contains a boolean data member indicating whether it is a passive or mutual relationship
```
