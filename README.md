📚Sistema de Cadastro de Livros
Descrição

O Sistema de Cadastro de Livros é um aplicativo em Java 25 que permite gerenciar uma coleção de livros diretamente pelo terminal.
Ele suporta cadastro, listagem, busca, atualização e exclusão de livros, mantendo as informações organizadas em arquivos locais.

O sistema foi projetado para ser intuitivo para usuários brasileiros, mas o enum de gêneros também aceita entradas em inglês.

Funcionalidades

Cadastrar livro

Solicita ao usuário: título, autor, gênero e número de páginas.

Valida os dados antes de salvar.

Os livros são registrados no diretório local C:\BooksRegistred\ como arquivos .txt.

Listar livros

Exibe todos os livros cadastrados.

Mostra: Título, Autor, Gênero e Número de Páginas.

O gênero é exibido em português.

Buscar livro por título

Permite pesquisar livros por palavra-chave no título.

A busca não diferencia maiúsculas de minúsculas.

Se nenhum livro for encontrado, o sistema avisa: "Não encontrado!".

Atualizar livro

Permite alterar qualquer informação do livro: título, autor, gênero ou número de páginas.

O usuário pode apertar ENTER para manter o valor atual.

Suporta digitar o gênero em português ou inglês.

Deletar livro

Exibe todos os livros cadastrados com um número de referência.

O usuário escolhe qual livro deseja remover.

O arquivo correspondente é excluído do diretório local.

Sair

Encerra o sistema de forma segura.

Estrutura do Projeto
src/
 ├─ app/
 │   └─ Program.java        # Classe principal que inicia o menu
 ├─ ui/
 │   └─ Menu.java           # Classe do menu interativo
 ├─ services/
 │   └─ BookService.java    # Lógica de cadastro, listagem, busca, atualização e exclusão
 ├─ entities/
 │   └─ Book.java           # Classe modelo do livro
 ├─ enums/
 │   └─ BookGenre.java      # Enumeração de gêneros de livros (português/inglês)
 ├─ repository/
 │   └─ BookRepository.java # Gerencia a leitura/escrita de arquivos
 └─ exceptions/
     └─ BookException.java  # Tratamento de exceções específicas
Enumeração de Gêneros (BookGenre)

O sistema suporta os seguintes gêneros, em português e inglês:

Enum Java	Português	Inglês
FICTION	Ficção	Fiction
TERROR	Terror	Horror
ROMANCE	Romance	Romance
ADVENTURE	Aventura	Adventure

O usuário pode digitar qualquer um desses nomes em português ou inglês ao cadastrar ou atualizar livros.

Tecnologias Utilizadas

Java 25

Scanner para entrada de dados pelo terminal

Enum para representação de gêneros de livros

Arquivos de texto (.txt) para persistência local

Como Executar

Clone o projeto ou faça download do código.

Abra o projeto em uma IDE compatível com Java (IntelliJ IDEA, Eclipse, VSCode com extensão Java).

Compile todas as classes.

Execute a classe Program:

java app.Program

O menu será exibido no terminal. Escolha a opção desejada digitando o número correspondente e pressione ENTER.

Exemplo de Uso
===============================================
1 - Cadastrar livro
2 - Listar livros
3 - Buscar livro por título
4 - Deletar livro
5 - Sair
Escolha uma opção: 1

Informe o título: O Senhor dos Anéis
Informe o autor: J.R.R. Tolkien
Informe o gênero: Ficção
Informe a quantidade de páginas: 1178
LIVRO CADASTRADO!

===============================================
1 - Cadastrar livro
2 - Listar livros
3 - Buscar livro por título
4 - Deletar livro
5 - Sair
Escolha uma opção: 2

1 - Title: O Senhor dos Anéis - Author: J.R.R. Tolkien - Genre: Ficção - Pages: 1178
Observações

Certifique-se de que o diretório C:\BooksRegistred\ exista, ou o sistema poderá falhar ao tentar salvar/excluir livros.

As opções do menu devem ser digitadas como números inteiros. Entradas inválidas gerarão a mensagem "Opção inválida!".

O sistema não diferencia maiúsculas e minúsculas nas buscas por título ou ao digitar o gênero.

O método updateBook() permite manter valores atuais pressionando ENTER, e converte automaticamente gêneros digitados em português ou inglês para o enum interno.
