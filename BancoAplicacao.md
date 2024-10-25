# Banco de Dados Aplicação

```
Criacao do database
```
> create database galeria;

```
Selecao do database
```
> use galeria;

```
Criacao tabela Clientes
```
> create table Clientes(
> 	id_cliente TINYINT not null primary key,
> 	nome varchar(50) not null,
> 	email varchar(30) not null
> );

```
Criacao tabela Produtos
```
> create table Produtos(
> 	id_produto TINYINT not null primary key, 
> 	descricao varchar(30)
> );

```
Criacao tabela Vendas
```
> create table Vendas(
> 	id_venda TINYINT not null primary key, 
> 	observacao varchar(30),
> 	fk_id_cliente TINYINT not null,
> 	fk_id_produto TINYINT not null,
> 	FOREIGN KEY ( fk_id_produto ) REFERENCES Produtos(id_produto),
> 	FOREIGN KEY ( fk_id_cliente ) REFERENCES Clientes(id_cliente) 
> );
