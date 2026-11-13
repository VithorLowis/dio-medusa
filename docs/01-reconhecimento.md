# 01 — Reconhecimento do Ambiente

## Objetivo
Identificar os serviços disponíveis no Metasploitable 2.

## Ambiente
- Atacante: Kali Linux
- Alvo: Metasploitable 2
- IP: 192.168.56.102
- Virtualização: VirtualBox
- Rede: Host-Only

## Comando utilizado
nmap -sV -p 21,80,139,445 192.168.56.102

## Serviços identificados
- 21/tcp — FTP — vsftpd 2.3.4
- 80/tcp — HTTP — Apache 2.2.8
- 139/tcp — NetBIOS/SMB — Samba
- 445/tcp — SMB — Samba

## Evidências
- evidencias/reconhecimento/nmap.txt
- evidencias/reconhecimento/ping.txt

## Recomendações
- Atualizar serviços.
- Restringir portas desnecessárias.
- Monitorar acessos.
- Desabilitar serviços não utilizados.
