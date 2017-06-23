### Relational Integrity:

These rules that ensures that data is accurate.

* Entity Integrity:
  - Primary keys must have a value (space is not considered a value).
* The Referential Integrity:
  is there if a foreign key exists in a relation. So if you have a relation you must make sure you have a foreign key somewhere. Either the foreign key value must match a candidate key value of some tuple in it’s home relation or the foreign key value must be wholly null. So either is always no value or always is some value, if it’s both, need to check what is going on.
 Constraints: additional rules specified by the users or by the database admin of a db.
 All this is established usually in very boring, but useful, meetings with the experts about your db data. There you decide how to categorise your data.


 Relationship
 The association among entities is called a relationship. For example, an employee works_at a department, a student enrolls in a course. Here, Works_at and Enrolls are called relationships.

 Relationship Set
 A set of relationships of similar type is called a relationship set. Like entities, a relationship too can have attributes. These attributes are called descriptive attributes.

 Degree of Relationship
 The number of participating entities in a relationship defines the degree of the relationship. Binary = degree 2, Ternary = degree 3, n-ary = degree n.
