# Syntax

## Grammar

### Programs
```
Program ::= Function | Function Program
```

### Functions
```
Function ::= FuncType LINEBREAK FUNCNAME '(' ParamList ')' Whitespaces '=' Whitespaces ExprChain TERMINATOR

FuncType ::= FUNCNAME WHITESPACE ':' WHITESPACE Mappings

Mappings ::= Mapping | Mapping Mappings
Mapping ::= TYPENAME WHITESPACE '->' WHITESPACE TYPENAME

ParamList ::= Param | Param ',' WHITESPACE ParamList
Param ::= IDENTIFIER
```

### Expressions
```
ExprChain ::= Expression
Expression ::= FuncInvoke | Literal
FuncInvoke ::= FUNCNAME Expressions
Expressions ::= Expression | Expression WHITESPACE Expressions

ExprList ::= Expression | Expression ',' WHITESPACE ExprList
```

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
TYPENAME ::= IDENTIFIER
IDENTIFIER ::= ALPHA (ALPHA | DIGIT)*
ALPHA ::= 'a' ... 'z' | 'A' ... 'Z' | '_' | '''
DIGIT ::= '0' ... '9'
NUMBER ::= DIGIT+ | (DIGIT+ '.' DIGIT+)
STRING ::= '"' (ALPHA | DIGIT)* '"'
WHITESPACE ::= ' ' | LINEBREAK
TERMINATOR ::= ';'
LINEBREAK ::= '\r\n' | '\r' | '\n'
```