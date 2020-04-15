# Binary:

## 1 wire electricity signal can be either:  
 
| 1| 0|
|:---:|:---:|
|true|false|
|on | Off |
|yes | no |

Eacho position is  *2 to the left

More wires = larger numbers

wire | signal
|:---:|:----:|
1 | 1
8 |255
32 | 4 billion

###All things can be represetned by numbers! 

- Alphabet: assign a number to a letter

- Images: Pixel = Color can be defined as numbers

- Sound: Vibrations can be represented graphically, all wave points can be defnied by a number (more bits = more steps) 


# Circuits:

## Tiny Electronic components that relay binary

### Main Circuts

```->-``` *Not* Circuit: is the signal the same or not?

```=>-``` *And* Circuit: only if both of the cirtcuits are 1 

```=o=``` *Adder* Circuit: sums 2 bits
>put multiple of these side by side to add huge numbers

Smaller the circuit = less distance it has to go (speed of light is constant)

# What do computers do?

- Input Information
- Store Information
- Process Information
- Output Information

| Computer| Fucntion |
|:----:|:----|
| Input | Converts physical input into binary information |
| Memory | Stores Binary Information |
| CPU | Calculates Information |
|Output | Converts Information into physical output  | 

### Keyboard converts press to a binary
### CPU requests instructions from the memory on how to make the Key
### CPU runs instructions and stores in memory
### Memory is then sent to the screen


### What is REST?

R - Resources: URLS tell the browser that concepts live somewhere, the browser then goes an asks for a reprsentation of that concept.
    - most resources usually only have a single representation

Use an HTTP Get to get a resource from a server adn return it to the browser

if a system needs to add to another system, HTTP Post

if a system needs to replace another system, HTTP Put


### SQL
Structured Query Language

Designed to work with tables

ex: 
Id |	Make/Model |	# Wheels |	# Doors	Type |
1	| Ford Focus| 	4	| 4	 | Sedan |
2	| Tesla Roadster |	4	 | 2| 	Sports|
3	Kawakasi Ninja |	2 |	0 |	Motorcycle |
4	|McLaren Formula | 1 |	4 |	0 |	Race |
5 |	Tesla S	| 4 |	4 |	Sedan |

How do you navigate this table?

Query - What are we looking for and where

```SELECT columnTitle, another_columnTitle, ... FROM myTable```
    - 2d set of rows and columns with only the coliuns requested

```SELECT * FROM myTable``` 
    - All of the table data

```SELECT column, another_column, …FROM mytable WHERE condition AND/OR another_condition AND/OR …;``` 
    - select columns where the conditions are met

Operator	| Condition	| SQL | Example| 
=, !=, < <=, >, >=	Standard numerical operators	col_name != 4
BETWEEN … AND …	Number is within range of two values (inclusive)	col_name BETWEEN 1.5 AND 10.5
NOT BETWEEN … AND …	Number is not within range of two values (inclusive)	col_name NOT BETWEEN 1 AND 10
IN (…)	Number exists in a list	col_name IN (2, 4, 6)
NOT IN (…)	Number does not exist in a list	col_name NOT IN (1, 3, 5)


=	Case sensitive exact string comparison (notice the single equals)	col_name = "abc"
!= or <>	Case sensitive exact string inequality comparison	col_name != "abcd"
LIKE	Case insensitive exact string comparison	col_name LIKE "ABC"
NOT LIKE	Case insensitive exact string inequality comparison	col_name NOT LIKE "ABCD"
%	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)	col_name LIKE "%AT%"
(matches "AT", "ATTIC", "CAT" or even "BATS")
_	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)	col_name LIKE "AN_"
(matches "AND", but not "AN")
IN (…)	String exists in a list	col_name IN ("A", "B", "C")
NOT IN (…)	String does not exist in a list	col_name NOT IN ("D", "E", "F")

```SELECT column, another_column, …FROM mytable WHERE condition(s) ORDER BY column ASC/DESC LIMIT num_limit OFFSET num_offset;```