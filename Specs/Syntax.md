# Syntax

## Grammar

### Programs
```c
Program ::= Procedure (Procedure | Function)*
```

### Procedures
```c
Procedure ::= ProcType NEWLINE PROCNAME Body
Body ::= LBRACE (Statement TERMINATOR)+ RBRACE
Statement ::= Declaration | Assignment | Expression | ConditionalStatement
```
#### Sample Procedure
```c
PrintLine : String
PrintLine str
{
    Print str
    Print "\n"
}
```

### Functions
```c
Function ::= FuncType NEWLINE FUNCNAME PARAM+ EQUALS PureExpression TERMINATOR
FuncType ::= FUNCNAME COLON Mapping
Mapping ::= TypeSet ARROW TypeSet
TypeSet ::= TYPENAME (CROSS TypeSet)*
```

#### Sample Function
```
id : Int -> Int
id x = x

add : Int x Int -> Int
```

### Types
```c
Type ::= TYPE TYPENAME EQUALS TYPENAME | RecordType
RecordType ::= RECORD TYPENAME (MEMBERNAME TYPENAME)+
```

### Expressions
```
Expression ::= ProcInvoke | PureExpression
ProcInvoke ::= ..
PureExpression ::= FuncInvoke | LPAREN PureExpression RPAREN | SwitchExpr | IDENTIFIER | Conditional | Literal
Conditional ::= IF PureExpression THEN PureExpression ELSE PureExpression
FuncInvoke ::= FUNCNAME PureExpression+
SwitchExpr ::= SWITCH PARAM DARROW (Pattern ARROW PureExpression TERMINATOR)+
LambdaExpr ::= (BSLASH | PARAM+) DARROW (BODY | PureExpression)
Pattern ::= Literal // TODO
```

#### Samples
##### Lambda
```
\ => { Print "Hey" }
x => { Print (add x 1) }
```
##### Switch
```
switch n => 
    0 -> 1;
    default -> n * factorial (n-1)
```

### Literals
```
Literal ::= NUMBER | STRING
```

### Misc.
```

```

### Lexical Grammar
```
TYPE ::= 'type'
RECORD ::= 'record'
IF ::= 'if'
THEN ::= 'then'
ELSE ::= 'else'
SWITCH ::= 'switch'
CROSS ::= 'X'
EQUALS ::= '='
COLON ::= ':'
ARROW ::= '->'
DARROW ::= '=>'
BSLASH ::= '\'
LPAREN ::= '('
RPAREN ::= ')'
LBRACE ::= '{'
RBRACE ::= '}'
FUNCNAME ::= IDENTIFIER
PARAM ::= IDENTIFIER
TYPENAME ::= IDENTIFIER
MEMBERNAME ::= IDENTIFIER
IDENTIFIER ::= ALPHA (ALPHA | DIGIT)*
ALPHA ::= 'a' ... 'z' | 'A' ... 'Z' | '_' | '''
DIGIT ::= '0' ... '9'
NUMBER ::= DIGIT+ | ('-' DIGIT+)
STRING ::= '"' (ALPHA | DIGIT)* '"'
TERMINATOR ::= ';' | NEWLINE
WHITESPACE ::= ' ' | NEWLINE
NEWLINE ::= '\r\n' | '\r' | '\n'
```