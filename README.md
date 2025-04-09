# Projeto-Tailwind
📩 ADDPRODUTO:
<!DOCTYPE html> <!-- Declara o tipo do documento como HTML5 -->
<html lang="pt-BR"> <!-- Define o idioma da página como português do Brasil -->
<head> <!-- Início do cabeçalho da página -->
  <meta charset="UTF-8" /> <!-- Define a codificação de caracteres como UTF-8 -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0" /> <!-- Configura a visualização para dispositivos móveis -->
  <script src="https://cdn.tailwindcss.com"></script> <!-- Importa o Tailwind CSS via CDN -->
  <title>Dashboard</title> <!-- Título da aba do navegador -->
</head>
<body class="bg-gray-100"> <!-- Início do corpo da página com fundo cinza claro -->

  <button id="menuButton" class="md:hidden p-4"> <!-- Botão de menu visível apenas em telas pequenas -->
    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor"> <!-- Ícone SVG do botão -->
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" /> <!-- Desenho do ícone de menu hambúrguer -->
    </svg>
  </button>

  <div class="flex"> <!-- Container flex para sidebar e conteúdo principal -->
    <aside id="sidebar" class="fixed top-0 left-0 w-64 h-screen bg-white p-5 shadow-md transform -translate-x-full transition-transform md:relative md:translate-x-0 md:block md:w-64 z-50"> <!-- Sidebar com comportamento responsivo -->
      <h1 class="text-2xl font-bold text-blue-500 p-2">TrendBox</h1> <!-- Título da sidebar -->
      <nav class="mt-10"> <!-- Navegação da sidebar -->
        <ul>
          <li class="mb-10 p-2"><a href="/index.html">Dashboard</a></li> <!-- Link para Dashboard -->
          <li class="mb-10 p-2"><a href="/addProduto.html">Adicionar Produto</a></li> <!-- Link para adicionar produto -->
          <li class="mb-10 p-2"><a href="/delProduto.html">Remover Produto</a></li> <!-- Link para remover produto -->
          <li class="mb-10 p-2"><a href="/produtos.html">Produtos</a></li> <!-- Link para página de produtos -->
        </ul>
      </nav>
    </aside>

    <main class="flex-1 h-screen flex justify-center items-center md:ml-50 bg-gray-100"> <!-- Área principal centralizada com fundo cinza -->
      <div class="w-full max-w-md"> <!-- Container com largura máxima média -->
        <h2 class="text-3xl font-bold mt-1 mb-10 text-center">Adicionar Produto</h2> <!-- Título do formulário -->
        <form id="productForm" class="bg-white p-6 rounded shadow-md"> <!-- Formulário com fundo branco e sombra -->
          <div class="mb-4"> <!-- Campo do nome do produto -->
            <label for="productName" class="block text-gray-700 font-bold mb-2">Nome do Produto</label>
            <input type="text" id="productName" class="w-full p-2 border border-gray-300 rounded" placeholder="Digite o nome do produto">
          </div>
          <div class="mb-4"> <!-- Campo do preço do produto -->
            <label for="productPrice" class="block text-gray-700 font-bold mb-2">Preço</label>
            <input type="number" id="productPrice" class="w-full p-2 border border-gray-300 rounded" placeholder="Digite o preço do produto">
          </div>
          <div class="mb-4"> <!-- Campo da descrição do produto -->
            <label for="productDescription" class="block text-gray-700 font-bold mb-2">Descrição</label>
            <textarea id="productDescription" class="w-full p-2 border border-gray-300 rounded" placeholder="Digite a descrição do produto"></textarea>
          </div>
          <div class="mb-4"> <!-- Campo da categoria do produto -->
            <label for="productCategory" class="block text-gray-700 font-bold mb-2">Categoria</label>
            <select id="productCategory" class="w-full p-2 border border-gray-300 rounded">
              <option value="">Selecione uma categoria</option> <!-- Opção padrão -->
              <option value="electronics">Eletrônicos</option> <!-- Categoria: Eletrônicos -->
              <option value="clothing">Roupas</option> <!-- Categoria: Roupas -->
              <option value="accessories">Acessórios</option> <!-- Categoria: Acessórios -->
            </select>
          </div>
          <button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Adicionar Produto</button> <!-- Botão de envio do formulário -->
        </form>
      </div>
    </main>    
  </div>

  <script src="/script/menu.js"></script> <!-- Script para o botão do menu lateral -->
</body>
</html> <!-- Fim do documento HTML -->
Esse código monta uma página chamada Adicionar Produto, que faz parte de um sistema chamado TrendBox. Ele é todo estilizado com Tailwind CSS e tem um visual bem moderno, limpo e responsivo, ou seja, funciona bem tanto no computador quanto no celular.

Logo no canto esquerdo, tem um menu lateral fixo que mostra links para as principais páginas do sistema: Dashboard, Adicionar Produto, Remover Produto e Produtos. Esse menu fica escondido no celular e aparece só quando o usuário clica no botão de menu (o ícone com três linhas).

No centro da tela, tem um formulário para cadastrar um novo produto. Esse formulário tem campos para o usuário digitar:

O nome do produto
O preço
Uma descrição
E escolher uma categoria (como Eletrônicos, Roupas ou Acessórios)
Depois que o usuário preenche tudo, ele pode clicar no botão “Adicionar Produto” pra enviar os dados. O formulário tá bem organizado, com tudo separado por blocos, e o layout ajuda bastante na hora de preencher.

Por fim, o código carrega um script chamado menu.js, que provavelmente cuida da lógica do botão de menu no celular — tipo abrir e fechar o menu lateral quando precisar.

No geral, essa página é feita pra facilitar o trabalho de quem tá gerenciando os produtos da loja, deixando tudo bem simples, claro e bonito de usar.
