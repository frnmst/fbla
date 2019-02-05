# fbla

Bash library of assertions

## Table of contents

[](TOC)

## Functions

| Function name | Description |
|---------------|-------------|
| `assert_isinstance` | checks if a variable correponds to a data type |

### Detailed description

- `assert_isinstance`

      prototype: assert_isinstance(value,type)
      input:
          value = <any value>
          type  = 'bool','int','str'
      output:
          return 0    if true
          return 1    if false
      notes:
          everything evaluates to a string, even an empty variable


## Version

0.0.1

See all [fbla releases](https://github.com/frnmst/fbla/releases).

## Usage

You can adapt and include the library as a separate part of your
program by using `source ./fbla` or `. ./fbla` from the main
script.

To allow inclusion in any project the template and its documentation is 
released under the CC0 1.0 license.

## Bashisms

[Bashisms](https://mywiki.wooledge.org/Bashism) are Bash specific syntax
elements. I decided to use these because of programming convenience rather than 
compliancy. 

You will find at least the following bashisms in the library

| Bashism | Example |
|---------|---------|
| local variables | `local variable='value'` |
| conditional expression | `[[ "${variable}" = 'hello' ]]` |
| regual expresion binary operator | `[[ "${variable}" =~ [0-9] ]]` |
| pattern matching |  `[[ "${variable}" =~ [:alnum:] ]]` |

## GNU Bash "strict mode"

This template enables the shell's ["strict mode"](http://redsymbol.net/articles/unofficial-bash-strict-mode/).
You can disable it by commenting or removing the following line inside 
`fbopt`:

    set -euo pipefail

## Conventions

The following elements should be common sense and not be specific to fbopt

| Convention | Notes | Examples |
|------------|-------|----------|
| all constants are enclosed within single quotes | elements within single quotes (only) are not interpreted by the shell | `'constant'` or `'this is a constant'` |
| some variables are enclosed within double quotes | double quotes serve as a delimiter between multiple variable names if these are consecutive. Every variable between the quotes is interpolated | `"${variable}"` |
| some variables are not enclosed within double quotes | the only variables allowed without double quotes are integers (such as return values) and loop iterators (because these won't work otherwise) | `${?}` or `for v in ${values}; do echo "${v}"; done` |
| all variables use the curly braces notation | curly braces serve as a delimiter between multiple variable names if these are consecutive | `"${variable}"` or `${variable}` |
| all variable names with a constant value must be capital case | you might want to load some constants from a configuration file to override the values of options within the fbopt file | `local flag_a="${FLAG_A_DEFAULT_VALUE}"` | 

## Dependencies

The template is known to work with the the packages listed here. These must be 
of course installed on your system.

| Package | Executable | Version command | Package Version |
|---------|------------|-----------------|-----------------|
| [GNU Bash](http://www.gnu.org/software/bash/bash.html) | `/bin/bash` | `$ bash --version` | `GNU bash, version 4.4.23(1)-release (x86_64-unknown-linux-gnu)` |

## Tests

You can run tests like this:

    $ ./test_fbla

## Software using fbla

- [get-fattura-pa](https://github.com/frnmst/get-fattura-pa)

## License

Written in 2019 by Franco Masotti/frnmst <franco.masotti@live.com>

To the extent possible under law, the author(s) have dedicated all 
copyright and related and neighboring rights to this software to the public 
domain worldwide. This software is distributed without any warranty.

You should have received a copy of the CC0 Public Domain Dedication along 
with this software. If not, see 
<http://creativecommons.org/publicdomain/zero/1.0/>. 
