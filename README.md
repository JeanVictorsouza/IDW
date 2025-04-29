# IDW

Abrir o DOCKER DESKTOP

--Criar pasta no diretorio raiz C: "C:\SI\3 ANO\IDW\DATA"

C:\SI\3 ANO\IDW\DATA
		  \__ Mapeamento dos dados.
				   
Salvar arquivo: vertica-jdbc-7.1.1-0.jar dentro da pasta IDW
	 C:\SI\3 ANO\IDW
		        \__vertica-jdbc-7.1.1-0.jar
					
					
			          __ Run: Apenas executa a instancia já instalada da Imagem.
Serach				 /
    \__ vertica/vertica-ce => Pull; Aguardar o processo de Download/Carregamento da Imagem.
				\__ Imagem official do VERTICA
	
Menu Images Fica as instancias já baixadas, prontas para execução.

Apos instalada:
	
	Inicializar o container
	
	Optional Setings
	
	Container Name  \\Codigo e nome pode ser usado para identificação do banco em projetos.
	--vertica_ce         \__ Codigo é visualizado abaixo do nome do Container.
	
	Ports:
	--15433 :5433/tcp
	--15444 :5444/tcp
	
	Volumes:
	--Caminho da pasta em Host path => em Container Path /data
	
	Apos preenchimento clicar em Run.
	
	Ira crair todo o banco e integrações. ("Processo pode ser um pouco demorado")
	

Abrir aba EXEC=> terminal linux
\\# apemas root pode executar o comando
\\$ pode ser executado por qualquer usuario

sudo sudo \\User Root

su dbadmin \\ User master

/opt/vertica/bin/admintools \\Acessando o Menu do Vertica

\\ Usar teclas para locomoção

\\ Para criar nova tabela.

Menu configuration

Stop data base

create database

\\ Inserir dados para criação da tabela



Conect database

-- create schema udw; \\ criar schema novo 

-- \dn \\mostra todos os schemas criados

create user udw identified by '1234'; \\ criando o usario 

grant all on database dw to udw; \\ Dando permissão de acesso da tabela ao usuario

\\ Apos esse processo.


abrir o dbeaver e conectar o banco.

Nova conexão
-- vertica
   -- mudar porta: 15433
   -- schema: dw
   -- usuario: udw
   -- Senha: 1234
   
-- Configuração de driver
	\__ Libraries
	       \__ Colocar arquivo => vertica-jdbc-7.1.1-0.jar
