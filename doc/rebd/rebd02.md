# C2 : Esquema conceptual

## Modelo E/A
Atributos:
- Cliente1 (clienteNIF, nome, morada, número de telemóvel ou telefone, email)
- Serviço1 (IDserviço, serviçoNome, serviçoPreço)
- Profissionais1 (IDprofissional, profissionalNome, profissionalContacto)
- Marcação1 (IDMarcação, dia, hora)

(*IDMarcação, clienteNIF, IDserviço, IDprofissional – atributo-chave*) 

Associações:
- Marcação -> EfetuadoPara -> Profissionais
- Marcação -> Agenda -> Serviços
- Marcação -> EfetuadoPor -> Cliente

A fotografia do diagrama irá estar anexada no repositório.

## Regras de negócio adicionais (Restrições)
O cliente só poderá cancelar a sua marcação até 24h antes. Caso pretenda cancelar, deve entrar em contacto com a Barbearia, para que lhe cancelem a marcação e só após a desmarcação, o cliente poderá novamente remarcar o seu pedido.

---
[< Previous](rebd01.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd03.md)
:--- | :---: | ---: 
