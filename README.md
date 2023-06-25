# trabajo
# Burdel Los Gusaneros

El programa comienza mostrando un mensaje de bienvenida al burdel.

Luego, utiliza un objeto Scanner para obtener la entrada del usuario. Solicita el número de prostitutas deseadas y el presupuesto.

Se crean varios arreglos para almacenar los datos de cada prostituta: precios, razas, géneros y resultados (vuelta).

A continuación, se utiliza un bucle for para iterar sobre cada prostituta y obtener su información. Pide el método de pago, la raza, el precio y el género. Verifica que se ingresen valores válidos para el método de pago y el género.

El programa calcula la vuelta restando el precio de cada prostituta al presupuesto ingresado.

Después de recopilar todos los datos, se muestra un resumen de los datos ingresados, incluyendo el número de prostitutas, la información detallada de cada una y la vuelta obtenida.

Finalmente, se muestra un mensaje de agradecimiento por la compra.

## Diagrama de Flujo de Uso

![Diagrama de Flujo de Uso](https://github.com/sergiodavid432/trabajo/blob/main/_Diagrama%20de%20flujo.png?raw=true)
## historia de usuario
![Diagrama de Flujo de Uso](

## Pseudocódigo

```plaintext
Escribir("±-----------------------------------------------+")
Escribir("| Bienvenido al burdel Los Gusaneros |")
Escribir("±-----------------------------------------------+")

Definir genero2 Como Carácter
Definir numeroProstitutas Como Entero
Definir precios Como Entero[10]
Definir raza Como Carácter[10]
Definir generoProstituta Como Carácter[10]
Definir presupuesto Como Entero
Definir resultado Como Entero[10]
Definir pago Como Carácter[10]

Escribir("Ingrese el número de prostitutas que desee (máximo 10): ")
Leer numeroProstitutas

Escribir("Digite su presupuesto para las prostitutas: ")
Leer presupuesto

Para i Desde 0 Hasta numeroProstitutas-1 Hacer
    Escribir("-------------------------------------------------")

    pagoValido <- Falso
    Mientras No pagoValido Hacer
        Escribir("Elija su método de pago para la prostituta ", i+1, " (E/T): ")
        Leer pago[i]

        Si pago[i] = "E" O pago[i] = "T" Entonces
            pagoValido <- Verdadero
        Sino
            Escribir("Perrito, este burdel solo acepta efectivo (E) o tarjeta de crédito (T).")
        FinSi
    FinMientras

    Escribir("Ingrese la raza de la prostituta ", i+1, ": ")
    Leer raza[i]

    Escribir("Ingrese el precio de la prostituta ", i+1, ": ")
    Leer precios[i]

    generoValido <- Falso
    Mientras No generoValido Hacer
        Escribir("Ingrese el género de su prostituta ", i+1, " (M/F): ")
        Leer genero2

        Si genero2 = "M" O genero2 = "F" Entonces
            generoValido <- Verdadero
        Sino
            Escribir("Perrito, este burdel solo acepta género 'M' o 'F'. Vuelva a intentarlo.")
        FinSi
    FinMientras

    generoProstituta[i] <- genero2
    resultado[i] <- presupuesto - precios[i]
FinPara

Escribir("+------------------------------------------------+")
Escribir("|             Datos ingresados                   |")
Escribir("+------------------------------------------------+")
Escribir("Número de prostitutas: ", numeroProstitutas)

Para i Desde 0 Hasta numeroProstitutas-1 Hacer
    Escribir("Prostituta ", i+1, "  Raza: ", raza[i], ", Precio: ", precios[i], ", Género elegido: ", generoProstituta[i], ", Su vuelta es: ", resultado[i])
FinPara

Escribir("+------------------------------------------------+")
Escribir("|           Gracias por su compra                |")
Escribir("+------------------------------------------------+")
