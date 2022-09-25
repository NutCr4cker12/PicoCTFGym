# Python Wrangling
## Description
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](./ende.py) using [this password](./pw.txt) to get [the flag](./flag.txt.en)?
### hints
1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: $ wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py
2. ```$ man python```
# Solution  
Downloading the provided files and seeking for usage help for the [python script](./ende.py) via -h command  
```
$ python ende.py -h  
Examples:
  To decrypt a file named 'pole.txt', do: '$ python ende.py -d pole.txt'
```
So running ```$ python ende.py -h flag.txt.en``` and entering the password from [pw.txt](./pw.txt) file when prompted resulted into the flag.

