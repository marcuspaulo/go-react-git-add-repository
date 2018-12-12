# Módulo 3 - GoReact - Redux

# Passo 1, criar um novo projeto com o create-react

´´´sh
\$ create-react-app.cmd app-goreact-03
´´´

# Passo 2, Instalar a dependência do Redux e React-redux

´´´sh
\$ yarn add redux react-redux
´´´

# Configurando o Redux e React-redux no projeto

1 - Criar a pasta store, dentro do src, em seguida, criar o arquivo index.js

```js
import { createStore } from "redux";

const store = createStore(() => {});

export default store;
```

2 - Ajustar o arquivo APP.js, englobando o Provider do React-redux

```js
import React from "react";
import { Provider } from "react-redux";

import store from "./store";

const App = () => (
    <Provider store={store}>
        <h1>Hello World</h1>
    </Provider>
);

export default App;
```

# Instalando o eslint Airbnb (Desenvolvimento)

```sh
$ yarn add eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react -D
```

# Próximo passo, criar uma pasta reducer, dentro de store e adicionar o arquivo todo.js (Reducer sempre é uma função)

# O Reducer altera o estado.

--> O State é exatamente o estado antigo do objeto (Antes de sofrer alterações)
--> Action: é a ação que foi disparada pela aplicação. Todos os redux's escutam todas as ações. Porém, dentro de cada redux é que define onde será alterado. Ex: type: 'ADD_TODO'.

```js
export default function todos(state, action) {}
```

# Ajustando o Reducer

```js
const INITIAL_STATE = [
    { id: 1, text: "Fazer Café" },
    { id: 2, text: "Estudar React" }
];

export default function todos(state = INITIAL_STATE, action) {
    switch (action.type) {
        default:
            return state;
    }
}
```

o import { connect } from 'react-redux'; - conecta o componente com algum estado do react

# Instalação dos PropTypes

```sh
$ yarn add prop-types
```

# Instalando a ferramenta Reactotron

1- Acessar o site: https://github.com/infinitered/reactotron
2 - Clicar em release: Escolha uma versão estável.

# Instalando o Reactotron no VSCode

```sh
$ yarn add reactotron-react-js
```

# Esse projeto é uma continuação do Go-React-Todo-List, porém, alguns arquivos do Todo, foram removidos

# Trabalhando com Navegação com o React-router-dom

```sh
$ yarn add react-router-dom
```

# Visual Code Adicionando caracteres estranhos, como por exemplo {' '}, para substituir os espaços.

--> Para desativar essa regra você pode adicionar dentro dos rules no arquivo .eslintrc:

```js
    "react/jsx-one-expression-per-line": "off"
```

# Instalando Redux-saga e o Axios

```sh
$ yarn add redux-saga axios
```

# Instalar e configurar um plugin para o Redux Saga - Reactotron

```sh
$ yarn add reactotron-redux-saga
```

---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
