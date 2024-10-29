# Documentação do projeto: Cadastro de Filmes

# 1 - Resumo do projeto
Cadastro de filmes é um sistema desenvolvido para um trabalho academico,
com o objetivo de gerenciar o cadastro de categorias de filmes e vincular filmes a essas categorias.
o projeto deve ser feita para uma aplicação web mas também mobile.

# 2 - Planejamento e Escopo
2.1 - Requisitos funcionais:
- CRUD de categoria de filmes.
- CRUD de filmes vinculados a uma categoria
- Interface web e uma mobile do sistema

2.2 - Requisitos Não Funcionais
- O sistema deve ter uma API para comunicação entre frontend e backend.
- O banco de dados deve ser estruturado de forma a permitir consultas eficientes.
- O sistema deve ser responsivo, permitindo o uso em diferentes dispositivos.

# 3 - Tecnologias utilizadas
Frontend : HTML, CSS, Vue.js
Frontmobile : XML 
Backend: Node.js ou Springboot
Banco de dados: MySQL
Ferramentas de desenvolvimento: Vscode, Git

# 4 - Modelo do banco de dados
Tabela Categoria: ID_Categoria, nome_categoria.
Tabela Filme: ID_fime, Nome_filme, Descricao, ID_categoria.
