
# Uso de npm con ejemplos prácticos

A continuación, te mostraré cómo usar npm con ejemplos prácticos:

## 1. Instalación de Node.js y npm

Primero, asegúrate de tener Node.js instalado en tu sistema. Puedes descargarlo desde el [sitio web oficial](https://nodejs.org/). La instalación de Node.js incluye automáticamente npm.

## 2. Crear un nuevo proyecto

Abre tu terminal y navega al directorio donde deseas crear el proyecto.

## 3. Inicializar un nuevo proyecto de Node.js

Ejecuta el siguiente comando para inicializar un nuevo proyecto de Node.js:

```shell
npm init -y
```

Esto crea un archivo `package.json`, que es un archivo de configuración para tu proyecto. Contiene información sobre las dependencias y configuraciones del proyecto.

## 4. Instalar paquetes

Puedes instalar paquetes usando el siguiente comando:

```shell
npm install <nombre_del_paquete>
```

Ejemplo: Para instalar el paquete lodash, que proporciona utilidades de JavaScript, ejecuta:

```shell
npm install lodash
```

## 5. Guardar dependencias en el archivo package.json

Cuando instalas un paquete, npm guarda automáticamente la información en tu archivo `package.json`.

## 6. Uso de dependencias

Una vez que tienes paquetes instalados, puedes usarlos en tu código. Ejemplo: Si instalaste lodash, puedes importarlo en tu archivo de JavaScript así:

```javascript
const _ = require('lodash');
```

## 7. Instalación global de paquetes

Algunos paquetes pueden ser instalados globalmente para usarlos en la línea de comandos. Usa `-g` para instalarlos globalmente. Ejemplo: Para instalar el paquete nodemon que facilita el reinicio automático de tu servidor, ejecuta:

```shell
npm install -g nodemon
```

## 8. Desinstalación de paquetes

Puedes desinstalar un paquete usando el comando:

```shell
npm uninstall <nombre_del_paquete>
```

## 9. Actualización de paquetes

Para mantener tus paquetes actualizados, usa `npm update`.

## 10. Buscar paquetes

Puedes buscar paquetes en el repositorio de npm usando `npm search <palabra_clave>`. Ejemplo: Para buscar paquetes relacionados con "database", ejecuta:

```shell
npm search database
```

## 11. Instalar dependencias de desarrollo

Usa la bandera `--save-dev` o `-D` para instalar paquetes que solo son necesarios durante el desarrollo. Ejemplo: Para instalar mocha como una dependencia de desarrollo para pruebas, ejecuta:

```shell
npm install mocha --save-dev
```

## Funcionalidades adicionales

### 1. Versiones de paquetes

Los paquetes npm siguen un sistema de versionado semántico (SemVer) que consiste en tres números: X.Y.Z. Puedes especificar qué versión de un paquete deseas instalar usando operadores como `>`, `<`, `>=`, `<=`, `~`, `^` en tu `package.json`.

Ejemplo:

- `^1.2.3` instalará la versión 1.2.3 o cualquier versión compatible hacia arriba hasta la 2.0.0.
- `~1.2.3` instalará la versión 1.2.3 o cualquier versión compatible hacia arriba hasta la 1.3.0.

### 2. Scripts en el `package.json`

En el archivo `package.json`, puedes definir scripts que puedes ejecutar con `npm run <script_name>`. Estos scripts pueden ser útiles para automatizar tareas como iniciar el servidor, ejecutar pruebas, entre otros.

Ejemplo:

```json
"scripts": {
  "start": "node index.js",
  "test": "mocha"
}
```

Puedes ejecutarlos usando `npm run start` o `npm test`.

### 3. Manejo de dependencias globales

Aunque se recomienda evitar las dependencias globales en la mayoría de los casos, a veces es necesario. Puedes listar las dependencias globales con `npm ls -g --depth=0`.

### 4. Publicar paquetes en el registro de npm

Si has desarrollado un paquete útil, puedes compartirlo con la comunidad al publicarlo en el registro de npm. Primero, necesitarás una cuenta de npm. Luego, puedes usar `npm login` y `npm publish` para subir tu paquete.

### 5. Actualizar paquetes de manera segura

Puedes usar `npm outdated` para verificar si hay actualizaciones disponibles para tus dependencias. Luego, puedes actualizar de manera segura con `npm update`.

### 6. Resolución de conflictos de dependencias

A veces, las dependencias pueden entrar en conflicto. Puedes usar `npm ls` para visualizar la estructura de dependencias y `npm ls <nombre_del_paquete>` para ver dónde se usa un paquete específico.

### 7. Evitar la instalación de paquetes de manera global

Puedes configurar npm para que instale paquetes en el ámbito local por defecto usando el comando `npm config set -g prefix $HOME/.npm-packages`.

Estas son solo algunas de las funcionalidades y técnicas que puedes utilizar con npm.
