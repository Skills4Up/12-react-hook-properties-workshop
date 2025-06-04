# Workshop: Manejo de Estado y Propiedades con Hooks

Aprende a gestionar el estado local de componentes y manejar propiedades dinámicas usando React Hooks. Este workshop está diseñado para que adquieras habilidades clave en el manejo de datos reactivos en React, combinando teoría, demostraciones y ejercicios guiados, siguiendo una estructura didáctica y progresiva.

---

## 🎯 Objetivos de aprendizaje y metodología

Al finalizar este workshop, serás capaz de:

- **Comprender** el concepto de estado en React y su importancia.
- **Utilizar** useState para manejar estado local en componentes funcionales.
- **Aplicar** useEffect para manejar efectos secundarios y ciclo de vida.
- **Gestionar** propiedades dinámicas y su comunicación entre componentes.
- **Implementar** patrones comunes de manejo de estado en aplicaciones React.

### Metodología de aprendizaje

- **Explicaciones visuales y ejemplos claros:** Cada concepto se ilustra con diagramas y código.
- **Demostraciones prácticas:** Ejemplos reales explicados paso a paso.
- **Ejercicios interactivos:** Práctica guiada para afianzar los conceptos.
- **Retos de aplicación:** Problemas para resolver de forma autónoma.
- **Proyecto integrador:** Casos de uso reales y ejercicios progresivos.

---

## 🗺️ Mapa de progresión de conocimientos

### Bloque 1: Fundamentos del Estado en React

- [¿Qué es el estado y por qué es importante?](1-estado/1-que-es-estado.md)
- [Estado vs Propiedades: diferencias clave](1-estado/2-estado-vs-props.md)
- [Cuándo usar estado local vs global](1-estado/3-cuando-usar-estado.md)

### Bloque 2: Hook useState

- [Introducción a useState](2-usestate/1-introduccion-usestate.md)
- [Manejo de estado primitivo y objetos](2-usestate/2-tipos-estado.md)
- [Actualizaciones de estado y renderizado](2-usestate/3-actualizaciones-estado.md)
- [Patrones comunes con useState](2-usestate/4-patrones-comunes.md)

### Bloque 3: Hook useEffect

- [Introducción a useEffect](3-useeffect/1-introduccion-useeffect.md)
- [Efectos sin dependencias y con dependencias](3-useeffect/2-dependencias-useeffect.md)
- [Cleanup y efectos de limpieza](3-useeffect/3-cleanup-efectos.md)
- [Casos de uso comunes con useEffect](3-useeffect/4-casos-uso-useeffect.md)

### Bloque 4: Integración Estado y Propiedades

- [Comunicación bidireccional con props y estado](4-integracion/1-comunicacion-bidireccional.md)
- [Lifting state up - Elevar el estado](4-integracion/2-lifting-state-up.md)
- [Patrones de composición con estado](4-integracion/3-patrones-composicion.md)
- [Casos de uso reales y mejores prácticas](4-integracion/4-casos-reales-practicas.md)

---

## 📚 Rutas de aprendizaje y práctica guiada

La ruta de aprendizaje está organizada en bloques temáticos.  
Cada bloque cuenta con archivos que explican los conceptos clave, ejemplos prácticos y buenas prácticas. Explora cada bloque para avanzar de lo fundamental a lo aplicado:

- **[Fundamentos del Estado](1-estado/README.md):**  
  Comprende qué es el estado, por qué es fundamental en React y cuándo utilizarlo.

- **[Hook useState](2-usestate/README.md):**  
  Domina el manejo de estado local con useState, desde tipos primitivos hasta objetos complejos.

- **[Hook useEffect](3-useeffect/README.md):**  
  Aprende a manejar efectos secundarios, ciclo de vida y operaciones asíncronas.

- **[Integración Estado y Propiedades](4-integracion/README.md):**  
  Descubre cómo combinar estado y propiedades para crear aplicaciones dinámicas y escalables.

En cada bloque encontrarás:

- Explicaciones claras y orientadas a resultados.
- Ejercicios prácticos y retos para afianzar los conceptos.
- Buenas prácticas para escribir código limpio y eficiente.

---

## 📋 Requisitos previos

- Haber completado el workshop de "Componentes y Propiedades en React".
- Conocimientos sólidos de JavaScript ES6+ (destructuring, arrow functions, etc.).
- Familiaridad con JSX y componentes funcionales.
- Comprensión básica de props y comunicación entre componentes.
- Node.js y npm instalados.
- Editor de código (Visual Studio Code recomendado).

---

## 🛠️ Configuración del entorno

Antes de comenzar, asegúrate de tener tu entorno configurado:

```bash
# Verificar versiones
node --version  # >= 14.0.0
npm --version   # >= 6.0.0

# Crear proyecto de práctica (opcional)
npx create-react-app estado-hooks-workshop
cd estado-hooks-workshop
npm start
```

---

## 🎯 Ejercicios y proyectos prácticos

Durante este workshop desarrollarás:

### Ejercicios de práctica

- **Contador interactivo** con useState
- **Formulario dinámico** con validación en tiempo real
- **Lista de tareas** con estado local
- **Reloj digital** con useEffect
- **Consumo de API** simulado con useEffect

