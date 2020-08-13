<h3 align="center">
  Desafio 06: GoFinances Web
</h3>

## :rocket: Sobre o desafio

Nesse desafio foi desenvolvida a aplicação web de gestão de transações, a GoFinances. Neste projeto foi exercitado o conteúdo básico do React.js junto com TypeScript, utilizando rotas e envio de arquivos por formulário.

Essa é uma aplicação que se conecta ao backend feito no Desafio 05, exibe as transações criadas e permite a importação de um arquivo CSV para gerar novos registros no banco de dados.

## Instalação

Para instalar o projeto localmente na sua máquina basta clonar o repositório:

```bash
git clone https://github.com/gpmarchi/gostack-nova-jornada-desafio-06.git && cd gostack-nova-jornada-desafio-06
```

E rodar o comando abaixo para instalar as dependências necessárias:

```bash
yarn
```

## Funcionalidades da aplicação

Abaixo seguem os pontos principais que a aplicação resolve:

- **`Listar as transações da sua API`**: A página `Dashboard` exibe uma listagem através de uma tabela, com o campo `title`, `value`, `type` e `category` de todas as transações que estão cadastradas na sua API.

- **`Exibir o balance da sua API`**: A página `Dashboard` exibe o balance que é retornado do backend, contendo o total geral, junto ao total de entradas e saídas.

- **`Importar arquivos CSV`**: Através da página Import, é permitido o envio de um arquivo no formato csv para o backend, que faz a importação das transações para o banco de dados. O arquivo csv deve seguir o seguinte [modelo](./assets/file.csv).

## Especificação dos testes

O desafio foi resolvido seguindo a técnica de TDD. Os testes podem ser encontrados na pasta ```src/__tests__``` e para executá-los rodar o comando:

```bash
yarn test
```

Para cada teste existe uma breve descrição do que a aplicação executa para que o mesmo passe:

- **`should be able to list the total balance inside the cards`**: Para que esse teste passe, a aplicação permite que seja exibido no `Dashboard`, cards contendo o total de `income`, `outcome` e o total da subtração de `income - outcome` que são retornados pelo balance do backend.

- **`should be able to list the transactions`**: Para que esse teste passe, a aplicação permite que sejam listados dentro de uma tabela, todas as transações que são retornadas do backend.

- **`should be able to navigate to the import page`**: Para que esse teste passe, é permitida a troca de página através do `Header`, pelo botão que contém o nome `Importar`.

- **`should be able to upload a file`**: Para que esse teste passe, é permitido que um arquivo seja enviado através do componente de drag-n-drop na página de import, e que exiba o nome do arquivo enviado para o input.
