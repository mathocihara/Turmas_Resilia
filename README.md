# Turmas_Resilia
Projeto com aprofundamento no MySQL com a temática de um banco de dado dos alunos da resília

CREATE DATABASE projeto_mod3

CREATE TABLE Facilitadores (
  id_do_facilitador INT PRIMARY KEY,
  nome_do_facilitador TEXT
);


CREATE TABLE Cursos (
  id_do_cursos INT PRIMARY KEY,
  nome_do_cursos VARCHAR(100),
  facilitador_selecionado INT,
  turmas_cursando_a_materia INT
);


CREATE TABLE Alunos (
  CPF_do_aluno INT PRIMARY KEY,
  nome_do_aluno VARCHAR(100),
  idade_do_aluno INT,
  turma_inserida INT,
  taxa_de_aprovacao INT
);


CREATE TABLE Turmas (
  id_da_turma INT PRIMARY KEY,
  data_de_formacao INT,
  identificador_dos_alunos INT
);


CREATE TABLE Aprovacao_na_materia (
  id_do_resultado INT PRIMARY KEY,
  taxa_de_aprovacao INT
);


CREATE TABLE Entregas (
  id_do_alunos INT PRIMARY KEY,
  modulo_do_projeto VARCHAR(100),
  conceito_do_projeto VARCHAR(100),
  links_do_repositorio TEXT
);

CREATE TABLE cadastro_do_aluno (
  id_do_alunos INT PRIMARY KEY,
  emails TEXT
);
