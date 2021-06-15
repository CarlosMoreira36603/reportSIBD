# C3 : SQL

## DDL

_(Apresentar o SQL para criação do esquema definido acima num SGBD MySQL.)_


```sql
USE `test`;

profissionaisprofissionaisCREATE TABLE `clientes` (
  `Nome` varchar(100) NOT NULL,
  `Morada` varchar(150) NOT NULL,
  `NIF` int(9) NOT NULL,
  `Email` varchar(100) NOT NULL,
  `Numero` int(9) NOT NULL,
  PRIMARY KEY (`NIF`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

CREATE TABLE `profissionais` (
  `id_Profissionais` int(11) NOT NULL AUTO_INCREMENT,
  `Nome` varchar(100) NOT NULL,
  `Contacto` int(9) NOT NULL,
  PRIMARY KEY (`id_Profissionais`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

CREATE TABLE `servicos` (
  `id_servicos` int(11) NOT NULL AUTO_INCREMENT,
  `servicos_nome` varchar(45) NOT NULL,
  `servicos_preco` double NOT NULL,
  PRIMARY KEY (`id_servicos`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1

CREATE TABLE `marcacoes` (
  `id_marcacoes` int(11) NOT NULL,
  `cliente_nif` int(11) NOT NULL,
  `id_servicos` int(11) NOT NULL,
  `id_profissional` int(11) NOT NULL,
  `dia` date NOT NULL,
  `hora` time NOT NULL,
  `estado` varchar(45) NOT NULL,
  PRIMARY KEY (`id_marcacoes`),
  KEY `cliente_nif` (`cliente_nif`),
  KEY `id_servicos` (`id_servicos`),
  KEY `id_profissional` (`id_profissional`),
  CONSTRAINT `marcacoes_ibfk_1` FOREIGN KEY (`cliente_nif`) REFERENCES `clientes` (`NIF`),
  CONSTRAINT `marcacoes_ibfk_2` FOREIGN KEY (`id_servicos`) REFERENCES `servicos` (`id_servicos`),
  CONSTRAINT `marcacoes_ibfk_3` FOREIGN KEY (`id_profissional`) REFERENCES `profissionais` (`id_Profissionais`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

```
## DML
Algumas das interrogações à Base de Dados
Quantos clientes tem?
SELECT COUNT(Id_Nome)
FROM table_clientes;

Quantos profissionais é que tem?
SELECT COUNT (Id_profissional)
FROM table_profissionais;



---
[< Previous](rebd04.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | Next >
:--- | :---: | ---: 
