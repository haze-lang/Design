# Syntax

## Grammar

### Programs
```c
Program ::= Procedure (Procedure | Function)*
```

### Procedures
```c
Procedure ::= ProcType NEWLINE PROCNAME 
```

### Functions
```c
Function ::= FuncType NEWLINE FUNCNAME PARAM+ '=' Expression TERMINATOR
FuncType ::= FUNCNAME ':' Mapping
Mapping ::= TypeSet '->' TypeSet
TypeSet ::= TYPENAME (CROSS TypeSet)*
```

#### Sample
`id : Int -> Int`  
`id x = x`

`add : Int x Int -> Int`  

### Expressions
```c
Expression ::= FuncInvoke | '(' Expression ')' | SwitchExpr | IDENTIFIER | Literal

FuncInvoke ::= FUNCNAME Expression+
SwitchExpr ::= 'switch' '=>' (Pattern '->' Expression TERMINATOR)+
Pattern ::= Literal //TODO
```

#### Sample
`switch n => `  
`0 -> 1;`  
`1 -> 1;`  
`default -> n * factorial (n-1)`

### Literals
```
Literal ::= NUMBER | STRING
```

### Misc.
```
Whitespaces ::= WHITESPACE | WHITESPACE Whitespaces
```

### Lexical Grammar
```c
FUNCNAME ::= IDENTIFIER
PARAM ::= IDENTIFIER
TYPENAME ::= IDENTIFIER
IDENTIFIER ::= ALPHA (ALPHA | DIGIT)*
CROSS ::= 'X'
ALPHA ::= 'a' ... 'z' | 'A' ... 'Z' | '_' | '''
DIGIT ::= '0' ... '9'
NUMBER ::= DIGIT+ | (DIGIT+ '.' DIGIT+)
STRING ::= '"' (ALPHA | DIGIT)* '"'
TERMINATOR ::= ';' | NEWLINE
WHITESPACE ::= ' ' | NEWLINE
SEPERATOR ::= TERMINATOR
NEWLINE ::= '\r\n' | '\r' | '\n'
```