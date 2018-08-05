Enter password: ************
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 17
Server version: 8.0.12 MySQL Community Server - GPL

Copyright (c) 2000, 2018, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> use MonitoringMyParkinsons
Database changed
mysql> create table Usuario(
    -> ID int PRIMARY KEY AUTO_INCREMENT,
    -> Nome varchar(30) NOT NULL,
    -> Email varchar(50) NOT NULL UNIQUE,
    ->
    -> CPF varchar(11) NOT NULL UNIQUE,
    -> Numero_pulseira int(32) UNIQUE,
    -> Medico int(32) NOT NULL
    -> );
Query OK, 0 rows affected (1.00 sec)

mysql> create table Enderecos(
    -> Id_Endereco int PRIMARY KEY AUTO_INCREMENT,
    -> Logradouro varchar(30) NOT NULL,
    -> Numero varchar(5) NOT NULL,
    -> CEP varchar(8) NOT NULL,
    -> Cidade varchar(30) NOT NULL,
    -> Estado char(2) NOT NULL
    -> );
Query OK, 0 rows affected (0.66 sec)

mysql> create table Telefone(
    -> ID_Telefone int PRIMARY KEY AUTO_INCREMENT,
    -> Numero varchar(10)
    -> );
Query OK, 0 rows affected (0.42 sec)

mysql> create table Nascimento(
    -> ID_Nascimento int PRIMARY KEY AUTO_INCREMENT,
    -> Data_de_Nascimento varchar(10) NOT NULL
    -> );
Query OK, 0 rows affected (0.50 sec)

mysql> create table Sexo(
    -> ID_Sexo int PRIMARY KEY AUTO_INCREMENT,
    -> SEXO ENUM ('F','M') NOT NULL
    -> );
Query OK, 0 rows affected (0.48 sec)

mysql> create table Medico(
    -> Id_Medico int PRIMARY KEY AUTO_INCREMENT,
    -> Nome varchar(30) NOT NULL,
    -> Email varchar(50) NOT NULL UNIQUE
    -> );
Query OK, 0 rows affected (0.55 sec)

mysql> create table Pulseira(
    -> ID_Dados int PRIMARY KEY AUTO_INCREMENT,
    -> Numero_Pulseira int(32) UNIQUE,
    -> Numero_Passos varchar(10) NOT NULL,
    -> Frequencia varchar(5) NOT NULL
    -> );
Query OK, 0 rows affected (0.54 sec)

mysql> create table Analise(
    -> Data varchar(10) NOT NULL,
    -> Hora varchar(5) NOT NULL,
    -> Intensidade varchar(3) NOT NULL
    -> );
Query OK, 0 rows affected (0.47 sec)

