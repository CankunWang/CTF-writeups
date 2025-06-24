#Disko-1
**Category**: Forensics  
**Difficulty**: Easy  
**Platform**: picoCTF  
**Points**: 100

#Analyzing

Directly search the .dd file to find the flag

#Using Strings and grep

strings -a disko-1.dd \ | grep -Eo 'picoCTF\{[^}]+\}'
