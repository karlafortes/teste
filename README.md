# Merchant's Guide to the Galaxy

This project consists on a program that converts numbers and units based on inputed notes to make buying and selling over the galaxy easier.

### Problem full description

You decided to give up on earth after the latest financial collapse left 99.99% of the earth's population with 0.01% of the wealth. Luckily, with the scant sum of money
that is left in your account, you are able to afford to rent a spaceship, leave earth, and fly all over the galaxy to sell common metals and dirt (which apparently is
worth a lot).

Buying and selling over the galaxy requires you to convert numbers and units, and you decided to write a program to help you.

The numbers used for intergalactic transactions follows similar convention to the roman numerals and you have painstakingly collected the appropriate translation
between them.

Roman numerals are based on seven symbols:

| Symbol | Value |
|--------|-------|
| I | 1 |
| V	| 5 |
| X |	10 |
| L	|	50 |
| C	|	100 |
| D	|	500 |
| M	|	1000 |

Numbers are formed by combining symbols together and adding the values. For example, MMVI is 1000 + 1000 + 5 + 1 = 2006. Generally, symbols are placed in order of value,
starting with the largest values. When smaller values precede larger values, the smaller values are subtracted from the larger values, and the result is added to the total.
For example MCMXLIV = 1000 + (1000 − 100) + (50 − 10) + (5 − 1) = 1944.

- The symbols "I", "X", "C", and "M" can be repeated three times in succession, but no more. (They may appear four times if the third and fourth are separated by a smaller
value, such as XXXIX.) "D", "L", and "V" can never be repeated.
- "I" can be subtracted from "V" and "X" only. "X" can be subtracted from "L" and "C" only. "C" can be subtracted from "D" and "M" only. "V", "L", and "D" can never be
subtracted.
- Only one small-value symbol may be subtracted from any large-value symbol.
- A number written in Arabic numerals can be broken into digits. For example, 1903 is composed of 1, 9, 0, and 3. To write the Roman numeral, each of the non-zero digits
should be treated separately. In the above example, 1,000 = M, 900 = CM, and 3 = III. Therefore, 1903 = MCMIII.

(Source: Wikipedia http://en.wikipedia.org/wiki/Roman_numerals)

Input to your program consists of lines of text detailing your notes on the conversion between intergalactic units and roman numerals.

You are expected to handle invalid queries appropriately.

Test input:

glob is I  
prok is V  
pish is X  
tegj is L  
glob glob Silver is 34 Credits  
glob prok Gold is 57800 Credits  
pish pish Iron is 3910 Credits  
how much is pish tegj glob glob ?  
how many Credits is glob prok Silver ?  
how many Credits is glob prok Gold ?  
how many Credits is glob prok Iron ?  
how much wood could a woodchuck chuck if a woodchuck could chuck wood ?  

Test Output:

pish tegj glob glob is 42  
glob prok Silver is 68 Credits  
glob prok Gold is 57800 Credits  
glob prok Iron is 782 Credits  
I have no idea what you are talking about  

## Installing / Getting started

To see it running you must have Microsoft Visual Studio 2017 or superior installed on your machine. You should then download the project and open the .sln file.

Once there, you will have to execute the program to get to see it working. For that, go to the superior menu and open the tab "Debug" and then click on "Start Debugging".
You can also just press "F5".

You will be asked to input your notes. It expects you to tell your insights about the units and conventions you know, so you can ask about its translations. It is
important to know that the numbers used for intergalactic transactions follows similar convention to the roman numerals. For example, you may type "banana is I" and
"apple is V" and ask the program "how much is banana apple?" which should returns "banana apple is 4".

Some important rules to make the program understands you well is to use the proper sentences to communicate with it:

- to set unit values (the banana and apple on our previous example), you should simply type "{{nameOfUnit}} is {{unitValue}}". The unit value here must be a Roman numeral.
- to set units with conventions like "banana apple Silver", you should place the convetion after all units and tell how many credits the unit worths with it. So you should
type your sentence like this "{{nameOfUnit}} {{nameOfUnit}} ... {{convention}} is {{value}} Credits". The value here is an Arabic number. Example: "banana apple Silver is 20 Credits", being "Silver" the convention. It is possible to set only one convention by sentence.
- to get the value of something, simply ask how much or how many credits does it worth. For example, "how much is banana apple?" or "how many credits is banana apple Silver?"

## A walk inside my mind

I tried to keep the architecture simple, so I separeted it in 3 project: the main project, one to hold the business logic and one for unit tests. On them I applied some concepts to make it clean, readable and scalable, however keeping in mind the current scope and focusing on solving the problem we have now.

## Contact

Created by [@karlafortes](https://www.linkedin.com/in/karlafortes/) - feel free to contact me!
