# Async/Await en JavaScript

> 🚧 **Contido en construción**
>
> Este tema está sendo desenvolvido. Volve pronto!

## O que aprenderás nesta sección

- Que é a programación asíncrona e por que é necesaria
- A palabra clave `async` e `await`
- Xestión de erros con `try/catch` en código asíncrono
- Patróns comúns: async en bucles, Promise.all con async/await

```js
// Exemplo básico
async function obtenerDatos() {
  try {
    const resposta = await fetch('https://api.exemplo.com/datos');
    const datos = await resposta.json();
    console.log(datos);
  } catch (erro) {
    console.error('Erro:', erro);
  }
}
```

---

[Fetch API →](02-fetch-api.md)
