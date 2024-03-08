# BD: Guião 3


## ​Problema 3.1
 
### *a)*

```
Estão incluídas as fk.

Cliente     : NIF, num_carta, endereco, nome;
Balcao      : numero, nome, endereco;
Veiculo     : matricula, marca, ano, TipoVeiculo_codigo;
Tipo Veiculo: codigo, arcondicionado, designacao;
Similaridade: TipoVeiculo_codigo1, TipoVeiculo_codigo2;
Aluguer     : numero, data, duracao, cliente_nif, veiculo_matricula, balcao_numero;
Ligeiro     : num_lugares, portas, combustivel, TV_Codigo:
Pesado      : peso, passageiros, TV_Codigo; 
```

### *b)* 

```
Chaves Candidatas/{Primarias}:
    Cliente     : {NIF}, num_carta;
    Balcao      : {numero};
    Veiculo     : {matricula};
    Tipo Veiculo: {codigo}, designacao (em princípio não existe 1 designação para 2 tipos);
    Similaridade: {TipoVeiculo_codigo1, TipoVeiculo_codigo2};
    Aluguer     : {numero},
    Ligeiro     : {TV_Codigo};
    Pesado      : {TV_Codigo};

Chaves Estrangeiras:
    Cliente     : --
    Balcao      : --
    Veiculo     : TipoVeiculo_codigo;
    Tipo Veiculo: --
    Similaridade: TipoVeiculo_codigo1, TipoVeiculo_codigo2;
    Aluguer     : cliente_nif, veiculo_matricula, balcao_numero;
    Ligeiro     : TV_Codigo;
    Pesado      : TV_Codigo;  

```


### *c)* 

![ex_3_1c!](ex_3_1c.jpg "AnImage")


## ​Problema 3.2

### *a)*

```
Estão incluídas as fk.

Airport         : Airport_code, City, State, Name;
Flight          : Number, Airline, Weekdays;
Flight_Leg      : Leg_no, Flight_Number, AirportDep_Code, AirportArr_Code, Scheduleded_dep_time, Scheduled_arr_time;
Leg_Instance    : Leg_no, Flight_Number, Date, No_of_avail_seats, Airplane_Id, AirportDep_Code, AirportArr_Code, Dep_time, Arr_time; 
Seat            : Leg_no, Flight_Number, Date, Seat_no, Customer_name, Cphone;
Airplane        : Airplane_id, Total_no_of_seats, AirplaneType_Type_name;
Airplane_Type   : Type_name, Max_seats, Company;
Can_Land        : Airport_Airport_Code, Airplane_Type_Type_name;
Fare            : Code, Amount, Restrictions, Flight_Number
```


### *b)* 

```
Chaves Candidatas/{Primárias}:
    Airport         : {Airport_code};
    Flight          : {Number};
    Flight_Leg      : {Leg_no, Flight_Number}, AirportDep_Code, AirportArr_Code, Scheduleded_dep_time, Scheduled_arr_time;
    Leg_Instance    : {Leg_no, Flight_Number, Date}, Airplane_Id, AirportDep_Code, AirportArr_Code, Dep_time, Arr_time; 
    Seat            : {Leg_no, Flight_Number, Date, Seat_no}, Customer_name, Cphone;
    Airplane        : {Airplane_id};
    Airplane_Type   : {Type_name};
    Can_Land        : {Airport_Airport_Code, Airplane_Type_Type_name};
    Fare            : {Code, Flight_Number};

Chaves Estrangeiras:
    Airport         : --
    Flight          : --
    Flight_Leg      : Flight_Number, AirportDep_Code, AirportArr_Code, Scheduleded_dep_time, Scheduled_arr_time;
    Leg_Instance    : Leg_no, Flight_Number, Airplane_Id, AirportDep_Code, AirportArr_Code, Dep_time, Arr_time; 
    Seat            : Leg_no, Flight_Number, Date, Customer_name, Cphone;
    Airplane        : AirplaneType_Type_name;
    Airplane_Type   : --
    Can_Land        : Airport_Airport_Code, Airplane_Type_Type_name;
    Fare            : Flight_Number;

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