### Proyecto integrador

- **Dashboard personal** que combine múltiples componentes con estado
- **Aplicación de gestión de productos** con comunicación entre componentes
- **Sistema de filtros** con estado compartido

---

## 🌐 Recursos recomendados

- [Documentación oficial de React Hooks](https://react.dev/reference/react)
- [useState Hook](https://react.dev/reference/react/useState)
- [useEffect Hook](https://react.dev/reference/react/useEffect)
- [Rules of Hooks](https://react.dev/warnings/invalid-hook-call-warning)
- [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/)

---

## 📖 Conceptos clave que aprenderás

### Estado en React

- Inmutabilidad y actualizaciones de estado
- Re-renderizado y optimización
- Estado local vs estado compartido

### Hook useState

- Sintaxis y uso básico
- Estado con tipos primitivos y objetos
- Múltiples estados en un componente
- Estado derivado y computado

### Hook useEffect

- Efectos secundarios y cuándo usarlos
- Array de dependencias y su importancia
- Efectos de limpieza (cleanup)
- Patrones comunes (fetch de datos, suscripciones, timers)

### Integración y patrones

- Lifting state up
- Props drilling y sus alternativas
- Comunicación padre-hijo bidireccional
- Composición de componentes con estado

---

## 🤝 Contribuciones

Este repositorio es de uso exclusivo interno de Skills4Up. No se aceptan contribuciones externas.

Si eres parte del equipo de Skills4Up y deseas proponer una mejora o corrección:

1. Crea un issue describiendo la mejora o problema.
2. Realiza cambios en una rama con prefijo según el tipo:
   - `feat/` para nuevas funcionalidades
   - `fix/` para correcciones
   - `docs/` para documentación
   - `refactor/` para refactorización
3. Usa mensajes de commit siguiendo el formato `type(scope): message`
4. Envía un Pull Request vinculado al issue original.

Todas las contribuciones internas incluirán los créditos correspondientes.

---

## 📜 Licencia

Copyright (c) 2024 Skills4Up

Todos los derechos reservados.

Este material es propiedad exclusiva de Skills4Up. Queda prohibida su reproducción, distribución, comunicación pública o transformación, total o parcial, sin la autorización expresa y por escrito de Skills4Up. El uso de este material está restringido únicamente a fines internos de Skills4Up.

Para autorizaciones especiales, contacta a [info@skills4up.com](mailto:info@skills4up.com).

---

## 🔄 Secuencia de aprendizaje recomendada

### Fase 1: Fundamentos (30 minutos)

1. Lee "¿Qué es el estado y por qué es importante?"
2. Comprende las diferencias entre estado y propiedades
3. Identifica cuándo usar cada tipo de estado

### Fase 2: useState en Profundidad (60 minutos)

1. Practica con ejemplos básicos de useState
2. Maneja diferentes tipos de datos en el estado
3. Implementa actualizaciones complejas de estado
4. Aplica patrones comunes

### Fase 3: useEffect y Efectos (60 minutos)

1. Comprende el concepto de efectos secundarios
2. Practica con diferentes arrays de dependencias
3. Implementa efectos de limpieza
4. Desarrolla casos de uso reales

### Fase 4: Integración y Proyecto (90 minutos)

1. Combina useState y useEffect
2. Practica comunicación bidireccional
3. Implementa lifting state up
4. Desarrolla el proyecto integrador

---

## 🧩 ¿Cómo usar este archivo como contexto para otros temas?

- **Estructura:** Cada sección y ejemplo muestra el código relevante y el contexto necesario para comprenderlo.
- **Progresión:** Los contenidos avanzan de conceptos básicos de estado hasta patrones complejos de manejo de datos.
- **Aplicación:** Usa este formato para enseñar otros hooks (useContext, useReducer, useMemo, etc.), mostrando siempre ejemplos claros e incrementando la dificultad gradualmente.
- **Recomendación:** Para cada nuevo hook o concepto, inicia con el problema que resuelve, presenta la sintaxis básica y avanza hacia casos de uso reales.
- **Importante:** Este workshop se enfoca únicamente en useState y useEffect. Los hooks más avanzados se cubrirán en workshops posteriores para mantener el aprendizaje progresivo y evitar sobrecarga cognitiva.

---

## 📝 Notas para el instructor

### Timing sugerido (3.5 horas)

- **Introducción y fundamentos:** 30 minutos
- **useState en profundidad:** 60 minutos
- **useEffect y efectos:** 60 minutos
- **Integración y práctica:** 60 minutos
- **Proyecto y cierre:** 30 minutos

### Puntos clave a enfatizar

- La inmutabilidad del estado en React
- La importancia del array de dependencias en useEffect
- Cuándo NO usar hooks (reglas de hooks)
- Patrones de composición escalables
- Debugging con React Developer Tools

### Errores comunes a evitar

- Mutar directamente el estado
- Olvidar dependencias en useEffect
- Usar hooks dentro de condicionales o loops
- No limpiar efectos cuando es necesario
- Crear dependencias infinitas en useEffect

---
