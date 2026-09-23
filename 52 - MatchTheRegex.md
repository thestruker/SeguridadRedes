How about trying to match a regular expression.
Access the webpage and try to match the regular expression associated with the text field
## Solución
```
|   |
|---|
|function send_request() {|
|let val = document.getElementById("name").value;|
|// ^p.....F!?|
|fetch(`/flag?input=${val}`)|
|.then(res => res.text())|
|.then(res => {|
|const res_json = JSON.parse(res);|
|alert(res_json.flag)|
|return false;|
|})|
|return false;|
|}|

picoCTF{succ3ssfully_matchtheregex_9080e406}
```

## Notas Adicionales
Evaluar expresion regular

## Referencias
https://regexr.com/