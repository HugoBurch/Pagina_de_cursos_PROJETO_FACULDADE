# 🎓 Página de Cursos

Landing page de uma plataforma de cursos, desenvolvida com **HTML5, CSS3 e JavaScript**, com catálogo de cursos carregado dinamicamente a partir de um arquivo JSON e um **carrinho lateral de compras**.

O projeto foi desenvolvido com foco em **hierarquia de informação, simplicidade, organização visual e experiência do usuário**, sendo também um projeto acadêmico para prática de desenvolvimento web.

🔗 **Projeto online:** https://hugoburch.github.io/Pagina_de_cursos_PROJETO_FACULDADE/

🔗 **Repositório:** https://github.com/HugoBurch/Pagina_de_cursos_PROJETO_FACULDADE

---

## 📌 Sobre o projeto

O projeto simula uma plataforma de cursos online, apresentando um catálogo organizado por categorias.

Os cursos são carregados dinamicamente através do arquivo `cursos.json`, permitindo separar os **dados** da aplicação da estrutura HTML.

Cada curso apresenta informações como:

- Nome do curso
- Carga horária
- Nível
- Preço
- Descrição
- Imagem

Além da visualização dos cursos, o usuário pode abrir os detalhes de um curso e adicioná-lo ao carrinho.

---

## ✨ Funcionalidades

### 📚 Catálogo de cursos

- Catálogo gerado dinamicamente com JavaScript.
- Cursos separados por categorias.
- Cards individuais para cada curso.
- Exibição de imagem, nome, carga horária, nível e preço.
- Informações detalhadas disponíveis através de um overlay.

### 🔎 Detalhes dos cursos

Ao clicar para visualizar os detalhes, o card apresenta informações adicionais sobre o curso.

O usuário pode:

- Abrir os detalhes.
- Fechar os detalhes.
- Adicionar o curso ao carrinho diretamente pelo card.

### 🛒 Carrinho lateral

O projeto possui um sistema de carrinho desenvolvido em JavaScript.

Funcionalidades:

- Abrir o carrinho pelo ícone.
- Adicionar cursos.
- Impedir a adição duplicada do mesmo curso.
- Exibir os cursos adicionados.
- Exibir o preço individual.
- Calcular o valor total.
- Remover cursos do carrinho.
- Fechar o carrinho pelo botão.
- Fechar o carrinho ao clicar fora dele.

O carrinho é mantido em memória durante a utilização da página.

---

## 🗂️ Categorias de cursos

Os cursos disponíveis no arquivo de dados estão organizados em categorias como:

- 💻 **DEV**
- 📊 **TECH & BUSINESS**
- 🎨 **FRONT-END**

Entre os cursos cadastrados estão exemplos como:

- Arquitetura de Sistemas .Net
- Desenvolvedor Java Enterprise
- Desenvolvedor FullStack
- Arquitetura de Software
- DevOps na Prática
- Engenharia de Software
- APIs e Microsserviços
- Cybersecurity
- Product Management
- Growth Marketing
- IA para Negócios
- Liderança em Tecnologia
- React Profissional
- Conceitos Profundos em JavaScript
- Desenvolvimento Web Moderno
- Design Systems
- Performance Web
- Acessibilidade na Web

Os dados podem ser alterados diretamente no arquivo `cursos.json`.

---

## 🛠️ Tecnologias utilizadas

- **HTML5** — estrutura da página.
- **CSS3** — estilização, layout e responsividade.
- **JavaScript** — lógica, interações, criação dos cards e carrinho.
- **JSON** — armazenamento dos dados dos cursos.
- **Fetch API** — carregamento dos dados do `cursos.json`.
- **Git/GitHub** — versionamento e hospedagem do projeto.
- **GitHub Pages** — publicação da aplicação.

O projeto não utiliza frameworks de frontend, trabalhando principalmente com APIs nativas do navegador e JavaScript.

---

## ⚙️ Funcionamento do JavaScript

O arquivo `script.js` é dividido em partes principais.

### 🛒 Sistema de carrinho

O carrinho utiliza um array chamado `cart` para armazenar temporariamente os cursos adicionados.

As principais funções são:

```text
addToCart()
updateCart()
removeFromCart()
```

### `addToCart()`

Adiciona um curso ao carrinho e verifica se o mesmo curso já foi adicionado.

### `updateCart()`

Atualiza a interface do carrinho, exibindo:

- Produtos;
- Preços;
- Total da compra;
- Botões para remoção.

### `removeFromCart()`

Remove um curso do carrinho utilizando seu índice no array.

---

## 📦 Carregamento dos cursos

