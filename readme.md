# Content created for Daruk team Tech Sharing

## API Testing using Postman + Newman Reporter HTMLextra

To demonstrate to the team how to use Postman for API testing, I used Paulo Gonçalves [ServeRest](https://serverest.dev/) REST API.

Concepts used in the tests:

- Dynamic variables
- Pre-request scripts
- Test scripts
- JSON schema validation

### Setup

To view the tests and scripts used, simply import the collection and environment files that were used here directly into Postman. To execute the tests via Newman, follow these steps:

- Download and install the latest version of [Node.js](https://nodejs.org/en/)

Install Newman:
```sh
npm install -g newman
```

Install the Newman report:
```sh
npm install -g newman-reporter-htmlextra
```

Run the tests through the project root directory:
```sh
newman run serverest-tech-sharing.postman_collection.json -e serverest-tech-sharing.postman_environment.json -r htmlextra
```

To view the test results, simply open the report that was created in newman folder in the project root.

You can also consult the test results on this [Page](https://samska.github.io/serverest-tech-sharing/report.html) as it is published with each new pipeline run.

### Badges

[![Run API Tests with Postman and Newman](https://github.com/Samska/serverest-tech-sharing/actions/workflows/postman.yml/badge.svg)](https://github.com/Samska/serverest-tech-sharing/actions/workflows/postman.yml)