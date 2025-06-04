# Hook useEffect

Aprende a manejar efectos secundarios, ciclo de vida y operaciones asíncronas. Domina el hook más versátil para interacciones con el mundo exterior.

---

## 🎯 Objetivos

- Comprender los efectos secundarios
- Dominar arrays de dependencias
- Implementar efectos de limpieza
- Aplicar casos de uso reales

---

## ⚡ Conceptos básicos

### Efecto sin dependencias

```javascript
useEffect(() => {
  console.log('Se ejecuta en cada render');
});
```

### Efecto con dependencias vacías

```javascript
useEffect(() => {
  console.log('Se ejecuta solo una vez');
}, []);
```

### Efecto con dependencias

```javascript
useEffect(() => {
  console.log('Se ejecuta cuando count cambia');
}, [count]);
```

---

## 🧹 Cleanup (limpieza)

### Timers

```javascript
useEffect(() => {
  const timer = setInterval(() => {
    setTime(new Date());
  }, 1000);
  
  return () => clearInterval(timer);
}, []);
```

### Event listeners

```javascript
useEffect(() => {
  const handleScroll = () => setScrollY(window.scrollY);
  window.addEventListener('scroll', handleScroll);
  
  return () => window.removeEventListener('scroll', handleScroll);
}, []);
```

---

## 📋 Casos de uso comunes

### Fetch de datos

```javascript
useEffect(() => {
  const fetchData = async () => {
    const response = await fetch('/api/data');
    setData(await response.json());
  };
  fetchData();
}, []);
```

### Sincronización

```javascript
useEffect(() => {
  document.title = `Contador: ${count}`;
}, [count]);
```

### Suscripciones

```javascript
useEffect(() => {
  const subscription = subscribe(callback);
  return () => subscription.unsubscribe();
}, []);
```

---

## 🐛 Errores comunes

| Error                      | Solución                    |
| -------------------------- | --------------------------- |
| **Dependencias faltantes** | Incluir todas las variables |
| **Loop infinito**          | Revisar dependencias        |
| **No hacer cleanup**       | Agregar función de retorno  |
| **Fetch en cada render**   | Usar array de dependencias  |

---

## 📚 Contenido detallado

Esta carpeta contiene:

- **Introducción** - Concepto de efectos secundarios
- **Dependencias** - Arrays vacíos, con valores y sin array
- **Cleanup** - Limpieza de efectos y memory leaks
- **Casos de uso** - Fetch, timers, suscripciones

---

useEffect te permite conectar React con sistemas externos de forma segura.
