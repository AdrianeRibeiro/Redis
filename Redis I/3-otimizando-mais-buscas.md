# Filtrando as buscas: *

Podemos utilizar o caractere * para buscar a correspondência de um ou mais caracteres dentro de uma chave. Portanto, se executarmos o comando KEYS al*ra temos correspondência com "alra", "alura" e "aluuura", por exemplo.
 

# Exemplos

Exemplo 1: Todas as chaves que possuem resultado:

```
> KEYS "resultado*"
```

Exemplo 2: Chaves que correspondem aos resultados de todos os sorteios da Mega-sena realizados no mês de Abril de 2015:

```
> KEYS "resultado*-04-2015:megasena"

O "*" indica que qualquer coisa depois de "resultado" e antes de "-04-2015:megasena" correspondem ao padrão.

```

Exemplo 3: Buscar os resultados entre o dia 01 e 09 de Maio de 2015?

```
> KEYS resultado:0*-05-2015:megasena
```

Exemplo 4: Buscar os resultados entre o dia 10 e 19 de Maio de 2015?

```
> KEYS "resultado:1*-05-2015:megasena"
> KEYS "resultado:1?-05-2015:megasena"
```

# Limitando dígitos: ?

Podemos garantir a existência de apenas um caractere utilizando um "?" no lugar do "*":

```
> KEYS resultado:0?-05-2015:megasena
1) "resultado:03-05-2015:megasena"
```

Dessa forma, uma chave que por acaso tenha o nome "resultado:0345-05-2015:megasena", não seria retornada na busca, como ocorreria se fosse usado "*".