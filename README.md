# Quiniela Selección Colombia gratis

Web para que 20+ personas pongan marcadores y se asignen puntos automáticamente.

## Qué incluye
- Predicciones para partidos de Colombia.
- Ranking automático.
- Panel de administrador para registrar resultados.
- Puntos:
  - 5 puntos: marcador exacto.
  - 3 puntos: ganador o empate acertado.
  - 1 punto: diferencia de gol acertada.
- Modo demo local si no configuras Firebase.
- Modo multiusuario real usando Firebase Realtime Database gratis.

## Cómo dejarla online gratis

### 1. Crear Firebase gratis
1. Entra a Firebase Console.
2. Crea un proyecto.
3. Ve a Realtime Database.
4. Crea una base de datos.
5. Para una quiniela privada entre amigos, puedes iniciar en modo test temporalmente.
6. Copia la configuración web de Firebase.

### 2. Pegar configuración
Abre `index.html` y reemplaza:

```js
const firebaseConfig = {
  apiKey: "PEGA_AQUI_TU_API_KEY",
  ...
};
```

También cambia:

```js
const ADMIN_PIN = "1234";
```

### 3. Publicar gratis
Opción fácil: GitHub Pages.
1. Crea un repositorio en GitHub.
2. Sube `index.html`.
3. Ve a Settings > Pages.
4. En Source selecciona Deploy from branch.
5. Elige branch `main` y carpeta `/root`.
6. Guarda y espera el enlace.

También puedes usar Cloudflare Pages subiendo este archivo como sitio estático.

## Entrar como administrador
Abre la URL así:

`https://tuweb.com/?admin=TU_PIN`

Desde ahí puedes poner los resultados finales.

## Nota de seguridad
El PIN del admin está en el HTML, por eso sirve para amigos/familia. Para una versión seria con usuarios y permisos reales, hay que agregar login.
