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

### Serviço `<n>`

* **Título do serviço**: `<título>`
* **Breve descrição**:
  > Breve descrição do serviço
* **URL completa da requisição**: `<URL>`
* **Cabeçalho HTTP da chamada**:
~~~http
<cabeçalho>
~~~
* **Cabeçalho HTTP da resposta**:
~~~http
<cabeçalho>
~~~
* **Conteúdo da resposta**:
~~~json
<conteúdo>
~~~
