# Integración Estado y Propiedades

Descubre cómo combinar estado y propiedades para crear aplicaciones dinámicas y escalables. Aprende patrones de comunicación y composición avanzados.

---

## 🎯 Objetivos

- Dominar comunicación bidireccional
- Aplicar lifting state up
- Implementar patrones de composición
- Desarrollar casos de uso reales

---

## 🔄 Comunicación bidireccional

### Padre a hijo

```javascript
function Padre() {
  const [dato, setDato] = useState('valor');
  return <Hijo valor={dato} />;
}

function Hijo({ valor }) {
  return <p>{valor}</p>;
}
```

### Hijo a padre

```javascript
function Padre() {
  const [dato, setDato] = useState('');
  return <Hijo onCambio={setDato} />;
}

function Hijo({ onCambio }) {
  return (
    <input onChange={(e) => onCambio(e.target.value)} />
  );
}
```

---

## ⬆️ Lifting state up

### Problema: Estado duplicado

```javascript
// ❌ Estado separado en cada componente
function ComponenteA() {
  const [valor, setValor] = useState(0);
}
function ComponenteB() {
  const [valor, setValor] = useState(0);
}
```

### Solución: Estado elevado

```javascript
// ✅ Estado compartido en el padre
function Padre() {
  const [valor, setValor] = useState(0);
  return (
    <>
      <ComponenteA valor={valor} onChange={setValor} />
      <ComponenteB valor={valor} onChange={setValor} />
    </>
  );
}
```

---

## 🧩 Patrones de composición

### Container/Presentational

```javascript
// Container: lógica
function UserContainer() {
  const [user, setUser] = useState(null);
  return <UserView user={user} />;
}

// Presentational: UI
function UserView({ user }) {
  return <div>{user?.name}</div>;
}
```

### Render Props

```javascript
function DataProvider({ children }) {
  const [data, setData] = useState(null);
  return children({ data, setData });
}

// Uso
<DataProvider>
  {({ data, setData }) => <Component data={data} />}
</DataProvider>
```

---

## 📋 Mejores prácticas

| Práctica                | Descripción                  |
| ----------------------- | ---------------------------- |
| **Una responsabilidad** | Cada componente una función  |
| **Estado mínimo**       | Solo estado necesario        |
| **Inmutabilidad**       | No mutar estado directamente |
| **Composición**         | Combinar componentes simples |

---

## 🐛 Errores comunes

| Error                       | Solución                  |
| --------------------------- | ------------------------- |
| **Props drilling**          | Lifting state up          |
| **Estado duplicado**        | Elevar al padre común     |
| **Componentes monolíticos** | Dividir responsabilidades |
| **Mutación de props**       | Props son de solo lectura |

---

## 📚 Contenido detallado

Esta carpeta contiene:

- **Comunicación bidireccional** - Patrones padre-hijo
- **Lifting state up** - Elevar estado al padre común
- **Patrones de composición** - Técnicas avanzadas
- **Casos reales** - Aplicaciones completas

---

La integración efectiva de estado y propiedades es clave para aplicaciones escalables.
