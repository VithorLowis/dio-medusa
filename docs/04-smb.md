# Etapa 04 — Enumeração SMB

## Objetivo

Investigar a exposição de informações
de usuários por meio do protocolo SMB.

## Ambiente

- Kali Linux
- Metasploitable 2
- IP: 192.168.56.102
- Portas: 139 e 445
- Ferramenta: enum4linux 0.9.1
- Data: 13/11/2026

## Comando utilizado

enum4linux -U 192.168.56.102

## Resultados

Workgroup identificado: WORKGROUP

Total de contas enumeradas: 35

O servidor permitiu estabelecer
uma sessão SMB sem usuário e senha.

Foi possível enumerar nomes de contas
e seus respectivos RIDs.

## Contas de interesse

- msfadmin
- user
- root
- postgres
- mysql
- www-data
- ftp
- backup

## Análise de segurança

A enumeração de contas pode fornecer
informações úteis para ataques contra
mecanismos de autenticação.

A aceitação de sessões anônimas e a
divulgação de usuários demonstram
exposição de informações no laboratório.

Não foi demonstrado acesso não autorizado
a arquivos ou autenticação privilegiada.

## Recomendações

1. Restringir enumeração anônima.
2. Revisar permissões de compartilhamento.
3. Restringir acesso às portas SMB.
4. Monitorar tentativas de autenticação.
5. Aplicar políticas de senhas fortes.
6. Implementar controles contra
   tentativas automatizadas.

## Evidência

evidencias/smb/usuarios.txt
