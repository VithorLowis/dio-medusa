# Etapa 03 — Análise de Autenticação DVWA

## Ambiente
- Kali Linux
- Metasploitable 2
- IP: 192.168.56.102
- Aplicação: DVWA
- Protocolo: HTTP

## Verificação inicial

URL:
http://192.168.56.102/dvwa/login.php

Resultado:
HTTP 200

## Interpretação

O servidor respondeu à requisição HTTP
para a página de autenticação.

Esse resultado não comprova que a
autenticação funciona nem que existe
uma vulnerabilidade explorável.

## Próximas verificações

- Identificar o formulário.
- Analisar os parâmetros HTTP.
- Verificar cookies e tokens.
- Realizar testes controlados.
- Documentar as medidas de mitigação.

## Análise do formulário

O formulário utiliza o método POST.

Endpoint:
`/dvwa/login.php`

Parâmetros identificados:
- username
- password
- Login

## Teste de autenticação inválida

Foi realizada uma requisição POST
utilizando credenciais fictícias.

### Resposta inicial

HTTP/1.1 302 Found

Location: login.php

Cookies observados:
- PHPSESSID
- security=high

### Resposta após redirecionamento

Mensagem identificada:

Login failed

## Interpretação

O servidor processou a tentativa de login
e redirecionou o cliente para login.php.

A página apresentou a mensagem
"Login failed", confirmando que a
autenticação foi recusada.

A resposta HTTP 302, isoladamente,
não comprova sucesso ou falha.

## Considerações de segurança

A mensagem de erro permite identificar
tentativas inválidas.

Entretanto, isso não comprova que
a aplicação esteja vulnerável a
ataques automatizados de força bruta.

## Recomendações

- Limitar tentativas de autenticação.
- Implementar MFA quando possível.
- Monitorar tentativas malsucedidas.
- Aplicar mecanismos de bloqueio progressivo.
- Utilizar HTTPS.
- Proteger cookies de sessão.
