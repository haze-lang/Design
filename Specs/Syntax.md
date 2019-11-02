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
ExprList ::= Expression | Expression ',' WHITESPACE ExprList
Expression ::= FuncInvoke
FuncInvoke ::= FUNCNAME '(' ExprList ')'
```

### Misc.
```
Whitespaces ::= WHITESPACE | WHITESPACE Whitespaces
```

### Lexical Grammar
```
FUNCNAME ::= IDENTIFIER
TYPENAME ::= IDENTIFIER
IDENTIFIER ::= ALPHA (ALPHA | DIGIT)*
ALPHA ::= 'a' ... 'z' | 'A' ... 'Z' | '_' | '''
DIGIT ::= '0' ... '9'
WHITESPACE ::= ' ' | LINEBREAK
TERMINATOR ::= ';'
LINEBREAK ::= '\r\n' | '\r' | '\n'
```