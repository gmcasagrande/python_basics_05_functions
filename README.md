# python_basics_functions
Learning Python. Using def
- def
- return
- None

# 1) Números primos - como encontrá-los
Um número natural é primo se for maior que 1 e não tiver divisores diferentes de 1 e ele próprio.\
Complicado? Não mesmo. Por exemplo, 8 não é um número primo, pois você pode dividi-lo por 2 e 4 (não podemos usar divisores iguais a 1 e 8, pois a definição proíbe isso).\
Por outro lado, 7 é um número primo, pois não podemos encontrar divisores legais para ele.\
Sua tarefa é escrever uma função verificando se um número é primo ou não.

A função:
- é chamado is_prime;
- requer um argumento (o valor a ser verificado)
- retorna True se o argumento for um número primo e False caso contrário.

Dicas:
- Tente dividir o argumento por todos os valores subsequentes (começando em 2) e verifique o restante - se for zero, seu número não pode ser um primo; pense bem quando deve interromper o processo.
- Se você precisar conhecer a raiz quadrada de qualquer valor, poderá utilizar o operador \*\*. Lembre-se: a raiz quadrada de x é o mesmo que x\*\*0.5

Preencha o código no editor.\
Execute o código e verifique se a saída é igual à nossa.\
Saída prevista:
> 2 3 5 7 11 13 17 19

```python
def is_prime(num):
  #
  # Escreva seu código aqui.
  #

for i in range(1, 20):
  if is_prime(i + 1):
  print(i + 1, end=" ")
print()
```

# 2. Convertendo combustíveis
O consumo de combustível de um carro pode ser expresso de várias maneiras diferentes. Por exemplo, na Europa, ele é mostrado como a quantidade de combustível consumida por 100 quilômetros.\
Nos EUA, é mostrado como o número de quilômetros percorridos por um carro usando um litro de combustível.\
Sua tarefa é escrever um par de funções convertendo l/100 km em mpg (milhas por galão) e vice-versa.

As funções:
- são nomeados liters_100km_to_miles_gallon e miles_gallon_to_liters_100km respectivamente;
- use um argumento (o valor correspondente aos nomes)

Aqui estão algumas informações para ajudá-lo:

- 1 milha americana = 1609.344 metros;
- 1 galão americano = 3,785411784 litros.

Saída prevista:

> 60.31143162393162\
> 31.36194444444444\
> 23.52145833333333\
> 3.9007393587617467\
> 7.490910297239916\
> 10.009131205673757

```python
def liters_100km_to_miles_gallon(liters):
  #
  # Escreva seu código aquie your code here.
  #

def miles_gallon_to_liters_100km(miles):
  #
  # Escreva seu código aqui.
  #

print(liters_100km_to_miles_gallon(3.9))
print(liters_100km_to_miles_gallon(7.5))
print(liters_100km_to_miles_gallon(10.))
print(miles_gallon_to_liters_100km(60.3))
print(miles_gallon_to_liters_100km(31.4))
print(miles_gallon_to_liters_100km(23.5))
```
\
\
*as tarefas 3, 4 e 5 são sobre ano bissexto e são codependentes, devem ser feitas em sequência*
# 3) Um ano bissexto
Sua tarefa é escrever e testar uma função que usa um argumento (um ano) e retorna True se o ano for um ano bissexto ou False caso contrário.
- A semente da função já é mostrada no código esqueleto do editor.
- Nota: também preparamos um código de teste curto, que você pode usar para testar sua função.
- O código usa duas listas - uma com os dados de teste e a outra contendo os resultados esperados. O código informará se algum dos resultados é inválido.
```python
def is_year_leap(year):
  #
  # Escreva seu código aqui
  #
test_data = [1900, 2000, 2016, 1987]
test_results = [False, True, True, False]
for i in range(len(test_data)):
  yr = test_data[i]
  print(yr,"->",end="")
  result = is_year_leap(yr)
  if result == test_results[i]:
    print("OK")
  else:
    print("Fracassado")
```
\
\
*as tarefas 3, 4 e 5 são sobre ano bissexto e são codependentes, devem ser feitas em sequência*
# 4) Quantos dias
Sua tarefa é escrever e testar uma função que usa dois argumentos (um ano e um mês) e retorna o número de dias para o determinado par de ano-mês (embora apenas fevereiro seja sensível ao valor do year, sua função deve ser universal).
- A parte inicial da função está pronta. Agora, convença a função a não retornar None se os argumentos não fizerem sentido.
- Obviamente, você pode (e deve) usar a função previamente testada e escrita da tarefa anterior. Pode ser muito útil. Recomendamos que você use uma lista com os comprimentos dos meses. Você pode criá-lo dentro da função - esse truque diminuirá significativamente o código.
- Preparamos um código de teste. Expanda-o para incluir mais casos de teste.
```python
def is_year_leap(year):
  #
  # Seu código da tarefa anterior.
  #

def days_in_month(year, month):
  #
  # Escreva seu novo código aqui.
  #

test_years = [1900, 2000, 2016, 1987]
test_months = [2, 2, 1, 11]
test_results = [28, 29, 31, 30]
for i in range(len(test_years)):
  yr = test_years[i]
  mo = test_months[i]
  print(yr, mo, "->", end="")
  result = days_in_month(yr, mo)
  if result == test_results[i]:
    print("OK")
  else:
    print("Fracassado")
```
\
\
*as tarefas 3, 4 e 5 são sobre ano bissexto e são codependentes, devem ser feitas em sequência*
# 5) Dia do ano
Sua tarefa é escrever e testar uma função que usa três argumentos (um ano, um mês e um dia do mês) e retorna o dia correspondente do ano ou retorna None se algum dos argumentos for inválido.
- Use as funções escritas e testadas anteriormente. Adicione seus próprios casos de teste ao código.
```python
def is_year_leap(year):
#
# Seu código da tarefa anterior.
#

def days_in_month(year, month):
#
# Seu código da tarefa anterior.
#

def day_of_year(year, month, day):
#
# Escreva seu código aqui.
#

print(day_of_year(2000, 12, 31))
```
\
\
*as tarefas 6, 7, 8 e 9 não são códigos para resolver, apenas para visualizar e responder*
# 6) Qual a saída do trecho de código?
```python
def hi():
  return
  print("Oi!")
 
hi()
```
\
\
*as tarefas 6, 7, 8 e 9 não são códigos para resolver, apenas para visualizar e responder*
# 7) Qual a saída do trecho de código?
```python
def is_int(data):
  if type(data) == int:
    return True
  elif type(data) == float:
    return False
 
print(is_int(5))
print(is_int(5.0))
print(is_int("5"))
```
\
\
*as tarefas 6, 7, 8 e 9 não são códigos para resolver, apenas para visualizar e responder*
# 8) Qual a saída do trecho de código?
```python
def even_num_lst(ran):
  lst = []
  for num in range(ran):
    if num % 2 == 0:
      lst.append(num)
    return lst
 
print(even_num_lst(11))
```
\
\
*as tarefas 6, 7, 8 e 9 não são códigos para resolver, apenas para visualizar e responder*
# 9) Qual a saída do trecho de código?
```python
def list_updater(lst):
  upd_list = []
  for elem in lst:
    elem **= 2
    upd_list.append(elem)
  return upd_list
 
foo = [1, 2, 3, 4, 5]
print(list_updater(foo))
```
