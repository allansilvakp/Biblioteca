📚 Sistema de Cadastro de Livros

Um aplicativo em Java 25 para gerenciar sua coleção de livros diretamente pelo terminal.
Permite cadastrar, listar, buscar, atualizar e deletar livros com facilidade e suporte a gêneros em português e inglês.

✨ Funcionalidades

📝 Cadastrar livro

Informe: título, autor, gênero e número de páginas

Validação automática dos dados

Armazena cada livro em arquivos .txt no diretório C:\BooksRegistred\

📋 Listar livros

Mostra todos os livros cadastrados

Exibe: Título, Autor, Gênero e Páginas

🔍 Buscar livro por título

Pesquisa por palavra-chave (não diferencia maiúsculas de minúsculas)

Retorna todos os livros correspondentes ou "Não encontrado!"

✏️ Atualizar livro

Permite alterar título, autor, gênero e páginas

Pressione ENTER para manter o valor atual

Aceita o gênero em português ou inglês

🗑️ Deletar livro

Exibe todos os livros com números de referência

Escolha qual livro remover

O arquivo correspondente é excluído

🚪 Sair

Encerra o sistema de forma segura

🏗 Estrutura do Projeto
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
 │   └─ BookGenre.java      # Enumeração de gêneros de livros (pt/en)
 ├─ repository/
 │   └─ BookRepository.java # Gerencia leitura/escrita de arquivos
 └─ exceptions/
     └─ BookException.java  # Tratamento de exceções específicas
📖 Gêneros Disponíveis (BookGenre)
Enum Java	Português	Inglês
FICTION	Ficção	Fiction
TERROR	Terror	Horror
ROMANCE	Romance	Romance
ADVENTURE	Aventura	Adventure

O usuário pode digitar português ou inglês ao cadastrar ou atualizar livros.

🛠 Tecnologias Utilizadas

Java 25

Scanner (entrada de dados pelo terminal)

Enum (para gêneros de livros)

Arquivos de texto (.txt) para persistência local

▶️ Como Executar

Clone ou baixe o projeto

Abra em uma IDE compatível (IntelliJ, Eclipse, VSCode)

Compile todas as classes

Execute Program.java:

java app.Program

O menu será exibido e você poderá interagir digitando números das opções.

🖼 Exemplo de Uso
===============================================
1 - Cadastrar livro
2 - Listar livros
3 - Buscar livro por título
4 - Deletar livro
5 - Sair
Escolha uma opção: 1

📝 Informe o título: O Senhor dos Anéis
📝 Informe o autor: J.R.R. Tolkien
📝 Informe o gênero: Ficção
📝 Informe a quantidade de páginas: 1178
✅ LIVRO CADASTRADO!

===============================================
1 - Cadastrar livro
2 - Listar livros
3 - Buscar livro por título
4 - Deletar livro
5 - Sair
Escolha uma opção: 2

📋 Lista de livros:
1 - Title: O Senhor dos Anéis - Author: J.R.R. Tolkien - Genre: Ficção - Pages: 1178
⚠️ Observações

Certifique-se de que o diretório C:\BooksRegistred\ exista antes de cadastrar ou deletar livros.

Entradas do menu devem ser números inteiros.

Pressionar ENTER ao atualizar mantém o valor atual.

Busca e entrada de gênero não diferenciam maiúsculas de minúsculas.

As opções do menu devem ser digitadas como números inteiros. Entradas inválidas gerarão a mensagem "Opção inválida!".

O sistema não diferencia maiúsculas e minúsculas nas buscas por título ou ao digitar o gênero.

O método updateBook() permite manter valores atuais pressionando ENTER, e converte automaticamente gêneros digitados em português ou inglês para o enum interno.
