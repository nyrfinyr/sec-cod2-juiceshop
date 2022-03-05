### Description
### Proof of Concept 
### Risk assessment
### Mitigation

# Vulnerabilità
* ## XSS: *iframe*
    ### Description
    La barra di ricerca nella pagina principale è vulnerabile agli xss usando gli iframe
    ### Proof of Concept 
    Scrivere il seguente payload nella barra di ricerca
    ```javascript
    <iframe src="javascript:alert(`xss`)">
    ```
    ### Risk assessment
    ...
    ### Mitigation
    ...
* ## Server misconfiguration: *robots.txt*
    ### Description
    E' possibile accedere al file robots.txt, il quale restituisce il seguente output:
    ```
    User-agent: *
    Disallow: /ftp
    ```
    Andando nella cartella /ftp è possibile accedere a diversi file
    ![](images/robots.png)
    ### Proof of Concept
    Andare all'url /robots.txt
    Andare all'url /ftp
    ### Risk assessment
    ### Mitigation


