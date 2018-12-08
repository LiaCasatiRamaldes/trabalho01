# TRABALHO 01:  Sensor de Violência Doméstica
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Gabriela Neves: gabrielasantosneves11@gmail.com <br>
Lia Casati Ramaldes:liac.ramaldes@gmail.com <br>
Thamiris Moreira:thamirismais@gmail.com <br>
...

### 2.INTRODUÇÃO E MOTIVAÇAO<br>
Este documento contém a especificação do projeto do banco de dados, Sensor de Violência Doméstica, <br>
e motivação da escolha realizada. <br>

> A empresa LiaThamirisLTDA visa colaborar com desenvolvimento de projetos para reduzir a violência doméstica. Sabendo dos desafios enfrentados por mulheres que residem junto de seus parceiros e que estão em um relacionamento abusivo. Ficamos motivados com o desenvolvimento deste sistema. O Sistema HomeViolence tem como objetivo captar sons que possam ser associados a violência como, tapas, socos, gritos, bater de portas, coisas quebrando e caso sejam analisados em conjuntos ou repetidamente, o sistema acionará o departamento policial mais próximo.


### 3.MINI-MUNDO Novo<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas) <br>
Entrevista com o usuário e identificação dos requisitos.<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O sistema proposto conterá as informacões aqui detalhadas. Serão armazenados dados pessoais do usário, dados do parceiro do usário, dados de endereço do usuário, dados do adiministrador, sons, dados das delegcias e sensores. Dos dados do usuário armazenaremos: codigo do sensor instalado em sua casa, nome, cpf, rg e celular(não obrigatório), sexo e tipo sanguíneo. Dos dados do parceiro do usário serão armazenados:Nome, cpf(não obrigatório), rg(não obrigatório) e celular(não obrigatório), sexo. Dos dados de endereço do usário serão armazenados: Estado, cidade, bairro, rua, complemento e número. Dos dados do adiministrador serão armazenados: Nome, delegacia, email, usuário(nickname), senha e uma foto do adiministrador. Dos dados sonoros serão armazenado: 100 tipos de gritos de medo femininos, 100 tipos de gritos de medo masculinos, 100 xingamentos em vozes masculinas, 100 xingamentos em vozes femininas, 100 sons de quebra de objetos, 100 sons de portas batendo de formas diferentes, 100 sons de tapas e 100 sons de socos. Dos dados do sensor serão armazenados: o tipo do sensor e o código do sensor. O sensor funciona 24 horas por dia captando e comparando os sons captados om os armazenados, quando encontra sons referentes aos que estão armazenados porém distintos entre si em um periodo de no máximo uma hora aciona a policia e envia as informações do cadastro. Somente os adiministradores podem adicionar ou alterar as informações dos usuários ou suas próprias, lembrando que os adiministradores devem ser policiais.

### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser desenvolvidas. O princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas e/ou descartadas <br>


![Arquivo PDF do Protótipo]
(https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/arquivos/Sensor%20de%20Viol%C3%AAncia%20Dom%C3%A9stica.pdf?raw=true "Sensor De Violencia Domestica")



#### 4.1 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    e deve ser criada antes do modelo conceitual
    c) Após criada esta tabela não deve ser modificada, pois será comparada com os resultados finais na conclusão do trabalho
![Exemplo de Tabela de dados do Sensor de Violência Doméstica](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/arquivos/Tabela%20MOD%20(1).xlsx?raw=true "Tabela - Sensor de Violência Doméstica") 
    
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!<br>
    
    1- Relatório com os sons mais captados.<br>
    2- Relatório com as idades das vitimas que mais registraram no sistema.<br>
    3- Relatório do adiministrador que mais registrou casos de violencia domestica.<br>
    4- Relatório com as cidades/bairros/estados onde mais ocorrem violências domésticas.<br>
    5- Relatório com as delegacias que mais registraram boletins de ocorrência.<br> 
    
>## Marco de Entrega 01 em: (24/03/2018)<br>

