# Wave a flag
## Description
Can you invoke help flags for a tool or binary? [This program](./warm) has extraordinarily helpful information...
### hints
1. This program will only work in the webshell or another Linux computer.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
3. Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm
4. -h and --help are the most common arguments to give to programs to get more information from them!
5. Not every program implements help features like -h and --help.
# Solution  
Started by running file on the excetubale to find out what are we dealing with:  
```
$ file warm  
warm: ELF 64-bit LSB pie executable, ...  
```  
But running ```$ ls -la``` show's that it doesn't have the executable bit, so adding it with ```$ chmod +x warm```.  

Running the program with -h flag resulted into pico CTF flag.