# CNF-Converter 🌊
Python code to convert First Order Logic statements into Conjunctive Normal Form
<br><br>
Input file is in the form of a count followed by that many FOL sentences on each line
<br><br>
Example: <br>
5<br>
statement 1<br>
statement 2<br>
statement 3<br>
statement 4<br>
statement 5<br>

<br>
Each FOL statement is represented as a python list in the form of operation followed by literals.<br><br>
Example A v B v C ^ !D would be written as:<br>
['or', 'A', 'B', ['and', 'C', ['not', 'D']]]

<br><br>
So an example of the input file could be:

5
<br>
['exor', 'A', 'B']
<br>
['and', ['or', 'A', 'B'], ['not', ['and', 'A', 'B']]]
<br>
['or', ['implies', 'A', 'B'], ['implies', ['not', 'A'], 'C']]
<br>
['ifte', 'A', 'B', 'C']
<br>
['exor', ['iff', 'P', 'Q'], ['and', 'R', ['not', 'P']]]

<br>

To run the code, you can simply exacute the following command: 

```
python CNFconverter.py -i input.txt -o output.txt
``` 
