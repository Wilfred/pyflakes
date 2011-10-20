# Pyflakes: static code analysis for Python 2

Pyflakes is a tool for finding mistakes in Python code. The code being
examined is never executed, so results are fast and accurate. On the
other hand, this won't catch everything.

## Versions supported

Python 2.5+

## Credits

Pyflakes was originally written by Divmod, which no longer appears to
exist. [kevinw](https://github.com/kevinw/pyflakes) took the code and
has maintained it since. This fork also takes a number of patches from
[dcramer](https://github.com/dcramer/pyflakes).

## Example

    from foo import bar # unused imports
    
    def my_function():
        x = 1 # unused variables
    
        return i_dont_exist() # undefined functions
        
## Usage

From source:

    $ sudo python2 setup.py install
    
This will place the pyflakes script on your $PATH. You can then do:

    $ pyflakes a_python_file.py
    
which will print any errors found. Alternatively, you can run pyflakes
directly:

    $ python2 pyflakes/scripts/pyflakes.py a_python_file.py

Integration with
[Emacs](http://www.plope.com/Members/chrism/flymake-mode) or
[vim](http://www.vim.org/scripts/script.php?script_id=2441) is also
possible, and highly recommended.

## Testing

TODO
        
## Limitations

Pyflakes performs a purely syntactic analysis. For example, if you try
to import from a non-existent file or access a non-existent object
attribute, pyflakes will not produce an error.

## Alternatives

[pylint](http://pypi.python.org/pypi/pylint) tries to solve a similar
problem, but performs a dynamic analysis
