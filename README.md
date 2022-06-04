# Turmas_Resilia
Projeto com aprofundamento no MySQL com a temática de um banco de dado dos alunos da resília

CREATE DATABASE projeto_mod3

CREATE TABLE Facilitadores (
  ID INT PRIMARY KEY,
  id_do_facilitador INT,
  nome_do_facilitador TEXT
);


CREATE TABLE Cursos (
  id_do_cursos INT PRIMARY KEY,
  nome_do_cursos VARCHAR(100),
  id_do_facilitador INT,
  turmas_cursando_a_materia INT
);


CREATE TABLE Alunos (
  CPF_do_aluno INT PRIMARY KEY,
  nome_do_aluno VARCHAR(100),
  idade_do_aluno INT,
  id_da_turma INT,
  taxa_de_aprovacao INT
);


CREATE TABLE Turmas (
  id_da_turma INT PRIMARY KEY,
  id_do_facilitador INT,
  data_de_formacao INT,
  CPF_do_aluno INT(11)
);


CREATE TABLE Aprovacao_na_materia (
  ID INT PRIMARY KEY,
  CPF_aluno INT(11),
  taxa_de_aprovacao INT,
  modulo INT(10)
);


CREATE TABLE Entregas (
   ID INT PRIMARY KEY,
   id_do_alunos INT,
  modulo_do_projeto VARCHAR(100),
  conceito_do_projeto VARCHAR(100),
  links_do_repositorio TEXT
);

CREATE TABLE cadastro_do_aluno (
  ID INT PRIMARY KEY,
  CPF_do_aluno INT(11),
  emails TEXT
);
