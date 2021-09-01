# BancoGangster
* --
* ---- Parceiros
* CREATE TABLE parceiros (
*  id_parceiros INT(10) NOT NULL AUTO_INCREMENT,
*  nome VARCHAR(255) NOT NULL,
*  codigo VARCHAR(50) NOT NULL,
*  cpf_cnpj VARCHAR(255) NULL DEFAULT NULL,
*  email VARCHAR(255) NULL DEFAULT NULL,
*  PRIMARY KEY (id_parceiros)
* );
* ---- Funcionarios
* CREATE TABLE funcionarios (
*  id_funcionarios INT(10) NOT NULL AUTO_INCREMENT,
*  salario DECIMAL(10,2) NULL DEFAULT NULL,
*  cargo VARCHAR(255) NULL DEFAULT NULL,
*  sexo VARCHAR(50) NULL DEFAULT NULL,
*  id_parceiros INT(10),
*  PRIMARY KEY (id_funcionarios),
*  FOREIGN KEY (id_parceiros) REFERENCES parceiros(id_parceiros)
* );
* ---- Usuarios
* CREATE TABLE usuarios (
*  id_usuarios INT(10) NOT NULL AUTO_INCREMENT,
*  nome_de_usuario VARCHAR(50) NOT NULL,
*  senha VARCHAR(255) NOT NULL,
*  id_parceiros INT(10),
*  PRIMARY KEY (id_usuarios),
*  FOREIGN KEY (id_parceiros) REFERENCES parceiros(id_parceiros)
* );
* ---- Motoristas
* ---- TipoDeParceiro
* ---- Grupos
* --
* ---- Veiculos
* ---- CategoriaDoVeiculo
* ---- TipoDeVeiculo
* --
* ---- FormaDePagamento
* ---- Tickets
* --
* ---- Estacionamento
* ---- Vagas
* ---- TipoDeVaga
* --
