# Dominando Postman - Teste de API Rest do manual a CI/CD
Este repositório foi criado para treinamento do Curso [Dominando Postman: Testando e Automatizando APIs](https://www.udemy.com/course/dominando-postman-2023-testando-e-automatizado-apis/?couponCode=BFCPSALE24).

## Tecnologias utilizadas - Postman versão web
- Docker version 27.3.1, build ce12230
- node version 23.3.0
- npm version 10.9.1
- newman version 6.2.1
- newman-reporter-html
- ## Documentações
- Analise Técnica: Analise/
- Doc da API: [Consulte Swagger](https://serverest.dev/#/)
## Como instalar o ambiente
- Primeiro: instale o node em seu computador [baixe aqui](https://nodejs.org/en/download)
- Segundo: realize a instalação do newman de forma global [baixe aqui a dependencia](https://www.npmjs.com/package/newman)
```
npm install -g newman
```
- Terceiro: realize a instalação da dependencia dos relatórios (opcional) [newman-reporter-html ](https://www.npmjs.com/package/newman-reporter-html)
```
npm install -g newman-reporter-html
```
## Para instalação em um contêiner Docker
```
docker pull node:latest
docker run -dti --nome node node:latest
docker exec -ti node bash
```
- Exportar a collection e o environment do Postman
- Copiar da pasta local para o contêiner do Docker
```
docker cp ServerRest.postman_collection.json node:/home/node/app/serveRest/
```
### Instalar o node no ambiente
```
apt install node
apt Install npm
node -v
npm -v
apt install newman
```
### Como rodar os testes - Postman web ou desktop
- Import a collection e o environment
- Execute os teste de forma manual ou automatizada
### Usando o newman - pelo bash
- Abra o console de preferência
- Execute a seguinte linha de comando para rodar os testes
```
newman run ServeRest.postman_collection.json -e serveRest_env.postman_environment.json -r cli
```
- Execute os teste com relatório
```
newman run ServeRest.postman_collection.json -e serveRest_env.postman_environment.json -r cli,htmlextra
```
### Report
Se você optou por rodar os teste com o report htmlextra, você gerou um arquivo html com o resultado dos testes e para verificar as validações você pode abrir a pasta newman que foi criada no local em que os arquivos de collection e environment se encontram.
## Entre em contato
[redes sociais](https://linktr.ee/techberlanda)
