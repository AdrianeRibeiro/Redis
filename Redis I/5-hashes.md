# Hashes

```
> HSET resultado:24-05-2015:megasena "numero" "13, 17, 19, 25, 28, 32"

> HSET resultado:24-05-2015:megasena "ganhadores" 23
```

```
> HGET resultado:24-05-2015:megasena "numero"

> HGET resultado:24-05-2015:megasena "ganhadores"
```

```
> HDEL resultado:24-05-2015:megasena "numero"
```

```
> HMSET resultado:05-06-2015:megasena "numeros" "5, 19, 23, 28, 46, 49" "ganhadores" "16"
```

```
> HGETALL "resultado:05-06-2015:megasena"
1) "numeros"
2) "5, 19, 23, 28, 46, 49"
3) "ganhadores"
4) "16"

```
