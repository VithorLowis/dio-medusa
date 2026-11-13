# Etapa 02 — Teste de Autenticação FTP

## Objetivo

Avaliar o comportamento da autenticação FTP
utilizando o Medusa em ambiente controlado.

## Ambiente

- Kali Linux
- Metasploitable 2
- IP: 192.168.56.102
- Serviço: FTP
- Software identificado: vsftpd 2.3.4
- Ferramenta: Medusa 2.3
- Data: 13/11/2026

## Metodologia

Foram utilizadas duas contas fictícias
e duas senhas de laboratório.

Total de combinações: 4.

## Comando

medusa -h 192.168.56.102 \
-U wordlists/usuarios.txt \
-P wordlists/senhas.txt \
-M ftp \
-t 1 \
-O evidencias/ftp/medusa.txt

## Resultados

O Medusa apresentou quatro verificações
de autenticação.

Nenhuma credencial válida foi registrada.

O teste foi encerrado normalmente.

## Análise

O resultado não demonstra comprometimento
do serviço FTP.

A ausência de credenciais válidas pode
estar relacionada à inexistência das
contas fictícias no servidor.

## Mitigações

- Utilizar senhas fortes e únicas.
- Restringir acesso ao serviço FTP.
- Monitorar falhas de autenticação.
- Aplicar limitação de tentativas.
- Preferir SFTP ou FTPS ao FTP tradicional.

## Evidência

evidencias/ftp/medusa.txt
