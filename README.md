📚 Exercícios SQL - DIO

Este repositório contém exercícios práticos de SQL realizados durante o curso da DIO.

---

📌 Exercícios

1 - Buscar o nome e ano dos filmes

SELECT Nome, Ano
FROM Filmes;

"Exercício 1" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex1.png)

---

2 - Buscar o nome e ano dos filmes ordenados por ano

SELECT Nome, Ano, Duracao
FROM Filmes
ORDER BY Ano;

"Exercício 2" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex2.png)

---

3 - Buscar o filme "De Volta Para o Futuro"

SELECT Nome, Ano, Duracao
FROM Filmes
WHERE Nome = 'De Volta Para o Futuro';

"Exercício 3" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex3.png)

---

4 - Filmes lançados em 1997

SELECT *
FROM Filmes
WHERE Ano = 1997;

"Exercício 4" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex4.png)

---

5 - Filmes após o ano 2000

SELECT *
FROM Filmes
WHERE Ano > 2000;

"Exercício 5" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex5.png)

---

6 - Filmes com duração entre 100 e 150

SELECT *
FROM Filmes
WHERE Duracao > 100 AND Duracao < 150
ORDER BY Duracao;

"Exercício 6" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex6.png)

---

7 - Quantidade de filmes por ano

SELECT Ano, COUNT(Ano) AS Quantidade
FROM Filmes
GROUP BY Ano
ORDER BY Quantidade DESC;

"Exercício 7" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex7.png)

---

8 - Atores do gênero masculino

SELECT PrimeiroNome, UltimoNome
FROM Atores
WHERE Genero = 'M';

"Exercício 8" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex8.png)

---

9 - Atores do gênero feminino

SELECT PrimeiroNome, UltimoNome
FROM Atores
WHERE Genero = 'F'
ORDER BY PrimeiroNome;

"Exercício 9" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex9.png)

---

10 - Nome do filme e gênero

SELECT f.Nome, g.Genero
FROM Filmes f
INNER JOIN FilmesGenero fg ON f.Id = fg.IdFilme
INNER JOIN Generos g ON fg.IdGenero = g.Id;

"Exercício 10" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex10.png)

---

11 - Filmes do gênero Mistério

SELECT f.Nome, g.Genero
FROM Filmes f
INNER JOIN FilmesGenero fg ON f.Id = fg.IdFilme
INNER JOIN Generos g ON fg.IdGenero = g.Id
WHERE g.Genero = 'Mistério';

"Exercício 11" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex11.png)

---

12 - Filmes e seus atores

SELECT f.Nome,
       a.PrimeiroNome,
       a.UltimoNome,
       ef.Papel
FROM Filmes f
INNER JOIN ElencoFilme ef ON f.Id = ef.IdFilme
INNER JOIN Atores a ON ef.IdAtor = a.Id;

"Exercício 12" (https://raw.githubusercontent.com/rubia-brito/banco-de-dados-dio/main/prints/printsex12.png)

---

🎯 Objetivo

Praticar consultas SQL e compreender o relacionamento entre múltiplas tabelas.
