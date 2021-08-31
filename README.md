# TRABALHO 01:  Sistema da empresa Casa Completa
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Manoel Rodrigues Loureiro:manoel.rl@gmail.com<br>
Rafael de Oliveira Kau Lyrio:rafakauifes@hotmail.com<br>
...<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados "Casa Completa" 
<br>e motivação da escolha realizada. <br>

> A empresa "Casa Completa" visa a venda de móveis e eletrodomésticos para aqueles que sonham em ter a casa toda mobiliada com ótimos produtos. Sabendo-se dos desafios que são atender a demanda das compras online, cadastro de clientes e empregados, e também a enmtrega em todo o Brasil de forma adequada, ficamos motivados com o desenvolvimento deste sistema. Para realizar suas operações adequadamente a empresa necessita que o sistema armazene informações relativas aos Clientes, Vendedores, Entregadores, Produtos, Vendas, Carrinho de Compras do Cliente e a Encomenda. O sistema deverá gerar um conjunto de relatórios que por sua vez atenderá os anseios da empresa.
 

### 3.MINI-MUNDO<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar) <br>
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente  real)<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O sistema proprosto para a "Casa Completa" conterá informações aqui detalhadas. Dos Clientes e Empregados serão armazenados o código, matrícula, nome, rg e email. Dos Produtos serão armazenados o código, nome e preço de cada produto. Da Venda serão armazedas codigo da venda e data da venda. A Venda deve obrigatoriamente estar associada a um Vendedor e um Cliente. Do Carrinho serão armazenados a quantidade de produtos e o codigo de cada produto escolhido pelo cliente. Da Encomenda serão armazedanas o código de rastreio, destino e codigo do entregador. Importante destacar que o Entregador pode ser responsável por várias encomendas. A empresa poderá ver as vendas feitas, quem realizou a venda e o cliente que comprou.

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser criadas, o princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/89e888eccf47ed77587293b3a9da106295d11cfa/images/balsamiq.PNG)
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Devcom](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/5a56cda9dc5e1c4d2e110e645aabc8b8542a0845/arquivos/Casa%20Completa.pdf)
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa Casa Completa precisa inicialmente dos seguintes relatórios:
* Relatório que mostre o nome de cada vendedor e a quantidade total de dinheiro que eles fizeram com as vendas.
* Relatório que mostra quais os produtos mais vendidos.
* Relatorio que mostre o produto, seu preço e a média geral do preço de todos os produtos ordenados pelo nome da cada produto.
* Relatório que mostre para qual estado saem mais encomendas.
* Relatório que mostre a quantidade de produtos totais que cada cliente comprou.

 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Casa Completa](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/abc91ab5fd6267934e7c821fb9822e282d7e172c/arquivos/TabelaEmpresaCasaCompleta1.xlsx)<br>
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Modelo Conceitual da Empresa Casa Completa](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/8874347b0f131caa4367652a629755f56965344d/images/modelo_conceitual_atualizado.PNG)
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
  PESSOA: Tabela que armazena informações relativas a pessoas, como codigo, nome, rg, email. Obs: CLIENTE, ENTREGADOR E VENDEDOR herdam os atributos de PESSOA;<br>
  PRODUTO: Tabela que armazena informações relativas aos produtos;<br>
  VENDA: Tabela que armazena inforamções relativas a venda;<br>
  CARRINHO: Tabela que armazena informacões relativas a quantidade de produtos selecionado para a compra de um CLIENTE;<br>
  ENCOMENDA: Tabela que armazena o código de rastreio e o destino da entrega.<br>


### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
        
   ![Modelo Lógico da Empresa Casa Completa](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/3a90f9c152514566f21d11ac4422f60e3f22628d/images/modelo_logico_atualizado4.PNG)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
