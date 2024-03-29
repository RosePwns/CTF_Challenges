# NodeJS - Proto & Prototype Pollution

## Description

The source code gave away that the application may be vulnerable to prototype pollution. A quick search for a prototype pollution PoC reveals a script on hacktricks. I take and modify the script a bit to fit my needs, obtaining the flag. 

## Framework

- NodeJS


## Exploit

The script takes advantage of a prototype pollution vulnerability in a web application. It sends a POST request to the '/api/submit' endpoint, injecting a payload that pollutes the 'proto' property with a 'block' object containing a command for child process execution (id > static/images/win.txt). Subsequently, it triggers this payload with a GET request to '/static/images/win.txt', attempting to execute the command and retrieve the output, showcasing the impact of the prototype pollution vulnerability.

## More Information

[NodeJS Prototype Pollution](https://book.hacktricks.xyz/pentesting-web/deserialization/nodejs-proto-prototype-pollution)

