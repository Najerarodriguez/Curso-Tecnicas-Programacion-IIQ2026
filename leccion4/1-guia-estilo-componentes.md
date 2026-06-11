# Guia de estilo consistente para componentes React

Este documento describe como aplicar una guia de estilo consistente a todos los componentes del proyecto usando ESLint con la configuracion de Airbnb.

## Configuracion de linter visible

El proyecto ya incluye un archivo visible en la raiz:

- `.eslintrc.json`

La configuracion propuesta extiende:

- `airbnb`
- `airbnb/hooks`

Y hace explicitas reglas para:

- indentacion de 2 espacios
- longitud maxima de linea de 100 caracteres
- orden consistente de imports
- espaciado en objetos
- indentacion de JSX

## Alcance

Se debe aplicar la misma guia a:

- `src/App.js`
- `src/index.js`
- `src/reportWebVitals.js`
- cualquier componente React nuevo dentro de `src`

## Pasos sugeridos

1. Instalar las dependencias de lint necesarias para Airbnb.
2. Asegurar que todos los archivos JSX y JS del proyecto sean analizados por ESLint.
3. Corregir primero errores automaticos con `eslint --fix`.
4. Resolver manualmente las reglas que no puedan corregirse de forma automatica.
5. Mantener la configuracion visible y versionada en el repositorio.

## Resultado esperado

Todos los componentes deben compartir:

- el mismo orden de imports
- la misma indentacion
- el mismo estilo de JSX
- limites razonables de longitud de linea
- reglas claras y reproducibles para futuras contribuciones
