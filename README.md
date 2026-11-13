# Simulando Ataques de Força Bruta com Medusa e Kali Linux

Projeto desenvolvido para o desafio prático da DIO.

## Objetivo

Demonstrar técnicas de auditoria de autenticação
utilizando Kali Linux, Medusa, Metasploitable 2 e DVWA
em ambiente virtual isolado.

## Ambiente

- Kali Linux: máquina atacante
- Metasploitable 2: máquina vulnerável
- Virtualização: Oracle VirtualBox
- Rede: Host-Only
- IP do alvo: 192.168.56.102

## Ferramentas utilizadas

- Nmap
- Medusa 2.3
- enum4linux
- curl
- DVWA

## Etapas do projeto

### 1. Reconhecimento

Identificação dos serviços FTP, HTTP e SMB.

[Documentação](docs/01-reconhecimento.md)

### 2. Força bruta FTP

Teste de autenticação com Medusa e wordlists
simples em ambiente controlado.

[Documentação](docs/02-ftp.md)

### 3. Autenticação Web — DVWA

Análise do formulário de login, parâmetros POST,
cookies de sessão e mensagens de falha.

[Documentação](docs/03-dvwa.md)

### 4. Enumeração SMB

Enumeração de 35 usuários com enum4linux.

[Documentação](docs/04-smb.md)

### 5. Teste de senhas SMB

Utilização do Medusa com usuários enumerados
e senhas comuns.

Resultados:
- 35 usuários identificados
- 8 senhas utilizadas
- 2 contas autenticadas com sucesso

Contas identificadas:
- msfadmin
- user

Resultado do Medusa:
SUCCESS (ADMIN$ - Access Allowed)

O teste utilizou múltiplas senhas por usuário,
caracterizando força bruta baseada em dicionário.

[Documentação](docs/05-password-spraying.md)

## Evidências

- evidencias/reconhecimento/
- evidencias/ftp/
- evidencias/smb/

As senhas válidas foram ocultadas na versão
pública das evidências SMB.

## Recomendações de segurança

- Eliminar senhas padrão.
- Utilizar senhas fortes e exclusivas.
- Restringir acesso a serviços administrativos.
- Monitorar tentativas de autenticação.
- Implementar controles contra tentativas repetidas.
- Atualizar serviços e protocolos obsoletos.

## Conclusão

O laboratório demonstrou como a enumeração
de usuários e o uso de credenciais previsíveis
podem comprometer serviços de autenticação.

Os testes foram realizados exclusivamente
em máquinas virtuais de laboratório.

## Aviso

Projeto educacional. Não realizar testes
em sistemas sem autorização.