### 5.MODELO CONCEITUAL<br>
    A) NOTACAO ENTIDADE RELACIONAMENTO 
        * Para nosso prótótipo limitaremos o modelo conceitual nas 5 principais entidades do escopo
        * O protótipo deve possui no mínimo duas relações N para N
        * o mínimo de entidades do modelo conceitual será igual a 5
        
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/Modelo_conceitual_VD.PNG)
    
    B) NOTACAO UML (Caso esteja fazendo a disciplina de analise)
    C) QUALIDADE 
        Garantir que a semântica dos atributos seja clara no esquema
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]
## Marco de Entrega 01 em: (20/04/2018)<br>
#### 5.2 DECISÕES DE PROJETO
   	Endereço: Em nosso projeto optamos por uma tabela endereço, para evitar que precisasse fazer os mesmos campos em tabelas diferentes.
   	<br>
  	 Pessoa: Em nosso projeto optamos por uma tabela pessoa, para armazenar as informaçôes referentes aos usuários cadastrados, para futuras consultas.
   	<br>
	Usuário: Em nosso projeto optamos por uma tabela usuário, para armazenar as outras informaçôes referentes aos usuários cadastrados, para futuras consultas. 
   	<br>
   	Delegacia: Em nosso projeto optamos por uma tabela delegacia, para armazenar informaçôes referentes as delegacias que auxiliam os usuários cadastrados em situação de de perigo(no caso, violência doméstica). 
   	<br>
   	Policial: Em nosso projeto optamos por uma tabela policial, para armazenar as informaçôes referentes aos policiais cadastrados, para futuras consultas.
   	<br>
   	Sensor: Em nosso projeto optamos por uma tabela sensor, para armazenar as informaçôes referentes aos sensores cadastrados, para futuras consultas.
   	<br>
   	Captura: Em nosso projeto optamos por uma tabela captura, para armazenar as informaçôes referentes aos audios capturados, para futuras consultas.
   
    
#### 5.3 DESCRIÇÃO DOS DADOS 
   
    PESSOA: Tabela que armazena as informações relativas ao usuário<br>
    Nome: Campo que armazena o nome completo de cada usuário cadastrado no sistema.<br>
    CPF: Campo que armazena o número de Cadastro de Pessoa Física para cada usuário cadastrado no sistema.<br>
    RG: Campo que armazena o número da Carteira de Identidade/RG (Registro Geral) de cada usuário cadastrado no sistema.<br>
    Idade: Campo que armazena a idade em anos de cada usuário cadastrado no sistema.<br>
    Sexo: Campo que armazena o sexo de cada usuário cadastrado no sistema.<br>  
    Celular: Campo não obrigatório que armazena o telefone movél para contato de cada usuário cadastrado no sistema.<br> 
    
    USUÁRIO: Tabela que herda os campos de Pessoa<br>
    (Nome, CPF, RG, Idade, Sexo, Celular) já citados acima.<br>
    Celular de emergência: Campo não obrigatório que armazena o telefone movél para contato de algum parente/amigo de confiança de cada     usuário cadastrado no sistema.<br> 
    Tipo Sanguíneo: Campo que armazena o tipo sanguíneo de cada usuário.<br>
    
    ENDEREÇO: Tabela que armazena as informações relativas ao endereço da delegacia ou do usuário<br>
    Estado: Campo que armazena o estado que está localizada a residência/delegacia.<br>
    Cidade: Campo que armazena a cidade que está localizada a residência/delegacia.<br>
    Bairro: Campo que armazena o bairro que está localizada a residência/delegacia.<br>
    Rua: Campo que armazena a rua que está localizada a residência/delegacia.<br>
    Complemento: Campo não obrigatório que armazena uma informação complementar ao endereço(Nome do prédio, ...) que está localizado a       residência/delegacia.<br>
    Número: Campo que armazena o número da residência/delegacia.<br>
    Código Endereço: Campo que atribui um código para o endereço cadastrado, para que aceite um endereço repetido e não cause nenhum         erro no sistema.<br>
    
    DELEGACIA: Tabela que herda os campos de Endereço<br>
    (Estado, Cidade, Bairro, Rua, Complemento, Número, Código Endereço) já citados acima.<br>
    Telefone: Campo que armazena o telefone para contato de cada delegacia cadastrado no sistema.<br> 
    Código: Campo que atribui um código para a delegacia cadastrada.<br>
    
    CASA: Tabela que herda os campos de Endereço.<br>
    
    POLICIAL: Tabela que armazena as informações relativas ao policial<br>
    Nome: Campo que armazena o nome completo de cada policial cadastrado no sistema.<br>
    EMAIL: Campo que armazena o email de contato de cada policial cadastrado no sistema.<br>
    Delegacia: Campo que armazena a delegacia que cada policial cadastrado no sistema pertence.<br>
    Usuário: Campo que armazena um nome de usuário único, utilizado como identificador para cada policial cadastrado no sistema.<br>
    Senha: Campo que armazena uma senha para reconhecimento do usuário.<br>
    
    CAPTURA: Tabela que armazena as informações relativas ao som capturado<br>
    Código Capturado: Campo que atribui um código para o som capturado.<br>
    Arquivo de Som: Campo que armazena a gravação do audio capturado.<br>
    Data Inicial: Campo que armazena a data que começou a gravação.<br>
    Data Final: Campo que armazena a data que terminou a gravação.<br>
    Hora Inicial: Campo que armazena o hórario que começou a gravação.<br>
    Hora Final: Campo que armazena o hórario que terminou a gravação.<br>
    
    SENSOR: Tabela que armazena as informações relativas ao som<br>
    Código do sensor: Campo que atribui um código para o sensor cadastrado.<br>
    Tipo: Campo que armazena o tipo do sensor.<br>
    Nome: Campo que armazena o nome do sensor.<br>
      