CREATE TABLE PESSOA (codigo INTEGER, nome VARCHAR(50), rg INTEGER, email VARCHAR(50));<br>
CREATE TABLE VENDEDOR (codigo_vendedor, PRIMARY KEY(codigo_vendedor)) INHERITS (PESSOA);<br>
CREATE TABLE CLIENTE (codigo_cliente, PRIMARY KEY(codigo_cliente)) INHERITS (PESSOA);<br>
CREATE TABLE ENTREGADOR (codigo_entregador, PRIMARY KEY(codigo_entregador)) INHERITS (PESSOA);<br>
CREATE TABLE VENDA (codigo_venda INTEGER, data_venda DATE, codigo_vendedor_fk INTEGER, codigo_cliente_fk INTEGER, PRIMARY KEY(codigo_venda));<br>
CREATE TABLE PRODUTO (codigo_produto INTEGER, nome VARCHAR(50), PRIMARY KEY(codigo_produto));<br>
CREATE TABLE CARRINHO (qtd_produto INTEGER, codigo_produto_fk INTEGER, codigo_venda_fk INTEGER);<br>
CREATE TABLE ENCOMENDA (codigo_rastreamento INTEGER, destino VARCHAR(50), codigo_entregador_fk INTEGER, codigo_venda_fk INTEGER , PRIMARY KEY(codigo_rastreamento));<br>

alter table PRODUTO add column preco FLOAT;<br>
alter table ENCOMENDA alter column destino type varchar(200);<br>

ALTER TABLE VENDA add foreign key(codigo_vendedor_fk) REFERENCES VENDEDOR(codigo_vendedor);<br>
ALTER TABLE VENDA add foreign key(codigo_cliente_fk) REFERENCES CLIENTE(codigo_cliente);<br>
alter table CARRINHO add foreign key(codigo_produto_fk) references PRODUTO(codigo_produto);<br>
alter table ENCOMENDA add foreign key(codigo_entregador_fk) references ENTREGADOR(codigo_entregador);<br>
alter table ENCOMENDA add foreign key(codigo_venda_fk) references VENDA(codigo_venda);<br>

ALTER TABLE VENDA DROP CONSTRAINT venda_codigo_vendedor_fk_fkey;<br>
ALTER TABLE VENDA ADD CONSTRAINT venda_codigo_vendedor_fk_fkey FOREIGN KEY(codigo_vendedor_fk) REFERENCES VENDEDORES(codigo_vendedor) MATCH FULL ON UPDATE CASCADE ON DELETE CASCADE;<br>

ALTER TABLE VENDA DROP CONSTRAINT venda_codigo_cliente_fk_fkey;<br>
ALTER TABLE VENDA ADD CONSTRAINT venda_codigo_cliente_fk_fkey FOREIGN KEY(codigo_cliente_fk) REFERENCES CLIENTES(codigo_cliente) MATCH FULL ON UPDATE CASCADE ON DELETE CASCADE;<br>

alter table CARRINHO add foreign key(codigo_venda_fk) references VENDA(codigo_venda);<br>
ALTER TABLE CARRINHO DROP CONSTRAINT carrinho_codigo_venda_fk_fkey;<br>
ALTER TABLE CARRINHO ADD CONSTRAINT carrinho_codigo_venda_fk_fkey FOREIGN KEY(codigo_venda_fk) REFERENCES VENDA(codigo_venda) MATCH FULL ON UPDATE CASCADE ON DELETE CASCADE;<br>

alter table ENCOMENDA drop constraint encomenda_codigo_venda_fk_fkey;<br>
alter table ENCOMENDA add constraint encomenda_codigo_venda_fk_fkey foreign key(codigo_venda_fk) references VENDA(codigo_venda) match full on update cascade on delete cascade;<br>

