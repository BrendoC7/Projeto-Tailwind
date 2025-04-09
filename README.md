# TrendBox - Adicionar Produto

Este projeto faz parte de um sistema de gerenciamento de produtos chamado **TrendBox**. A página **Adicionar Produto** foi construída com HTML5 e estilizada utilizando **Tailwind CSS**. O layout é moderno, limpo e responsivo, garantindo uma boa experiência tanto em dispositivos móveis quanto em desktops.

## Funcionalidades

- **Menu Lateral**: Um menu fixo no lado esquerdo da tela com links para as principais páginas do sistema:
  - Dashboard
  - Adicionar Produto
  - Remover Produto
  - Produtos

  O menu é **responsivo**: em dispositivos móveis, ele fica oculto até que o usuário clique no botão de menu (ícone de três linhas).

- **Formulário de Adicionar Produto**: Permite ao usuário cadastrar um novo produto, preenchendo os seguintes campos:
  - **Nome do Produto**
  - **Preço**
  - **Descrição**
  - **Categoria**: O usuário pode escolher entre as opções de categorias: *Eletrônicos*, *Roupas* e *Acessórios*.

  Após preencher os dados, o usuário pode clicar no botão "Adicionar Produto" para submeter o formulário.

## Estrutura do Código

O código é composto por um **HTML5** organizado e um **formulário responsivo**, com o auxílio de **Tailwind CSS** para a estilização. O layout é bem estruturado, com as seções do conteúdo divididas em blocos para facilitar a navegação.

### HTML - Estrutura da Página

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <script src="https://cdn.tailwindcss.com"></script>
  <title>Dashboard</title>
</head>
<body class="bg-gray-100">
  <button id="menuButton" class="md:hidden p-4">
    <!-- Ícone do menu -->
  </button>

  <div class="flex">
    <!-- Sidebar -->
    <aside id="sidebar" class="fixed top-0 left-0 w-64 h-screen bg-white p-5 shadow-md transform -translate-x-full transition-transform md:relative md:translate-x-0 md:block md:w-64 z-50">
      <h1 class="text-2xl font-bold text-blue-500 p-2">TrendBox</h1>
      <nav class="mt-10">
        <ul>
          <li class="mb-10 p-2"><a href="/index.html">Dashboard</a></li>
          <li class="mb-10 p-2"><a href="/addProduto.html">Adicionar Produto</a></li>
          <li class="mb-10 p-2"><a href="/delProduto.html">Remover Produto</a></li>
          <li class="mb-10 p-2"><a href="/produtos.html">Produtos</a></li>
        </ul>
      </nav>
    </aside>

    <!-- Formulário de Adicionar Produto -->
    <main class="flex-1 h-screen flex justify-center items-center md:ml-50 bg-gray-100">
      <div class="w-full max-w-md">
        <h2 class="text-3xl font-bold mt-1 mb-10 text-center">Adicionar Produto</h2>
        <form id="productForm" class="bg-white p-6 rounded shadow-md">
          <div class="mb-4">
            <label for="productName" class="block text-gray-700 font-bold mb-2">Nome do Produto</label>
            <input type="text" id="productName" class="w-full p-2 border border-gray-300 rounded" placeholder="Digite o nome do produto">
          </div>
          <div class="mb-4">
            <label for="productPrice" class="block text-gray-700 font-bold mb-2">Preço</label>
            <input type="number" id="productPrice" class="w-full p-2 border border-gray-300 rounded" placeholder="Digite o preço do produto">
          </div>
          <div class="mb-4">
            <label for="productDescription" class="block text-gray-700 font-bold mb-2">Descrição</label>
            <textarea id="productDescription" class="w-full p-2 border border-gray-300 rounded" placeholder="Digite a descrição do produto"></textarea>
          </div>
          <div class="mb-4">
            <label for="productCategory" class="block text-gray-700 font-bold mb-2">Categoria</label>
            <select id="productCategory" class="w-full p-2 border border-gray-300 rounded">
              <option value="">Selecione uma categoria</option>
              <option value="electronics">Eletrônicos</option>
              <option value="clothing">Roupas</option>
              <option value="accessories">Acessórios</option>
            </select>
          </div>
          <button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Adicionar Produto</button>
        </form>
      </div>
    </main>
  </div>

  <script src="/script/menu.js"></script>
</body>
</html>
