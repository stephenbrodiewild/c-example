# c-example
Example C project layout for a friend

# Project layout
Put your .c files in src, your .h files in include, your tests in tests.

# Building, running, cleaning
I just copy-pasted the Makefile from some repo, edited it a little, and it seems to work fine.

This will build your binary and place it in bin, and a symbolic link to it in the root directory
```bash
make
```

I chucked the bin and build directories in the .gitignore so that you don't push them up to github etc.

Say the generated executable is called 'hello', execute it by running:

```bash
./hello
```

Delete the old binary and related build artifacts by running

```bash
make clean
```

I haven't made any nice test stuff yet.

Say you want to run the tests in __test_maths.c__.
```bash
gcc src/maths.c tests/test_maths.c -I include/ -o test
./test
``` 

That'll do it.