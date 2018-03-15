# Prompt and Print

The purpose of this exercise is to help students understand the role of `syscall` in assembly language, as well as how to use it. The exercise is straight forward: use `syscall` in MIPS to accept some user input as text, and print it to the screen. The execution of this assembly should result in the same behavior as running this Python script:

```python
x = raw_input()
print(x)
```

# Then Ask Yourself:

* Why do we use a system call for this?
* Why do you suppose `$v0` is the register chosen for the service number, as opposed to one of the argument registers?
* Why are there different service numbers for printing floats, ints, and strings?