mysql> insert into Usuario values(01, 'Carlos Fernando Nóbrega', 'carlos.nobrega@gmail.com, 05016978620, 500, 21);
    '> insert into Usuario values(02, 'Francisca Azevedo Lira', 'franciscaazevedo_01@hotmail.com', 70083911150, 501,22);
    '> insert into Usuario values(03, 'Carla Bruna Pereira', 'pereirabruna10@gmail.com', 80093051131, 502, 22);
    '> insert into Usuario values(04, 'Teresa Cristina Santos', 'teresa123@gmail.com', 23067798515, 503,23);
    '> insert into Usuario values(05, 'Pablo Rodolfo Vargas', 'pablovargas@hotmail.com', 17042235690, 504, 24);
    '> insert into Usuario values(06, 'Anderson Freitas Carvalho', 'carvalhofreitas@gmail.com', 18076503573, 505, 25);
    '> insert into Usuario values(07, 'José Farias Teixeira', 'jose.farias@yahoo.com.br', 45032187615, 506, 26);

    '> insert into Enderecos values(01, 'Rua Juscelino Chagas', 530, 56320123, 'Rio de Janeiro', 'RJ');
    '> insert into Usuario values(02, 'Av. Rui Carneiro', 412, 58631244, 'João Pessoa', 'PB');
    '> insert into Usuario values(03, 'Rua Coronel Américo Porto', 150, 58431381, 'Campina Grande, 'PB');
    '> insert into Usuario values(04, 'Rua José Américo Franco', 230, 58411114, 'Boa Vista', 'RR');
    '> insert into Usuario values(05, 'Av. Emanuel Alves de Oliveira', 687, 59781321, 'Natal', 'RN');
    '> insert into Usuario values(06, 'Rua Benedito Rui Barbosa', 725, 54245338, 'Gramado', 'RS');
    '> insert into Usuario values(07, 'Rua Nossa Senhora da Conceição', 913, 56320123, 'Uberlândia', 'MG');

    '> insert into Enderecos values(01, 2130559311);
    '> insert into Enderecos values(02, 83996873211);
    '> insert into Enderecos values(03, 83999457865);
    '> insert into Enderecos values(04, 953332-7889);
    '> insert into Enderecos values(05, 84999392111);
    '> insert into Enderecos values(06, 54998766543);
    '> insert into Enderecos values(07, 34987541433);

    '> insert into Nascimento values(01,30/10/1987);
    '> insert into Nascimento values(02,14/06/1990);
    '> insert into Nascimento values(03,21/05/1979);
    '> insert into Nascimento values(04,03/07/1992);
    '> insert into Nascimento values(05,19/08/1982);
    '> insert into Nascimento values(06,27/11/1971);
    '> insert into Nascimento values(07,09/02/1961);

    '> insert into Sexo values(01, 'M');
    '> insert into Sexo values(02, 'F');
    '> insert into Sexo values(03, 'F');
    '> insert into Sexo values(04, 'F');
    '> insert into Sexo values(05, 'M');
    '> insert into Sexo values(06, 'M');
    '> insert into Sexo values(07, 'M');

    '> insert into Medico values(21, 'Dr.Robson Fernandes Carvalho', 'drrobsonfernandes@gmail.com');
    '> insert into Medico values(22, 'Dr.Patrícia Nóbrega Pires', 'drpatriciapires@gmail.com');
    '> insert into Medico values(23, 'Dr.Antônio da Silva Costa', 'drantoniocosta@gmail.com');
    '> insert into Medico values(24, 'Dr.Eva Castro Cordeiro', 'drevacordeiro@gmail.com');
    '> insert into Medico values(25, 'Dr.Pedro Olímpio de Sousa', 'drpedroolimposousa@gmail.com');
    '> insert into Medico values(26, 'Dr.José Clementino Paiva', 'drjoseclementinopaiva@gmail.com');

    '> insert into Pulseira values(31, 500, 4538, 57);
    '> insert into Pulseira values(32, 501, 3467, 60);
    '> insert into Pulseira values(33, 502, 1953, 70);
    '> insert into Pulseira values(34, 503, 2955, 63);
    '> insert into Pulseira values(35, 504, 1521, 80);
    '> insert into Pulseira values(36, 505, 4431, 55);

    '> insert into Analise values(31, 15/06/2018, 13:20, 30);
    '> insert into Analise values(31, 15/06/2018, 13:21, 32);
    '> insert into Analise values(31, 15/06/2018, 13:22, 30);
    '> insert into Analise values(31, 15/06/2018, 13:23, 31);
    '> insert into Analise values(32, 10/05/2018, 01:17, 46);
    '> insert into Analise values(32, 10/05/2018, 01:18, 44);
    '> insert into Analise values(32, 10/05/2018, 01:19, 45);
    '> insert into Analise values(32, 10/05/2018, 01:20, 43);
    '> insert into Analise values(33, 23/03/2018, 11:43, 24);
    '> insert into Analise values(33, 23/03/2018, 11:44, 25);
    '> insert into Analise values(33, 23/03/2018, 11:45, 23);
    '> insert into Analise values(33, 23/03/2018, 11:46, 20);
    '> insert into Analise values(34, 30/07/2018, 14:11, 33);
    '> insert into Analise values(34, 30/07/2018, 14:12, 30);
    '> insert into Analise values(34, 30/07/2018, 14:13, 35);
    '> insert into Analise values(34, 30/07/2018, 14:14, 33);
    '> insert into Analise values(35, 27/02/2018, 22:56, 51);
    '> insert into Analise values(35, 27/02/2018, 22:57, 55);
    '> insert into Analise values(35, 27/02/2018, 22:58, 53);
    '> insert into Analise values(35, 27/02/2018, 22:59, 51);
    '> insert into Analise values(36, 05/08/2018, 09:34, 27);
    '> insert into Analise values(36, 05/08/2018, 09:35, 29);
    '> insert into Analise values(36, 05/08/2018, 09:36, 30);
    '> insert into Analise values(36, 05/08/2018, 09:37, 26);