>## Marco de Entrega 01 em: (12/05/2018)<br>
### 6	MODELO LÓGICO<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/Modelo_logico_VD.PNG)
        a) inclusão do modelo lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..)
        
        
/* modelo_logico_VD(novo): */

CREATE TABLE Endereco (
    numero int,
    cod_end Serial PRIMARY KEY,
    fk_complemento_cod_complemento Serial
);

CREATE TABLE Sensor (
    cod_sensor Serial PRIMARY KEY,
    tipo varChar(100),
    nome varChar(100)
);

CREATE TABLE Pessoa (
    nome varChar(100),
    cod_pessoa Serial PRIMARY KEY,
    fk_Sexo_cod_sexo Serial
);

CREATE TABLE Delegacia (
    cod_delegacia Serial PRIMARY KEY,
    fk_Endereco_cod_end Serial
);

CREATE TABLE Captura (
    cod_captura Serial PRIMARY KEY,
    data_ini date,
    data_fim date,
    hora_ini time,
    hora_fim time,
    arquivo varChar(100),
    fk_Sensor_cod_sensor Serial,
    fk_tipo_arquivo_cod_arquivo Serial
);

CREATE TABLE Casa (
    cod_casa Serial PRIMARY KEY,
    fk_Endereco_cod_end Serial,
    fk_Delegacia_cod_delegacia Serial
);

CREATE TABLE Sexo (
    cod_sexo Serial PRIMARY KEY,
    tipo varChar(100)
);

CREATE TABLE Sangue (
    cod_Sanguineo Serial PRIMARY KEY,
    tipo_sanguineo varChar(100)
);

CREATE TABLE Bairro (
    cod_bairro Serial PRIMARY KEY,
    nome_bairro varChar(100),
    fk_Endereco_cod_end Serial,
    fk_Cidade_cod_cidade Serial
);

CREATE TABLE Estado (
    cod_estado Serial PRIMARY KEY,
    nome_estado varChar(100)
);

CREATE TABLE Cidade (
    cod_cidade Serial PRIMARY KEY,
    nome_cidade varChar(100),
    fk_Estado_cod_estado Serial
);

CREATE TABLE Contato (
    cod_contato Serial PRIMARY KEY,
    descricao varChar(100),
    fk_Tipo_contato_cod_tipo Serial
);

CREATE TABLE Tipo_contato (
    desc_tipo varChar(100),
    cod_tipo Serial PRIMARY KEY
);

CREATE TABLE Cadastrados (
    cpf varChar(100),
    rg varChar(100),
    fk_Pessoa_cod_pessoa Serial PRIMARY KEY
);

CREATE TABLE Policial (
    senha varChar(100),
    fk_Pessoa_cod_pessoa Serial PRIMARY KEY,
    fk_Delegacia_cod_delegacia Serial
);

CREATE TABLE Logradouro (
    cod Serial PRIMARY KEY,
    descricao varChar(100),
    tipo varChar(100)
);

CREATE TABLE complemento (
    cod_complemento Serial PRIMARY KEY,
    desc_complemento varChar(100)
);

CREATE TABLE som (
    cod_som Serial PRIMARY KEY,
    local_som varChar(100),
    tipo_som varChar(100)
);

CREATE TABLE Usuario (
    fk_Cadastrados_fk_Pessoa_cod_pessoa Serial PRIMARY KEY,
    fk_Sangue_cod_Sanguineo Serial
);

CREATE TABLE Parceiro (
    fk_Cadastrados_fk_Pessoa_cod_pessoa Serial PRIMARY KEY,
    fk_Relacao_cod_relacao Serial
);

CREATE TABLE Relacao (
    cod_relacao Serial PRIMARY KEY,
    tipo_relacao varChar(100)
);

CREATE TABLE tipo_arquivo (
    cod_arquivo Serial PRIMARY KEY,
    tipo_arquivo varChar(100)
);

CREATE TABLE possui_cadastrados_casa (
    fk_Casa_cod_casa Serial,
    fk_Cadastrados_fk_Pessoa_cod_pessoa Serial
);

CREATE TABLE possui_contato_delegacia (
    fk_Contato_cod_contato Serial,
    fk_Delegacia_cod_delegacia Serial
);

CREATE TABLE possui_cadastrados_contato (
    fk_Contato_cod_contato Serial,
    fk_Cadastrados_fk_Pessoa_cod_pessoa Serial
);

CREATE TABLE possui_end_logradouro (
    fk_Endereco_cod_end Serial,
    fk_Logradouro_cod Serial
);

CREATE TABLE possui_capt_som (
    fk_som_cod_som Serial,
    fk_Captura_cod_captura Serial
);

CREATE TABLE possui_casa_captura (
    fk_Casa_cod_casa Serial,
    fk_Captura_cod_captura Serial
);
 
ALTER TABLE Endereco ADD CONSTRAINT FK_Endereco_1
    FOREIGN KEY (fk_complemento_cod_complemento)
    REFERENCES complemento (cod_complemento)
    ON DELETE CASCADE;
 
