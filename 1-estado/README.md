# Fundamentos del Estado en React

Comprende qué es el estado, por qué es fundamental en React y cuándo utilizarlo. Esta sección establece las bases conceptuales para el manejo efectivo de datos reactivos.

---

## 🎯 Objetivos

- Entender qué es el estado en React
- Diferenciar estado de propiedades
- Identificar cuándo usar estado local vs global
- Reconocer patrones de estado

---

## 🧠 Conceptos clave

### ¿Qué es el estado?

```javascript
// Estado: datos que cambian en el tiempo
const [contador, setContador] = useState(0);
const [usuario, setUsuario] = useState(null);
```

### Estado vs Props

```javascript
// Props: datos que vienen del padre
function Hijo({ nombre, edad }) {
  return <p>{nombre} tiene {edad} años</p>;
}

// Estado: datos internos del componente
function Padre() {
  const [nombre, setNombre] = useState('Ana');
  return <Hijo nombre={nombre} edad={25} />;
}
```

### Cuándo usar estado

```javascript
// ✅ Datos que cambian
const [isVisible, setIsVisible] = useState(false);

// ✅ Datos de formularios
const [email, setEmail] = useState('');

// ❌ Datos que no cambian
const CONSTANTE = 'valor fijo';
```

---

## 📋 Diferencias clave

| **Estado**            | **Props**             |
| --------------------- | --------------------- |
| Interno al componente | Externo al componente |
| Mutable               | Inmutable             |
| Se puede actualizar   | Solo lectura          |
| useState/setState     | Parámetro de función  |

---

## 🔧 Tipos de estado

### Estado local

```javascript
function Contador() {
  const [count, setCount] = useState(0);
  // Solo este componente usa 'count'
}
```

### Estado compartido

```javascript
function App() {
  const [datos, setDatos] = useState([]);
  return (
    <>
      <ComponenteA datos={datos} />
      <ComponenteB datos={datos} />
    </>
  );
}
```

---

## 🐛 Errores comunes

| Error                     | Solución              |
| ------------------------- | --------------------- |
| **Mutar estado directo**  | Usar función setter   |
| **Estado innecesario**    | Verificar si cambia   |
| **Duplicar estado**       | Elevar al padre común |
| **No sincronizar estado** | Usar lifting state up |

---

## 📚 Contenido detallado

Esta carpeta contiene:

- **¿Qué es el estado?** - Concepto fundamental y importancia
- **Estado vs Props** - Diferencias y cuándo usar cada uno
- **Cuándo usar estado** - Decisiones de arquitectura

---

Dominar estos fundamentos es esencial para entender useState y useEffect.
