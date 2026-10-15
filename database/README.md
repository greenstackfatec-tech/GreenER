
# Database — GreenER

## 1. Visão Geral

Esta pasta contém os arquivos responsáveis pela definição e organização da estrutura do banco de dados do projeto GreenER.

O banco de dados é responsável por armazenar e organizar as informações utilizadas por uma aplicação, permitindo que sejam consultadas, inseridas, atualizadas e removidas de maneira estruturada.

## 2. Objetivo

O objetivo desta camada é disponibilizar uma estrutura de armazenamento organizada, consistente e confiável para os dados da aplicação.

Os arquivos deste diretório documentam e definem a estrutura necessária para a criação e a manutenção do banco de dados.

## 3. Tecnologia Utilizada

| Tecnologia | Descrição |
|---|---|
| PostgreSQL | Sistema gerenciador de banco de dados relacional de código aberto. |
| SQL | Linguagem utilizada para definir estruturas, consultar e manipular dados. |

### 3.1. PostgreSQL

O PostgreSQL é um sistema gerenciador de banco de dados relacional que permite armazenar informações em tabelas e estabelecer relacionamentos entre elas.

### 3.2. SQL

SQL (*Structured Query Language*) é a linguagem utilizada para interagir com o banco de dados. Por meio dela, é possível criar tabelas, definir restrições, consultar informações e realizar operações sobre os dados.

## 4. Organização do Diretório

Os arquivos presentes neste diretório são utilizados para definir e documentar a estrutura do banco de dados.

```text
database/
├── README.md
└── modelagem_bd.png
└── schema.sql
```

A organização definitiva deve refletir os arquivos efetivamente existentes no diretório.


## 5. Requisitos

Para trabalhar com os arquivos deste diretório, é necessário ter:

- PostgreSQL instalado ou acesso a uma instância PostgreSQL.
- Um cliente SQL, como o `psql` ou o pgAdmin.
- Os arquivos SQL disponibilizados no repositório.
- As permissões necessárias para executar os comandos no banco de dados.

## 6. Execução

A execução dos scripts depende da estrutura e das instruções definidas nos arquivos SQL.

De forma geral, o processo consiste em:

1. Preparar o ambiente PostgreSQL.
2. Verificar o conteúdo e a finalidade dos scripts.
3. Criar ou selecionar o banco de dados de destino, conforme as instruções do projeto.
4. Executar os scripts na ordem adequada.
5. Verificar se as estruturas foram criadas corretamente.

**Atenção:** antes de executar um script, verifique os comandos presentes no arquivo e confirme o banco de dados selecionado. Operações de criação, alteração ou remoção podem afetar os dados existentes.


### 7. [Documentação Complementar](https://github.com/greenstackfatec-tech/greener/blob/develop/README.md)

Para informações gerais sobre o projeto, sua arquitetura e suas demais tecnologias, consulte o arquivo `README.md` localizado na raiz do repositório.

Eles podem ser encontrados <a href="https://github.com/greenstackfatec-tech/greener/blob/develop/README.md">aqui</a>

---