ALTER TABLE Pessoa ADD CONSTRAINT FK_Pessoa_1
    FOREIGN KEY (fk_Sexo_cod_sexo)
    REFERENCES Sexo (cod_sexo)
    ON DELETE RESTRICT;
 
ALTER TABLE Delegacia ADD CONSTRAINT FK_Delegacia_1
    FOREIGN KEY (fk_Endereco_cod_end)
    REFERENCES Endereco (cod_end)
    ON DELETE CASCADE;
 
ALTER TABLE Captura ADD CONSTRAINT FK_Captura_1
    FOREIGN KEY (fk_Sensor_cod_sensor)
    REFERENCES Sensor (cod_sensor)
    ON DELETE CASCADE;
 
ALTER TABLE Captura ADD CONSTRAINT FK_Captura_2
    FOREIGN KEY (fk_tipo_arquivo_cod_arquivo)
    REFERENCES tipo_arquivo (cod_arquivo)
    ON DELETE CASCADE;
 
ALTER TABLE Casa ADD CONSTRAINT FK_Casa_1
    FOREIGN KEY (fk_Endereco_cod_end)
    REFERENCES Endereco (cod_end)
    ON DELETE CASCADE;
 
ALTER TABLE Casa ADD CONSTRAINT FK_Casa_2
    FOREIGN KEY (fk_Delegacia_cod_delegacia)
    REFERENCES Delegacia (cod_delegacia)
    ON DELETE RESTRICT;
 
ALTER TABLE Bairro ADD CONSTRAINT FK_Bairro_1
    FOREIGN KEY (fk_Endereco_cod_end)
    REFERENCES Endereco (cod_end)
    ON DELETE CASCADE;
 
ALTER TABLE Bairro ADD CONSTRAINT FK_Bairro_2
    FOREIGN KEY (fk_Cidade_cod_cidade)
    REFERENCES Cidade (cod_cidade)
    ON DELETE RESTRICT;
 
ALTER TABLE Cidade ADD CONSTRAINT FK_Cidade_1
    FOREIGN KEY (fk_Estado_cod_estado)
    REFERENCES Estado (cod_estado)
    ON DELETE RESTRICT;
 
ALTER TABLE Contato ADD CONSTRAINT FK_Contato_1
    FOREIGN KEY (fk_Tipo_contato_cod_tipo)
    REFERENCES Tipo_contato (cod_tipo)
    ON DELETE CASCADE;
 