alter table ENCOMENDA drop constraint encomenda_codigo_entregador_fk_fkey;<br>
alter table ENCOMENDA add constraint encomenda_codigo_entregador_fk_fkey foreign key(codigo_entregador_fk) references ENTREGADOR(codigo_entregador) match full on update cascade on delete cascade;<br>
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
insert into VENDEDOR (matricula, nome, rg, email, codigo_vendedor) values(1, 'Heitor Cunha', 1001, 'heitorcunha@hotmail.com', 1);<br>
insert into VENDEDOR (matricula, nome, rg, email, codigo_vendedor) values(2, 'Rafael Oliveira', 2002, 'rafaeloliveira@hotmail.com', 2), (3, 'Monique Luz', 3003, 'moniqueluz@hotmail.com', 3), (4, 'Ana Luiza Martins', 4004, 'analuizamartins@hotmail.com', 4), (5, 'Rodrigo Luxo', 5005, 'rodrigoluxo@hotmail.com', 5);<br>
insert into VENDEDOR (matricula, nome, rg, email,codigo_vendedor) values(6, 'Rosangela Lazaria', 6006, 'rosangelalazaria@hotmail.com', 6), (7, 'Romulo Mendonça', 7007, 'romulomendonca@hotmail.com', 7), (8, 'Fernanda Gomes', 8008, 'fernandagomes@hotmail.com', 8), (9, 'Filipe Coutinho', 9009, 'filipecoutinho@hotmail.com', 9), (10, 'Thiago Chiste', 1111, 'thiagochiste@hotmail.com', 10);<br>

insert into CLIENTE (matricula, nome, rg, email, codigo_cliente) values(1, 'Mauricio Souza', 9900, 'mauriciosouza@hotmail.com', 1);<br>
insert into CLIENTE (matricula, nome, rg, email, codigo_cliente) values(2, 'Edilson Silva', 8800, 'edilsonsilva@hotmail.com', 2), (3, 'Edgar Marins', 7700, 'edgarmarins@hotmail.com', 3), (4, 'Luis Rodrigues', 6600, 'luisrodrigues@hotmail.com', 4), (5, 'Levi Sacro', 5500, 'levisacro@hotmail.com', 5);<br>
insert into CLIENTE (matricula, nome, rg, email, codigo_cliente) values(6, 'Livia Castro', 4400, 'liviacastro@hotmail.com', 6), (7, 'Luiza Zanetti', 3300, 'luizazanetti@hotmail.com', 7), (8, 'Lucas Gonzalez', 2200, 'lucasgonzalez@hotmail.com', 8), (9, 'Nicole Lorena', 1100, 'nicolelorena@hotmail.com', 9), (10, 'Ubiratã Leal', 9911, 'ubirataleal@hotmail.com', 10);<br>

insert into ENTREGADOR (matricula, nome, rg , email, codigo_entregador_fk) values(1, 'Ronaldo Lima', 1234, 'ronaldolima@hotmail.com', 1);<br>
insert into ENTREGADOR (matricula, nome, rg, email, codigo_entregador_fk) values(2, 'Carlos Busquets', 1478, 'carlosbusquets@hotmail.com', 2), (3, 'Jordan Riso', 2587, 'jordanriso@hotmail.com', 3);<br>
insert into ENTREGADOR (matricula, nome, rg, email, codigo_entregador) values(4, 'Revson Loco', 3698, 'revsonloco@hotmail.com', 4), (5, 'Luciano Ramalho', 3216, 'lucianoramalho@hotmail.com', 5);<br>

insert into VENDA (codigo_venda, data_venda, codigo_vendedor_fk, codigo_cliente_fk) values(1, '2021-08-01', 1, 1);<br>
insert into VENDA (codigo_venda, data_venda, codigo_vendedor_fk, codigo_cliente_fk) values(2, '2021-08-01', 5, 3), (3, '2021-08-01', 2, 4), (4, '2021-08-02', 3, 5);<br>
insert into VENDA (codigo_venda, data_venda, codigo_vendedor_fk, codigo_cliente_fk) values(6, '2021-02-06', 6, 2), (7, '2020-09-23', 2, 1), (8, '2020-10-05', 8, 6), (9, '2021-07-07', 4, 9), (10, '2020-08-15', 7, 7);<br>

