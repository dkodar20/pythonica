Pythonica
=========

This is the new home of Pythonica. It was written by Joe Strout. Until this
page is fleshed out, information on Pythonica can be found here.

http://www.strout.net/info/coding/python/pythonica.html


Changes
=======

6/10/04
-------
*   Added list support. Lists are encased in square brackets ([])
*   Added slice support. A slice is written as [[args]] right after an
    expression and returns the component of the expression described by args.
    The first arg acts on the expression, the second arg acts on the result of
    the first, etc. A value of 0 returns a symbol for the head of the
    expression, a positive integer returns that component of the expression (as
    if the expression was a 1-based list) and a negative number returns the
    component that number from the end of the expression.
*   Fixed parsing such that a+b*c+d works and that a=c*d+k*r works
*   Fixed complex number parsing such that j by itself is equivalent to 1j

5/27/04
-------
*   Fixed floating point numbers to not complain that "." isn't an operator
*   Complex number shorthand now works! 2j now becomes Complex[0,2], and 2+2j
    now becomes Plus[2,Complex[0,2]]
*   Number detection is now better. Instead of saying "Syntax error" if you
    type an invalid token that begins with a digit, it now tells you
    specifically that symbols can't begin with a digit

5/25/04
-------
*   Added functions Sqrt/Root/Exp/Abs/Mod/Round
*   Re-wrote a bunch of logic concerning parsing tokens and groups
*   Fixed some strange bugs, like Sin[3,2],2 becoming Sin[3,2,2]
*   Made non-alphanumeric chars treated as operators
*   Added an undefined operator message for undefined operators
*   Added fairly comprehensive complex number support - currently you have to
    write complex numbers as Complex[real,imag] (imag being optional and defaults
    to 0). In the future you will be able to write them like (3+2j)

5/23/04
-------
*   Added functions Sin/Cos/Tan/ASin/ACos/ATan/Rad2Deg/Deg2Rad
*   Divide is no longer chainable
*   You can put full-form functions next to each other and it assumes multiply:
    Sin[3]Sin[4] is equivalent to Sin[3]*Sin[4]
*   If an exception occurs while running as a program, it outputs information
    and continues. If an exception occurs while running from the interpreter
    (i.e. imported as a module) it passes the exception on for debugging
*   Other miscellaneous bugfixes