ALTER TABLE Cadastrados ADD CONSTRAINT FK_Cadastrados_1
    FOREIGN KEY (fk_Pessoa_cod_pessoa)
    REFERENCES Pessoa (cod_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE Policial ADD CONSTRAINT FK_Policial_1
    FOREIGN KEY (fk_Pessoa_cod_pessoa)
    REFERENCES Pessoa (cod_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE Policial ADD CONSTRAINT FK_Policial_2
    FOREIGN KEY (fk_Delegacia_cod_delegacia)
    REFERENCES Delegacia (cod_delegacia)
    ON DELETE RESTRICT;
 
ALTER TABLE Usuario ADD CONSTRAINT FK_Usuario_1
    FOREIGN KEY (fk_Cadastrados_fk_Pessoa_cod_pessoa)
    REFERENCES Cadastrados (fk_Pessoa_cod_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE Usuario ADD CONSTRAINT FK_Usuario_2
    FOREIGN KEY (fk_Sangue_cod_Sanguineo)
    REFERENCES Sangue (cod_Sanguineo)
    ON DELETE CASCADE;
 
ALTER TABLE Parceiro ADD CONSTRAINT FK_Parceiro_1
    FOREIGN KEY (fk_Cadastrados_fk_Pessoa_cod_pessoa)
    REFERENCES Cadastrados (fk_Pessoa_cod_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE Parceiro ADD CONSTRAINT FK_Parceiro_2
    FOREIGN KEY (fk_Relacao_cod_relacao)
    REFERENCES Relacao (cod_relacao)
    ON DELETE CASCADE;
 
ALTER TABLE possui_cadastrados_casa ADD CONSTRAINT FK_possui_cadastrados_casa_0
    FOREIGN KEY (fk_Casa_cod_casa)
    REFERENCES Casa (cod_casa)
    ON DELETE RESTRICT;
 
ALTER TABLE possui_cadastrados_casa ADD CONSTRAINT FK_possui_cadastrados_casa_1
    FOREIGN KEY (fk_Cadastrados_fk_Pessoa_cod_pessoa)
    REFERENCES Cadastrados (fk_Pessoa_cod_pessoa)
    ON DELETE RESTRICT;
 
ALTER TABLE possui_contato_delegacia ADD CONSTRAINT FK_possui_contato_delegacia_0
    FOREIGN KEY (fk_Contato_cod_contato)
    REFERENCES Contato (cod_contato)
    ON DELETE RESTRICT;
 
ALTER TABLE possui_contato_delegacia ADD CONSTRAINT FK_possui_contato_delegacia_1
    FOREIGN KEY (fk_Delegacia_cod_delegacia)
    REFERENCES Delegacia (cod_delegacia)
    ON DELETE SET NULL;
 
ALTER TABLE possui_cadastrados_contato ADD CONSTRAINT FK_possui_cadastrados_contato_0
    FOREIGN KEY (fk_Contato_cod_contato)
    REFERENCES Contato (cod_contato)
    ON DELETE RESTRICT;
 
ALTER TABLE possui_cadastrados_contato ADD CONSTRAINT FK_possui_cadastrados_contato_1
    FOREIGN KEY (fk_Cadastrados_fk_Pessoa_cod_pessoa)
    REFERENCES Cadastrados (fk_Pessoa_cod_pessoa)
    ON DELETE SET NULL;
 
ALTER TABLE possui_end_logradouro ADD CONSTRAINT FK_possui_end_logradouro_0
    FOREIGN KEY (fk_Endereco_cod_end)
    REFERENCES Endereco (cod_end)
    ON DELETE SET NULL;
 
ALTER TABLE possui_end_logradouro ADD CONSTRAINT FK_possui_end_logradouro_1
    FOREIGN KEY (fk_Logradouro_cod)
    REFERENCES Logradouro (cod)
    ON DELETE SET NULL;
 
ALTER TABLE possui_capt_som ADD CONSTRAINT FK_possui_capt_som_0
    FOREIGN KEY (fk_som_cod_som)
    REFERENCES som (cod_som)
    ON DELETE RESTRICT;
 
ALTER TABLE possui_capt_som ADD CONSTRAINT FK_possui_capt_som_1
    FOREIGN KEY (fk_Captura_cod_captura)
    REFERENCES Captura (cod_captura)
    ON DELETE SET NULL;
 
ALTER TABLE possui_casa_captura ADD CONSTRAINT FK_possui_casa_captura_0
    FOREIGN KEY (fk_Casa_cod_casa)
    REFERENCES Casa (cod_casa)
    ON DELETE RESTRICT;
 
ALTER TABLE possui_casa_captura ADD CONSTRAINT FK_possui_casa_captura_1
    FOREIGN KEY (fk_Captura_cod_captura)
    REFERENCES Captura (cod_captura)
    ON DELETE SET NULL;
           
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físic
        b) formato .SQL
        
 insert into estado(nome_estado)
values  ('AC'), 
	('AL'), 
      	('AP'), 
      	('AM'), 
      	('BA'), 
      	('CE'), 
      	('DF'), 
      	('ES'), 
      	('GO'),
      	('MA'),
      	('MT'),
      	('MS'),
      	('MG'),
      	('PA'),
      	('PB'),
      	('PR'),
      	('PE'),
      	('PI'),
      	('RJ'),
      	('RN'),
      	('RS'),
      	('RO'),
      	('RR'),
      	('SC'),
      	('SP'),
      	('SE'),
      	('TO'); 

insert into cidade(nome_cidade, fk_estado_cod_estado)
values('Serra', 8), 
	('Vitória', 8), 
    	('Cariacica', 8), 
    	('Guarapari', 8), 
    	('Serra', 8), 
    	('Vitória', 8), 
    	('Cachoeiro de Itapemirim', 8), 
    	('Linhares', 8), 
    	('Viana', 8), 
    	('São Mateus', 8);

insert into complemento(desc_complemento)
values  ('Ed. Coral'),
	(null),
        (null),
        ('Ed. Porto Branco'),
        ('Ed. Flores de maio'),
        (null),
        ('Ed. Coqueiros verdes'),
        ('Residencial Modular 6'),
        (null),
        ('Residencial Campos');
     
insert into endereco(numero)
values  (123),
        (234),
        (13),
        (124),
        (543),
        (45),
        (576),
        (102),
        (223),
        (456);

insert into bairro(nome_bairro, fk_cidade_cod_cidade, fk_endereco_cod_end)
values  ('Laranjeiras', 1, 1),
	('Horto', 2, 1),
	('Rio Branco', 3, 3),
	('Praia do Morro', 4, 3),
	('Morada de Laranjeiras', 5, 4),
	('Barro Vermelho', 6, 5),
        ('Coramara', 7, 2),
        ('Barras', 8, 2),
        ('Centro-Viana', 9, 2),
        ('Centro-São Mateus', 10, 4);

insert into logradouro(tipo, descricao)
values  ('rua', 'céu azul'),
	('avenida', 'zumbi dos palmares'),
        ('rua', 'Juscelino Almeida'),
        ('beco', 'beco sem saida'),
        ('avenida', 'Brasil'),
        ('rua', 'rua das Oliveiras'),
        ('rua', 'Lorelau diniz'),
        ('rua', 'rua de pedrinhas de brilhante'),
        ('avenida', 'Vi nilde'),
        ('beco', 'das preta');
  
insert into delegacia(fk_endereco_cod_end)
values  (1),
	(2),
        (3),
        (4),
        (5);
        
insert into casa(fk_endereco_cod_end, fk_delegacia_cod_delegacia)
values (6, 2),
	(7, 3),
        (8, 1),
        (9, 2),
        (10, 5);
        
insert into sensor (tipo, nome) 
values ('Microfone Mega', 'tapa023.wav'),
       ('Sensor Sonoro Ky-038', 'tapa077.wav'),
       ('Microfone Mega', 'soco002.wav'),
       ('Microfone Mega', 'baterPorta015.wav'),
       ('Sensor Sonoro Ky-038', 'xingamentoVM008.wav'),
       ('Sensor Sonoro Ky-038', 'xingamentoVF008.wav'),
       ('Microfone Mega', 'coisaQeubrando007.wav'),
       ('Sensor Sonoro Ky-033', 'soco038.wav'),
       ('Microfone Mega', 'baterPorta100.wav'),
       ('Sensor Sonoro Ky-035', 'tapa056.wav');

insert into som (local_som, tipo_som)
values  ('Endereco x no comp', 'tapa'),
        ('Endereco q no comp', 'soco'),
        ('Endereco w no comp', 'coisa quebrando'),
        ('Endereco e no comp', 'xingamento masculino'),
        ('Endereco r no comp', 'grito feminino'),
        ('Endereco t no comp', 'xingamento feminino'),
        ('Endereco y no comp', 'tapa'),
        ('Endereco u no comp', 'tapa'),
        ('Endereco i no comp', 'soco'),
        ('Endereco o no comp', 'grito masculino');

insert into tipo_arquivo (tipo_arquivo)
values  ('WAV'),
        ('MP3'),
        ('ACC');

insert into captura (arquivo, data_ini, data_fim, hora_ini, hora_fim, fk_tipo_arquivo_cod_arquivo, fk_sensor_cod_sensor)
values  ('capCasa1', '2018-06-01', '2018-06-01', '10:27:38', '10:28:07', 1, 10),
        ('capCasa67', '2018-04-12', '2018-04-12', '11:28:49', '11:29:22', 1, 9),
        ('capCasa1', '2018-02-27', '2018-02-27', '17:59:11', '18:04:33', 1, 10),
        ('capCasa2', '2018-10-09', '2018-10-09', '18:17:00', '18:20:33', 1, 5),
        ('capCasa44', '2018-12-25', '2018-12-25', '20:00:00', '20:05:59', 1, 8),
        ('capCasa10', '2018-03-01', '2018-03-01', '10:30:45', '10:32:55', 1, 2),
        ('capCasa9', '2018-09-10', '2018-09-10', '09:30:54', '09:31:55', 1, 10),
        ('capCasa9', '2018-03-10', '2018-03-10', '19:22:22', '19:28:22', 1, 9),
        ('capCasa10', '2018-05-29', '2018-05-29', '18:00:56', '18:06:56', 1, 4),
        ('capCasa3', '2018-10-31', '2018-10-31', '04:33:00', '04:34:00', 1, 6);

insert into sexo(tipo)
values  ('F'),
	('M');

insert into pessoa(nome, fk_sexo_cod_sexo)
values  ('Ana Laura Mendes',1),
        ('Matheus Andrade', 2),
        ('Carlos da Silva',2),
        ('Carla Santos',1),
        ('Antonio Fernandes', 2),
        ('Vitor Costa', 2),
        ('Arthur Miranda', 2),
        ('Bruna Almeida', 1),
        ('Marcos Sousa', 2),
	('Rosana Gabriel', 1),
	('Jislaine Russo', 1),
 	('Joana Avila', 1),
  	('Maria Penhor', 1),
   	('Marina Valter', 1),     
  	('Gabriel Penhasco',2),
  	('Juliano Almaral', 2),
        ('Cristiano Louve', 2),
        ('Christian de Jesus',2),
       	('Betina Oliveira', 1);


insert into cadastrados(cpf, rg, fk_pessoa_cod_pessoa)
values  ('123.456.789-01', 1010, 4),
	('765.234.987-08', 2345, 7),
        ('324.960.845-07', 2020, 8),
        ('196.936.726-09', 8080, 9),
        ('275.874.098-12', 3030,10),
        ('562.916.734-55', 9090, 11),
        ('165.079.945-16', 4040, 12),
        ('065.164.807-03', 5050, 13),
        ('761.092.845-05', 9876, 14),
        ('495.812.384-04', 4567, 15),
        ('567.890.245-07', 2345 , 16),
        ('135.589.654.-09', 3579, 17),
        ('247.986.750-46', 4679, 18),
        ('123.064.379-67', 6679, 19);

insert into sangue(tipo_sanguineo)
values  ('A+'),
	('A-'),
        ('O+'),
        ('O-'),
        ('AB+'),
        ('AB-'),
        ('B+'),
        ('B-');

insert into usuario(fk_cadastrados_fk_pessoa_cod_pessoa, fk_sangue_cod_sanguineo)
values  (4, 1),
        (8, 1),
        (10, 3),
        (11, 2),
        (12, 2),
        (13, 8),
        (14, 6);
        
insert into relacao(tipo_relacao)
values  ('filho'),
	('marido'),
        ('pai'),
        ('avô'),
        ('tio');
        
insert into parceiro(fk_cadastrados_fk_pessoa_cod_pessoa, fk_relacao_cod_relacao)  
values  (7, 2),
	(9, 2),
        (15, 2),
        (16, 1),
        (17, 1),
        (18, 3),
        (19, 2);

insert into policial(senha, fk_pessoa_cod_pessoa, fk_delegacia_cod_delegacia)
values  ('1234', 1, 5),
	('1234', 2, 3),
        ('1234', 3, 1),
        ('1234', 4, 2),
        ('1234', 5, 4);

insert into tipo_contato(desc_tipo)
values  ('telefone'),
	('email');

insert into contato(descricao, fk_tipo_contato_cod_tipo)
values  ('pauloC@gmail.com', 2),
	('anaLaura24@gmail.com', 2),
        ('matheusand1@gmail.com',2),
        ('carlos71@gmail.com',2),
        ('carlaS13@gmail.com', 2),
        ('antonioFer@gmail.com', 2),
        ('vitorcosta5@gmail.com', 2),
        ('arthurM4@gmail.com',2),
        ('brunaAl902@gmail.com',2),
        ('marcosS36@gmail.com', 2),
        ('9812-6456',1),
        ('99887-7766',1),
        ('99855-6689',1),
        ('99334-9911',1),
        ('99865-0977',1),
        ('99345-1235', 1),
        ('98980-7578', 1),
        ('93578-3679', 1),
        ('99340-6568', 1);

insert into possui_cadastrados_casa(fk_casa_cod_casa, fk_cadastrados_fk_pessoa_cod_pessoa)
values (1, 4),
	(1, 7),
        (2, 8),
        (2, 13),
        (2, 9),
        (2, 19),
        (3, 10),
        (3, 18),
        (4, 11),
        (4, 16),
        (5, 12),
        (5, 14),
        (5, 17),
        (5, 15);
        
insert into possui_cadastrados_contato(fk_cadastrados_fk_pessoa_cod_pessoa, fk_contato_cod_contato)
values (4, 11),
	(8, 12),
        (10, 13),
        (11, 14),
        (12, 15),
        (13, 16),
        (14, 17),
        (7, 18),
        (18, 19);

        
delete from som where cod_som > 0;
ALTER SEQUENCE som_cod_som_seq RESTART WITH 1;
insert into som (local_som, tipo_som)
values (null, 'tapa'),
        (null, 'soco'),
        (null, 'vidro quebrando'),
        (null, 'xingamento masculino'),
        (null, 'grito feminino'),
        (null, 'xingamento feminino'),
        (null, 'choro'),
        (null, 'panela caindo'),
        (null, 'porta batendo'),
        (null, 'grito masculino');

       
insert into possui_capt_som( fk_captura_cod_captura, fk_som_cod_som)
values (1,10),
	(1,3),
        (1,9),
        (2,4),
        (2,1),
        (3,2),
        (3,4),
        (3,8),
        (3,9),
        (3,5),
        (4,7),
        (4,1),
        (4,2),
        (4,4),
        (5,9),
        (5,4),
        (6,3),
        (7,5),
        (7,8),
        (8,10),
        (8,1),
        (8,8),
        (9,2),
        (9,4),
        (9,3),
        (10,9),
        (10,7);
       
insert into possui_casa_captura(fk_casa_cod_casa, fk_captura_cod_captura)
values (1, 1),
	(1, 2),
        (1, 3),
        (2, 4),
        (3, 5),
        (3, 6),
        (5, 7),
        (5, 8),
        (5, 9),
        (5, 10);

insert into contato(descricao, fk_tipo_contato_cod_tipo)
values('3325-4537', 2),
	('3137-1652', 2),
        ('3224-3186', 2),
        ('3325_3955', 2),
        ('3314-4287', 2);
        
insert into possui_contato_delegacia(fk_contato_cod_contato, fk_delegacia_cod_delegacia)
values (20, 1),
        (21, 2),
        (22, 3),
        (23, 4),
        (24, 5);
        
insert into possui_end_logradouro(fk_endereco_cod_end, fk_logradouro_cod)
values (1, 1),
	(2, 2),
        (3, 3),
        (4, 4),
        (5, 5),
        (6, 6),
        (7, 7),
        (8, 8),
        (9, 9),
	(10, 10);

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
	
	https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/arquivos/CodigoSQL_VD.docx
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (Drop table + Create de tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
	https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/arquivos/Codigo%2BdropSQL_VD.docx



### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
select * from Usuario;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img1.png)
<br>
select * from Pessoa;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img2.png)
<br>
select * from Delegacia;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img3.png)
<br>
select * from Endereço;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img4.png)
<br>
select * from Sensor;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img5.png)
<br>
select * from Policial;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img6.png)
<br>
select * from Casa;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img7.png)
<br>
select * from Captura;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img8.png)
<br>
select * from Depende;
<br>
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/img9.png)

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
    
