---------------------------------------------
Biblioteca de integração PagSeguro em PHP
v.2.1.4
---------------------------------------------


= Descrição =

A biblioteca PagSeguro em PHP é um conjunto de classes de domínio que facilitam, para o desenvolvedor PHP, a utilização das funcionalidades que o PagSeguro oferece na forma de APIs. Com a biblioteca instalada e configurada, você pode facilmente integrar funcionalidades como:

	- Criar requisição de pagamento;
	- Consultar transações por código;
	- Consultar transações por intervalo de datas;
	- Receber notificações;


= Requisitos =

A biblioteca PagSeguro em PHP é compatível com a versão 5.1.6 (ou superior) do PHP.


= Instalação =


1. Faça o download da Biblioteca PagSeguro em PHP;
2. Descompacte os arquivos em seu computador;
3. Dentro do diretório 'source' existem dois diretórios, o 'examples' e o 'PagSeguroLibrary'. O diretório 'examples' contém exemplos de chamadas utilizando a API para que você possa se basear e o diretório 'PagSeguroLibrary' contém a biblioteca propriamente dita. Caso queira importar somente a biblioteca ao seu sistema, faça upload do diretório 'PagSeguroLibrary' e inclua a classe 'PagSeguroLibrary.php'. Essa classe se encarregará de importar todas as funcionalidades da biblioteca no seu sistema. Caso queira importar a biblioteca juntamente com os exemplos, faça o upload de todos os arquivos descompactados. Não se esqueça de incluir a classe 'PagSeguroLibrary.php' encontrada no diretório 'PagSeguroLibrary' ao seu projeto para que você possa fazer uso da API em seu sistema;
4. Faça o upload dos arquivos descompactados para o diretório público do seu servidor. Os nomes mais comuns para este diretório são: htdocs, www ou o mesmo nome do domínio de seu website.


= Configuração =

	- A biblioteca possui um arquivo de configurações que deve ser configurado para que se possa fazer real uso da mesma. Esse arquivo chama-se 'PagSeguroConfig.php' e encontra-se em no diretório config da biblioteca;
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

Informações adicionais podem ser obtidas em: https://pagseguro.uol.com.br/v2/guia-de-integracao/tutorial-da-biblioteca-pagseguro-em-php.html


= Changelog =

v2.1.4
Adicionado : Classe para manipulação de moedas permitidas nas transações com o PagSeguro.

v2.1.3
Correção: A requisição era abortada se a geração de log estivesse ativa e o usuário não possuisse arquivo para geração de log nem permissão de escrita e leitura para o arquivo;

v2.0.0 - v2.1.2
Classes de domínios que representam pagamentos, notificações e transações;
Criação de checkouts via API;
Controller para processar notificações de pagamento enviadas pelo PagSeguro;
Módulo de consulta de transações.


= NOTAS =

	- Certifique-se que o email e o token informados estejam relacionados a uma conta que possua o perfil de vendedor ou empresarial.
	- Certifique-se que tenha definido corretamente o charset de acordo com a codificação (ISO-8859-1 ou UTF-8) do seu sistema. Isso irá prevenir que as transações gerem possíveis erros ou quebras ou ainda que caracteres especiais possam ser apresentados de maneira diferente do habitual.
	- Para que ocorra normalmente a geração de logs, certifique-se que o diretório e o arquivo de log tenham permissões de leitura e escrita.