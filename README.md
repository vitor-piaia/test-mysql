# Teste MySQL para Desenvolvedor

## SQL:
select cliente.*, casa.cor, bairro.nome, GROUP_CONCAT(carro.modelo) as modelos
from cliente
inner join casa on cliente.id_cliente = casa.fk_cliente
inner join bairro on casa.fk_bairro = bairro.id_bairro
left join carro on cliente.id_cliente = carro.fk_cliente
group by cliente.id_cliente, cliente.nome, cliente.sobrenome, cliente.data_nascimento, casa.cor, bairro.nome;

## Objetivo:
Fazer uma query que retorne o relatório abaixo:
- Todos os clientes, cor de suas casas, seus bairros, seus carros

## Requisitos:
- Utilizar o dump desse projeto;
