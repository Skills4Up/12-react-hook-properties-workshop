# Hook useState

Domina el manejo de estado local con useState, desde tipos primitivos hasta objetos complejos. Aprende a crear componentes dinámicos y reactivos.

---

## 🎯 Objetivos

- Dominar la sintaxis de useState
- Manejar diferentes tipos de estado
- Entender actualizaciones y renderizado
- Aplicar patrones comunes

---

## ⚡ Sintaxis básica

### Estado primitivo

```javascript
const [count, setCount] = useState(0);
const [name, setName] = useState('');
const [isActive, setIsActive] = useState(false);
```

### Estado de objeto

```javascript
const [user, setUser] = useState({
  name: '',
  email: '',
  age: 0
});
```

### Estado de array

```javascript
const [items, setItems] = useState([]);
const [todos, setTodos] = useState([
  { id: 1, text: 'Aprender React', done: false }
]);
```

---

## 🔄 Actualizaciones

### Inmutabilidad

```javascript
// ✅ Correcto
setUser(prev => ({ ...prev, name: 'Ana' }));
setItems(prev => [...prev, newItem]);

// ❌ Incorrecto
user.name = 'Ana';
items.push(newItem);
```

### Función vs valor

```javascript
// Con función (recomendado)
setCount(prev => prev + 1);

// Con valor directo
setCount(count + 1);
```

---

## 📋 Patrones comunes

### Toggle boolean

```javascript
const [isOpen, setIsOpen] = useState(false);
const toggle = () => setIsOpen(prev => !prev);
```

### Formularios

```javascript
const [form, setForm] = useState({ name: '', email: '' });
const handleChange = (field, value) => {
  setForm(prev => ({ ...prev, [field]: value }));
};
```

### Listas

```javascript
const [tasks, setTasks] = useState([]);
const addTask = (task) => setTasks(prev => [...prev, task]);
const removeTask = (id) => setTasks(prev => prev.filter(t => t.id !== id));
```

---

## 🐛 Errores comunes

| Error                 | Solución                  |
| --------------------- | ------------------------- |
| **Mutación directa**  | Usar spread operator      |
| **Estado stale**      | Usar función en setter    |
| **Múltiples renders** | Combinar actualizaciones  |
| **Estado derivado**   | Usar variables calculadas |

---

## 📚 Contenido detallado

Esta carpeta contiene:

- **Introducción** - Sintaxis y conceptos básicos
- **Tipos de estado** - Primitivos, objetos y arrays
- **Actualizaciones** - Inmutabilidad y renderizado
- **Patrones comunes** - Casos de uso frecuentes

---

useState es la base para crear componentes interactivos en React.
