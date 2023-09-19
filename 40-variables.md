---
layout: page
title: Variables
permalink: variables.html
---

```javascript
// easy version
noFill();
int diam = 10; // diam for "diameter",
circle(50,50, diam);
diam = diam + 10;
circle(50,50, diam);
diam += 10; // "a += b" is a shortcut for "a = a + b"
circle(50,50, diam);
// etc...
```

ensuite…

```javascript
// Version using 2 variables
noFill();
int diam = 10;
int step = 8;
circle(50,50, diam);
diam += step;
circle(50,50, diam);
diam += step;  circle(50,50, diam);
diam += step;  circle(50,50, diam);
diam += step;  circle(50,50, diam);
diam += step;  circle(50,50, diam);
```


## Declarer une variable

```javascript
// I need to remember a number. 
// Call it ‘lucky’. 
// It’s 7.

int lucky = 7;
```


- `int` : pour enregistrer un nombre entier
- `lucky` : le nom de notre variable
- `=` : l'opérateur permettant d'assigner une valeur à la variable 
- `7` : la valeur 


## Modifier une variable

```javascript
// I changed my mind, my lucky number is now 9.

lucky = 9;

// No, wait, my lucky number is now whatever it was minus 3.

lucky = lucky - 3;

// Add 2 to my lucky number.

lucky += 2;

// Your lucky number is 5.

int yourNum = 5;

// Let’s add your number to my number.

lucky += yourNum;
```
