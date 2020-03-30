<h2 align="center">The Monkey Language Interpreter</h2>

<div align="center">
  <img width="150" src="https://www.oreilly.co.jp/books/images/picture_large978-4-87311-822-2.jpeg" />
</div>
<p align="center">
  <a href="https://www.oreilly.co.jp/books/9784873118222/">Go言語でつくるインタプリタ</a>
</p>
<div align="center"></div>



This is an interpreter for the Monkey language. Try REPL.


```shell
$ go get -u github.com/raahii/monkey-interpreter
```

```shell
❯ monkey
Hello, ${username}! This is the Monkey programming language!
Feel free to type in commands
>> 5
5
>> -5
-5
>> 2 * (3 + 2) / 3
3
>> let x = 3
>> if ( x > 5 ) { true } else { false }
false
>> let add = fn(x, y) { return x + y; };
>> add(x, 5)
8
>> let newAdder = fn(x) { fn(y) { return x + y } };
>> let addTwo = newAdder(2);
>> addTwo(x);
5
```



## Monkey Language

- integer, boolean, string, array, hash
- `+`, `-`. `*`, `/`, `(`, `)`  
- `puts(<string>)`, `len(<array>)`, `first(<array>)`, `last(array)`, `rest(<array>)`

## Lexer (chapter1)

![lexer](https://user-images.githubusercontent.com/13511520/77818620-32e0c800-7117-11ea-9236-a45e101a56ca.gif)

## Parser (chapter2)

![parser](https://user-images.githubusercontent.com/13511520/77818622-396f3f80-7117-11ea-89d9-fd07fd8acdfa.gif)

## Evaluator (chapter3)

![evaluator](https://user-images.githubusercontent.com/13511520/77818628-42f8a780-7117-11ea-90d9-370174ac6229.gif)

## Updated interpreter (chapter4)

- Add support for new literals and builtin functions.

  - String (litral, `+`)
  - Array (literal, indexing, `len()`, `push()`, `first()`, `rest()`, `last()`)
  - Hash (literal, indexing)
  - `puts()`

  

![updated](https://user-images.githubusercontent.com/13511520/77881222-7400e580-7299-11ea-98e9-476370e31eda.gif)
