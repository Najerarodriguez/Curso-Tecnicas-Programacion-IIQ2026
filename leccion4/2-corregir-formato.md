# Guia para corregir problemas de formato

Este documento sirve para corregir los problemas de formato identificados en el proyecto.

## Problemas a corregir

- indentacion incorrecta en bloques, funciones y JSX
- espaciado inconsistente entre imports, parametros y atributos
- lineas demasiado largas
- imports desordenados
- multiples sentencias en una sola linea

## Criterios de correccion

### Indentacion

- usar 2 espacios por nivel
- alinear bloques `if`, `return`, `useEffect` y funciones auxiliares
- mantener el JSX con indentacion uniforme

### Espaciado

- dejar un solo espacio despues de comas y alrededor de operadores cuando aplique
- evitar multiples espacios para alinear manualmente codigo
- separar imports por grupos cuando la guia lo requiera

### Longitud de lineas

- dividir lineas largas en varias lineas legibles
- evitar callbacks, objetos o JSX completos en una sola linea cuando excedan el maximo permitido

### Organizacion de imports

- colocar primero imports externos
- luego imports internos del proyecto
- dejar el archivo de estilos en una posicion consistente
- ordenar alfabeticamente dentro de cada grupo si la regla configurada lo exige

## Procedimiento recomendado

1. Ejecutar ESLint con la configuracion visible del proyecto.
2. Aplicar `--fix` para resolver problemas triviales.
3. Revisar manualmente `src/App.js` porque contiene varios bloques extensos y JSX largo.
4. Separar expresiones largas en constantes o bloques multilinea.
5. Repetir el proceso hasta que no queden advertencias relevantes.

## Meta final

El codigo debe quedar legible, uniforme y facil de mantener sin depender de estilos individuales de cada autor.
