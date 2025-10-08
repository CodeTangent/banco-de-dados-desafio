# Sistema de Banco de Dados de Filmes

## Visão Geral
O sistema permite realizar consultas SQL em um banco de dados de filmes, atores e gêneros, extraindo informações relevantes para análises. Desenvolvido como parte de um desafio guiado da Trilha .NET da DIO, o projeto foca na prática de consultas, relacionamentos e manipulação de dados.

## Funcionalidades Principais
- Estruturação de banco de dados com tabelas para Filmes, Atores e Gêneros  
- Relacionamentos muitos-para-muitos entre filmes-atores e filmes-gêneros  
- Execução de 12 consultas SQL diferentes para retorno de dados específicos:  
  - Listagem de filmes por nome, ano e duração  
  - Filtros por ano e duração  
  - Contagem de filmes por ano  
  - Listagem de atores por gênero  
  - Relação de filmes com gêneros  
  - Associação de filmes com atores e papéis  

## Conceitos Aplicados
- Modelagem de banco de dados relacional  
- Consultas SQL com filtros, ordenações e agrupamentos  
- Relacionamentos muitos-para-muitos  
- Validação e integridade de dados  

## Preparando o Banco
- Executar o script **Script Filmes.sql** no SQL Server (localizado na pasta `Scripts`)  
- O script cria o banco **Filmes** com todas as tabelas e dados necessários para as consultas
