# Conteúdo feito para o Tech Sharing da equipe Daruk

## Testes de API utilizando Postman + Newman Reporter HTMLextra

Para demonstrar ao time como utilizar o Postman para testes de API, utilizei a API REST [ServeRest](https://serverest.dev/) do Paulo Gonçalves.

Conceitos utilizados nos testes:

Dynamic variables;
Pre-request scripts;
Test scripts;
JSON schema validation.

### Configuração

Para consultar os testes e scripts utilizados, basta importar a collection e environment aqui utilizados, diretamente no Postman. Já para executar os testes via Newman, basta seguir esses passos:

- Baixar e instalar a última versão do [Node.js](https://nodejs.org/en/)

Instalar o newman:
```sh
npm install -g newman
```

Instalar o newman report:
```sh
npm install -g newman-reporter-htmlextra
```

Executar os testes através da raíz do projeto:
```sh
newman run serverest-tech-sharing.postman_collection.json -e serverest-tech-sharing.postman_environment.json -r htmlextra
```