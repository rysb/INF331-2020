# Lab04 - Serviços

Estrutura de pastas:

~~~
├── README.md  <- arquivo apresentando a tarefa
│
└── images     <- arquivos de imagens usadas no documento
~~~

## Tarefa 1

> ![tarefa1](images/tarefa1.png)

## Tarefa 2

> ![tarefa2](images/tarefa2.png)

## Tarefa 3

> ![tarefa3](images/tarefa3.png)

## Tarefa 4

### Serviço Consulta de CEP

* **Título do serviço**: `ViaCEP`
* **Breve descrição**:
   Serviço para consulta e validação de CEP para todo o Brasil.
* **URL completa da requisição**: `https://viacep.com.br/ws/02011100/json/`
* **Cabeçalho HTTP da chamada**:
~~~http
GET /ws/02011100/json/ HTTP/1.1
Host: viacep.com.br
Connection: keep-alive
Pragma: no-cache
Cache-Control: no-cache
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate, br
Accept-Language: pt-BR,pt;q=0.9,en-US;q=0.8,en;q=0.7,es;q=0.6
Cookie: _ga=GA1.3.249156166.1598577127; _gid=GA1.3.1754035581.1598577127
~~~
* **Cabeçalho HTTP da resposta**:
~~~http
HTTP/1.1 200 OK
Server: nginx/1.18.0
Date: Fri, 28 Aug 2020 01:15:00 GMT
Content-Type: application/json; charset=utf-8
Transfer-Encoding: chunked
Connection: keep-alive
Access-Control-Allow-Origin: *
Access-Control-Allow-Methods: GET, OPTIONS
Access-Control-Allow-Headers: Content-Type, X-Request-With, X-Requested-By
Access-Control-Allow-Credentials: true
Access-Control-Max-Age: 86400
Expires: Fri, 28 Aug 2020 02:15:00 GMT
Cache-Control: max-age=3600
Pragma: public
Cache-Control: public
~~~
* **Conteúdo da resposta**:
~~~json
{
  "cep": "02011-100",
  "logradouro": "Rua Voluntários da Pátria",
  "complemento": "de 893 a 1411 - lado ímpar",
  "bairro": "Santana",
  "localidade": "São Paulo",
  "uf": "SP",
  "ibge": "3550308",
  "gia": "1004",
  "ddd": "11"
}
~~~

### Serviço Consulta de Músicas

* **Título do serviço**: `Vagalume API`
* **Breve descrição**:
  Serviço para pequisa de letras de músicas e traduções, cifras, biografias, discografias, etc.
* **URL completa da requisição**: `http://api.vagalume.com.br/search.artmus?apikey=660a4395f992ff67786584e238f501aa&q=Skank%20Vamos%20Fugir&limit=5`
* **Cabeçalho HTTP da chamada**:
~~~http
GET /search.artmus?apikey=660a4395f992ff67786584e238f501aa&q=Skank%20Vamos%20Fugir&limit=5 HTTP/1.1
Host: api.vagalume.com.br
Connection: keep-alive
Pragma: no-cache
Cache-Control: no-cache
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Referer: http://api.vagalume.com.br/docs/search/
Accept-Encoding: gzip, deflate
Accept-Language: pt-BR,pt;q=0.9,en-US;q=0.8,en;q=0.7,es;q=0.6
~~~
* **Cabeçalho HTTP da resposta**:
~~~http
HTTP/1.1 200 OK
Date: Fri, 28 Aug 2020 01:29:28 GMT
Content-Type: text/plain;charset=utf-8
Content-Length: 758
Connection: keep-alive
Content-Security-Policy: default-src 'none'; base-uri 'none'; connect-src 'self'; form-action 'self'; font-src 'self'; frame-ancestors 'none'; img-src 'self'; media-src 'self'; style-src 'self' 'unsafe-inline'; script-src 'self'; worker-src 'self';
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
X-XSS-Protection: 1; mode=block
Expires: Thu, 27 Aug 2020 20:54:00 GMT
Cache-Control: max-age=72000
Access-Control-Allow-Origin: *
Content-Encoding: gzip
Vary: Accept-Encoding
~~~
* **Conteúdo da resposta**:
~~~json
{
  "response":{"numFound":1711,"start":0,"numFoundExact":true,"docs":[
      {
        "id":"b3ade68b3g8e86eda3",
        "url":"/skank/",
        "band":"Skank",
        "fmRadios":["14623883771774082279|vagalume-vibe",
          "14671417541091220806|pop-rock-br",
          "1470169276225492|pop-nacional",
          "1474482422796242|ferias",
          "1476469524740247|lancamentos",
          "1487701935336993|musicas-para-relaxar",
          "1506975770142563|pop-rock",
          "1508779923321353|para-viajar",
          "1521491976152594|letras-conhecidas",
          "1522261529679510|depre",
          "1524081924608496|nostalgia-anos-2000",
          "1528233925925603|dia-dos-namorados",
          "1528745033453663|clima-de-copa",
          "1534352328636564|skank"]},
      {
        "id":"b3ade68b5g2b97eda3",
        "url":"/skankin-pickle/",
        "band":"Skankin' Pickle"},
      {
        "id":"b3ade68b7g78101ea3",
        "url":"/grupo-vamos-nessa/",
        "band":"Grupo Vamos Nessa"},
      {
        "id":"b3ade68b6gcfc7fda3",
        "url":"/mamma-mia/",
        "band":"Mamma Mia"},
      {
        "id":"l3ade68b7g3be34ea3",
        "langID":1,
        "url":"/skank/vamos-fugir.html",
        "title":"Vamos Fugir",
        "band":"Skank",
        "fmRadios":["1534352328636564|skank"]},
      {
        "id":"l3ade68b6g3e9aeda3",
        "langID":1,
        "url":"/gilberto-gil/vamos-fugir.html",
        "title":"Vamos Fugir",
        "band":"Gilberto Gil",
        "fmRadios":["151742478997108|flashback-brasil"]},
      {
        "id":"l3ade68b8gb0bac0b3",
        "langID":1,
        "url":"/mc-cabelinho/vamos-fugir.html",
        "title":"Vamos Fugir",
        "band":"MC Cabelinho"},
      {
        "id":"l3ade68b7gcafa8ea3",
        "langID":1,
        "url":"/badalada/vamos-fugir.html",
        "title":"Vamos Fugir",
        "band":"Badalada"},
      {
        "id":"l3ade68b8gd9c820b3",
        "langID":1,
        "url":"/seu-jorge/vamos-fugir.html",
        "title":"Vamos Fugir",
        "band":"Seu Jorge"}]
  },
  "highlighting":{
    "b3ade68b3g8e86eda3":{},
    "b3ade68b5g2b97eda3":{},
    "b3ade68b7g78101ea3":{},
    "b3ade68b6gcfc7fda3":{},
    "l3ade68b7g3be34ea3":{},
    "l3ade68b6g3e9aeda3":{},
    "l3ade68b8gb0bac0b3":{},
    "l3ade68b7gcafa8ea3":{},
    "l3ade68b8gd9c820b3":{}}
}
~~~
