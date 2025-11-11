# 🛠️ Install Flex and Bison

To set up the environment for Lex and Yacc development, install the required packages:

```shell
$ sudo apt-get install flex bison build-essential vim
```

---

# 📄 Lex Workflow

Use Lex to generate a lexical analyzer:

```shell
$ vim <file_name>.l
-> esc
-> :wq
$ lex <file_name>.l         # Generate lex.yy.c from the .l file
$ cc lex.yy.c -ll           # Compile the lexer with the lex library
$ ./a.out                   # Run the compiled lexer
```

---

# 📄 Yacc Workflow

Use Yacc (via Bison) to generate a parser and integrate it with Lex:

```shell
$ vim <file_name>.l
-> esc
-> :wq
$ lex <file_name>.l         # Generate lexer code
$ yacc -d <file_name>.y     # Generate parser code and header file
$ gcc y.tab.c lex.yy.c -lfl  # Compile both lexer and parser
$ ./a.out                   # Run the combined program
```

## Practical :
### lex
`1)Theory assignment for writing details about LEX and YACC compilation.` <br>
`2) Count the number of comments, keywords, identifiers, words, lines and spaces from input file.` <br>
`3) Count number of words starting with 'A'.` <br>
`4) Conversion of lowercase to uppercase and vice versa.` <br>
`5) Conversion of decimal to hexadecimal number in a file.`<br>
`6) Test lines ending with ''com''.`<br>
### lex + YACC
`7) Postfix Expression Evaluation.`<br>
`8) Desk calculator with error recovery.`<br>
`9) Parser for ''FOR'' loop statements.`<br>
### C
`10) Intermediate code (IC) generator for arithmetic expression.`<br>
