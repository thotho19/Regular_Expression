# Regular Expression <br/>
[![Website](https://img.shields.io/badge/Using-JavaScript-green)]()
#### What is Regular Expression ? <br/>
A regular expression is a mechanism or a method  that can be used in any programming language for **Pattern Matching**. <br/>
#### What is Pattern Matching ? <br/>
Pattern matching is finding whether the given sub string **(Input)** is available in a specific paragraph **(bunch of texts)** by matching it's characters.<br/>
> Regular Expression is abbreviated by lazy people as **regex** or **regexp** <br/>
#### Why Regula Expression is a very fast method for matching patterns ?
Becuase **Regular Expressio** used an algorithms such as Deterministic Finite Automation **(DFA)** and Non-deterministic Finite Automation **(NFA)** to match a string.
## What are the common usage for Regular Expression ?
**Methods** | **Definition** | **Return** 
------------|----------- |-----------
Search | searching a string for specific value |return the the index of the match **OR** return -1 if no match is found 
Replace | searching a string for specific value and replace it with new string | return the new string if matched **OR** return all text
Match | searching a string for specific value | return the matches as **Array object** 
Split | split a string into an array of substrings | return the **new array**
Test | testing if match a string or not | return **True** if finds a match **OR** return **False** if doesn't find a match 
#### Regular Expression Syntax in JS
```javascript
let reg = /pattern/Modifiers
// OR 
let reg = new RegExp('pattern' , 'Modifiers');
```
## modifiers list
**Modifiers** | **Description** |
------------|----------- |
g	  |Global search.
i	|Case-insensitive search.
m	|Multi-line search.	
s	|Allows . to match newline characters.	
u	|"unicode"; treat a pattern as a sequence of unicode code points.	this modifier will be very usefull with *Arabic Patterns*
y	|Perform a "sticky" search that matches starting at the current position in the target string. See sticky.
## Brackets Use
**Brackets** | **Description** |
------------|----------- |
[...] | Character
[^....] | Not Character
[a-z] or [0-9] or [A-Z] | find any Range
[A-g] | Range[A-Z] , Range[a-g]
[0-9a-z] | Double Range **(all digits and alphabet)**
## Quantifiers Use
**Quantifiers** | **Description** 
------------|----------- 
n$ | Matches any string with n at the end of it 
^n |	Matches any string with n at the beginning of it
n+	| Matches any string of n in text
n{X} | 	Matches any string that contains a sequence of X n's
n{X,Y} | Matches any string that contains a sequence of X to Y n's
n{X,} | Matches any string that contains a sequence of at least X n's

## JavaScript Practice Task <br/>
> Write a js code to extract the item weight from the following string **"Product Weight: 11.5 pounds"** ?
```javascript
const itemData = "Product Weight: 11.5 pounds";
var itemWeight = itemData.match(/(\d+[.]\d|\d+)/g),
    weightType = itemData.match(/(pounds|ounces|lb)/gi);
    
console.log(`itemWeight:${itemWeight} weightType:${weightType}`);
```
