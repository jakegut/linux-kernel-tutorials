learning linux kernel development through modules for now

## hello_params
A driver based off of the tutorial from [here](http://derekmolloy.ie/writing-a-linux-kernel-module-part-1-introduction/)

In the directory: run `make`

You should now see `hello.ko` in directory

Add the module using `insmod hello.ko`

You can now see the module loaded using `lsmod` and specific info using `modinfo hello.ko`

See the module output using `dmesg`

```sh
...
[ 1834.843039] Hello world from the LKM
```

Remove the module by doing `rmmod hello.ko`

`dmesg` output:

```sh
...
[ 1834.843039] Hello world from the LKM
[ 2018.943685] Goodbye world from the LKM
```

Install module with name paramater: `insmode hello.ko name=Jake`

`dmesg` output:

```sh
...
[ 1834.843039] Hello world from the LKM
[ 2018.943685] Goodbye world from the LKM
[ 2022.097507] Hello Jake from the LKM
```


