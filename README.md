# 🎬 Grafo de Conhecimento - Filmes e Séries
**Este projeto apresenta um modelo conceitual de grafo desenvolvido no Neo4j, representando relações entre pessoas, filmes, séries, gêneros, atores e diretores.
O objetivo é demonstrar como construir e visualizar conexões semânticas entre entidades do domínio de entretenimento.**

## 🧩 Estrutura do Grafo

- Entidades ( Nós)

- Tipo de Nó	Descrição

- Pessoa	Representa um usuário ou espectador.

- Filmes	Representa obras cinematográficas.

- Séries	Representa séries de TV ou streaming.

- Gênero	Categoria do conteúdo (Ex: Ação, Drama, Comédia).

- Ator	Pessoa que atua em filmes ou séries.

- Diretor	Profissional responsável pela direção da obra.



## 💾 Criação do Grafo (Cypher)

**CREATE:** 
 - (p:Pessoa {nome: 'Usuário Exemplo'}),
 - (m1:Filmes {titulo: 'Filme Exemplo'}),
 - (s1:Series {titulo: 'Série Exemplo'}),
 - (g1:Genero {nome: 'Ação'}),
 - (a2:Ator {nome: 'Ator Exemplo'}),
 - (d1:Diretor {nome: 'Diretor Exemplo'}),

**Relationship:** 
  - (p)-[:ASSISTIU]->(m1),
  - (p)-[:ASSISTIU]->(s1),
  - (a2)-[:ATUOU]->(m1),
 - (a2)-[:ATUOU]->(s1),
 - (d1)-[:DIRIGIU]->(m1),
 - (d1)-[:DIRIGIU]->(s1),
 - (m1)-[:GENERO]->(g1),
 - (s1)-[:GENERO]->(g1);

## 🔗 Relacionamentos

Relacionamento	Direção	Descrição

- (:Pessoa)-[:ASSISTIU]->(:Filmes)	Pessoa → Filmes	Pessoa assistiu determinado filme.
- (:Pessoa)-[:ASSISTIU]->(:Series)	Pessoa → Series	Pessoa assistiu determinada série.
- (:Ator)-[:ATUOU]->(:Filmes)	Ator → Filmes	O ator participou de um filme.
- (:Ator)-[:ATUOU]->(:Series)	Ator → Series	O ator participou de uma série.
- (:Diretor)-[:DIRIGIU]->(:Filmes)	Diretor → Filmes	Diretor responsável por um filme.
- (:Diretor)-[:DIRIGIU]->(:Series)	Diretor → Series	Diretor responsável por uma série.
- (:Filmes)-[:GENERO]->(:Genero)	Filmes → Gênero	Filme pertence a determinado gênero.
- (:Series)-[:GENERO]->(:Genero)	Séries → Gênero	Série pertence a determinado gênero.

## 🧠 Objetivo do Modelo

- Analisar o comportamento de usuários (o que assistem e preferências de gênero).
- Explorar colaborações entre atores e diretores.
- Descobrir relações indiretas (ex: usuários que assistiram produções com o mesmo ator).

## 📊 Visualização
- O modelo pode ser visualizado no Neo4j Browser ou Neo4j Bloom, permitindo explorar conexões de forma intuitiva:

![Uploading visualisation (1).png…]()


## 🚀 Tecnologias Utilizadas
- Neo4j Desktop / AuraDB
- Linguagem Cypher
- Graph Data Modeling

## 🤝 Contribuições
Contribuições são bem-vindas!

Se este projeto te ajudou, não esqueça de deixar uma ⭐ no repositório.

**Você pode:**

- Abrir issues com sugestões de melhorias 📝

- Enviar pull requests com novas funcionalidades 💡

- Compartilhar com outros devs interessados em aprender Modelagem com Neo4J🚀

## 📬 Autor
👨‍💻 Deryck Silva

Desenvolvedor Java | Estudante de Ciência de Dados

🌐 GitHub: (https://github.com/NEO4J)
