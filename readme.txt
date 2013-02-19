Esta é uma biblioteca de integração do seu sistema de vendas com o PagSeguro escrita em PHP, ela contém:

- Versão : 2.1.3
- Classes de domínios que representam pagamentos, notificações e transações;
- Criação de checkouts via API;
- Controller para processar notificações de pagamento enviadas pelo PagSeguro;
- Módulo de consulta de transações.


- Instalação
	Para instalar a biblioteca siga as instruções abaixo:
	- Descompacte os arquivos em seu computador;
	- Faça o upload dos arquivos descompactados para o diretório público do seu servidor. Os nomes mais comuns para este diretório são: htdocs, www ou o mesmo nome do domínio de seu website;
	- Importe a biblioteca para o seu sistema fazendo a inclusão do arquivo PagSeguroLibrary.php encontrado no diretório raiz da biblioteca.

	Pronto! A biblioteca PagSeguro em PHP está instalada.


- Configurações
	- A biblioteca possui um arquivo de configurações que deve ser configurado para que se possa fazer real uso da mesma. Esse arquivo chama-se PagSeguroConfig.php e encontra-se em no diretório config da biblioteca;
	- Nele são configurados:
		- ambiente;
		- credenciais de acesso composta por email e token;
		- Caso ainda não possua token, ele pode ser gerado na seguinte url: https://pagseguro.uol.com.br/integracao/token-de-seguranca.jhtml;
		- codificação:
			- ISO-8859-1 ou
			- UTF-8.
		- log:
			- ativo ou não;
			- diretório de geração do log das transações do sistema com o PagSeguro.

			
* NOTAS
	- As credenciais de acesso devem pertencer a uma conta no PagSeguro que tenha perfil de vendedor ou empresarial;
	- Para que não haja problemas com a transação de informações com o PagSeguro, certifique-se que informou a codificação (ISO-8859-1 ou UTF-8) correta do seu sistema ao arquivo de configurações.
	- Certifique-se que o arquivo que for definir para geração de log possua permissões de leitura e escrita para que seja possível cria-lo e/ou inserir registros de log.

	
Para maiores informações, acesse https://pagseguro.uol.com.br/v2/guia-de-integracao/tutorial-da-biblioteca-pagseguro-em-php.html