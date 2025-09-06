# Pruebas de creación de usuario – Validación de parámetro firstName
Este proyecto, realizado como parte del practicum de TripleTen LatAm, valida el comportamiento del parámetro firstName al crear un usuario en el servicio proporcionado.
Las pruebas comprueban escenarios positivos y negativos, incluyendo longitudes permitidas, uso de caracteres válidos, ausencia de parámetros y envío de valores incorrectos.

## Tecnologías y técnicas utilizadas
- Python como lenguaje.
- pytest como framework de pruebas.
- requests para envío de peticiones HTTP.
- Aserciones para validar códigos de estado, mensajes de error y contenido en la base de datos simulada.
- Pruebas positivas y negativas para verificar cumplimiento de restricciones (longitud mínima/máxima, tipo de dato, caracteres válidos).

## Instrucciones para ejecutar las pruebas
- Clona el repositorio en tu entorno local con SSH. Reemplaza "username" con tu usuario:
  ```sh
    git clone git@github.com:username/qa-project-create-user.git
    ```
- Instala las dependencias necesarias:
  ```sh
    pip install pytest requests
    ```
- Ejecuta todas las pruebas con:
  ```sh
    pytest
    ```

## Estructura de las pruebas automatizadas
- Validaciones positivas:
  - Creación de usuario con 2 caracteres en firstName.
  - Creación de usuario con 15 caracteres en firstName.
  - Creación de usuario con letras latinas o inglesas válidas.
- Validaciones negativas:
  - firstName con un (1) solo caracter.
  - firstName con más de 15 caracteres.
  - Números en firstName.
  - Símbolos especiales en firstName.
  - Ausencia del parámetro firstName.
  - Envío de firstName vacío.
  - Envío de un valor numérico en lugar de string para firstName.