insert into PRODUTO (codigo_produto, nome) values(1, 'Geladeira');<br>
insert into PRODUTO (codigo_produto, nome) values(2, 'Guarda-Roupas'), (3, 'Televisão'), (4, 'Cama de Solteiro'), (5, 'Cama de Casal'), (6, 'Cristaleira');<br>

insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(1, 1, 1), (1, 2, 1), (3, 3, 2);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(1, 1, 3), (2, 7, 3), (2, 4, 3), (1, 5, 3);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(1, 6, 4), (4, 3, 4), (1, 1, 4), (5, 2, 4), (2, 7, 4);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(1, 3, 5);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(2, 1, 6), (1, 5, 6);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(1, 2, 7), (5, 3, 7), (1, 4, 7);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(4, 6, 8);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(10, 3, 9);<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk, codigo_venda_fk) values(3, 7, 10), (2, 5, 10);<br>

insert into ENCOMENDA (codigo_rastreamento, destino, codigo_entregador_fk, codigo_venda_fk) values (10001, 'Espirito Santo, Serra, São Domingos, Número 26', 1, 1);<br>
insert into ENCOMENDA (codigo_rastreamento, destino, codigo_entregador_fk, codigo_venda_fk) values (20002, 'São Paulo, Guarulhos, Picanço, Número 300', 1, 2), (30003, 'Distrito Federal, Ceilândia, Ceilândia Centro, Número 4', 2, 3), (40004, 'Bahia, Salvador, Cidade Baixa, Número 657', 3, 4);<br>
insert into ENCOMENDA (codigo_rastreamento, destino, codigo_entregador_fk, codigo_venda_fk) values(60006, 'Minas Gerais, Belo Horizonte, Anchieta, Número 24', 5, 6);<br>
insert into ENCOMENDA (codigo_rastreamento, destino, codigo_entregador_fk, codigo_venda_fk) values(70007, 'Paraná, Curitiba, Alto da Glória, Número 10', 6, 7), (80008, 'Acre, Rio Branco, Capoeira, Número 77', 4, 8), (90009, 'Tocantins, Palmas, Morada do Sol, Número 23', 2, 9), (11111, 'Piauí, Teresina, Mafuá, Número 55', 3, 10);<br>

update PRODUTO set preco = 3520.90 where nome = 'Geladeira';<br>
update PRODUTO set preco = 800 where nome = 'Guarda-Roupas';<br>
update PRODUTO set preco = 2399.9 where nome = 'Televisão';<br>
update PRODUTO set preco = 550 where nome = 'Cama de Solteiro';<br>
update PRODUTO set preco = 1099.99 where nome = 'Cama de Casal';<br>
update PRODUTO set preco = 450 where nome = 'Cristaleira';<br>


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
select * from VENDEDOR;<br>
![Tabela Vendedor](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c6d3d3e397d3d355bc6e6516f3d17d023dfa1e92/images/selectVendedor.PNG)

select * from CLIENTE;<br>
![Tabela Cliente](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c6d3d3e397d3d355bc6e6516f3d17d023dfa1e92/images/selectCliente.PNG)

select * from ENTREGADOR;<br>
![Tabela Entregador](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c6d3d3e397d3d355bc6e6516f3d17d023dfa1e92/images/selectEntregador.PNG)

select * from VENDA;<br>
![Tabela Venda](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c6d3d3e397d3d355bc6e6516f3d17d023dfa1e92/images/selectVenda.PNG)

select * from PRODUTO;<br>
![Tabela Produto](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-produto.PNG)

select * from CARRINHO;<br>
![Tabela Carrinho](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c6d3d3e397d3d355bc6e6516f3d17d023dfa1e92/images/selectCarrinho.PNG)

select * from ENCOMENDA;<br>
![Tabela Encomenda](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c6d3d3e397d3d355bc6e6516f3d17d023dfa1e92/images/selectEncomenda.PNG)

