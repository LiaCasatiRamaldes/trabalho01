# TRABALHO 01:  Sensor de Violência Doméstica
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
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
        
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/modelo_conceitualVD.png)
    
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
   
   Campo endereço: em nosso projeto optamos por um campo emdereço, porque...
   Campo pessoa:
    
    
    

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
![Alt text](https://github.com/SensorDeViolenciaDomestica/trabalho01/blob/master/imagens/modelo_logicoVD.png)
        a) inclusão do modelo lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..)
        
        
CREATE TABLE Endereço (
    estado varChar(100),
    cidade varChar(100),
    bairro varChar(100),
    compl varChar(100),
    Nº int,
    rua varChar(100),
    cod_end varChar(100) PRIMARY KEY
);

CREATE TABLE Sensor (
    cod_sensor varChar(100) PRIMARY KEY,
    tipo varChar(100),
    nome varChar(100)
);

CREATE TABLE Pessoa (
    nome varChar(100),
    cpf varChar(100) PRIMARY KEY,
    rg int,
    sexo char,
    idade int,
    celular varChar(100)
);

CREATE TABLE Usuário (
    tipo_sanguineo Varchar(3),
    numero_emergencial varchar(100),
    FK_Pessoa_cpf varChar(100) PRIMARY KEY
);

CREATE TABLE Policial (
    nome varChar(100),
    email varChar(100),
    usuário varChar(100) PRIMARY KEY,
    senha varChar(100),
    FK_Delegacia_Codigo varChar(100)
);

CREATE TABLE Casa (
    FK_Endereço_cod_end varChar(100),
    FK_Delegacia_Codigo varChar(100)
);

CREATE TABLE Delegacia (
    Telefone varChar(100),
    Codigo varChar(100) PRIMARY KEY,
    FK_Endereço_cod_end varChar(100)
);

CREATE TABLE Captura (
    codigo_captura varChar(100) PRIMARY KEY,
    arquivo_som varChar(100),
    data_ini date,
    data_fim date,
    hora_ini time,
    hora_fim time
);

CREATE TABLE Possui (
    FK_Pessoa_cpf varChar(100)
);

CREATE TABLE depende (
    FK_Sensor_cod_sensor varChar(100),
    FK_Captura_codigo_captura varChar(100)
);

CREATE TABLE possui (
    FK_Captura_codigo_captura varChar(100)
);
 
ALTER TABLE Usuário ADD CONSTRAINT FK_Usuário_1
    FOREIGN KEY (FK_Pessoa_cpf)
    REFERENCES Pessoa (cpf)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Policial ADD CONSTRAINT FK_Policial_1
    FOREIGN KEY (FK_Delegacia_Codigo)
    REFERENCES Delegacia (Codigo)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Casa ADD CONSTRAINT FK_Casa_0
    FOREIGN KEY (FK_Endereço_cod_end)
    REFERENCES Endereço (cod_end)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Casa ADD CONSTRAINT FK_Casa_1
    FOREIGN KEY (FK_Delegacia_Codigo)
    REFERENCES Delegacia (Codigo)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Delegacia ADD CONSTRAINT FK_Delegacia_1
    FOREIGN KEY (FK_Endereço_cod_end)
    REFERENCES Endereço (cod_end)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Possui ADD CONSTRAINT FK_Possui_0
    FOREIGN KEY (FK_Pessoa_cpf)
    REFERENCES Pessoa (cpf)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE depende ADD CONSTRAINT FK_depende_0
    FOREIGN KEY (FK_Sensor_cod_sensor)
    REFERENCES Sensor (cod_sensor)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE depende ADD CONSTRAINT FK_depende_1
    FOREIGN KEY (FK_Captura_codigo_captura)
    REFERENCES Captura (codigo_captura)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE possui ADD CONSTRAINT FK_possui_0
    FOREIGN KEY (FK_Captura_codigo_captura)
    REFERENCES Captura (codigo_captura)
    ON DELETE SET NULL ON UPDATE CASCADE;
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físic
        b) formato .SQL
        
 insert into endereco(estado, cidade, bairro, compl, nº, rua, cod_end )
