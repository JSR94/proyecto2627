# **Práctica 02: Cálculo de sueldo**

### 1. Formulario del sueldo y puesto

En este apartado se muestra el formulario donde se introduce el sueldo del trabajador y se selecciona el puesto.

El sueldo debe ser un número entero mayor de 1000 €.

___

### 2. Selección del puesto

El puesto se selecciona mediante un desplegable con tres opciones: **Base**, **Directivo** y **Alto cargo**.

La primera opción, "Selecciona un puesto", está deshabilitada para obligar a seleccionar un puesto válido.


___

### 3. Cálculo del salario

Al enviar el formulario, la segunda página recibe los datos y calcula el complemento según el puesto seleccionado:

* Base: 10%
* Directivo: 15%
* Alto cargo: 20%


___

### 4. Resultado final

Finalmente, se muestra el sueldo base, el porcentaje de complemento y el sueldo final.

Por ejemplo, con un sueldo de **1200 €** y el puesto **Base**, el resultado es:

```text
Sueldo base: 1200€
Complemento: 10%
Sueldo final: 1320€
```