### A Simple Example to use a function written in Assembly Script in JS

Install the Assembly Script complier
https://github.com/AssemblyScript/assemblyscript


```
npm install --save-dev AssemblyScript/assemblyscript
```

Create necessary structure and files

```
npx asinit .
```

You can either build the ts/as files to web assembly manually using asc or use the below command that is added in the package json 

```
npm run asbuild
```

The generated wasm file is read using the fetch api into an array buffer and the buffer is passed to the instantiate method of WebAssembly object that is available globally in the browsers. From the instance that is returned, all the exports can be accessed as if it was a JS function.

In this example, it is being done in the html file directly for the sake of simplicity.