#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
select * from VENDEDOR where codigo_vendedor > 5;<br>
![Where 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/22a36aa7629b8c13b84c65e9eb56ac2e4b31cc1c/images/whereAtt1.PNG)

select nome, preco from PRODUTO where preco < 1000;<br>
![Where 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/ea680af1f1f63dfc74d62ff82f193b01215283e7/images/where2.PNG)

select destino from ENCOMENDA where codigo_rastreamento = 30003;<br>
![Where 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/ea680af1f1f63dfc74d62ff82f193b01215283e7/images/where3.PNG)

select nome, email from CLIENTE where codigo_cliente = 9;<br>
![Where 4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/ea680af1f1f63dfc74d62ff82f193b01215283e7/images/where4.PNG)


#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

##### A)
select nome, email from VENDEDOR where codigo_vendedor > 1 and codigo_vendedor < 5;<br>
![AND 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and1.PNG)

select nome from PRODUTO where codigo_produto > 4 and preco > 1000;<br>
![AND 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and2.PNG)

select nome, rg from CLIENTE where not codigo_cliente > 5;<br>
![AND 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and3.PNG)

select codigo_venda, data_venda from VENDA where codigo_vendedor_fk = 2 or codigo_cliente_fk = 3;<br>
![AND 4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1c9b67a0809bcbc1579bde1ca8903824da612e7f/images/and4att.PNG)

select nome, preco from PRODUTO where not codigo_produto = 1 or codigo_produto = 7;<br>
![AND 5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and5.PNG)

##### B)
select codigo_produto, nome, preco, (preco*0.9) as preco_desconto from PRODUTO where nome = 'Televisão';<br>
![ARITMETICO 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/aritmetico1.PNG)

select C.codigo_produto_fk, P.nome, C.qtd_produto, (P.preco*C.qtd_produto) as valor_total from CARRINHO as C, PRODUTO as P where C.qtd_produto >= 2 and C.codigo_produto_fk = P.codigo_produto;<br>
![ARITMETICO 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/aritmetico2.PNG)

select C.codigo_produto_fk, P.nome, C.qtd_produto, (P.preco*C.qtd_produto) as valor_total from CARRINHO as C, PRODUTO as P where C.codigo_produto_fk = P.codigo_produto;<br>
![ARITMETICO 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/aritmetico3.PNG)

##### C)
alter table if exists VENDEDOR rename to VENDEDORES;<br>

alter table if exists CLIENTE rename to CLIENTES;<br>

alter table if exists PRODUTO rename to PRODUTOS;<br>

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.
##### A)
select codigo_cliente, nome, rg, email from CLIENTES where nome like 'E%';<br>
![LIKE 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1c9b67a0809bcbc1579bde1ca8903824da612e7f/images/like1att.PNG)

select codigo_cliente, nome, rg, email from CLIENTES where nome like 'E%' or nome like 'L%';<br>
![LIKE 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1c9b67a0809bcbc1579bde1ca8903824da612e7f/images/like2att.PNG)

select codigo_rastreamento, destino from ENCOMENDA where destino ilike 'e%';<br>
![LIKE 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1c9b67a0809bcbc1579bde1ca8903824da612e7f/images/like3att.PNG)

select C.nome as nome_cliente, V.nome as nome_vendedor from CLIENTES as C, VENDEDORES as V where C.nome ilike 'm%' and V.nome ilike 'm%';<br>
![LIKE 4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/like4.PNG)

select codigo_vendedor, nome, rg, email from VENDEDORES where nome ilike 'ra%';<br>
![LIKE 5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1c9b67a0809bcbc1579bde1ca8903824da612e7f/images/like5att.PNG)

##### B)
select current_date - V.data_venda as qtd_dias from VENDA as V where V.codigo_venda = 7;<br>
![DATE 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/date1.PNG)

select age(current_date, V.data_venda) as qtd_dias from VENDA as V where V.codigo_venda = 8;<br>
![DATE 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/date2.PNG)

