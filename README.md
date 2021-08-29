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
* Relatório que mostre as vendas realizadas por cada vendedor.
* Relatório relativo a quantidade de cada produto vendido no mês.
* Relatorio que mostre todos os clientes cadastrados.
* Relatório que mostre para qual destino saem mais encomendas.
* Relatório do faturamento total no mês.

 
 
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
        
   ![Modelo Lógico da Empresa Casa Completa](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/a105f35a34c29c7e0f6124ad958c7b53ca8bf9a9/images/modelo_logico_atualizado2.PNG)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
CREATE TABLE PESSOA (codigo INTEGER, nome VARCHAR(50), rg INTEGER, email VARCHAR(50), PRIMARY KEY(codigo));<br>
CREATE TABLE VENDEDOR () INHERITS (PESSOA);<br>
CREATE TABLE CLIENTE () INHERITS (PESSOA);<br>
CREATE TABLE ENTREGADOR () INHERITS (PESSOA);<br>
CREATE TABLE VENDA (codigo_venda INTEGER, data_venda DATE, codigo_vendedor INTEGER, codigo_cliente INTEGER, PRIMARY KEY(codigo_venda));<br>
CREATE TABLE PRODUTO (codigo_produto INTEGER, nome VARCHAR(50), PRIMARY KEY(codigo_produto));<br>
CREATE TABLE CARRINHO (qtd_produto INTEGER, codigo_produto_fk INTEGER);<br>
CREATE TABLE ENCOMENDA (codigo_rastreamento INTEGER, destino VARCHAR(50), codigo_entregador INTEGER, PRIMARY KEY(codigo_rastreamento));<br>

alter table PRODUTO add column preco FLOAT;<br>
alter table ENCOMENDA alter column destino type varchar(200);<br>
alter table VENDEDOR add primary key(codigo);<br>
alter table CLIENTE add primary key(codigo);<br>
alter table ENTREGADOR add primary key(codigo);<br>

ALTER TABLE VENDA add foreign key(codigo_vendedor) REFERENCES VENDEDOR(codigo);<br>
ALTER TABLE VENDA add foreign key(codigo_cliente) REFERENCES CLIENTE(codigo);<br>
alter table CARRINHO add foreign key(codigo_produto_fk) references PRODUTO(codigo_produto);<br>

ALTER TABLE VENDA DROP CONSTRAINT venda_codigo_vendedor_fkey;<br>
ALTER TABLE VENDA ADD CONSTRAINT venda_codigo_vendedor_fkey FOREIGN KEY(codigo_vendedor) REFERENCES VENDEDOR(codigo) MATCH FULL ON UPDATE CASCADE ON DELETE CASCADE;<br>

ALTER TABLE VENDA DROP CONSTRAINT venda_codigo_cliente_fkey;<br>
ALTER TABLE VENDA ADD CONSTRAINT venda_codigo_cliente_fkey FOREIGN KEY(codigo_cliente) REFERENCES CLIENTE(codigo) MATCH FULL ON UPDATE CASCADE ON DELETE CASCADE;<br>

