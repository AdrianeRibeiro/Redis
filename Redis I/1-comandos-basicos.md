# Redis 

- Redis é uma ferramenta usada para armazenamento de chave:valor 
Tem o com intuito de melhorar a performance de sistemas
- Podemos utilizar o Redis para armazenar informações da sessão web de um usuário para os casos em que um site possui mais de um servidor. Ao utilizar o Redis nesse cenário, temos o compartilhamento de informações entre diferentes instâncias.

# Comandos Básicos

- ECHO: escrever
- SET: setar chave-valor
- GET: pegar valor
- DEL: deletar chave-valor
- MSET: setar múltiplos valores de uma vez:

# Exemplos:

```
> SET "ultimo_sorteio" "2, 15, 18, 30, 35, 42"

> GET "ultimo_sorteio"
```

```
> MSET resultado:03-05-2015:megasena "1, 3, 17, 19, 24, 26" 
resultado:22-04-2015:megasena "15, 18, 20, 32, 27, 41" 
resultado:15-04-2015:megasena "10, 15, 18, 22, 35, 43"
```