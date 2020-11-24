### gcc

* preprocess
```shell
cpp main.c -o main.i
# -> main.i
```

* compile
```shell
cc -S main.i
# -> main.s

# or

cc -S main.c
# -> main.s
```

* assemble
```shell
as main.s -o main.o
# -> main.o
```

* link
```shell
ld main.o
# -> cannot link, required other libraries (libc and ...)
gcc main.o
# -> a.out

# shared library
gcc -shared main.o -o libmain.so
# -> libmain.so
```

##### other

* gcc
```shell
gcc main.c
# -> a.out

# preprocess only
gcc -E main.c

# compile only
gcc -S main.c

# compile and assemble
gcc -c main.c
```

* create static library
```shell
ar r libmain.a main.o
```