ALTER TABLE CARRINHO DROP CONSTRAINT carrinho_codigo_produto_fk_fkey;<br>
ALTER TABLE CARRINHO ADD CONSTRAINT carrinho_codigo_produto_fk_fkey FOREIGN KEY(codigo_produto_fk) REFERENCES PRODUTO(codigo_produto) MATCH FULL ON UPDATE CASCADE ON DELETE CASCADE;<br>
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
insert into VENDEDOR (codigo, nome, rg, email) values(1, 'Heitor Cunha', 1001, 'heitorcunha@hotmail.com');<br>
insert into VENDEDOR (codigo, nome, rg, email) values(2, 'Rafael Oliveira', 2002, 'rafaeloliveira@hotmail.com'), (3, 'Monique Luz', 3003, 'moniqueluz@hotmail.com'), (4, 'Ana Luiza Martins', 4004, 'analuizamartins@hotmail.com'), (5, 'Rodrigo Luxo', 5005, 'rodrigoluxo@hotmail.com');<br>
insert into VENDEDOR (codigo, nome, rg, email) values(6, 'Rosangela Lazaria', 6006, 'rosangelalazaria@hotmail.com'), (7, 'Romulo Mendonça', 7007, 'romulomendonca@hotmail.com'), (8, 'Fernanda Gomes', 8008, 'fernandagomes@hotmail.com'), (9, 'Filipe Coutinho', 9009, 'filipecoutinho@hotmail.com'), (10, 'Thiago Chiste', 1111, 'thiagochiste@hotmail.com');<br>
insert into CLIENTE (codigo, nome, rg, email) values(1, 'Mauricio Souza', 9900, 'mauriciosouza@hotmail.com');<br>
insert into CLIENTE (codigo, nome, rg, email) values(2, 'Edilson Silva', 8800, 'edilsonsilva@hotmail.com'), (3, 'Edgar Marins', 7700, 'edgarmarins@hotmail.com'), (4, 'Luis Rodrigues', 6600, 'luisrodrigues@hotmail.com'), (5, 'Levi Sacro', 5500, 'levisacro@hotmail.com');<br>
insert into CLIENTE (codigo, nome, rg, email) values(6, 'Livia Castro', 4400, 'liviacastro@hotmail.com'), (7, 'Luiza Zanetti', 3300, 'luizazanetti@hotmail.com'), (8, 'Lucas Gonzalez', 2200, 'lucasgonzalez@hotmail.com'), (9, 'Nicole Lorena', 1100, 'nicolelorena@hotmail.com'), (10, 'Ubiratã Leal', 9911, 'ubirataleal@hotmail.com');<br>
insert into ENTREGADOR (codigo, nome, rg , email) values(1, 'Ronaldo Lima', 1234, 'ronaldolima@hotmail.com');<br>
insert into ENTREGADOR (codigo, nome, rg, email) values(2, 'Carlos Busquets', 1478, 'carlosbusquets@hotmail.com'), (3, 'Jordan Riso', 2587, 'jordanriso@hotmail.com');<br>
insert into ENTREGADOR (codigo, nome, rg, email) values(4, 'Revson Loco', 3698, 'revsonloco@hotmail.com'), (5, 'Luciano Ramalho', 3216, 'lucianoramalho@hotmail.com');<br>
insert into VENDA (codigo_venda, data_venda, codigo_vendedor, codigo_cliente) values(1, '2021-08-01', 1, 1);<br>
insert into VENDA (codigo_venda, data_venda, codigo_vendedor, codigo_cliente) values(2, '2021-08-01', 5, 3), (3, '2021-08-01', 2, 4), (4, '2021-08-02', 3, 5);<br>
insert into PRODUTO (codigo_produto, nome) values(1, 'Geladeira');<br>
insert into PRODUTO (codigo_produto, nome) values(2, 'Guarda-Roupas'), (3, 'Televisão'), (4, 'Cama de Solteiro'), (5, 'Cama de Casal'), (6, 'Cristaleira');<br>
insert into CARRINHO (qtd_produto, codigo_produto_fk) values(1, 1), (1, 2), (3, 3);<br>
insert into ENCOMENDA (codigo_rastreamento, destino, codigo_entregador) values (10001, 'Espirito Santo, Serra, São Domingos, Número 26', 1);<br>
insert into ENCOMENDA (codigo_rastreamento, destino, codigo_entregador) values (20002, 'São Paulo, Guarulhos, Picanço, Número 300', 1), (30003, 'Distrito Federal, Ceilândia, Ceilândia Centro, Número 4', 2), (40004, 'Bahia, Salvador, Cidade Baixa, Número 657', 3);<br>

update PRODUTO set preco = 3520.90 where nome = 'Geladeira';<br>
update PRODUTO set preco = 800 where nome = 'Guarda-Roupas';<br>
update PRODUTO set preco = 2399.9 where nome = 'Televisão';<br>
update PRODUTO set preco = 550 where nome = 'Cama de Solteiro';<br>
update PRODUTO set preco = 1099.99 where nome = 'Cama de Casal';<br>
update PRODUTO set preco = 450 where nome = 'Cristaleira';<br>


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
select * from VENDEDOR;<br>
![Tabela Vendedor](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-vendedor.PNG)

select * from CLIENTE;<br>
![Tabela Cliente](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-cliente.PNG)

select * from ENTREGADOR;<br>
![Tabela Entregador](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-entregador.PNG)

select * from VENDA;<br>
![Tabela Venda](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-venda.PNG)

select * from PRODUTO;<br>
![Tabela Produto](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-produto.PNG)

select * from CARRINHO;<br>
![Tabela Carrinho](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-carrinho.PNG)

select * from ENCOMENDA;<br>
![Tabela Encomenda](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/0fd5470a4dc73c44fc64d9391239849a3bd1c361/images/tabela-encomenda.PNG)

#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
select * from VENDEDOR where codigo > 5;<br>
![Where 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/ea680af1f1f63dfc74d62ff82f193b01215283e7/images/where1.PNG)

