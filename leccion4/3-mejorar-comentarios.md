# Guia para mejorar comentarios

Este documento explica como corregir los problemas de comentarios en el proyecto.

## Problemas detectados

- comentarios obvios que solo repiten lo que el codigo ya dice
- comentarios desactualizados que ya no describen el comportamiento real
- funciones complejas sin documentacion util

## Que eliminar

Eliminar comentarios como:

- "esto guarda cosas"
- "tambien cambia otro form"
- "sale de la app"

Ese tipo de comentario no agrega contexto tecnico.

## Que agregar

Agregar JSDoc o comentarios de alto valor en funciones que concentran logica importante, por ejemplo:

- autenticacion y registro
- sincronizacion con Firebase y `localStorage`
- actualizacion de estadisticas por usuario
- construccion de datos para reportes o graficas

## Criterios para comentarios utiles

- explicar decisiones no obvias
- documentar efectos secundarios importantes
- aclarar contratos de entrada y salida
- describir riesgos, dependencias o limitaciones

## Ejemplo de enfoque correcto

En lugar de un comentario obvio:

```js
// cambia el valor del form
```

Conviene documentar funciones complejas con JSDoc:

```js
/**
 * Registra un nuevo usuario o autentica uno existente y sincroniza
 * los cambios con Firebase y el estado local.
 * @param {'login' | 'registro'} modo
 */
```

## Resultado esperado

Todos los comentarios del proyecto deben aportar contexto real al lector, y las funciones complejas deben tener documentacion breve pero precisa.
