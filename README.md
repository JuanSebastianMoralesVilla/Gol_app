# GOL 2026

Web para organizar una polla futbolera de la Seleccion Colombia: los participantes registran marcadores, compiten por ranking y los administradores gestionan usuarios, grupos, partidos y resultados.

## Produccion

Sitio publicado con GitHub Pages:

https://juansebastianmoralesvilla.github.io/Gol_app/

Versiones guardadas:

- `prod`: version original de produccion.
- `prod-nueva`: nueva version de produccion con login actualizado de GOL 2026.

## Funciones principales

- Registro e inicio de sesion con Firebase Authentication.
- Predicciones por partido y por grupo.
- Usuarios asignables a uno o varios grupos.
- Ranking automatico por puntos.
- Historial de marcadores por participante.
- Panel administrador para gestionar usuarios, grupos, partidos y resultados.
- Exportacion de datos a Excel.
- Roles:
  - `user`: participante.
  - `admin_player`: administrador que tambien participa.
  - `admin`: administrador puro, sin participar en la polla.

## Sistema de puntos

- 5 puntos: marcador exacto.
- 3 puntos: ganador o empate correcto.
- 0 puntos: cualquier otro resultado.

## Flujo de trabajo recomendado

- `root`: rama de produccion. Lo que se sube aqui se publica en la web.
- `dev`: rama para probar mejoras antes de produccion.
- `produccion-original`: respaldo de la primera version estable.

Para trabajar cambios nuevos:

```bash
git switch dev
```

Para publicar una mejora ya probada:

```bash
git switch root
git merge dev
git push origin root
```

## Desarrollo local

Como la app es un `index.html` estatico, se puede probar con un servidor local simple:

```bash
python3 -m http.server 8080
```

Luego abrir:

```text
http://localhost:8080/
```

## Firebase

La app usa Firebase para autenticacion y base de datos en tiempo real. La configuracion esta incluida en `index.html` para este proyecto.

Los datos principales se guardan bajo:

```text
/quiniela_colombia
```