select nome, preco from PRODUTO where preco < 1000;<br>
![Where 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/ea680af1f1f63dfc74d62ff82f193b01215283e7/images/where2.PNG)

select destino from ENCOMENDA where codigo_rastreamento = 30003;<br>
![Where 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/ea680af1f1f63dfc74d62ff82f193b01215283e7/images/where3.PNG)

select nome, email from CLIENTE where codigo = 9;<br>
![Where 4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/ea680af1f1f63dfc74d62ff82f193b01215283e7/images/where4.PNG)


#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

##### A)
select nome, email from VENDEDOR where codigo > 1 and codigo < 5;<br>
![AND 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and1.PNG)

select nome from PRODUTO where codigo_produto > 4 and preco > 1000;<br>
![AND 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and2.PNG)

select nome, rg from CLIENTE where not codigo > 5;<br>
![AND 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and3.PNG)

select codigo_venda, data_venda from VENDA where codigo_vendedor = 2 or codigo_cliente = 3;<br>
![AND 4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c5cc05c13ce305e55eabacf2393a4fcf2c4f2d8f/images/and4.PNG)

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
select * from CLIENTES where nome like 'E%';<br>
![LIKE 1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/like1.PNG)

select * from CLIENTES where nome like 'E%' or nome like 'L%';<br>
![LIKE 2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/like2.PNG)

select * from ENCOMENDA where destino ilike 'e%';<br>
![LIKE 3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/like3.PNG)

select C.nome as nome_cliente, V.nome as nome_vendedor from CLIENTES as C, VENDEDORES as V where C.nome ilike 'm%' and V.nome ilike 'm%';<br>
![LIKE 4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/like4.PNG)

select * from VENDEDORES where nome ilike 'ra%';<br>
![LIKE 5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/c49eb03eabe53b39d24070cc82b440ae56246d34/images/like5.PNG)

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
delete from VENDEDOR where codigo = 12;<br>

delete from CLIENTE where codigo = 12;<br>

delete from ENTREGADOR where codigo = 7;<br>

##### B)
update PRODUTO set preco = 3600 where nome = 'Geladeira';

update PRODUTO set preco = 1000 where codigo_produto = 2;

update PRODUTO set preco = 570.90 where nome = 'Cama de Solteiro';

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
##### A)
select carrinho.qtd_produto , produtos.nome from produtos inner join carrinho on(carrinho.codigo_produto_fk = produtos.codigo_produto) inner join venda on(venda.codigo_venda = carrinho.codigo_produto_fk) inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) inner join entregador on(encomenda.codigo_entregador = entregador.codigo) inner join vendedores on(vendedores.codigo = venda.codigo_vendedor) inner join clientes on(clientes.codigo =vendedores.codigo) inner join pessoa on(pessoa.codigo =clientes.codigo) order by carrinho.qtd_produto asc;<br>
![Imagem0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/a1caaf3af93d22c8c02567d219581ddff8418a51/images/9.1(00).png)

select venda.data_venda , entregador.nome from produtos inner join carrinho on(carrinho.codigo_produto_fk = produtos.codigo_produto) inner join venda on(venda.codigo_venda = carrinho.codigo_produto_fk) inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) inner join entregador on(encomenda.codigo_entregador = entregador.codigo) inner join vendedores on(vendedores.codigo = venda.codigo_vendedor) inner join clientes on(clientes.codigo =vendedores.codigo) inner join pessoa on(pessoa.codigo =clientes.codigo) order by venda.data_venda asc;<br>
![Imagem1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/a1caaf3af93d22c8c02567d219581ddff8418a51/images/9.1(1).png)

select pessoa.rg as rg_pessoa , encomenda.destino from produtos inner join carrinho on(carrinho.codigo_produto_fk = produtos.codigo_produto) inner join venda on(venda.codigo_venda = carrinho.codigo_produto_fk) inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) inner join entregador on(encomenda.codigo_entregador = entregador.codigo) inner join vendedores on(vendedores.codigo = venda.codigo_vendedor) inner join clientes on(clientes.codigo =vendedores.codigo) inner join pessoa on(pessoa.codigo =clientes.codigo) order by pessoa.rg asc;<br>
![Imagem2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/a1caaf3af93d22c8c02567d219581ddff8418a51/images/9.1(2).png)

##### B)
select venda.data_venda, encomenda.destino  from venda inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) order by data_venda desc;<br>
![Imagem3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/a1caaf3af93d22c8c02567d219581ddff8418a51/images/9.1(3).png)