select date_part('year',(age(current_date, data_venda))) as idade from VENDA where codigo_venda = 10;<br>
![DATE 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/date3.PNG)

select codigo_venda, current_date as data_atual, data_venda, extract('year' from data_venda) as ano_venda from VENDA;<br>
![DATE 4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/date4.PNG)

select codigo_venda, data_venda, current_date as data_atual, current_date - data_venda as qtd_dias from VENDA;<br>
![DATE 5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/date5.PNG)

select codigo_venda, data_venda, current_date as data_atual, date_part('month',(age(current_date,data_venda))) as qtd_meses from VENDA where date_part('month',(age(current_date,data_venda))) > 0;<br>
![DATE 6](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/date6.PNG)

select * from VENDA where date_part('year',(age(current_date, data_venda))) >= 1;<br>
![DATE 7](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/date7.PNG)

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização
##### A)
delete from VENDEDORES where codigo_vendedor = 12;<br>

delete from CLIENTES where codigo_cliente = 12;<br>

delete from ENTREGADOR where codigo_entregador = 7;<br>

##### B)
update PRODUTOS set preco = 3600 where nome = 'Geladeira';

update PRODUTOS set preco = 1000 where codigo_produto = 2;

update PRODUTOS set preco = 570.90 where nome = 'Cama de Solteiro';

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
##### A)
select vendedores.nome as nome_vendedor, clientes.nome as nome_cliente, entregador.nome as nome_entregador, produtos.nome as nome_produto
from clientes inner join pessoa on(pessoa.email = clientes.email) inner join vendedores on(vendedores.matricula = clientes.matricula)
inner join venda on(venda.codigo_cliente_fk = clientes.codigo_cliente) inner join encomenda on(encomenda.codigo_venda_fk = venda.codigo_venda)
inner join entregador on(entregador.codigo_entregador = encomenda.codigo_entregador_fk) inner join carrinho on(carrinho.codigo_venda_fk = venda.codigo_venda) inner join produtos on(produtos.codigo_produto = carrinho.codigo_produto_fk) order by vendedores.nome asc;<br>
![Imagem1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/345d8a93fbfe2dd2ae0d02ea74330696d83906e5/images/9.6.1.jpeg)

select sum(carrinho.qtd_produto) as qnt_vendida, produtos.nome as nome_do_produto from carrinho inner join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by carrinho.codigo_produto_fk, produtos.nome order by qnt_vendida asc;<br>
![Imagem2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1e7268f191bb2c826be97f76f7c8d5e78d02d043/images/9.6.2.jpeg)

select vendedores.nome as nome_vendedor, clientes.nome as nome_cliente, entregador.nome as nome_entregador from clientes inner join pessoa
on(pessoa.email = clientes.email) inner join vendedores on(vendedores.matricula = clientes.matricula) inner join venda on(venda.codigo_cliente_fk = clientes.codigo_cliente) inner join encomenda on(encomenda.codigo_venda_fk = venda.codigo_venda) inner join entregador on(entregador.codigo_entregador = encomenda.codigo_entregador_fk) order by vendedores.nome asc;<br>
![Imagem3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1e7268f191bb2c826be97f76f7c8d5e78d02d043/images/9.6.3.jpeg)

##### B)
select entregador.nome as nome_do_entregador, count(encomenda.codigo_entregador_fk) as qnt_de_entregas from entregador inner join encomenda
on(encomenda.codigo_entregador_fk = entregador.codigo_entregador) group by entregador.nome order by entregador.nome asc;<br>
![Imagem4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1e7268f191bb2c826be97f76f7c8d5e78d02d043/images/9.6.4.jpeg)

select encomenda.destino as endereço_do_cliente, clientes.nome as nome_do_cliente 
from encomenda
inner join venda
on(encomenda.codigo_venda_fk = venda.codigo_venda)
inner join clientes
on(clientes.codigo_cliente = venda.codigo_cliente_fk)
order by encomenda.destino asc;<br>
![Imagem5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1e7268f191bb2c826be97f76f7c8d5e78d02d043/images/9.6.5.jpeg)