select * from Sensor where tipo = 'Microfone Mega';

select * from Usuário where tipo_sanguineo = 'A+' or tipo_sanguineo = 'O-';

select * from Pessoa where sexo = 'F' and idade = '49';

select * from Pessoa where sexo = 'M' and idade < 40;

select * from Pessoa where nome = 'Rosana Gabriel' or nome = 'Marina Valter';

select nome from Pessoa where nome is not null;

select nome_completo, idade, (idade*10) as idade_vezes_dez from Pessoa;

select nome_completo, idade, (idade-12) as idade_menos_doze from Pessoa where sexo = 'M' ;

select nome_completo, rg, (rg/10) as rg_dividido_por_dez from Pessoa;

alter table Pessoa rename nome to nome_completo;

alter table Pessoa rename celular to telefone_móvel;

alter table Usuário rename numero_emergencial to nu_emergencial;
   
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.
	
select nome_completo, cpf from Pessoa where nome_completo ilike '%o%';

select nome_completo from Pessoa where nome_completo like 'J%';

select * from Endereço where cidade like 'S%';

select * from Endereço where bairro ilike '%l%';

select * from Endereço where compl like 'Ed.%';

select now();

select current_date;

select current_time;

select age(current_date, ('2002-12-26'));

select date_part('year',age(current_date, ('2002-12-26')));