select venda.codigo_vendedor, vendedores.nome  from venda inner join vendedores on(venda.codigo_vendedor = vendedores.codigo) order by codigo_vendedor;<br>
![Imagem4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/a1caaf3af93d22c8c02567d219581ddff8418a51/images/9.1(4).png)

select carrinho.qtd_produto, produtos.nome  from carrinho inner join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) order by qtd_produto;<br>
![Imagem5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/abbbf46d23a6cd64139a2cd8805f87416b2dd37d/images/9.1(5).png)

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção
    
select carrinho.qtd_produto,produtos.nome,count(*) from carrinho inner join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by carrinho.qtd_produto,produtos.nome order by qtd_produto asc;<br>
![2IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28470e7af24d2398272fea943e56b7bd124670e0/images/9.7.0.png)

select venda.codigo_vendedor, vendedores.nome, count(*) from venda inner join vendedores on(venda.codigo_vendedor = vendedores.codigo)  group by venda.codigo_vendedor, vendedores.nome order by codigo_vendedor asc;<br>
![2IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28470e7af24d2398272fea943e56b7bd124670e0/images/9.7.1.png)

select venda.data_venda, encomenda.codigo_entregador, count(*) from venda inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) group by venda.data_venda, encomenda.codigo_entregador order by data_venda desc;<br>
![2IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28470e7af24d2398272fea943e56b7bd124670e0/images/9.7.2.png)

select venda.codigo_vendedor , encomenda.codigo_rastreamento , count(*) from venda inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) group by venda.codigo_vendedor, encomenda.codigo_rastreamento order by codigo_vendedor desc;<br>
![2IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28470e7af24d2398272fea943e56b7bd124670e0/images/9.7.3.png)

select carrinho.codigo_produto_fk ,produtos.preco,count(*) from carrinho inner join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by carrinho.codigo_produto_fk,produtos.preco order by codigo_produto_fk asc;<br>
![2IMAGEM4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28470e7af24d2398272fea943e56b7bd124670e0/images/9.7.4.png)

select carrinho.qtd_produto , produtos.nome,count(*) from produtos inner join carrinho on(carrinho.codigo_produto_fk = produtos.codigo_produto) inner join venda on(venda.codigo_venda = carrinho.codigo_produto_fk) inner join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) inner join entregador on(encomenda.codigo_entregador = entregador.codigo) inner join vendedores on(vendedores.codigo = venda.codigo_vendedor) inner join clientes on(clientes.codigo =vendedores.codigo) inner join pessoa on(pessoa.codigo =clientes.codigo) group by carrinho.qtd_produto , produtos.nome order by carrinho.qtd_produto asc;<br>
![2IMAGEM5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28470e7af24d2398272fea943e56b7bd124670e0/images/9.7.5.png)


#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

select carrinho.qtd_produto,produtos.nome,count(*) from carrinho left outer join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by carrinho.qtd_produto,produtos.nome order by qtd_produto asc;<br>
![3IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28c9bbd0c9309a79fdfc4d39ccbf7d3f7d3c8bd6/images/9.8.0.png)

select carrinho.qtd_produto,produtos.nome,count(*) from carrinho right outer join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) group by carrinho.qtd_produto,produtos.nome order by qtd_produto asc;<br>
![3IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28c9bbd0c9309a79fdfc4d39ccbf7d3f7d3c8bd6/images/9.8.1.png)

select venda.codigo_vendedor, vendedores.nome, count(*) from venda right outer join vendedores on(venda.codigo_vendedor = vendedores.codigo)  group by venda.codigo_vendedor, vendedores.nome order by codigo_vendedor asc;<br>
![3IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28c9bbd0c9309a79fdfc4d39ccbf7d3f7d3c8bd6/images/9.8.2.png)

select venda.data_venda, encomenda.codigo_entregador, count(*) from venda full outer join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) group by venda.data_venda, encomenda.codigo_entregador order by data_venda desc;<br>
![3IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/28c9bbd0c9309a79fdfc4d39ccbf7d3f7d3c8bd6/images/9.8.3.png)

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
##### A)
create view v1_datavenda1_e_v2codigovenda2 as select v1.data_venda as data_venda1, v2.codigo_venda as codigo_venda2, count(*) from venda as v1 inner join venda as v2 on(v1.codigo_venda = v2.codigo_vendedor) group by v1.data_venda, v2.codigo_venda;
select * from v1_datavenda1_e_v2codigovenda2;<br>
![4IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/17db39a0f891600ee116e463da7c61b325b490da/images/9.9.0.png)

