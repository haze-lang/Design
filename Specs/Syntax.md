# Syntax

## Grammar
```
Program ::= Function | Function Program

Function ::= FuncType LineBreak FuncName '(' ParamList ')' Whitespaces '=' Whitespaces ExprChain Terminator

FuncType ::= FuncName Whitespace ':' Whitespace Mappings

Mappings ::= Mapping | Mapping Mappings
Mapping ::= TypeName Whitespace '->' Whitespace TypeName

FuncName ::= Identifer

ParamList ::= Param | Param ',' Whitespace ParamList
Param ::= Identifer

ExprChain ::= Expression

Expression ::= 

Identifer ::= 

Terminator ::= ';'

Whitespaces ::= Whitespace | Whitespace Whitespaces
Whitespace ::= ' '
LineBreaK ::= 
```