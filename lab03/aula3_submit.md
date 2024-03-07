# BD: Guião 3


## ​Problema 3.1
 
### *a)*

```
Cliente     : NIF, num_carta, endereco, nome;
Balcao      : numero, nome, endereco;
Veiculo     : matricula, marca, ano;
Tipo Veiculo: codigo, arcondicionado, designacao;
Aluguer     : numero, data, duracao;
Ligeiro     : num_lugares, portas, combustivel:
Pesado      : peso, passageiros; 
```

### *b)* 

```
Chaves Candidatas/{Primarias}:
    Cliente     : {NIF}, num_carta;
    Balcao      : {numero};
    Veiculo     : {matricula};
    Tipo Veiculo: {codigo}, designacao (em princípio não existe 1 designação para 2 tipos);
    Aluguer     : {numero},
    Ligeiro     : {TV_Codigo};
    Pesado      : {TV_Codigo};

Chaves Estrangeiras:


```


### *c)* 

![ex_3_1c!](ex_3_1c.jpg "AnImage")


## ​Problema 3.2

### *a)*

```
... Write here your answer ...
```


### *b)* 

```
... Write here your answer ...
```


### *c)* 

![ex_3_2c!](ex_3_2c.jpg "AnImage")


## ​Problema 3.3


### *a)* 2.1

![ex_3_3_a!](ex_3_3a.jpg "AnImage")

### *b)* 2.2

![ex_3_3_b!](ex_3_3b.jpg "AnImage")

### *c)* 2.3

![ex_3_3_c!](ex_3_3c.jpg "AnImage")

### *d)* 2.4

![ex_3_3_d!](ex_3_3d.jpg "AnImage")