select venda.data_venda, encomenda.destino from venda inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador_fk) 
order by data_venda desc;<br>
![Imagem6](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/1e7268f191bb2c826be97f76f7c8d5e78d02d043/images/9.6.6.jpeg)

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção
    
select produtos.nome as nome_do_produto,sum(carrinho.qtd_produto) as quantidade_vendida from carrinho left outer join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by carrinho.codigo_produto_fk, produtos.nome order by carrinho.codigo_produto_fk asc;<br>
![2IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.7.1.jpeg)

select venda.codigo_vendedor_fk as codigo_do_vendedor, vendedores.nome as nome_do_vendedor from venda inner join vendedores  on(venda.codigo_vendedor_fk = vendedores.codigo_vendedor) group by venda.codigo_vendedor_fk, vendedores.nome order by
venda.codigo_vendedor_fk asc;<br>
![2IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/fd51459bf2e066d3ea6f61eb875a937adf5c7b56/images/9.7.2.jpeg)

select venda.data_venda, encomenda.codigo_entregador_fk as codigo_entregador from venda inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador_fk) group by venda.data_venda, encomenda.codigo_entregador_fk order by encomenda.codigo_entregador_fk desc;<br>
![2IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.7.3.jpeg)

select venda.codigo_vendedor_fk , encomenda.codigo_rastreamento from venda inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador_fk) group by venda.codigo_vendedor_fk, encomenda.codigo_rastreamento order by venda.codigo_vendedor_fk desc;<br>
![2IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.7.4.jpeg)

select produtos.nome as nome_do_produto ,produtos.preco as preco_do_produto from carrinho inner join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by nome_do_produto, preco_do_produto order by preco_do_produto asc;<br>
![2IMAGEM4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.7.5.jpeg)

select entregador.nome as nome_do_entregador, count(encomenda.codigo_entregador_fk) as qnt_de_entregas from entregador left outer join encomenda
on(encomenda.codigo_entregador_fk = entregador.codigo_entregador) group by entregador.nome order by qnt_de_entregas asc;<br>
![2IMAGEM5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.7.6.jpeg)


#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

select sum(carrinho.qtd_produto) as qnt_de_produtos,produtos.nome as nome_do_produto from carrinho left outer join produtos  on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by produtos.nome order by qnt_de_produtos asc;<br>
![3IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.8.1.jpeg)

select produtos.nome as nome_do_produto ,produtos.preco as preco_do_produto from carrinho right outer join produtos 
on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by nome_do_produto, preco_do_produto order by preco_do_produto asc;<br>
![3IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.8.2.jpeg)

select venda.codigo_vendedor_fk, vendedores.nome as nome_do_vendedor from venda full outer join vendedores on(venda.codigo_vendedor_fk = vendedores.codigo_vendedor) group by venda.codigo_vendedor_fk, vendedores.nome order by  venda.codigo_vendedor_fk asc;<br>
![3IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.8.3.jpeg)

select entregador.nome as nome_do_entregador, count(encomenda.codigo_entregador_fk) as qnt_de_entregas from entregador
full join encomenda on(encomenda.codigo_entregador_fk = entregador.codigo_entregador) group by entregador.nome order by qnt_de_entregas asc;<br>
![3IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.8.4.jpeg)

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
##### A)
select v1.codigo_vendedor_fk as codigo_vendedor, v2.codigo_venda as codigo_venda from venda v1 inner join venda v2 on(v1.codigo_vendedor_fk =  v2.codigo_cliente_fk);<br>
![4IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.9.1.jpeg)

create view codigo_vendedor_e_venda as select venda.data_venda, encomenda.destino from venda inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador_fk) order by data_venda desc; select * from codigo_vendedor_e_venda;<br>
![4IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.9.2.jpeg)

