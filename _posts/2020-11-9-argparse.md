---
layout: post
title:  "Python argparse and namespace"
date:   2020-11-09 10:22:12 -0700
categories: Python
---

## What is argparse?
The Python `argparse` module defines what arguments it requires, and `argparse` will figure out how to parse those out of `sys.argv`. It also automatically generates help and usage messages and issues errors when users give the program incalid arguments. 

## How to use the `argparse` program?
__create an ArgumentParser object__

`parser = argparse.ArgumentParse(description="Process some integers")`

 - description: a brief description of what the program does and how it works.

__add argument__

```
parser.add_argument('integers', metavar='N', type=int, nargs="+", help='an integer for the accumulator')
parser.add_argument('--sum', const=sum, default=max, help='sum the integers (default: find the max)')
```

* nargs="+": '+' just like '*', all command-line args present are gathered into a list. 
* help message: when type `python <name of script> -h`, it shows a list of available arguments and its associated help message if the help message is specified in `ArgumentParser` object. 
* 

__parse argument__

```
parser.parse_args(['--sum', '7', '-1', '-42'])
=> Namespace(accumulate=<built-in function sum>, integers=[7, -1, 42])
```

- The `Namespace` object: it is an object created by the `argparse.Namespace` class used by default by `parse_args()`. This object holds attributes and its value in the `ArgumentParser` object. 

Example 1: 
```
args = parser.parse_args(['--foo', BAR]) => type(args) is an Namespace object
vars(args) => {'foo': 'BAR'}
```

Example 2: have an `ArgmentPaser` assign attributes to an already existing object, rather than a new `NameSpace` object.
```
class C:
    pass
c = C()
parser = argparse.ArgumentParser()
parser.add_argument('--foo')
parser.parse_args(['--foo', BAR], namespace=c)
c.foo => 'BAR'
```

Example 3: directly create a Namespace object
```
from argparse import Namespace
args = Namespace(foo='bar')
```
* Namespace object can be saved and re-loaded using pickle. 
