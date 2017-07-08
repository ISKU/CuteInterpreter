# Cute Interpreter
CuteInterpreter is a Scheme interpreter similar to Racket

Description
----------
**CuteInterpreter requires Python.**
- Just run
``` bash
$ python CuteInterpreter.py
```

Example
----------
- ( car ' ( 2 3 4 ) ) <br>
- ( cdr ' ( 2 3 4 ) ) <br>
- ( cons ' ( 2 3 ) ' ( 4 5 6 ) ) <br>
- ( null? ' ( ) <br>
- ( atom? ' a ) <br>
- ( atom? ' ( ) ) <br>
- ( eq? 3 3 ) <br>
- ( eq? ' a ' a ) <br>
- ( car ( cdr ' ( 2 3 4 ) ) <br>
- ( cdr ' ( 3 4 5 ) ) ) <br>
- ( cons ( car ( cdr ' ( 2 3 4 ) ) ) ( cdr ' ( 3 4 5 ) ) ) <br>
- ( + 1 2 ) <br>
- ( - ( + 1 2 ) 4 ) <br>
- ( > 1 5 ) <br>
- ( cond ( ( null? ' ( 1 2 3 ) ) 1 ) ( ( > 100 10 ) 2 ) ( #T 3 ) ) <br>

- ( ( lambda ( x ) ( + x 1 ) ) 2 ) <br>
- ( define plus1 ( lambda ( x ) ( + x 1 ) ) ) <br>
- ( plus1 3 ) <br>
- ( define plus2 ( lambda ( x ) ( + ( plus1 x ) 1 ) ) ) <br>
- ( plus2 100 ) <br>

- ( define cube ( lambda ( n ) ( define sqrt ( lambda ( n ) ( * n n ) ) ) ( * ( sqrt n ) n ) ) ) <br>
- ( cube 10 ) <br>

- ( define lastitem ( lambda ( ls ) ( cond ( ( null? ( cdr ls ) ) ( car ls ) ) ( #T ( lastitem ( cdr ls ) ) ) ) ) ) <br>
- ( lastitem ' ( 1 2 3 4 5 ) ) <br>

- ( define a 10 ) <br>
- ( define scope ( lambda ( x ) ( define test1 ( lambda ( x ) ( define test2 ( lambda ( x ) ( + a x ) ) ) ( + ( test2 x ) x ) ) ) ( + ( test1 x ) x ) ) ) <br>
- ( scope 5 ) <br>

- ( define fact ( lambda ( x ) ( cond ( ( < x 1 ) 1 ) ( #T ( * ( fact ( - x 1 ) ) x  ) ) ) ) ) <br>
- ( fact 4 ) <br>

- ( define length ( lambda ( ls ) ( cond ( ( null? ls ) 0 ) ( #T ( + 1 ( length ( cdr ls ) ) ) ) ) ) ) <br>
- ( length ' ( a b c ) ) <br>

- ( define sum ( lambda ( ls ) ( cond ( ( null? ls ) 0 ) ( #T ( + ( car ls ) ( sum ( cdr ls ) ) ) ) ) ) ) <br>
- ( sum ' ( 3 8 6 ) <br>
   
- ( define pow5 ( lambda ( x ) ( define sqrt ( lambda ( x ) ( * x x ) ) ) ( define cube ( lambda ( x ) ( * x ( * x x ) ) ) ) ( * ( sqrt x ) ( cube x ) ) ) ) <br>
- ( pow5 2 ) <br>
