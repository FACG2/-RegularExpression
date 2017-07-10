# Regular Expressions

- ### What is Regular Expressions ?
 
  Regular expressions are patterns used to match character combinations in strings. 

### Pattern creation and repitions:
  Using a regular expression literal, which consists of a pattern enclosed between slashes, as follows:
var re = /ab+c/;

Or calling the constructor function of the RegExp object, as follows:
  var re = new RegExp('ab+c');

- #### Charcter Classes
|                |         |
|---------------:| --------|
| match any      | [\s\s]  |
| word           | \w      |
| not word       | \W      |
| digit          | \d      |
| not digit      | \D      |
| whitespace     | \s      |
| not whitespace | \S      |
| character set  | [ABC]   |
| negated set    | [^ABC]  |
| range          | [A-Z]   |

- #### Anchors
|                   |       |
| -----------------:|:------|
| beginning         | ^     |
| end               | $     |
| word boundary     | \b    |
| not word boundary | \B    |

- #### Escaped Characters
|                 |         |
| ---------------:|:--------|
| tab             | \t      |
| line feed       | \n      |
| carriage return | \r      |
| null            | \0      |

if we want to get ont of these characters ., \ , + , * , ? , ^ , $ , ( , { , [ , ] , } , ) , | , /
just put backslash "\" before it.

- #### Flags
|                |       |
|---------------:|:------|
| ignore case    | i     |
| global search  | g     |
| multiline      | m     |

Expression flags change how the expression is interpreted. There are three flags in JS: i, g, and m. Flags follow the closing backslash of the expression (ex. /.+/igm ).

note: if we want to get except some characters we just put dash "-" in the first of [] and we write these characters we wan to ignore.

- #### Groups & Lookaround
**capturing group** (ABC)

**Example:**
```javascript
  var re = /(\w+)\s(\w+)/;
  var str = 'John Smith';
  var newstr = str.replace(re, '$2, $1');
  console.log(newstr)
```
- #### Quantifiers & Alternation
|           |       |
|----------:|:------|
| plus      | +     |
| star      | *     |
| quantifier| {1,3} |
| quantifier| 2     |

### on-line tools

1. [RegExr](http://regexr.com/)

   We recommend using it because of it's many advantges like: syntax highlighting, contextual help, video tutorial.

2. [Scriptular](http://scriptular.com/)

3. [Regex Tester](http://www.regexpal.com/)


### Email validator
  * this is an email validator written by regular expression:
```javascript
/[\w.]+@\w{3,}\.[a-z]{2,}/gi
```


### Resources
  * [Regular Expressions MDN](https://developer.mozilla.org/en/docs/Web/JavaScript/Guide/Regular_Expressions)  
  * [30 Useful Tools and Resources](http://www.hongkiat.com/blog/regular-expression-tools-resources/)
  * [online course](https://www.youtube.com/watch?v=7DG3kCDx53c&list=PLRqwX-V7Uu6YEypLuls7iidwHMdCM6o2w)
