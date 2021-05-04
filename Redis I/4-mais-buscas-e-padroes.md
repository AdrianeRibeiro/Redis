- "*" diversos caracteres
- ? um caracter

# ou: []

Exemplo 1: Pegar resultados da megasena do dia 3 ou 7:

```
> KEYS "resultado:?3-??-????:megasena"

> KEYS "resultado:?7-??-????:megasena"

> KEYS "resultado:?[37]-??-????:megasena"
```

Exemplo 2: Obter as chaves que representam os resultados dos dias 15 ou 17 de qualquer mês, de qualquer ano, da Mega-sena ou da Giga-sena?

```
> KEYS "resultado:1[57]-??-????:*sena"
```