
# Aula 04 - React: App.js e index.js

## Estrutura do Projeto

Na aula de hoje, discutimos sobre a estrutura básica de um projeto React, focando nos arquivos `App.js` e `index.js`.

### App.js

- A função `App` deve começar com letra maiúscula.
- O nome do arquivo deve ser `App.js` para corresponder ao nome da função.
- Utilizamos `export default` para exportar a função `App`.

Exemplo:
```javascript
// App.js
import React from 'react';

function App() {
  return (
    <div>
      <h1>Olá, Mundo!</h1>
    </div>
  );
}

export default App;
```

### index.js

- No arquivo `index.js`, importamos o `App` e o utilizamos dentro do método `ReactDOM.render`.
- O componente `App` deve ser chamado com a primeira letra maiúscula.

Exemplo:
```javascript
// index.js
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(<App />, document.getElementById('root'));
```

## Arrow Function

Também mostramos como transformar a função `App` em uma arrow function.

Exemplo:
```javascript
// App.js
import React from 'react';

const App = () => {
  return (
    <div>
      <h1>Olá, Mundo!</h1>
    </div>
  );
}

export default App;
```

## useState

Introduzimos o hook `useState` para gerenciar o estado dentro de um componente funcional. Explicamos que a alteração do estado re-renderiza a página e atualiza o valor.

Exemplo:
```javascript
// App.js
import React, { useState } from 'react';

const App = () => {
  const [contador, setContador] = useState(0);

  const incrementar = () => {
    setContador(contador + 1);
  };

  return (
    <div>
      <h1>Contador: {contador}</h1>
      <button onClick={incrementar}>Incrementar</button>
    </div>
  );
}

export default App;
```

Neste exemplo, `contador` é a variável de estado e `setContador` é a função que atualiza o estado. Quando o botão é clicado, `setContador` é chamado, o que re-renderiza o componente com o novo valor de `contador`.

## Conclusão

Nesta aula, aprendemos sobre a estrutura básica de um projeto React, a importância de nomear corretamente os arquivos e funções, como utilizar `export default`, e como gerenciar o estado com `useState`. Pratique criando seus próprios componentes e manipulando o estado para reforçar o aprendizado.
