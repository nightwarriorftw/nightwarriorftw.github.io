---

title: Invoking the command line with python 
date: "2019-01-28T17:12:33.962Z"
---

cmd2 is a tool for building interactive command line applications in python. It's main aim is to help developers work fast and efficiently.

### Description 
```cmd2``` is a python module and is an extension of ```Cmd``` (which is a simple framework for writing line-oriented command interpreters).It's main feature is autocompletion. 

### Installation
```pip install cmd2```

### Basics 

```
from cmd2 import Cmd

class Demo(Cmd):
	def __init__(self):
		Cmd.__init__(self)

if __name__ == '__main__':
	app = Demo()
	app.cmdloop()
```
