# Projeto Medusa - Laboratório de Segurança

Este projeto foi desenvolvido para estudar ferramentas de segurança da informação e entender como funcionam alguns testes de autenticação em serviços de rede.

**Ambiente utilizado**
- Kali Linux: 192.168.56.102
- Metasploitable 2: 192.168.56.101
- VirtualBox
- Rede Host-only

**Ferramentas**
- Medusa 2.3
- Nmap
- Netcat
- SMBClient
- FTP (ProFTPD)
- DVWA
- Samba

**Testes realizados**

**FTP com Medusa**

Foi identificado o serviço ProFTPD na porta 2121. Em seguida, foi utilizado o Medusa para realizar um teste de autenticação com uma conta criada para o laboratório.

Resultado: ACCOUNT FOUND.

**DVWA**

Foi acessado o módulo Brute Force do DVWA, configurado no nível Low.

Durante a análise, foi identificado que o formulário utiliza o método HTTP GET e possui os campos username e password. Também foi realizada uma tentativa manual de autenticação, que retornou sucesso.

**SMB/Samba**

Foram identificadas as portas 139 e 445 abertas no Metasploitable 2.

Com o SMBClient, foi possível listar os compartilhamentos disponíveis sem autenticação. Também foi identificado que o compartilhamento tmp permite visualizar arquivos anonimamente.

**Medidas de segurança**

- Utilizar senhas fortes.
- Limitar tentativas de login.
- Monitorar registros de autenticação.
- Restringir acessos por firewall.
- Desabilitar acesso anônimo quando não necessário.
- Configurar corretamente as permissões dos compartilhamentos.
- Manter os serviços atualizados.

**Estrutura do projeto**

- README.md: documentação do projeto.
- wordlists/: listas de teste utilizadas.
- imagens/: capturas de tela das atividades.

**Conclusão**

Com este laboratório, consegui praticar o uso do Medusa, conhecer melhor os serviços FTP e SMB e entender como funciona a análise de formulários de autenticação no DVWA.

A atividade também ajudou a compreender alguns riscos relacionados a senhas fracas, acessos anônimos e configurações inadequadas de serviços de rede.

Todos os testes foram realizados em ambiente virtualizado e autorizado.
