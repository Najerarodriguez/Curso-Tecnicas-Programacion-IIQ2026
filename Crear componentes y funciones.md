```javascript
// src/components/Boton.js
export default function Boton({sumar}) {
  return <button onClick={sumar}>Sumar</button>;
}
```

```javascript
// src/components/Contador.js
import {useState} from "react";
import Boton from "./Boton";

export default function Contador() {
  const [n,setN]=useState(0);

  return (
    <div>
      <h2>Contador: {n}</h2>
      <Boton sumar={() => setN(n+1)}/>
    </div>
  );
}
```

```javascript
// src/components/Perfil.js
import React,{Component} from "react";

export default class Perfil extends Component {
  render() {
    return <h3>Usuario: {this.props.nombre}</h3>;
  }
}
```

```javascript
// src/App.js
import Perfil from "./components/Perfil";
import Contador from "./components/Contador";

export default function App() {
  return (
    <div>
      <h1>Mini App React</h1>
      <Perfil nombre="Juan"/>
      <Contador/>
    </div>
  );
}
```

```bash
npm start
```



```javascript
// importamos useState desde React porque permite crear y manejar estados
// dentro de componentes funcionales
import {useState} from "react";

// export default permite exportar este componente como principal
// para poder importarlo fácilmente en otros archivos
export default function Contador() {

  // useState(0) crea una variable de estado llamada n con valor inicial 0
  // setN es la función que actualiza el valor de n
  const [n,setN]=useState(0);

  return (
    <div>
      <h2>Contador: {n}</h2>

      {/* sumar={() => setN(n+1)}
      crea una función callback que aumenta el estado en 1
      cuando el usuario hace clic */}
      <button onClick={() => setN(n+1)}>
        Sumar
      </button>
    </div>
  );
}
```

```javascript
// importamos React y Component porque las clases en React
// necesitan heredar de Component para funcionar
import React,{Component} from "react";

// export default permite usar este componente en otros archivos
// class Perfil extends Component crea un componente basado en clases
export default class Perfil extends Component {

  // render() es obligatorio en componentes de clase
  // y devuelve el HTML que se mostrará en pantalla
  render() {

    // this.props.nombre recibe datos enviados desde el componente padre
    // props permite comunicación entre componentes
    return <h3>Usuario: {this.props.nombre}</h3>;
  }
}
```