extract ('year' from ('2002-12-26'));


#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>

update Pessoa set nome_completo = 'Maria Penhores' where cpf = '196.936.726-09';

delete from Pessoa where nome_completo = 'Cristiane Louve';

update Delegacia set telefone = '(31)9453-5218' where codigo = '1';

delete from Delegacia where codigo = '10';

update Policial set email = 'pauloCR@gmail.com' where nome = 'Paulo Correia';

delete from Policial where fk_delegacia_codigo = '9';

#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
        

## Marco de Entrega 02 em: (16/06/2018)<br>
### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (30/06/2018)
<br>

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

#### 9.11	LISTA DE CODIGOS DAS FUNÇÕES E TRIGGERS<br>
        Detalhamento sobre funcionalidade de cada código.
        a) Objetivo
        b) Código do objeto (função/trigger)
        c) exemplo de dados para aplicação
        d) resultados em forma de tabela/imagem
<br>


#### 9.12	GERACAO DE DADOS (MÍNIMO DE 100 MIL REGISTROS PARA PRINCIPAL RELAÇAO)<br>
        a) principal tabela do sistema deve ter no mínimo 100 mil registros
        b) tabelas diretamente relacionadas a tabela principal 10 mil registros
        c) tabelas auxiliares de relacao multivalorada mínimo de 10 registros
        d) registrar o tempo de inserção em cada uma das tabelas do banco de dados
        e) especificar a quantidade de registros inseridos em cada tabela
        Para melhor compreensão verifiquem o exemplo na base de testes:<br>
        https://github.com/discipbd2/base-de-testes-locadora
        

