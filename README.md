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

