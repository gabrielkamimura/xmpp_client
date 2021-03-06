xmpp_client
===========

Cliente XMPP básico em Javascript

### [Visite nossa Wiki](https://github.com/nawarian/xmpp_client/wiki)

# Servidor XMPP
Este projeto é acompanhado de um Vagrantfile que provisiona
um servidor OpenFire XMPP (3.9.3).

Digite `vagrant up` na raiz deste projeto para iniciar o provisionamento.

Atualmente o script só foi testado utilizando o OpenFire, outros
servidores serão testados posteriormente.

* Importante
Para que o servidor inicie com sucesso, certifique-se de que seu computador
não esteja utilizando as portas: `7070`, `5222` e `9090`.

* Importante (2)
O servidor OpenFire deve ser configurado pela primeira execução, faça-o através
do endereço: `http://localhost:9090`.
Os itens das dicas abaixo já estão implementados de acordo com o provisionamento.

* Dica
Em alguns casos será necessário criar a propriedade de sistema seguinte:
`xmpp.httpbind.scriptSyntax.enabled` com o valor `true` e não encriptada.

* Dica (2)
É recorrente, também, presenciar algumas exceções do lado servidor por conta de
configuração:
- xmpp.httpbind.scriptSyntax.enabled ==> true
- xmpp.client.processing.threads ==> 16
- xmpp.httpbind.worker.threads ==> 16

# Cliente XMPP
Certifique-se de que instalou as dependências através do comando: `bower install`

Após isto, basta utilizar o objeto XMPPClient em sua página.
Inclua, antes de `XMPPClient.js`, os arquivos: `strophe.js` e `rsvp.js`. Ambos
disponíveis na pasta `bower_components` (após o `bower install`)
