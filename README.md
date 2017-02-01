# Post-Fix Truth Table Generator
A little python file that creates your school assinment truth tables

### What does post-fix mean?
Good question. It means that you put the math symbol after the variables, so instead of saying `A+B` you say `AB+` it is confusing at first, but doing post fix is the easiest way to program expressions, because you don't have to worry about order of operations or parenthesis or anything. For example `(A+B)*C` is `AB+C*` in postfix. It takes a while to get used to it but you'll get it!

### What symbols am I working with?
Another good question, wow where are you coming up with these? ;)

Symbol | Expression
-------|-----------
`&` | AND
`|` | OR
`^` | XOR
`!` or `~` | NOT
`>` | IF..THEN
`<` | THEN..IF

### Now what is a Truth Table?
It is when you take your exprression such as `AB&C!|` *or `(A&B)|!C` * and evaluate every possible outcome
```
A B & C ! |
0 0 0 0 1 1
0 0 0 1 0 0
0 1 0 0 1 1
0 1 0 1 0 0
1 0 0 0 1 1
1 0 0 1 0 0
1 1 1 0 1 1
1 1 1 1 0 1
```
The last column is the final outcome, the columns under the letters are what they were initally set to *(in the first row they are all 0s then it goes through every combination till they are all 1s).* The columns under the symbols are sub sets to the solution, so like under the `&` it is the result when the `A` and `B` where AND togther. Similarly under the `!` is the NOT of `C`

Lets do one more `AB|AB&!&` *or `A|B&!(A&B)`*
```
A B | A B & ! &
0 0 0 0 0 0 1 0
0 1 1 0 1 0 1 1
1 0 1 1 0 0 1 1
1 1 1 1 1 1 0 0
```
Which is just the long way of doing XOR
```
A B ^
0 0 0
0 1 1
1 0 1
1 1 0
```

