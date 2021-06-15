# C4 : Esquema Relacional  <!-- omit in toc -->
_(Apresentar o esquema físico da Base de Dados. Para cada relação resultante, apresente a descrição da tabela correspondente usando o exemplo apresentado.)_

- [Relações](#relações)
  - [Tabela_Clientes](#tabela_Clientes)
  - [Tabela_Profissionais](#tabela_Profissionais)
  - [Tabela_Serviços](#tabela_Serviços)
  - [Tabela_Marcações](#tabela_Marcações)

## Relações

### Tabela_Clientes

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da Tabela Clientes

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                  | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------  | :---------- | :---------- | :--------- | :--- |
| Nome     | Nome do Cliente            | Varchar(100)| -           | Sim        | Não  |
| Morada   | Morada do cliente          | Varchar(150)| -           | Não        | Não  |
| NIF      | Contribuinte do cliente    | Int(9)      | -           | Não        | Não  |
| E-mail   | Correio eletronico cliente | Varchar(100)| -           | Não        | Não  |
| Número   | Número do cliente          | Int(9)      | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| NIF       |

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| NIF         | NIF       | Sim     |


### Tabela_Profissionais

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da Tabela Profissionais

#### COLUNAS <!-- omit in toc -->

| Nome            | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| Id_Profissionais| Número do Profissional    | Int(11)     | -           | Sim        | Não  |
| Nome            | Nome do profissional      | DATE        | -           | Não        | Não  |
| Contacto        | Contacto do profissional  | Int(9)      | -           | Não        | Não  |


#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s)       |
| ---------       |
| id_profissionais|

- **Unicidade** (valores únicos)*:

| Nome             | Coluna(s)       | Indexar |
| -----------      | ---------       | ------- |
| id_profissionais | id_profissionais| Sim     |


### Tabela_Serviços

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da Tabela Serviços

#### COLUNAS <!-- omit in toc -->

| Nome          | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------      | :------------------------ | :---------- | :---------- | :--------- | :--- |
| Id_serviços   | Número do Profissional    | Int(11)     | -           | Sim        | Não  |
| Serviço_nome  | Nome do profissional      | VARCHAR(45) | -           | Não        | Não  |
| Serviço_preço | Contacto do profissional  | Double      | -           | Não        | Não  |


#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s)  |
| ---------  |
| id_serviços|

- **Unicidade** (valores únicos)*:

| Nome       | Coluna(s)  | Indexar |
| -----------| ---------  | ------- |
| id_serviços| id_serviços| Sim     |


### Tabela_Marcações

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da Tabela Marcações

#### COLUNAS <!-- omit in toc -->

| Nome           | Descrição                    | Domínio     | por Omissão | Automático | Nulo |
| :-------       | :------------------------    | :---------- | :---------- | :--------- | :--- |
| Id_Marcações   | Identificador da marcação    | Int(11)     | -           | Sim        | Não  |
| Cliente_NIF    | NIF do cliente               | Int(11)     | -           | Não        | Não  |
| Id_Serviços    | Identificador dos serviços   | Int(11)     | -           | Não        | Não  |
| Id_Profissional| Identificador do profissional| Int(11)     | -           | Não        | Não  |
| Dia            | Dia da marcação              | Date        | -           | Não        | Não  |
| Hora           | Hora da marcação             | TIME        | -           | Não        | Não  |
| Estado         | Estado do marcação           | VARCHAR(45) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s)   |
| ---------   |
| Id_Marcações|

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| Cliente_NIF | Nome      | Sim     |

---
| [< Previous](rebd03.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd05.md) |
| :---------------------- | :------------------------------------------------------: | ------------------: |
