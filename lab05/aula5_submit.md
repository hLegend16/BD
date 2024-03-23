# BD: Guião 5


## ​Problema 5.1
 
### *a)*

```
Write here your answer:
π employee.Fname, employee.Lname, employee.Ssn, project.Pname (project ⨝ project.Pnumber = works_on.Pno works_on ⨝ works_on.Essn = employee.Ssn employee)
```


### *b)* 

```
... Write here your answer ...
π employee.Fname, employee.Minit, employee.Lname (employee ⨝ ( Super_ssn = carlos.Ssn ) ρ carlos ( π Ssn ( σ Fname = 'Carlos' and Minit = 'D' and Lname = 'Gomes' (employee))))
```


### *c)* 

```
... Write here your answer ...
γ Pname; SUM(Hours)→WORKED_HOURS (employee ⨝ Ssn = Essn (project ⨝ project.Pnumber = works_on.Pno works_on))
```


### *d)* 

```
... Write here your answer ...
π employee.Fname, Minit, Lname ( σ Dno = 3 and Hours > 20 and Pname = 'Aveiro Digital' (employee ⨝ employee.Ssn = works_on.Essn works_on ⨝ works_on.Pno = project.Pnumber project))
```


### *e)* 

```
... Write here your answer ...
π employee.Fname, Lname, Ssn ( σ Pno = null (employee ⟕ Ssn = Essn works_on))
```


### *f)* 

```
... Write here your answer ...
γ Dname; AVG(Salary)→meida_salarios σ Sex = 'F' (department ⨝ Dnumber = Dno employee)
```


### *g)* 

```
... Write here your answer ...
π employee.Fname, Minit, Lname, Ssn (employee ⨝ Ssn = Essn ( σ number_dependets > 2 γ Essn; COUNT(Dependent_name)→number_dependets dependent))
```


### *h)* 

```
... Write here your answer ...
π employee.Fname, Minit, Lname, Ssn σ dependent.Essn = null ((employee ⨝ Ssn = Mgr_ssn department) ⟕ Ssn = Essn dependent)
```


### *i)* 

```
... Write here your answer ...
π employee.Fname, Minit, Lname, Address ( σ dept_location.Dlocation ≠ 'Aveiro' and project.Plocation = 'Aveiro' ((project ⨝ Pnumber = Pno (employee ⨝ Ssn = Essn works_on)) ⨝ Dno = department.Dnumber (department ⨝ department.Dnumber = dept_location.Dnumber dept_location)))
```


## ​Problema 5.2

### *a)*

```
... Write here your answer ...
π fornecedor.nif, nome, endereco, tipo ( σ numero = null (fornecedor ⟕ nif = fornecedor encomenda))
```

### *b)* 

```
... Write here your answer ...
γ codigo, nome, preco; AVG(item.unidades)→med_unidades (produto ⨝ codigo = codProd item)
```


### *c)* 

```
... Write here your answer ...
γ ; AVG(total_produto)→med_prod_enc ( γ numero, data; COUNT(numEnc)→total_produto (encomenda ⨝ numero = numEnc item))
```


### *d)* 

```
... Write here your answer ...
γ fornecedor.nome, produto.codigo, produto.nome; SUM(item.unidades)→total_unidades (((fornecedor ⨝ nif = fornecedor encomenda) ⨝ numero = numEnc item) ⨝ codProd = codigo produto)
```


## ​Problema 5.3

### *a)*

```
... Write here your answer ...
π paciente.numUtente, nome, dataNasc ( σ prescricao.numPresc = null (paciente ⟕ paciente.numUtente = prescricao.numUtente prescricao))
```

### *b)* 

```
... Write here your answer ...
γ especialidade; COUNT(numPresc)→pres_especialidade (medico ⨝ numSNS = numMedico prescricao)
```


### *c)* 

```
... Write here your answer ...
γ farmacia; COUNT(numPresc)→num_pres (farmacia ⨝ nome = farmacia prescricao)
```


### *d)* 

```
... Write here your answer ...
( π farmaco.nome ( σ numRegFarm = 906 (farmaco))) - ( π presc_farmaco.nomeFarmaco ( σ numRegFarm = 906 (presc_farmaco)))
```

### *e)* 

```
... Write here your answer ...
γ farmacia.nome, farmaceutica.nome; COUNT(farmaceutica.nome)→vendas (farmaceutica ⨝ numReg = numRegFarm ( π presc_farmaco.numPresc, numRegFarm, nomeFarmaco, nome (presc_farmaco ⨝ presc_farmaco.numPresc = prescricao.numPresc (farmacia ⨝ nome = farmacia prescricao))))
```

### *f)* 

```
... Write here your answer ...
σ medicos > 1 ( γ paciente.nome, paciente.numUtente; COUNT(medico.nome)→medicos (medico ⨝ numSNS = numMedico (paciente ⨝ paciente.numUtente = prescricao.numUtente prescricao)))
```
