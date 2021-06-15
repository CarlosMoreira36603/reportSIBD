# C3 : Esquema conceptual

## Modelo E/A
Atributos:
- Cliente1 (clienteNIF, nome, morada, número de telemóvel ou telefone, email)
- Serviço1 (IDserviço, serviçoNome, serviçoPreço)
- Profissionais1 (IDprofissional, profissionalNome, profissionalContacto)
- Marcação1 (IDMarcação, dia, hora)

(*IDMarcação, clienteNIF, IDserviço, IDprofissional – atributo-chave*) 

Associações:
-Marcação -> EfetuadoPara -> Profissionais
-Marcação -> Agenda -> Serviços
-Marcação -> EfetuadoPor -> Cliente


Diagrama do modelo relacional. A fotografia da mesma irá estar anexada no repositório.   



## Regras de negócio adicionais (Restrições)
_(Apresentar uma lista detalhada das regras e restrições não possíveis de representar no modelo E/A, que visam a manutenção da consistência e integridade da modelação do problema)_

---
[< Previous](rei02.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | Next >
:--- | :---: | ---: 
