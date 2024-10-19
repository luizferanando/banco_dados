create table investimentos(
    id_investimento integer primary key not null,
    nome varchar(100),
    valor_inicial numeric(7,2),
    rendimento_mensal numeric(6,2),
    recebimento_mensal numeric(6,2),
)
select * from investimentos

INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (1, 'tesouro direto', 5000.00, 50.00, 52.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (2, 'fundo imobiliário', 10000.00, 120.00, 124.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (3, 'XPMM', 15000.00, 200.00, 205.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (4, 'mini dólar', 8000.00, 80.00, 82.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (5, 'Criptomoedas', 3000.00, 40.00, 41.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (6, 'PetroGás', 7000.00, 70.00, 72.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (7, 'fundo imobiliário', 11000.00, 130.00, 134.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (8, 'XPMM', 16000.00, 210.00, 215.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (9, 'mini dólar', 9000.00, 90.00, 92.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (10, 'Criptomoedas', 4000.00, 50.00, 52.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (11, 'PetroGás', 7500.00, 75.00, 77.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (12, 'tesouro direto', 5200.00, 52.00, 54.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (13, 'fundo imobiliário', 10200.00, 122.00, 126.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (14, 'XPMM', 15200.00, 202.00, 207.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (15, 'mini dólar', 8200.00, 82.00, 84.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (16, 'Criptomoedas', 3200.00, 42.00, 43.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (17, 'PetroGás', 7200.00, 72.00, 74.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (18, 'tesouro direto', 5400.00, 54.00, 56.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (19, 'fundo imobiliário', 10400.00, 124.00, 128.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (20, 'XPMM', 15400.00, 204.00, 209.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (21, 'mini dólar', 8400.00, 84.00, 86.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (22, 'Criptomoedas', 3400.00, 44.00, 45.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (23, 'PetroGás', 7400.00, 74.00, 76.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (24, 'tesouro direto', 5600.00, 56.00, 58.00);
INSERT INTO investimentos(id_investimento, nome, valor_inicial, rendimento_mensal, recebimento_mensal) VALUES (25, 'fundo imobiliário', 10600.00, 126.00, 130.00);

--retornar o número total de investimentos cadastrados
select count(*) from investimentos
--Retornar o número total de investimentos cadastrados no tesouro direto:
select count(*) from investimentos where nome = 'tesouro direto'

---descobrir o maior valor investido
select max(valor_inicial) from investimentos
---descobrir o menor valor investido
select min(valor_inicial) from investimentos

--Descobri a média do rendimento mensal
select avg(recebimento_mensal) from investimentos

--select o valor total dos investimentos
select sum(valor_inicial) from investimentos

--colocar um apelido na coluna do select
--sem apelido (aliás)
select sum(valor_inicial),sum(rendimento_mensal),sum(recebimento_mensal) from investimentos
--com aliás
select sum(valor_inicial) as valor_inicial,sum(rendimento_mensal) "rendimento_mensal",sum(recebimento_mensal) recebimento_mensal from investimentos

--concatenação
select 'Investimento : '|| sum(valor_inicial) ||' Rendimentos: '|| sum(rendimento_mensal) as Valores  from investimentos

--Descobri a média do rendimento mensal com round -Arredonda v com s casas decimais
select avg(recebimento_mensal),round(avg(recebimento_mensal)) from investimentos
select round(avg(recebimento_mensal),2) from investimentos
