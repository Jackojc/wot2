# wot2
wot2 is an experimental offshoot of wot++ that uses term rewriting instead
of functions and function application.

wot2 draws heavy inspiration from [mlatu](https://github.com/mlatu-lang/mlatu).

Like its predecessor, wot2 reduces from a higher level representation of a
document down to a single large string of text. In effect, it allows you to
write a DSL that better conforms to your problem and have it produce some more
common format. In wot2, all terms must eventually be reduced down to a series of
strings which are then concatenated to produce the final document. Any terms which
are not rewritten will result in an error.

```
: # 'x => "<h1>" x "</h1>" ;

# foo
```
=>
```
<h1>foo</h1>
```
