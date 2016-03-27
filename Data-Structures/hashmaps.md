# Hashmaps
<hr>
***Hashmaps*** are helpful tools that allow us to store a key and a value. Unlike Arrays and Arraylists, with ***Hashmaps*** we can easily look up a value if we know its key. 
<br>
<br>
With that said, lets say you are creating a piece of software that stores student grades throughout a school. We want to be able to look up a student's grade by their name, so we will need to use a ***Hashmap***.

### What a Hashmap Looks Like
<hr>
With Hashmaps we can have keys and assign each key a value. So, if we are creating a piece of software to store student grades, our keys are the student's names and the value is the grade itself. It is important to remember that each key can only have **one** value.

This would look like:

| Key | Value |
| -- | -- |
| Wezley Sherman | 85 |
| Wade Adams | 95 |
| Julio Rodriguez | 84 |
| Trevor Forrey | 100 |
| Ada Lovelace | 96 |
| Sally Pants | 98 |
| Sarah Abe | 86 |

The ***Key*** is the element we use to look up a specific ***Value*** in the map.
<br>
The ***Value*** is the result we get when we look up a specific item with a ***Key***. 
<br>
The ***Key-Value Pair*** is the combination of the ***Key*** and the ***Value*** associated.
<br>

### Utilizing Hashmaps
<hr>

##### Creating Hashmaps:
In order to create a ***Hashmap*** we use: `Hashmap<key_type, value_type> name = new Hashmap<key_type, value_type>();`. 
<br>
<br>
If we were to create our gradebook ***Hashmap*** we would use: `Hashmap<String, Integer> gradeBook = new Hashmap<String, Integer>();`
<br>
<br>

##### Adding Items:
To add an item to a ***Hashmap*** we use: `map.put(key, value);`
<br>
<br>
If we were to add grades to our gradebook ***Hashmap*** we would use:
```Java
gradeBook.put("Wezley Sherman", 85);
gradeBook.put("Wade Adams", 95);
gradeBook.put("Julio Rodriguez", 84);
...
```
<br>

##### Retrieving Items:
To retrieve an item from a ***Hashmap*** we use: `map.get(key);`
<br>
<br>
Lets say we wanted to access Trevor Forry's and Ada Lovelace's grades. To do so we would use:
```Java
int adaGrade = gradeBook.get("Ada Lovelace");
int trevGrade = gradeBook.get("Trevor Forrey");
```
<br>

#####


