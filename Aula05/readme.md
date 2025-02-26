# Aula 05 - React: Passagem de Parâmetros de Pai para Filho

## Introdução

Nesta aula, vamos aprender como passar parâmetros de um componente pai para um componente filho em React. Isso é essencial para criar componentes reutilizáveis e dinâmicos.

## Exemplo Básico

### Componente Pai

```javascript
// ParentComponent.js
import React from 'react';
import ChildComponent from './ChildComponent';

const ParentComponent = () => {
  const mensagem = "Olá do componente pai!";
  
  return (
    <div>
      <ChildComponent mensagem={mensagem} />
    </div>
  );
}

export default ParentComponent;
```

### Componente Filho

```javascript
// ChildComponent.js
import React from 'react';

const ChildComponent = ({ mensagem }) => {
  return (
    <div>
      <p>{mensagem}</p>
    </div>
  );
}

export default ChildComponent;
```

## Exercícios

### Exercício 1

Crie um componente pai que passe uma lista de itens para um componente filho. O componente filho deve renderizar a lista de itens.

### Exercício 2

Crie um componente pai que passe uma função para um componente filho. O componente filho deve chamar essa função quando um botão for clicado.

### Exercício 3

Crie um componente pai que passe um objeto com várias propriedades para um componente filho. O componente filho deve exibir essas propriedades.

## Conclusão

Nesta aula, aprendemos como passar parâmetros de um componente pai para um componente filho em React. Pratique os exercícios para reforçar o aprendizado e entender melhor como os componentes podem se comunicar entre si.
