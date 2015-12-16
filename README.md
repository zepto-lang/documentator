# documentator

Automatic documentation generation from function information and
docstrings. Requires that the zepto version of
[mustache](http://github.com/zepto-land/mustache) is installed.

# Usage

A command-line tool is included so as to make working with the tool
easier:

```bash
git clone https://github.com/zepto-lang/documentator
# This will generate documentation for a single function
zepto documentator/cmd.zp --output-file foo.html --function vector:head
# This will generate documentation for a namespace
zepto documentator/cmd.zp --output-file foo.html --function "vector:*"
# "*" will be treated as a wildcard and make documentation
# for all of zeptos prelude. This generates documentation
# for 459 function at the time of writing and takes some time
# (13 seconds on my machine)
zepto documentator/cmd.zp --output-file foo.html --function "*"
```

# Hacking your own documentation tool

Of course you can hack your own documentation tool on top of documentator,
although for now it is not intended to be used as a framework and very specifc.
The code underlying this module can be easily modified for generalization,
though.

<br/>

*Have fun!*
