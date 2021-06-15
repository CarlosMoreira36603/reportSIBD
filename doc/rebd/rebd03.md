# C3 : Normalização

## Relações
Relação:
- Marcacao (Id_Marcacao, Cliente_NIF, Id_servicos, Id_profissional, Dia, Hora, Estado)
(Marcacao – Cumpre com a 4NF)

- Chaves Primarias:
(idmarcacao)

- Chaves estrangeira:
(clienteNIF, idservicos, idprofissional)

Relações Encontradas:
- ClienteNIF (nome, morada, numero, email)
- idservicos (servico_nome, servico_preco)
- idprofissional (profissionalnome, profissionalcontacto)



## Normalização do Esquema Relacional

Dependências Funcionais:
- Id_Marcacao -> Cliente_NIF, Id_servicos, Id_profissional, Dia, Hora, Estado


---
[< Previous](rebd02.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd04.md)
:--- | :---: | ---: 