Os dados são carregados através da API `fetch()`:

```javascript
fetch('cursos.json')
```

Após o carregamento, o JavaScript:

1. Recebe o arquivo JSON.
2. Converte a resposta para um objeto JavaScript.
3. Obtém a imagem principal.
4. Localiza o container do catálogo.
5. Percorre as categorias.
6. Cria os cards dos cursos.
7. Adiciona os cards à página.
8. Configura os eventos de interação.

Caso o arquivo `cursos.json` não seja carregado, um erro é registrado no console e uma mensagem é apresentada ao usuário.

---

## 🧩 Estrutura dos dados

O arquivo `cursos.json` possui uma estrutura organizada em categorias e cursos.

Exemplo:

```json
{
  "categorias": [
    {
      "nome": "DEV",
      "cursos": [
        {
          "titulo": "Desenvolvedor FullStack",
          "horas": 660,
          "nivel": "Avançado",
          "preco": 4999.9,
          "detalhes": "Front-end, back-end, banco de dados, APIs e deploy em nuvem.",
          "imagem": "img/Full-stack.png"
        }
      ]
    }
  ]
}
```

Essa abordagem permite adicionar ou modificar cursos sem precisar alterar diretamente a estrutura dos cards no HTML.

---

## 📁 Estrutura do projeto

```text
Pagina_de_cursos_PROJETO_FACULDADE/
│
├── .vscode/
│
├── icons/
│   └── ícones utilizados pela interface
│
├── img/
│   └── imagens dos cursos e elementos visuais
│
├── cursos.json
├── index.html
├── script.js
├── style.css
└── README.md
```

### Principais arquivos

**`index.html`**  
Contém a estrutura principal da landing page, catálogo, cards e carrinho.

**`style.css`**  
Responsável pela aparência da aplicação, layout, cards, carrinho lateral, detalhes dos cursos e responsividade.

**`script.js`**  
Responsável pela lógica da aplicação, carregamento dos cursos, criação dinâmica dos cards, interação com os detalhes e funcionamento do carrinho.

**`cursos.json`**  
Arquivo responsável por armazenar os dados dos cursos, categorias, preços, níveis, cargas horárias, descrições e imagens.

**`img/`**  
Contém as imagens utilizadas nos cursos e na interface.

**`icons/`**  
Contém os ícones utilizados no projeto.

---

## 🚀 Como executar

Como o projeto utiliza `fetch()` para carregar o arquivo `cursos.json`, é recomendado executá-lo através de um servidor local.

### 1. Clone o repositório

```bash
git clone https://github.com/HugoBurch/Pagina_de_cursos_PROJETO_FACULDADE.git
```

### 2. Entre na pasta

```bash
cd Pagina_de_cursos_PROJETO_FACULDADE
```

### 3. Execute com Live Server

No Visual Studio Code, pode ser utilizada a extensão **Live Server**.

Depois:

1. Abra o projeto no VS Code.
2. Clique com o botão direito em `index.html`.
3. Selecione **Open with Live Server**.
4. O projeto será aberto no navegador.

---

## 🌐 Projeto publicado

A aplicação também está disponível através do GitHub Pages:

**https://hugoburch.github.io/Pagina_de_cursos_PROJETO_FACULDADE/**

---

## 🎯 Objetivos do projeto

Este projeto foi desenvolvido para praticar conceitos de desenvolvimento frontend, principalmente:

- Estruturação de páginas com HTML.
- Estilização com CSS.
- Responsividade.
- Manipulação do DOM.
- Eventos JavaScript.
- Arrays e objetos.
- Funções.
- Template literals.
- Manipulação de dados JSON.
- `fetch()`.
- Criação dinâmica de elementos.
- Delegação de eventos.
- Organização de código.
- Desenvolvimento de componentes visuais.
- Implementação de um carrinho de compras.

---

## 📱 Responsividade

A interface foi desenvolvida considerando diferentes tamanhos de tela, buscando proporcionar uma experiência adequada em:

- 💻 Computadores
- 💻 Notebooks
- 📱 Smartphones
- 📱 Tablets

---

## 🔒 Observação

Este projeto possui caráter **acadêmico e demonstrativo**.

O carrinho implementado é apenas uma simulação de compra. Não existe, atualmente, integração com:

- Gateway de pagamento;
- Banco de dados;
- Sistema de usuários;
- Processamento real de pedidos;
- Backend.

---

## 👨‍💻 Autor

**Hugo Burch**

GitHub:  
https://github.com/HugoBurch

---

## 📄 Licença

Projeto desenvolvido para fins acadêmicos e de aprendizado.
