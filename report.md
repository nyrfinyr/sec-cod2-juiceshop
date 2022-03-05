# Summary
* [XSS: iframe](#xss_iframe)
* [Sensitive Data Exposure: robots.txt](#robots_txt)
* [SQL Injection: 'OR true--](#sql_injection_1)

# Vulnerabilities

## XSS: *iframe* <a name="xss_iframe"></a>
### Description
La barra di ricerca nella pagina principale è vulnerabile agli xss usando gli iframe
### Proof of Concept 
Scrivere il seguente payload nella barra di ricerca
```javascript
<iframe src="javascript:alert(`xss`)">
```
### Risk assessment
### Mitigation

## Server misconfiguration: *robots.txt* <a name="robots_txt"></a>
### Description
E' possibile accedere al file robots.txt, il quale restituisce il seguente output:
```
User-agent: *
Disallow: /ftp
```
Andando nella cartella /ftp è possibile accedere a diversi file
![](images/robots.png)
### Proof of Concept
Andare all'url /robots.txt \
Andare all'url /ftp
### Risk assessment
### Mitigation

## Sql Injection: *'OR true--* <a name="sql_injection_1"></a>
### Description
E' possibile autenticarsi come admin sfruttando una sql injection 
nella pagina di login. 
### Proof of concept
Andare all'url /#/login
scrivere nel campo email 
```
'OR true--
```
Andando su /profile si vede che si è stati autenticati come admin,
con email admin@juice-sh.op.
![](images/sql-inj1.png)
### Risk Assessment
### Mitigation





