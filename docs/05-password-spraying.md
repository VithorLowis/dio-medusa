
## Execução real — Medusa SMB

Data: 13/11/2026
Alvo: 192.168.56.102
Ambiente: Metasploitable 2 / VirtualBox Host-Only

### Metodologia

Foram utilizados os 35 usuários identificados
pelo enum4linux e uma lista de 8 senhas comuns.

Ferramenta: Medusa 2.3
Módulo: smbnt.mod 3.0
Grupo: LOCAL
Modo: AUTO
Concorrência: 1

### Resultados

O Medusa identificou duas contas com
credenciais válidas:

- msfadmin
- user

Ambas retornaram:

SUCCESS (ADMIN$ - Access Allowed)

As senhas foram omitidas da documentação pública.

### Interpretação

O laboratório apresenta credenciais padrão
que podem ser identificadas por tentativas
automatizadas de autenticação SMB.

O resultado demonstra o risco de manter
senhas previsíveis e permitir tentativas
sucessivas sem controles suficientes.

### Limitações

O Metasploitable 2 é um ambiente
intencionalmente vulnerável.

Não foram realizados testes de persistência,
movimentação lateral ou alteração de arquivos.

### Recomendações

- Substituir credenciais padrão.
- Aplicar senhas fortes e exclusivas.
- Restringir o acesso ao serviço SMB.
- Monitorar tentativas de autenticação.
- Aplicar controles de limitação de tentativas.
- Desabilitar versões obsoletas de SMB.
