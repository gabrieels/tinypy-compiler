# TINYPy Compiler

A compiler for the simple language [TINYPy](TINYPy.md).

The assignment must comply three basic components of a compiler:

### Lexical Analyzer

Component responsable for the first stage of a compiler,  known as *lexical analysis* or *scanning*. The lexical analyzer reads the stream of characters making up the source program and groups the characters into  meaningful sequences called *lexemes*. For each lexeme the lexical analyzer produces as output a *token* of the form `<token-name, attribute-value>` that it passes on to the subsequent stage, the syntax analysis. The first component of a token, *token-name*, is an abstract symbol that is used during the syntax analysis and the second component, *attribute-value*, points to an entry in the symbol table for this token.

### Syntax Analyzer

Component responsable for the second stage of a compiler, the *syntax analysis* or *parsing*. The syntax analyzer or *parser* uses the first components of the tokens produced by the lexical analyzer to create a tree like intermediate representation &mdash; *syntax tree* &mdash; that depicts the grammatical structure of the token stream.

### Semantic Analyzer and Code Generator
Component responsable for the *semantic analysis* and *intermediate code generation* stages of compiler. The semantic analyzer uses the syntax tree and the information in the symbol table to check the source program for semantic consistency with the language definition. It also gathers type information and saves it in either the syntax tree or the symbol table for subsequent use during intermediate code generation. An important part of semantic analysis is *type checking* where the compiler checks that each operator has matching operands. The code generator aims to generate an explicit machine like intermediate representation from the syntax tree, which will be later translated into the target machine language.


Under [GPLv2 license](../LICENSE).
