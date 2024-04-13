# A Kernel Seedling
For Lab 0, we created a kernel module, proc_count, that counts the number of active processes in the kernel.

## Building
```shell
make
```

## Running
```shell
sudo insmod proc_count.ko   # loads the module in the kernel
cat /proc/count
```
The results are:
```
173
```

## Cleaning Up
```shell
sudo rmmod proc_count   # removes the module from the kernel
make clean
```

## Testing
```python
python -m unittest
```
The results of the test are:
```
Ran 3 tests in 1.658s

OK
```

Report which kernel release version you tested your module on
(hint: use `uname`, check for options with `man uname`).
It should match release numbers as seen on https://www.kernel.org/.

```shell
uname -r -s -v
```
The kernel version of my virtual machine is: 
```
Linux 5.14.8-arch1-1 #1 SMP PREEMPT
```