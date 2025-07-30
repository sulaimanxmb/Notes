
windows commands after reverse connection:
```bash
Start-Process "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
Add-Type -AssemblyName PresentationFramework
[System.Windows.MessageBox]::Show("Get better 😈", "LOL")
```

also be familiar with `Fabric and boto3` libraries of python

Some practice script see :
```python
#!/Users/sulaimaneksambi/Desktop/Python/.venv/bin/python

import random
import os

Dict = {"Job": "Software Engineer", "Company": "TechCorp", "Location": "New York"}
print(Dict.keys())
print(Dict.values())
print(Dict.items())
Dict['Job'] = 'Plumber'   # changes the value from saftware engneer 
Dict['J-word'] = Dict.pop('Job')   # chages the key




IP = ["192", "168", "29", "1"]
print(".".join(IP))


#Loops :

List = "Devops"
for i in List:

	print(i)
	#1 2 3 4 5

  

def Arguments(*args, **kwargs): #*ardgs use for any number of numeric and **kwargs for any numebers of string arguments
	print(args) #args is a tuple
	print(kwargs) #kwargs is a dictionary
	
	choice = random.choice(list(kwargs.keys()))
	print(choice)

Arguments(1, 2, 3, 4, 5, a1="D1", a2="D2", a3="D3", a4="D4", a5="D5",)
# If u dont know how many arguments you will pass, use *args and **kwargs

  
  
os.system("ls") # Direct system command and the output is displayed as exit codes
os.path.isdir("/etc/passwd/uk/ik") # Check if the path is a directory
os.path.isfile("/etc/passwd/uk/ik/path.txt") # Check if the path is
```
