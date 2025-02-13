# Aula 02 - React (Data: 2023-10-05)

## Conteúdo da Aula

### npm
- O que é: npm (Node Package Manager) é um gerenciador de pacotes para o Node.js. Ele permite que você instale, compartilhe e gerencie dependências de projetos JavaScript.
- Para que serve: npm é usado para instalar pacotes necessários para o desenvolvimento de aplicações. Ele também permite que você gerencie scripts de execução definidos no arquivo `package.json`.
- Exemplos de uso:
  - `npm install`: Instala todas as dependências listadas no arquivo `package.json`.
  - `npm install <package-name>`: Instala um pacote específico e adiciona-o ao `package.json`.
  - `npm run <script>`: Executa um script definido na seção "scripts" do `package.json`.

### npx
- Diferença para o npm: npx é uma ferramenta que vem junto com o npm (a partir da versão 5.2.0) e permite executar pacotes diretamente sem precisar instalá-los globalmente.
- Para que serve: npx é útil para executar comandos de pacotes que você não deseja instalar globalmente. Ele baixa e executa o pacote temporariamente.
- Exemplo: `npx create-react-app` permite criar uma nova aplicação React sem instalar o create-react-app globalmente.

### Comando `npx create-react-app`
- O que faz: Cria uma nova aplicação React com uma estrutura de projeto padrão.
- Exemplo de uso: `npx create-react-app my-app`
  - Este comando cria uma nova pasta chamada `my-app` com a estrutura de um projeto React.
  - Dentro dessa pasta, você encontrará subpastas como `node_modules`, `public`, e `src`.

### Estrutura de Pastas Criadas
- `node_modules`: Contém todas as dependências do projeto. Esta pasta é gerada automaticamente pelo npm quando você instala pacotes.
- `public`: Contém arquivos públicos, como o `index.html`, que são servidos diretamente pelo servidor web.
- `src`: Contém o código-fonte da aplicação React. É onde você escreverá a maior parte do seu código.

### Arquivo `index.html` e a div `root`
- `index.html`: Arquivo HTML principal que será servido ao navegador. Ele está localizado na pasta `public`.
  - Exemplo de conteúdo:
    ```html
    <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>React App</title>
      </head>
      <body>
        <div id="root"></div>
      </body>
    </html>
    ```
- `div root`: Div com o id `root` onde a aplicação React será montada. O React usa essa div como ponto de entrada para renderizar a aplicação.

### Novo App.js
- Após apagar os arquivos originais da pasta `src`, criaremos um novo `App.js` com o seguinte conteúdo:

```javascript
// filepath: /c:/Users/Rodrigo/Desktop/aulas/tasi-2025/Aula02-React/src/App.js
import React from 'react';

function App() {
  return (
    <div className="App">
      <h1>Hello, React!</h1>
    </div>
  );
}

export default App;
```
