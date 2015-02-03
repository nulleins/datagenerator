# DataGenerator
Utility to create test data strings, specified by a 'picture' definition, e.g.,
* `A(12)` - alphabetic string, twelve characters long
* `N(2)` - numeric string, two characters long
* `AN(20)` - alpha-numeric string, twent characters long
* `A(1),N(8)` - a single alphabetic character, followed by a eight-digit number

Example
-------
``` java
final String code = DataGenerator.create("A(2),N(1)");
```    

(solution uses a matcher/stream utility based on a solution by:[Marko Topolnik](http://stackoverflow.com/users/1103872/marko-topolnik))
