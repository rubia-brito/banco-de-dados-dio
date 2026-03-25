📚 Exercícios SQL - DIO

Este repositório contém exercícios práticos de SQL realizados durante o curso da DIO, com foco em consultas, filtros, ordenação, agregações e relacionamento entre tabelas.

---

🧠 Conteúdos praticados

- SELECT
- WHERE
- ORDER BY
- GROUP BY
- INNER JOIN
- Relacionamentos entre tabelas

---

📌 Exercícios

1 - Buscar o nome e ano dos filmes

SELECT Nome, Ano
FROM Filmes;

📷 Resultado:
"Exercício 1" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex1.pn)

---

2 - Buscar o nome e ano dos filmes, ordenados por ordem crescente pelo ano

SELECT Nome, Ano, Duracao
FROM Filmes
ORDER BY Ano;

📷 Resultado:
"Exercício 2" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex2.png)

---

3 - Buscar o filme "De Volta para o Futuro", trazendo nome, ano e duração

SELECT Nome, Ano, Duracao
FROM Filmes
WHERE Nome = 'De Volta Para o Futuro';

📷 Resultado:
"Exercício 3" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex3.png)


---

4 - Buscar os filmes lançados em 1997

SELECT *
FROM Filmes
WHERE Ano = 1997;

📷 Resultado:
"Exercício 4" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex4.png)

---

5 - Buscar os filmes lançados após o ano 2000

SELECT *
FROM Filmes
WHERE Ano > 2000;

📷 Resultado:
"Exercício 5" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex5.png)

---

6 - Buscar os filmes com duração maior que 100 e menor que 150, ordenando pela duração

SELECT *
FROM Filmes
WHERE Duracao > 100 AND Duracao < 150
ORDER BY Duracao;

📷 Resultado:
"Exercício 6" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex6.png)

---

7 - Buscar a quantidade de filmes lançados por ano, ordenando pela quantidade em ordem decrescente

SELECT Ano, COUNT(Ano) AS Quantidade
FROM Filmes
GROUP BY Ano
ORDER BY Quantidade DESC;

📷 Resultado:
"Exercício 7" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex7.png)

---

8 - Buscar os atores do gênero masculino, retornando primeiro e último nome

SELECT PrimeiroNome, UltimoNome
FROM Atores
WHERE Genero = 'M';

📷 Resultado:
"Exercício 8" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex8.png)

---

9 - Buscar os atores do gênero feminino, retornando primeiro e último nome e ordenando pelo primeiro nome

SELECT PrimeiroNome, UltimoNome
FROM Atores
WHERE Genero = 'F'
ORDER BY PrimeiroNome;

📷 Resultado:
"Exercício 9" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex9.png)

---

10 - Buscar o nome do filme e seu gênero

SELECT f.Nome, g.Genero
FROM Filmes f
INNER JOIN FilmesGenero fg ON f.Id = fg.IdFilme
INNER JOIN Generos g ON fg.IdGenero = g.Id;

📷 Resultado:
"Exercício 10" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex10.png)

---

11 - Buscar o nome do filme e o gênero do tipo "Mistério"

SELECT f.Nome, g.Genero
FROM Filmes f
INNER JOIN FilmesGenero fg ON f.Id = fg.IdFilme
INNER JOIN Generos g ON fg.IdGenero = g.Id
WHERE g.Genero = 'Mistério';

📷 Resultado:
"Exercício 11" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex11.png)

---

12 - Buscar o nome do filme e os atores, trazendo primeiro nome, último nome e o papel

SELECT f.Nome,
       a.PrimeiroNome,
       a.UltimoNome,
       ef.Papel
FROM Filmes f
INNER JOIN ElencoFilme ef ON f.Id = ef.IdFilme
INNER JOIN Atores a ON ef.IdAtor = a.Id;

📷 Resultado:
"Exercício 12" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex12.png)

---

🎯 Objetivo

Praticar consultas SQL e compreender o relacionamento entre múltiplas tabelas, aplicando boas práticas na construção de consultas SQL.
