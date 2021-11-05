# Minhas anotações sobre o curso Trabalhando com módulos em JavaScript 
### Curso feito na ([DIO](https://digitalinnovation.one/)):

## Aula 1 O que são módulos:

Módulos são arquivos Javascript que tem a capacidade de exportar e importar informações de outros arquivos do mesmo tipo.

### Algumas vantagens são:

- Organização do código.
- Compartilhamento de variáveis em escopos diferentes.
- Explicita as dependências dos arquivos.

## Exportar

### Named exports:
```js
export function mostraIdade(pessoa) {
 return 'A idade de ${pessoa.nome} é ${pessoa.idade}`;
}

export function mostraCidade(pessoa) {
 return 'A cidade de ${pessoa.nome} é ${pessoa.cidade}`;
}

export function mostraHobby(pessoa) {
 return 'O hobby de ${pessoa.nome} é ${pessoa.hobby}`;
}
```
Outra maneira

```js
export function mostraIdade(pessoa) {
 return 'A idade de ${pessoa.nome} é ${pessoa.idade}`;
}

export function mostraCidade(pessoa) {
 return 'A cidade de ${pessoa.nome} é ${pessoa.cidade}`;
}

export function mostraHobby(pessoa) {
 return 'O hobby de ${pessoa.nome} é ${pessoa.hobby}`;
}

export {
 mostraIdade,
 mostraCidade,
 mostraHobby
}
```
### Default exports:
```js
export function mostraIdade(pessoa) {
 return 'A idade de ${pessoa.nome} é ${pessoa.idade}`;
}

export function mostraCidade(pessoa) {
 return 'A cidade de ${pessoa.nome} é ${pessoa.cidade}`;
}

export function mostraHobby(pessoa) {
 return 'O hobby de ${pessoa.nome} é ${pessoa.hobby}`;
}

export {
 mostraIdade,
 mostraCidade,
 mostraHobby
}

export default mostraHobby;
```

## Importar

### Named exports:
```js
import {funcao, variavel, classe} from './arquivo.js'
```

### Default exports:
```js
import valorDefault from './arquivo.js'

export default mostraHobby;
```

### Trocando nome de imports
```js
import {arquivo as Apelido} from './arquivo.js';

Apelido.metodo();
```

### Importando todos os dados de um arquivo
```js
import * as INFOS from './arquivo.js';

INFOS.metodoA();

console.log(INFOS.variavel);
```

### Vinculando ao HTML
```js
<script type="module" src="./main.js"></script>
```

Para fazer testes localmente (de um arquivo no seu computador), será necessário estar rodando um servidor. Isso pode ser feito utilizando a extensão ```"Live Server"```, do VSCode.

## Outras curiosidades

- Módulos sempre estão em "strict mode";
- Podem ser utilizadas as extensões ```.js e .mjs```;
- Para testes locais, é necessário utilizar um servidor;
- Ao importar, sempre lembre da extensão ```(.js, .mjs)```;
- Ao importar, sempre utilize ````"./"``` como ponto de partida