create view relacaoes_mais_importantes as select vendedores.nome as nome_vendedor, clientes.nome as nome_cliente, entregador.nome as nome_entregador, produtos.nome as nome_produto from clientes inner join pessoa on(pessoa.email = clientes.email) inner join vendedores on(vendedores.matricula = clientes.matricula) inner join venda on(venda.codigo_cliente_fk = clientes.codigo_cliente) inner join encomenda on(encomenda.codigo_venda_fk = venda.codigo_venda) inner join entregador on(entregador.codigo_entregador = encomenda.codigo_entregador_fk) inner join carrinho on(carrinho.codigo_venda_fk = venda.codigo_venda) inner join produtos on(produtos.codigo_produto = carrinho.codigo_produto_fk) order by vendedores.nome asc; select * from relacaoes_mais_importantes;<br>
![4IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.9.3.jpeg)

##### B)
create view qnt_e_nome_dos_produtos as select sum(carrinho.qtd_produto) as qnt_de_produtos,produtos.nome as nome_do_produto from carrinho 
left outer join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by produtos.nome order by qnt_de_produtos asc;
select * from qnt_e_nome_dos_produtos;<br>
![4IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.9.4.jpeg)

create view qnt_e_preco_dos_produtos as select produtos.nome as nome_do_produto ,produtos.preco as preco_do_produto from carrinho right outer join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by nome_do_produto, preco_do_produto order by preco_do_produto asc;
select * from qnt_e_preco_dos_produtos;<br>
![4IMAGEM4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.9.5.jpeg)

create view data_da_venda_e_codigo_entregador as select venda.data_venda, encomenda.codigo_entregador_fk as codigo_entregador from venda 
inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador_fk) group by venda.data_venda, encomenda.codigo_entregador_fk order by encomenda.codigo_entregador_fk desc; select * from data_da_venda_e_codigo_entregador;<br>
![4IMAGEM5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.9.6.jpeg)

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção
##### A)
select sum(carrinho.qtd_produto) as qnt_de_produtos,produtos.nome as nome_do_produto from carrinho left outer join produtos  on(carrinho.codigo_produto_fk = produtos.codigo_produto) where carrinho.qtd_produto in (select carrinho.qtd_produto 
from carrinho where produtos.codigo_produto < 5) group by produtos.nome order by qnt_de_produtos asc;<br>
![5IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.10.1.jpeg)

select venda.codigo_vendedor_fk as codigo_vendedor, vendedores.nome from venda right outer join vendedores on(venda.codigo_vendedor_fk = vendedores.codigo_vendedor) where venda.codigo_vendedor_fk in (select venda.codigo_vendedor_fk from venda where vendedores.codigo_vendedor > 4) 
group by venda.codigo_vendedor_fk, vendedores.nome,vendedores.codigo_vendedor order by vendedores.codigo_vendedor asc;<br>
![5IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.10.2.jpeg)

##### B)
select venda.codigo_vendedor_fk as codigo_vendedor, vendedores.nome from venda inner join vendedores on(venda.codigo_vendedor_fk = vendedores.codigo_vendedor) where venda.codigo_vendedor_fk in (select venda.codigo_vendedor_fk from venda where vendedores.codigo_vendedor < 7) 
group by venda.codigo_vendedor_fk, vendedores.nome,vendedores.codigo_vendedor order by vendedores.codigo_vendedor asc;<br>
![5IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.10.3.jpeg)

select venda.data_venda, encomenda.codigo_entregador_fk as codigo_entregador from venda full outer join encomenda on(venda.codigo_venda = encomenda.codigo_entregador_fk) where venda.data_venda in (select venda.data_venda from venda where encomenda.codigo_entregador_fk > 1) 
group by venda.data_venda, encomenda.codigo_entregador_fk order by data_venda desc;<br>
![5IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/94217ec5bc0dab683991281989366262d90123f6/images/9.10.4.jpeg)

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
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
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


