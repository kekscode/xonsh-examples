### Basic Usage

```
>>> print("xonsh is a superset of python 3.4, so you can write python code)
```

```
>>> echo "and also use most of the BASH goodness you're accustomed to"
```

```
>>> import sys; print(sys.version)
```

```
>>> print("2 + 1.4 = {:f}".format(2+1.4))
```

```
>>> l = "all the python types are here to play".split()
```

```
>>> $PATH
>>> $ENV_VARIABLE = 'Just a Python Variable (though $ is now allowed in this case!)'
>>> del $ENV_VARIABLE
>>> ${'H' + 1*'O' + 'ME'}  # Inside the curly braces is a Python <expr>
```

```
>>> for i, x in enumerate("niiice!"):
      print(i, x)
```

```
>>> def magic(word):
      return word[::-1]
>>> magic("Never odd or even"")
```

```
>>> print("Python first, subprocesses afterwards:")
>>> ls -l
>>> ls = 2
>>> l = 1
>>> ls -l
>>> del ls
>>> del l
```

```
>>> print("Catch output form a subprocess using $()")
>>> now = $(date)
>>> now.split()[-2]
```

```
>>> print("Print output directly to screen and don't capture anything")
>>> useless_var = $[date]
>>> type(useless_var)
```

```
>>> print("Now let us get crazy: Mix @Python and $Subprocesses")
>>> for i in range(100):
        $[touch @('file_{}'.format(i))]  # @() is Python and $[] is shell
```

```
>>> print("entering the dangerzone(TM)")
>>> $[$(echo ls) @('-' + $(echo l).strip())]  # Baaad stuff. But fun.
```

```
>>> touch "I love whitespaces. lots  of $&§  them."  # easy
>>> rm 'I love whitespaces. lots  of $&§  them.'  # handy!
```

```
>>> print("Backtick-Syntax in xonsh is very different from bash: Its for regexes!")
>>> touch a aa aaa aba abba aab aabb abcba
>>> ls `a(a+|b+)a`
>>> print(`a(a+|b+)a`)
>>> len(`a(a+|b+)a`)
```

```
>>> print("how do i get help? iPython-Style!")
>>> import socket
>>> socket?
>>> socket.getaddrinfo??
>>> dict?.keys??
```

### Advanced Usage
