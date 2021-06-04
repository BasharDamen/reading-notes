# **Operators and Loops.**

# Expressions and Operators #

## operators : ##
_**Operators**_ could be a _keywords_, _numbers_, or _symbols_ that are beeing used in the process of making a website. Opertators help you as a developer through assigning values to a variable, making calculations, comparingm, and so on.  

In **JS** there are a lot of operators and has both _binary_ and _unary_ operators. 

When we said a **_Binary Operator_**, we mean that the operator requires two _operands_, one before and one after the operator.

`operand1 operator operand2`  
such as `x+y` or `x=y`

On the other hand, the **_Unary Operator_** requires one _operand_.  

`Operand Operator` or `Operator Operand`  
such as `x++` or `++x`

**JS** has wide types of operators:

* [Assignment operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#assignment_operators)
* [Comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#comparison_operators)
* [Arithmetic operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#arithmetic_operators)
* [Bitwise operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#bitwise_operators)
* [Logical operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#logical_operators)
* [String operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#string_operators)
* [Conditional (ternary) operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#conditional_ternary_operator)
* [Comma operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#comma_operator)
* [Unary operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#unary_operators)
* [Relational operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#relational_operators)

## Expressions ##
_**Expressions**_ are a set of codes that are being used in order to resolve to a value. Expressions can be either those that assigning value to a variable for example, or those who evaluate in order to esolve to a value.

Referring to the first type we can say that `x=10`, whilst in the second example the `10` value can be evaluated with a different ways such as `5+5` or `3+7`.

**_JS_** contains the following expressions:
* Arithmetic
* String
* Logical
* Primary expressions
* Left-hand-side expressions  

# Loops #
**loops** are a type of codes can be used in JavaScript in order to make an action being repeated. Using loops is sufficient and effective because it give you the ability to make your website make something ,that requires a lot of codes to be done, more simply and easily.

There are a lot of loops types provided by JavaScript :
* for statement
* do...while statement
* while statement
* labeled statement
* break statement
* continue statement
* for...in statement
* for...of statement

but we will talk about two types:

## For statement ##

A **_For loop_** statement is used to make an action reapeats until a specific condition evaluates to ** `False` ** .
and it consists of: 

> ` for ([initialExpression]; [conditionExpression]; [incrementExpression]){statement} `.

1- initialExpression: works as initializer for one or more loops counter.   
2- conditionExpression: this part is being evaluated every loop if it evaluate _true_ until it being evaluated _false_, then the for loop breaks.  
3- incrementExpression: will be excuted after the conditionExpression has been evaluated as _false_.


## While statement ##

As a specific condition is being evaluated as _true_, then _while statement_ will continue to excute its statement until that condition being evaluated as _false_.  
It looks like:   
> ` while (condition){statement}`

The _while statement_ is being tasted for its value all over again until it becomes evaluated as _false_.
