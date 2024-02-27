# Projeto Biblioteca com Flask e SQLite

Este é um projeto simples de uma API de biblioteca que permite realizar operações CRUD (Criar, Ler, Atualizar, Deletar) em um banco de dados de livros utilizando Flask e SQLite.

## Configuração do Ambiente

Antes de iniciar, certifique-se de que você tem Python instalado em sua máquina. Este projeto foi desenvolvido utilizando Python 3.8.5, mas deve ser compatível com outras versões que suportam Flask.

### Clonar o Repositório

Primeiro, clone o repositório para a sua máquina local:

```bash
git clone https://seu-repositorio-aqui/projeto-biblioteca.git
cd projeto-biblioteca
```

Instalar Dependências
Crie um ambiente virtual e instale as dependências utilizando pip:

```bash
python -m venv venv
venv\Scripts\activate  # No Windows
source venv/bin/activate  # No Linux ou macOS
pip install Flask Flask-SQLAlchemy
```

Inicializar a Aplicação
Para iniciar a aplicação, execute:

```bash
python app.py
```
A aplicação estará rodando no endereço http://127.0.0.1:5000/.

## Estrutura do Banco de Dados

O banco de dados consiste em uma única tabela chamada `Livro`, com as seguintes colunas:

- `id`: ID único do livro (chave primária).
- `titulo`: Título do livro.
- `autor`: Autor do livro.

## Testando a API com Postman

A seguir, exemplos de como testar as operações CRUD utilizando o Postman.

### Adicionar um Novo Livro

- **URL**: `http://127.0.0.1:5000/livro`
- **Método**: `POST`
- **Body** (raw, JSON):
  ```json
  {
    "titulo": "Nome do Livro",
    "autor": "Autor do Livro"
  }


## Operações da API

### Listar Todos os Livros

- **URL**: `http://127.0.0.1:5000/livros`
- **Método**: `GET`

Esta operação lista todos os livros disponíveis no banco de dados.

### Obter Detalhes de um Livro

- **URL**: `http://127.0.0.1:5000/livro/<id>`
- **Método**: `GET`
- **URL Params**: Substitua `<id>` pelo ID do livro para obter seus detalhes completos.

Esta requisição retorna os detalhes de um livro específico, incluindo título e autor.

### Atualizar um Livro

- **URL**: `http://127.0.0.1:5000/livro/<id>`
- **Método**: `PUT`
- **URL Params**: Substitua `<id>` pelo ID do livro que deseja atualizar.
- **Body** (raw, JSON):
  ```json
  {
    "titulo": "Novo Nome do Livro",
    "autor": "Novo Autor do Livro"
  }

### Atualizar um Livro

Esta operação permite a atualização dos detalhes de um livro específico no banco de dados. Certifique-se de fornecer as informações atualizadas no corpo da requisição.

### Deletar um Livro

- **URL**: `http://127.0.0.1:5000/livro/<id>`
- **Método**: `DELETE`
- **URL Params**: Substitua `<id>` pelo ID do livro que deseja deletar.

Esta operação remove um livro do banco de dados de forma permanente. **Atenção**: Esta ação é irreversível.

## Conclusão

Este guia oferece uma visão detalhada de como configurar, inicializar e testar o Projeto Biblioteca utilizando a combinação de Flask e SQLite. Ele visa facilitar o entendimento e a execução das operações CRUD, essenciais para a gestão da biblioteca virtual.

Para maiores informações e suporte técnico, é recomendável consultar a documentação oficial do [Flask](https://flask.palletsprojects.com/) e do [SQLite](https://www.sqlite.org/docs.html). Estes recursos oferecem um vasto material sobre configurações avançadas, otimizações e melhores práticas para desenvolvimento de aplicações robustas e eficientes.