create view carrinho1_e_carrinho2 as select c1.qtd_produto as carrinho1_qtd_produto, c2.codigo_produto_fk as c2_codigo_produto_fk, count(*) from carrinho as c1 inner join carrinho as c2 on(c1.qtd_produto = c2.codigo_produto_fk) group by c1.qtd_produto , c2.codigo_produto_fk ;
select * from v1_datavenda1_e_v2codigovenda2;<br>
![4IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/17db39a0f891600ee116e463da7c61b325b490da/images/9.9.1.png)

create view v1_codigovenda1_e_v2_codigocliente2 as select v1.codigo_venda as codigo_venda1, v2.codigo_cliente as codigo_cliente2, count(*) from venda as v1 inner join venda as v2 on(v1.codigo_venda = v2.codigo_vendedor) group by codigo_venda1, codigo_cliente2;
select * from v1_datavenda1_e_v2codigovenda2;<br>
![4IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/17db39a0f891600ee116e463da7c61b325b490da/images/9.9.2.png)

##### B)
create view v1_codigovendedor1_e_v2_codigocliente2 as select v1.codigo_vendedor as codigo_vendedor1, v2.codigo_cliente as codigo_cliente2, count(*) from venda as v1 inner join venda as v2 on(v1.codigo_vendedor = v2.codigo_cliente) group by codigo_vendedor1, codigo_cliente2;
select * from v1_codigovendedor1_e_v2_codigocliente2;<br>
![4IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/17db39a0f891600ee116e463da7c61b325b490da/images/9.9.3.png)

create view vend1_e_vend2 as
select v1.nome as nome_vendedor1, v2.email as email_vendedor2, count(*) from vendedores as v1 inner join vendedores as v2 on(v1.nome = v2.email) group by v1.nome, v2.email;
select * from vend1_e_vend2;<br>
(Na seleção não aparece nada pois ná ha elementos que se autorreferem)<br>
![4IMAGEM4](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/17db39a0f891600ee116e463da7c61b325b490da/images/9.9.4.png)

create view a1_codigorastreamento1_e_v2_codigoentregador2 as select a1.codigo_rastreamento as codigo_rastreamento1, a2.codigo_entregador as codigo_entregador2, count(*) 
from encomenda as a1 inner join encomenda as a2 on(a1.codigo_rastreamento = a2.codigo_entregador) group by codigo_rastreamento1, codigo_entregador2;
select * from a1_codigorastreamento1_e_v2_codigoentregador2;<br>
(Na seleção não aparece nada pois ná ha elementos que se autorreferem)<br>
![4IMAGEM5](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/17db39a0f891600ee116e463da7c61b325b490da/images/9.9.5.png)

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção
##### A)
select carrinho.qtd_produto,produtos.nome,count(*) from carrinho left outer join produtos on(carrinho.codigo_produto_fk = produtos.codigo_produto) where carrinho.qtd_produto in (select carrinho.qtd_produto from carrinho where produtos.codigo_produto < 5) group by carrinho.qtd_produto,produtos.nome order by qtd_produto asc;<br>
![5IMAGEM0](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/26c74ba9af275ec9d33f40946d9c31422ddf563e/images/9.10.0.png)

select venda.codigo_vendedor, vendedores.nome, count(*) 
from venda right outer join vendedores on(venda.codigo_vendedor = vendedores.codigo)  
where venda.codigo_vendedor in (select venda.codigo_vendedor from venda where vendedores.codigo > 4)
group by venda.codigo_vendedor, vendedores.nome order by codigo_vendedor asc;<br>
![5IMAGEM1](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/26c74ba9af275ec9d33f40946d9c31422ddf563e/images/9.10.1.png)

##### B)
select venda.codigo_vendedor, vendedores.nome, count(*) 
from venda inner join vendedores on(venda.codigo_vendedor = vendedores.codigo)
where venda.codigo_vendedor in (select venda.codigo_vendedor from venda where vendedores.codigo < 7)
group by venda.codigo_vendedor, vendedores.nome order by codigo_vendedor asc;<br>
![5IMAGEM2](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/26c74ba9af275ec9d33f40946d9c31422ddf563e/images/9.10.2.png)

select venda.data_venda, encomenda.codigo_entregador, count(*) 
from venda full outer join encomenda on(venda.codigo_venda = encomenda.codigo_entregador) 
where venda.data_venda in (select venda.data_venda from venda where encomenda.codigo_entregador > 1)
group by venda.data_venda, encomenda.codigo_entregador order by data_venda desc;<br>
![5IMAGEM3](https://github.com/ManoelRL/Template_Trab_BD1_2020/blob/26c74ba9af275ec9d33f40946d9c31422ddf563e/images/9.10.3.png)

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


