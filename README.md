# 🎬 Sistema de Banco de Dados de Filmes

## 🚀 Descrição

Projeto desenvolvido para modelar e consultar um banco de dados relacional de filmes, permitindo a extração de informações relevantes através de consultas SQL.

O sistema simula um cenário real de catálogo de filmes, com relacionamentos entre filmes, atores e gêneros.

---

## 🧠 Problema resolvido

Como estruturar e consultar dados relacionais de forma eficiente, permitindo análises como:

* Quais filmes foram lançados em determinado ano
* Quantidade de filmes por período
* Relação entre filmes, atores e gêneros
* Identificação de padrões nos dados

---

## 🛠 Tecnologias

* SQL Server
* T-SQL

---

## 🧱 Estrutura do Banco

* **Filmes** → informações gerais (nome, ano, duração)
* **Atores** → dados dos atores
* **Gêneros** → categorias dos filmes
* **FilmesGenero** → relacionamento muitos-para-muitos
* **ElencoFilme** → associação entre atores e filmes

---

## 💡 Exemplos de consultas

### 📊 Contagem de filmes por ano

```sql
SELECT Ano, COUNT(*) AS Quantidade
FROM Filmes
GROUP BY Ano
ORDER BY Quantidade DESC;
```

### 🎭 Relação entre filmes e gêneros

```sql
SELECT F.Nome AS Filme, G.Genero
FROM FilmesGenero FG
INNER JOIN Filmes F ON FG.IdFilme = F.Id
INNER JOIN Generos G ON FG.IdGenero = G.Id;
```

### 🎬 Associação de atores aos filmes

```sql
SELECT 
    F.Nome AS Filme,
    A.PrimeiroNome,
    A.UltimoNome,
    EF.Papel
FROM ElencoFilme EF
INNER JOIN Atores A ON EF.IdAtor = A.Id
INNER JOIN Filmes F ON EF.IdFilme = F.Id;
```

---

## ⚙️ Como executar

1. Executar o script `Script Filmes.sql` para criação do banco
2. Utilizar o arquivo `SQL_Resolvido.sql` para executar as consultas

---

## 🎯 Objetivo do projeto

Praticar modelagem de banco de dados relacional e construção de consultas SQL aplicadas a um cenário próximo ao real.

---

## 📈 Possíveis melhorias

* Criação de Views para consultas frequentes
* Implementação de Stored Procedures
* Integração com API em C# ou Python
* Criação de interface para consulta de dados

---
