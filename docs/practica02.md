# **Práctica 02: Cálculo de sueldo**

### 1. Formulario del sueldo y puesto

En el archivo html se muestra el formulario donde se introduce el sueldo del trabajador y se selecciona el puesto.

El sueldo debe ser un número entero mayor de 1000 €.

```text
<form name="myform" method="post" action="UT02P02.php">
        Sueldo:
        <input class="input is-link" type="number" min="1000" name="sueldo" placeholder="Sueldo" required>
        Puesto:
        <select class="input is-link" name="puesto" required>
            <option disabled selected>Seleccione un puesto</option>
            <option value="base">Base</option>
            <option value="directivo">Directivo</option>
            <option value="altoCargo">Alto Cargo</option>
        </select>
        <input type="submit" value="Enviar" class="button is-link">
```

___

### 2. Selección del puesto

El puesto se selecciona mediante un desplegable con tres opciones: **Base**, **Directivo** y **Alto cargo**.

La primera opción, "Selecciona un puesto", está deshabilitada para obligar a seleccionar un puesto válido.


___

### 3. Cálculo del salario

Al enviar el formulario, la segunda página (.php) recibe los datos y calcula el complemento según el puesto seleccionado:

* Base: 10%
* Directivo: 15%
* Alto cargo: 20%

```text
        $sueldo = $_POST["sueldo"] ?? 1000;
        $puesto = $_POST["puesto"] ?? 'base';

        switch ($puesto) {
            case 'base':
                $complemento = 10;
                break;
            case 'directivo':
                $complemento = 15;
                break;
            case 'altoCargo':
                $complemento = 20;
                break;
            default:
                $complemento = 0;
        }

        $sueldoFinal = $sueldo + ($sueldo * $complemento / 100);
```
___

### 4. Resultado final

Finalmente, se muestra el sueldo base, el porcentaje de complemento y el sueldo final.

Por ejemplo, con un sueldo de **1200 €** y el puesto **Base**, el resultado es:

```text
Sueldo base: 1200€
Complemento: 10%
Sueldo final: 1320€
```