values ('ES', 'Serra', 'Laranjeiras', 'Ed.Coloral', 123, '1', '29170-001'),
		('ES', 'Vitória',	'Horto', null, 234, '2', '29010-002'),
        ('ES', 'Cariacica',	'Rio Branco', null, 13,	'3', '29111-003'),
        ('ES', 'Guarapari', 'Praia do Morro', 'Ed. Porto Branco', 124, '4', '29200-004'),
        ('ES', 'Serra', 'Morada de Laranjeiras', 'Ed.Flores De Maio', 543, '5', '29170-005'),
        ('ES', 'Vitória', 'Barro Vermelho', null, 45, '6', '29010-006'),
        ('ES', 'Cachoeiro Itapemirim', 'Coramara', 'Ed. Coqueiros Verdes', 576, '7', '29300-007'),
        ('ES', 'Linhares', 'Barras', 'Residencial Modular 6', 102, '8', '29900-008'),
        ('ES', 'Viana', 'Centro-Viana', null, 223, '9', '29130-009'),
        ('ES', 'São Mateus', 'Centro-São Mateus', 'Residencial Campos', 456, '10', '29310-010');

insert into sensor (cod_sensor, tipo, nome) 
values('123-456-789', 'Microfone Mega', 'tapa023.wav'),
       ('234-567-897', 'Sensor Sonoro Ky-038', 'tapa077.wav'),
       ('435-769-142',	'Microfone Mega', 'soco002.wav'),
       ('268-916-031', 'Microfone Mega', 'baterPorta015.wav'),
       ('469-911-270',	'Sensor Sonoro Ky-038', 'xingamentoVM008.wav'),
       ('927-881-236',	'Sensor Sonoro Ky-038', 'xingamentoVF008.wav'),
       ('871-903-054',	'Microfone Mega', 'coisaQeubrando007.wav'),
       ('673-189-037',	'Sensor Sonoro Ky-033', 'soco038.wav'),
       ('824-517-900',	'Microfone Mega', 'baterPorta100.wav'),
       ('735-357-573',	'Sensor Sonoro Ky-035', 'tapa056.wav');
                                                    

insert into pessoa (nome, cpf, rg, sexo, idade, celular)
values ('Rosana Gabriel', '123.456.789-01',	1010, 'F', 48, '9999-8765'),
		('Jislaine Russo', '765.234.987-08', 2345, 'F',	36,	'9999-7654'),
        ('Joana Avila', '324.960.845-07', 2020,	'F', 41, '9999-6543'),
        ('Maria Penhor', '196.936.726-09', 8080, 'F', 53, '9999-5432'),
        ('Marina Valter', '275.874.098-12', 3030, 'F', 33, '9999-4321'),
        ('Gabriel Penhasco', '562.916.734-55', 9090, 'M', 50, '9998-0987'),
        ('Juliana Almaral',	'165.079.945-16', 4040, 'F', 45, '9998-0876'),
        ('Cristiane Louve', '065.164.807-03', 5050, 'F', 49, '9998-9876'),
        ('Christian de Jesus', '761.092.845-05', 9876, 'M', 38, '9998-7654'),
        ('Betina Oliveira',	'495.812.384-04', 4567, 'F', 49, '9998-5432');
        
insert into usuario(tipo_sanguineo, numero_emergencial, fk_pessoa_cpf)
values ('O+', '99123-4567', '123.456.789-01'),
		('A-', '9123-4567', '765.234.987-08'),
        ('O+', '9812-6456', '324.960.845-07'),
        ('AB-', '99887-7766', '196.936.726-09'),
        ('B+', '99855-6689', '275.874.098-12'),
        ('A+', '99334-9911', '562.916.734-55'),
        ('O-', '99865-0977', '165.079.945-16'),
        ('AB+', '99345-1235', '065.164.807-03'),
        ('AB-', '98980-7578', '761.092.845-05'),
        ('A+', '99340-6568', '495.812.384-04');
        
