# x)
- John Hammond analyzes the PicoCTF 2022 reverse engineering challenge “bbbloat”.
- He first runs the program, which asks for a “favorite number” and exits if the input is wrong.
- He tries basic dynamic analysis tools such as ltrace (library calls) and strace (system calls), but they do not reveal the correct value.
- He then opens the binary in Ghidra and creates a new project.
- Using Ghidra’s Code Browser, he explores strings, functions, variables, and cross-references.
- By searching for the string “favorite number”, he finds the exact location in the code where the check is performed.
- Ghidra’s decompiler reveals a hardcoded hexadecimal value, 0x86187.
- Converting this value to decimal gives 549255, which is the correct input to reveal the flag picoCTF{…}.
# a)

```sh
sudo apt-get install ghidra
```

# b)

![Pastedimage](Pastedimage20260208202620.png)
i remember that this package is packed with upx so i unpacked
![Pastedimage]({078F3EAC-E0CD-4C1B-823A-964E243C8E38}.png)
now we can read the file and find the main
i rename the variable so that we see more clearly what it does
![Pastedimage]({9A0BA661-C7F4-49FC-98C3-B0FBDD55F53A}.png)
and with the same function we can see the password and the flag
# c)

![Pastedimage]({E0BA60E9-3898-491C-AA1F-DA3CCFDA14C2}.png)

the comparison is here
![Pastedimage](Pastedimage20260208205523.png)

we need to modified the JNZ (jump if no zero) into a JZ (jump if zero) so that instead of if the comparison is true it goes right when the comparison is wrong
now we export the file and test it


![Pastedimage]({004638A6-C873-48D8-9DD5-391809DF1D1B}.png)

and it work

# d)

```
git clone https://github.com/NoraCodes/crackmes.git
cd crackmes
make
```
# e)

we found the main
![Pastedimage](Pastedimage20260208211118.png)
we can see the password in the comparison 
![Pastedimage]({BFDE4EF7-49DF-4B51-96FE-8F61B3DDBFC4} 1.png)

# e)

it seems to be approximately the same here 
![Pastedimage](Pastedimage20260208212004.png)
just the password is different that the only difference and the password is annoying because there is a '!' and in Linux it does something so we need to evade it with a '\\'
![Pastedimage]({3534A535-2D66-45DD-82CF-A2E2DB8CE5F1}.png)
# f)

it's the same but with just  a modification of the password, it was modified by add number in the ascii table


![Pastedimage](Pastedimage20260208213308.png)