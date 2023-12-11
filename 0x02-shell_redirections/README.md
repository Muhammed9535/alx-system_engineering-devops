Attempt 1 - When piping commands, I need to explicitly add quotations around *.js and I get the output I want.
vagrant@vagrant-ubuntu-trusty-64:~/philip$ ls -laR . | find -name '*.js' -type 'f' | wc -l 4

Attempt 2 - Without the quotations...
vagrant@vagrant-ubuntu-trusty-64:~/philip$ ls -laR | find -name *.js -type f | wc -l find: paths must precede expression: dir.js Usage: find [-H] [-L] [-P] [-Olevel] [-D help|tree|search|stat|rates|opt|exec] [path...] [expression] 0

However, if I just did:
$ find -name *.js -type f | wc -l This works and returns the output I look for. I guess the extra ls command is unneccessary, but am curious why the quotations matter only in certain cases