#### 9.13	Backup do Banco de Dados<br>
        Detalhamento do backup.
        a) Tempo
        b) Tamanho
        c) Teste de restauração (backup)
        d) Tempo para restauração
        e) Teste de restauração (script sql)
        f) Tempo para restauração (script sql)
<br>

Data de Entrega: (Data a ser definida)
<br>

#### 9.14	APLICAÇAO DE ÍNDICES E TESTES DE PERFORMANCE<br>
    a) Lista de índices, tipos de índices com explicação de porque foram implementados nas consultas 
    b) Performance esperada VS Resultados obtidos
    c) Tabela de resultados comparando velocidades antes e depois da aplicação dos índices (constando velocidade esperada com planejamento, sem indice e com índice Vs velocidade de execucao real com índice e sem índice).
    d) Escolher as consultas mais complexas para serem analisadas (consultas com menos de 2 joins não serão aceitas)
    e) As imagens do Explain devem ser inclusas no trabalho, bem como explicações sobre os resultados obtidos.
    f) Inclusão de tabela mostrando as 10 execuções, excluindo-se o maior e menor tempos para cada consulta e 
    obtendo-se a media dos outros valores como resultado médio final.
<br>
    Data de Entrega: (Data a ser definida)
<br>   

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (Data a ser definida)
<br>

### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

    
### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho

### 13	DIFICULDADES ENCONTRADAS PELO GRUPO<br>  

    
>## Marco de Entrega 04/Entrega Final em: (Data definida no cronograma)<br>

       
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")
