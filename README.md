# Configuração inicial padrão para construção de API

Esta aplicação é uma configuração padrão para o desenvolvimento de APIs usando `Node.js`, `TypeScript`, e outras ferramentas como `Docker` e `Prisma`.

## Pré-Requisitos

Certifique-se de ter instalado:
- [Node.js](https://nodejs.org/en/docs/)
- [Docker](https://docs.docker.com/get-started/)
- [Docker Compose](https://docs.docker.com/compose/)

## Configuração Inicial

Primeiro, clone o repositório para a sua máquina local e navegue até o diretório do projeto.

```bash
git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_DIRETORIO>
``` 

### Configuração das Variáveis de Ambiente
Copie o arquivo  `.env.example` para `.env` e atualize as variáveis de ambiente conforme necessário.

```bash
cp .env.example .env
```
Altere o nome do banco de dados e a senha no arquivo `docker-compose.yml` e no arquivo `.env` para garantir que as configurações estejam sincronizadas.

### Subindo o Container
Para construir e subir o container usando o `Docker Compose`, execute:

```bash
docker-compose up -d
```

Isso irá subir o container do `PostgreSQL` e configurar tudo conforme definido no `docker-compose.yml`.

### Executando a Primeira Migration

Para executar a primeira migration e criar as tabelas no banco de dados, use o Prisma Migrate:

```bash
npx prisma migrate dev
```

Este comando irá aplicar as migrações pendentes no seu banco de dados.

### Abrindo o Prisma Studio

Para abrir o `Prisma Studio`, que é uma interface gráfica para visualizar e editar os dados no banco de dados, execute:

```bash
Copiar código
npx prisma studio
```
O `Prisma Studio` será aberto no seu navegador padrão.

### Links Úteis
- [Documentação do Fastify](https://fastify.dev/docs/latest/)
- [Documentação do Docker](https://docs.docker.com/manuals/)
- [Documentação do Docker Compose](https://docs.docker.com/compose/)
- [Documentação do Prisma](https://www.prisma.io/docs)
- [Documentação do TypeScript](https://www.typescriptlang.org/docs/)

### Conclusão
Sua aplicação agora deve estar rodando com um banco de dados configurado e pronto para ser utilizado. Para mais informações sobre as operações específicas, consulte a documentação das ferramentas utilizadas.
