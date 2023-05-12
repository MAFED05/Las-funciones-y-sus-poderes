# LAS FUNCIONES Y SUS PODERES
## Punto 1

De los retos anteriores seleciones 3 funciones y escribalas en forma de lambdas.

### A. Calcular el perímetro de un rectángulo

#### Solución

``` python
if __name__ == "__main__":
  base = float(input("Ingrese la base del rectángulo: ")) #Se le solicita al usuario que ingrese los datos para poder realizar la operación
  altura = float(input("Ingrese la altura del rectángulo: "))
  perímetroRectángulo = lambda base, altura: (base*2)+(altura*2) #Definimos la operación por medio de lamba
  perímetro_rectángulo = perímetroRectángulo(base, altura) #Le damos un nombre al resultado de la operación
  print("El perímetro del rectángulo con base", base, "y altura", altura, "es", perímetro_rectángulo) #Imprimimos el resultado
```

#### Código funcionando

[![Captura-de-pantalla-2023-04-25-124843.png](https://i.postimg.cc/ht261nsZ/Captura-de-pantalla-2023-04-25-124843.png)](https://postimg.cc/3kDt3PP2)

### B. Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses

#### Solución

``` python
if __name__ == "__main__":
  c = float(input("Introduce el monto del préstamo: ")) #Le solicitamos al usuario que ingrese los datos necesarios para la operación
  i = float(input("Introduce la tasa de interés en porcentaje: "))
  n = int(input("Introduce el número de meses: "))
  valorPrestamo = lambda c, i, n: c * (1 + (i/100)) ** n #Definimos la operación a realizar
  valor_prestamo = valorPrestamo(c, i, n) #Le damos un nombre al resultado de la operación anterior 
  print("El valor del préstamo después de", n, "meses es:", round(valor_prestamo, 3)) #Imprimimos el resultado
```

#### Código funcionando

[![Captura-de-pantalla-2023-04-25-125740.png](https://i.postimg.cc/Bv4FfQqM/Captura-de-pantalla-2023-04-25-125740.png)](https://postimg.cc/VJZvjw0C)

### C. Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

#### Solución

``` python
if __name__ == "__main__":
  n = int(input("Ingrese la cantidad de gallinas: ")) #Solicitamos los datos con los que vamos a hacer el procedimiento
  m = int(input("Ingrese la cantidad de gallos: "))
  k = int(input("Ingrese la cantidad de pollitos: "))
  pesoAnimales = lambda n, m, k: (6*n)+(7*m)+(1*k) #Colocamos el procedimiento en forma de Lambda
  peso_animales = pesoAnimales(n, m, k) #Le definimos un nommbre al resultado del procedimiento
  print("El peso total de", n , "gallinas", m , "gallos y", k , "pollitos es de", peso_animales, "kg") #Imprimimos el resultado
```

#### Código funcionando

[![Captura-de-pantalla-2023-04-25-125840.png](https://i.postimg.cc/wMp789Y9/Captura-de-pantalla-2023-04-25-125840.png)](https://postimg.cc/qh1k2V7F)

## Punto 2

De los retos anteriores seleciones 3 funciones y escribalas con argumentos no definidos (*args).

### A. Calcular el área de un rectángulo

#### Solución

``` python
def area_rectangulo(*args): #Creamos la función y como podemos ver no le otorgamos argumentos definidos
    if len(args) == 2: #Como no trabajaremos un bucle sino una operación definida entonces definimos que se deberan ingresar 2 argumentos
        base, altura = args #Colocamos que la base y la altura serán los argumentos a ingresar
        area = base * altura # Definimos la operación a realizar
        return area

if __name__=="__main__": #Definimos la función principal
    base = float (input("Ingrese la base del rectángulo")) #Le solicitamos al usuario que ingrese los datos necesarios
    altura = float (input("Ingrese la altura del rectángulo"))
    print ("El área del rectángulo es: ", str(area_rectangulo(base,altura))) #Imprimimos el resultado}
```

#### Código funcionando

[![Captura-de-pantalla-2023-04-25-130013.png](https://i.postimg.cc/MGp7Q6X2/Captura-de-pantalla-2023-04-25-130013.png)](https://postimg.cc/K1C3XynJ)

### B. Calcular el perímetro rectángulo

#### Solución

``` python
def calcularPerímetroRectángulo (*args)->float: #Definimos la función sin argumentos
    if len(args) == 2: #Le indicamos a la función que serán necesarios 2 argumentos para que pueda operarse 
        base, altura = args #Le indicamos a la función cuales son los argumentos para que funcione
        perímetroRectángulo=(base*2)+(altura*2) #Definimos el procedimiento a realizar
        return perímetroRectángulo #Le decimos a la función que nos devuelva el resultado de la operación anterior

if __name__=="__main__": #Definimos la función principal
    base = float (input("Ingrese la base del rectángulo")) #Le solicitamos al usuario que ingrese los datos necesarios para la función
    altura = float (input("Ingrese la altura del rectángulo"))

    print ("El perímetro del rectángulo es: ", str(calcularPerímetroRectángulo(base,altura)))#Imprimimos el resultado final
```

#### Código funcionando

[![Captura-de-pantalla-2023-04-25-130128.png](https://i.postimg.cc/pLG93DV4/Captura-de-pantalla-2023-04-25-130128.png)](https://postimg.cc/xXmTzNz3)

### C. Calcular el área de un círculo

#### Solución

``` python
from math import pi #De la libreria importamos pi
def calcularAreaCírculo(*args)->float: #Definimos la función de la operación
   if len (args) == 2: #Le indicamos a la función que deberá tener 2 argumentos para que funcione
    radio, pi =args #Le decimos cuales son los argumentos 
   areaCírculo=((pi)*(radio**2)) #Definimos la operación a realizar
   return areaCírculo #Retornamos el resultado de la operación realizada

if __name__=="__main__": #Definimos la función principal
    radio = float (input("Ingrese el radio del círculo"))#Le solicitamos al usuario que ingrese el dato necesario
    print ("El área del círculo con radio:", radio, "es", str(calcularAreaCírculo(radio,pi))) #Imprimimos el resultado
```
#### Código funcionando

[![Captura-de-pantalla-2023-04-25-130300.png](https://i.postimg.cc/wj7xynH4/Captura-de-pantalla-2023-04-25-130300.png)](https://postimg.cc/bZff4CZ1)

## Punto 3

Escriba una función recursiva para calcular la operación de la potencia.

#### Solución

``` python
def potencia_recursiva(base:float, exponente:int):#Definimos la función para la operación
    """
    Esta función calcula una potencia
    Argumentos:
    base: float 
    exponente: int #numero que multiplica cierta cantidad de veces
    Devuelve: el resultado de la base elevada a exponente veces
    """
    if exponente==0:# Caso base: Cualquier número elevado a o es 1
        return 1
    if exponente== 1:# Cualquier número elevado a 1 es ese mismo número
        return base
    else:
        return base*potencia_recursiva(base, exponente-1) #Caso recursivo
if __name__ == "__main__":  #Función principal
    base= float(input("ingrese el numero base:")) #Solicitar los datos necesarios
    exponente= int(input("Ingrese su exponente:"))
    print("El resultado de", base, "con exponente", exponente, "es:", str(potencia_recursiva(base, exponente))) #Imprimimos el resultado final
```


#### Código funcionando

[![Captura-de-pantalla-2023-04-25-130341.png](https://i.postimg.cc/sD2sqbBf/Captura-de-pantalla-2023-04-25-130341.png)](https://postimg.cc/yW2MSQX2)

## Punto 4

Realice pruebas para calcular fibonacci con iteración o con recursión. Determine desde que número de la serie la diferencia de tiempo se vuelve significativa.

``` python
import timeit #Se importa la libreria a ser utilizada

def fibo(n : int )-> int: #Se define la función base
  i : int = 1
  # Caso base
  n1 : int = 0
  n2 : int = 1
  while(i <= n):
    # Condición
    sumFibo = n1 + n2
    # Actualización
    n1 = n2
    n2 = sumFibo
    i += 1
  return sumFibo #Retorna el resultado

if __name__ == "__main__": #Función principal
  num = int(input("Ingrese numero: ")) #Solicitamos el dato necesario   
  start_time1 = timeit.default_timer() #Sew inicia a contar el tiempo de ejecución
  serieFibo = fibo(num)
  timer1= timeit.default_timer() - start_time1 #Se finaliza de contar el tiempo de ejecución
  print(f"El último número de la serie de Fibonacci hasta {num} es {serieFibo}") #Se imprimen los resultados
print(f"fibo se demoró {timer1} en correr")


def fiboRecursivo(n : int )-> int: #Se define la función del caso recursivo
    if n <=1:
        # Caso base
        return 1
    else:
        # Condición
        return fiboRecursivo(n-1)+fiboRecursivo(n-2)  #Retorna el resultado
    
if __name__ == "__main__": #Función principal 
  num = int(input("Ingrese numero: ")) #Solicitamos los datos necesarios
  start_time2 = timeit.default_timer() #Se inicia a contabilizar el tiempo
  serieFibo = fiboRecursivo(num)
  timer2 = timeit.default_timer() - start_time2 #Se detiene el contador
  print(f"El último número de la serie de Fibonacci hasta {num} es {serieFibo}") #Se imprimen los resultados
print(f"fiboRecursivo se demoró {timer2} en correr")
```

#### Código funcionando

[![Captura-de-pantalla-2023-05-12-113253.png](https://i.postimg.cc/xjpRMR6H/Captura-de-pantalla-2023-05-12-113253.png)](https://postimg.cc/6TRnNdJ5)

## Punto 5

Crear cuenta en stackoverflow y adjuntar imagen en el repo

[![Captura-de-pantalla-2023-04-25-130449.png](https://i.postimg.cc/B6ykz7Rb/Captura-de-pantalla-2023-04-25-130449.png)](https://postimg.cc/XGfsGLj6)

## Punto 6
Crear perfil en Linkedin

[Perfil personal](https://www.linkedin.com/in/maria-fernanda-duarte-parra-106a7a272/)