insert into delegacia(telefone, codigo, fk_endereco_cod_end)
values ('(27) 3138-8103', '1', '29170-001'),
		('(27) 3137 9025', '2', '29010-002'),
        ('(27) 3136-3111', '3', '29111-003'),
        ('3161-1220', '4', '29200-004'),
        ('(27) 3138-8103', '5', '29170-005'),
        ('3137 9111', '6', '29010-006'),
        ('(28) 3155-5046', '7', '29300-007'),
        ('3264-2537', '8', '29900-008'),
        ('3314-5401', '9', '29130-009'),
        ('3767-9694', '10', '29310-010');
        

insert into policial(nome, email, usuário, senha, fk_delegacia_codigo)
values ('Paulo Correia', 'pauloC@gmail.com', 'PauloC', '******', '1'),
		('Ana Laura Mendes', 'anaLaura24@gmail.com', 'AnaLaura2', '******', '2'),
        ('Matheus Andrade', 'matheusand1@gmail.com', 'MatheusS', '******', '3'),
        ('Carlos da Silva', 'carlos71@gmail.com', 'Carlos71', '******', '4'),
        ('Carla Santos', 'carlaS13@gmail.com', 'Carla13', '******', '5'),
        ('Antonio Fernandes', 'antonioFer@gmail.com', 'AntonioFer', '******', '6'),
        ('Vitor Costa', 'vitorcosta5@gmail.com', 'VitorCost', '******', '7'),
        ('Arthur Miranda', 'arthurM4@gmail.com', 'ArthurM', '******', '8'),
        ('Bruna Almeida', 'brunaAl902@gmail.com', 'Bruna902', '******', '9'),
        ('Marcos Sousa', 'marcosS36@gmail.com', 'Marcos36', '******', '10');
        
insert into casa(FK_Endereço_cod_end, FK_Delegacia_Codigo)
values ('29170-001', '1'),
		('29010-002', '2'),
        ('29111-003', '3'),
        ('29200-004', '4'),
        ('29170-005', '5'),
        ('29010-006', '6'),
        ('29300-007', '7'),
        ('29900-008', '8'),
        ('29130-009', '9'),
        ('29310-010', '10');
        
insert into captura (codigo_captura, arquivo_som, data_ini, data_fim, hora_ini, hora_fim)
values ('1230', 'wav', '2018-06-01', '2018-06-01', '10:27:38', '10:28:07'),
		('1240', 'wav', '2018-04-12', '2018-04-12', '11:28:49', '11:29:22'),
        ('1250', 'wav', '2018-02-27', '2018-02-27',	'17:59:11', '18:04:33'),
        ('1260', 'wav', '2018-10-09', '2018-10-09',	'18:17:00', '18:20:33'),
        ('1270', 'wav', '2018-12-25', '2018-12-25', '20:00:00', '20:05:59'),
        ('1280', 'wav', '2018-03-01', '2018-03-01', '10:30:45', '10:32:55'),
        ('1290', 'wav', '2018-09-10', '2018-09-10', '09:30:54', '09:31:55'),
        ('1210', 'wav', '2018-03-10', '2018-03-10', '19:22:22', '19:28:22'),
        ('1220', 'wav', '2018-05-29', '2018-05-29', '18:00:56', '18:06:56'),
        ('1100', 'wav', '2018-10-31', '2018-10-31', '04:33:00', '04:34:00');
        
        
insert into depende (FK_Sensor_cod_sensor, FK_Captura_codigo_captura)
values ('123-456-789', '1230'),
		('234-567-897', '1240'),
        ('435-769-142', '1250'),
        ('268-916-031', '1260'),
        ('469-911-270', '1270'),
        ('927-881-236', '1280'),
        ('871-903-054', '1290'),
        ('673-189-037', '1210'),
        ('824-517-900', '1220'),
        ('735-357-573', '1100'); 

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (Drop table + Create de tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


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
