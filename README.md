# Aula: Introdução a Async/Await e Promises em JavaScript

## Descrição

Este código foi preparado para uma aula introdutória sobre programação assíncrona em JavaScript. O objetivo é explicar o conceito de Promises, o uso de `async` e `await`, e como lidar com operações assíncronas de forma mais legível e organizada.

---

## Objetivos da Aula

- Entender o que é uma Promise e para que serve.
- Aprender a criar funções que retornam Promises.
- Compreender o funcionamento do `async` e do `await`.
- Mostrar como controlar a ordem de execução em operações assíncronas.
- Apresentar um exemplo prático com delay usando `setTimeout`.

---

## Explicação do Código

```js
function primeiraFuncao() {
    return new Promise((resolve) => {
        setTimeout(() => {
            console.log('Esperar aqui!')
            resolve()
        }, 1000)
    })
}

async function segundaFuncao() {
    console.log('iniciou')
    await primeiraFuncao()
    console.log('terminou')
}

segundaFuncao()
```
**primeiraFuncao:** cria e retorna uma Promise que resolve após 1 segundo (simulando uma operação assíncrona).

**segundaFuncao:** função assíncrona que usa await para esperar a resolução da primeiraFuncao antes de continuar.

A execução demonstra como o **console.log('terminou')** só acontece depois do delay de 1 segundo.

## Pontos para Discussão
- Diferença entre funções síncronas e assíncronas.
- Vantagens do uso de async/await frente a .then() e callbacks.
- Cenários práticos em que essas técnicas são úteis (ex: requisições HTTP, leitura de arquivos).

***Este material foi preparado para ajudar alunos a compreenderem conceitos essenciais de JavaScript moderno, facilitando o entendimento de código assíncrono.***
