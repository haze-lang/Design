# Syntax

## Grammar

### Programs
```
Program ::= (Type | Function)* Procedure (Procedure | Function | Type)*
```

### Procedures
```
Procedure ::= ProcType NEWLINE PROCNAME PARAM* NEWLINE Block
ProcType ::= PROCNAME COLON Mapping
Block ::= LBRACE (Statement TERMINATOR)+ RBRACE
Statement ::= Assignment
            | Expression
Assignment ::= IDENTIFIER EQUALS Expression
```
#### Sample Procedures
```c
ScanLine : U -> U
ScanLine
{
    ...
}

PrintLine : String -> U
PrintLine str
{
    Print str
    Print "\n"
}
```

### Functions
```
Function ::= FuncType NEWLINE FUNCNAME PARAM* EQUALS (Application | PureExpression) TERMINATOR
FuncType ::= FUNCNAME COLON Mapping

Mapping ::= TypeSet (ARROW TypeSet)*
TypeSet ::= TypeUnit (CROSS TypeUnit)*
TypeUnit ::= TYPENAME
        | LPAREN Mapping RPAREN
```

#### Sample Function
```
x : U -> Nat
x = 2

f : Int X (Int -> Int) -> Int
f : a b = b a

id : Int -> Int
id x = x

add : Int X Int -> Int
```

### Types
```haskell
Type ::= SumType | RecordType
RecordType ::= RECORD TYPENAME EQUALS CONS (MEMBERNAME COLON TYPENAME)+
SumType ::= TYPE TYPENAME EQUALS ProductType (BAR ProductType)*
ProductType ::= CONS (TYPENAME (CROSS TYPENAME)*)?
```
#### Sample Types
```haskell
type Unit = U
type Bool = True | False
type Pair = Pair Int X Int
```

#### Sample Types
```
type Point = Int X Int X Int

record Point = P
X : Int
Y : Int
Z : Int
```

### Expressions
```
Expression ::= Application
            | PureExpression
            | GroupedExpression

Application ::= (PureExpression | GroupedExpression) Expression+

GroupedExpression ::= LPAREN Expression RPAREN

PureExpression ::= SwitchExpr
            | ConditionalExpression
            | LambdaExpr
            | IDENTIFIER
            | LITERAL

ConditionalExpression ::= IF PureExpression THEN PureExpression ELSE PureExpression

SwitchExpr ::= SWITCH PureExpression NEWLINE (Pattern ARROW PureExpression TERMINATOR)+ DEFAULT ARROW PureExpression

LambdaExpr ::= PARAM+ DARROW (Block | PureExpression)

Pattern ::= LITERAL // TODO
```

#### Samples
##### Lambda
```
\ => { Print "Hey" }
x => add x 1
```
##### Switch

```
switch n
    0 -> 1;
    default -> n * factorial (n-1)
```

### Lexical Grammar
```
TYPE ::= 'type'
RECORD ::= 'record'
IF ::= 'if'
THEN ::= 'then'
ELSE ::= 'else'
SWITCH ::= 'switch'
DEFAULT ::= 'default'
BAR ::= '|'
CROSS ::= 'X'
UNIT ::= '()'
EQUALS ::= '='
COLON ::= ':'
ARROW ::= '->'
DARROW ::= '=>'
BSLASH ::= '\'
LPAREN ::= '('
RPAREN ::= ')'
LBRACE ::= '{'
RBRACE ::= '}'
PROCNAME ::= IDENTIFIER
FUNCNAME ::= IDENTIFIER
PARAM ::= IDENTIFIER
TYPENAME ::= IDENTIFIER
CONS ::= IDENTIFIER
MEMBERNAME ::= IDENTIFIER
IDENTIFIER ::= ALPHA (ALPHA | DIGIT)*
ALPHA ::= 'a' ... 'z' | 'A' ... 'Z' | '_' | '''
DIGIT ::= '0' ... '9'
LITERAL ::= NUMBER | STRING | CHAR | UNIT
NUMBER ::= DIGIT+ | ('-' DIGIT+)
CHAR ::= ''' (ALPHA | DIGIT) '''
STRING ::= '"' (ALPHA | DIGIT)* '"'
TERMINATOR ::= ';' | NEWLINE
WHITESPACE ::= ' ' | 't' | NEWLINE
NEWLINE ::= '\r\n' | '\r' | '\n'
```