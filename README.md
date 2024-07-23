# Algoritmo del Banquero

Este programa implementa el Algoritmo del Banquero para la gestión de recursos en sistemas operativos. Permite ingresar el número de procesos y recursos, así como las matrices de asignación y de máximos, para determinar si existe una secuencia segura para la ejecución de los procesos sin que ocurra un bloqueo.

## Requisitos

- Un compilador de C++ (por ejemplo g++, Codeblocks 20.03)
- Sistema operativo Windows, Linux o MacOS

## Compilación y Ejecución

1. **Compilación**:

    ```sh
    g++ -o algoritmo_del_banquero algoritmo_del_banquero.cpp
    ```

2. **Ejecución**:

    ```sh
    ./algoritmo_del_banquero
    ```

## Uso

1. **Menú Principal**:

    Al iniciar el programa, se presenta el siguiente menú:
    ```
    MENU
    1. Ingresar Datos y Ejecutar Algoritmo
    2. Salir
    ```

    Seleccione la opción `1` para ingresar los datos y ejecutar el algoritmo, o `2` para salir del programa.

2. **Ingreso de Datos**:

    - **Número de Procesos**: Ingrese un número entre 1 y 6.
    - **Número de Recursos**: Ingrese un número entre 1 y 4.
    - **Matriz de Asignación (A)**: Ingrese los valores de la matriz de asignación.
    - **Matriz de Máximos (C)**: Ingrese los valores de la matriz de máximos.
    - **Total de Recursos**: Ingrese el total de instancias disponibles para cada recurso.
    - **Recursos Disponibles**: Ingrese el número de instancias disponibles actualmente para cada recurso.

3. **Salida del Programa**:

    El programa mostrará:
    - Las matrices ingresadas y la matriz `C - A`.
    - El estado del sistema y los recursos disponibles después de cada iteración.
    - La secuencia segura de procesos (si existe).

    Ejemplo de salida:
    ```
    Matriz de Maximos (C)
    |7| |5| |3| 
    |3| |2| |2| 
    |9| |0| |2| 
    |2| |2| |2| 
    |4| |3| |3| 
    |3| |3| |2| 

    Matriz de Asignacion (A)
    |0| |1| |0| 
    |2| |0| |0| 
    |3| |0| |2| 
    |2| |1| |1| 
    |0| |0| |2| 
    |0| |0| |2| 

    Matriz C - A
    |7| |4| |3| 
    |1| |2| |2| 
    |6| |0| |0| 
    |0| |1| |1| 
    |4| |3| |1| 
    |3| |3| |0| 

    Proceso P1 se puede completar.
    Estado del Sistema tras completar P1:
    Matriz de Asignacion (A)
    |0| |1| |0| 
    |2| |0| |0| 
    |3| |0| |2| 
    |2| |1| |1| 
    |0| |0| |2| 
    |0| |0| |2| 
    Matriz de Maximos (C)
    |7| |5| |3| 
    |3| |2| |2| 
    |9| |0| |2| 
    |2| |2| |2| 
    |4| |3| |3| 
    |3| |3| |2| 
    Matriz C - A
    |7| |4| |3| 
    |1| |2| |2| 
    |6| |0| |0| 
    |0| |1| |1| 
    |4| |3| |1| 
    |3| |3| |0| 

    Recursos Disponibles: R1=3 R2=3 R3=2 
    ```

## Archivos de Salida

- `salida.txt`: El programa genera un archivo `salida.txt` que contiene el mismo detalle mostrado en la consola.

## Notas

- Asegúrese de que los datos ingresados sean correctos y que los recursos disponibles no excedan el total de recursos especificados.
- El programa verifica automáticamente si existe una secuencia segura y proporciona una salida detallada del estado del sistema en cada paso.

## Contacto

Para más información, sugerencias o reportar errores, por favor contacte a: [malbizu@utem.cl] [walvarezq@utem.cl] 
