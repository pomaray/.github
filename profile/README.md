<h1 align="center">
    <a href="https://amplication.com/#gh-light-mode-only">
    <img src="https://avatars.githubusercontent.com/u/146970277?s=200&v=4">
    </a>
</h1>

<p align="center">
  <i align="center">Centro Educativo de excelencia Politécnico Madre Rafaela 🚀</i>
</p>

<h4 align="center">

  <a href="https://github.com/pomaray/.github/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/amplication/amplication/ci.yml?branch=master&label=pipeline&style=flat-square" alt="continuous integration" style="height: 20px;">
  </a>
  <a href="https://opensource.org/licenses/Apache-2.0">
    <img src="https://img.shields.io/badge/apache%202.0-blue.svg?style=flat-square&label=license" alt="license" style="height: 20px;">
  </a>
  <br>
  <a href="https://instagram.com/yoamoapomaray">
    <img src="https://img.shields.io/badge/instagram-whitesmoke.svg?style=flat-square&logo=instagram" alt="instagram" style="height: 20px;">
  </a>
  <a href="https://facebook.com/lovepomaray">
    <img src="https://img.shields.io/badge/facebook-blue.svg?style=flat-square&logo=facebook" alt="instagram" style="height: 20px;">
  </a>

  <br/>

<p align="center">
<a href="https://amplication.com/#gh-light-mode-only">
    <img src="https://github.com/pomaray/pomaray-app/blob/main/public/images/banner/home.png?raw=true">
    </a>
</p>

## Introducción

`Pomaray` es una plataforma de desarrollo robusta y de código abierto diseñada para revolucionar la creación de aplicaciones escalables y seguras con tecnologías como Node.js y Python. Eliminamos tareas de codificación repetitivas y entregamos código de infraestructura listo para producción, meticulosamente adaptado a sus especificaciones y siguiendo las mejores prácticas de la industria.

Nuestra interfaz de usuario amigable fomenta la integración perfecta de API, modelos de datos, bases de datos, autenticación y autorización. Construido sobre una arquitectura flexible y basada en plugins, Pomaray permite la personalización del código sin esfuerzo y ofrece una amplia gama de integraciones.

Con un fuerte enfoque en la colaboración, Pomaray agiliza el desarrollo orientado a equipos, lo que lo convierte en una opción ideal para grupos de todos los tamaños, desde startups hasta grandes empresas. Nuestra plataforma le permite concentrarse en la lógica de su negocio, mientras nosotros nos encargamos del trabajo pesado.

Experimente la forma más rápida de desarrollar aplicaciones con Node.js y Python con Pomaray.

<details open>

## Uso 

Para comenzar con Pomaray, se puede utilizar la versión alojada del producto. Puedes comenzar de inmediato en [app.pomaray.com](https://app.pomaray.com). Después de la página de inicio de sesión, se le guiará a través de la creación de su primer servicio. El [sitio web](https://pomaray.com) proporciona una visión general de la aplicación, y se pueden encontrar información adicional sobre el producto y guías en la [documentación](https://docs.pomaray.com).

<details>
<summary>
  Tutoriales
</summary> <br />

- [Aplicación de lista de tareas usando Pomaray y Angular](https://docs.pomaray.com/tutorials/angular-todos)
- [Aplicación de lista de tareas usando Pomaray y React](https://docs.pomaray.com/tutorials/react-todos)
</details>

## Desarrollo

Alternativamente, en lugar de usar la versión alojada del producto, Pomaray puede ejecutarse localmente para fines de generación de código o contribuciones. Si es así, consulte nuestra [sección de contribución](#contributing_anchor).

<details open>
<summary>
Pre-requisitos
</summary> <br />
Para poder comenzar el desarrollo en Pomaray, asegúrese de tener instalados los siguientes requisitos previos:

###

- Node.js
- Docker
- Git
</details>

<details open>
<summary>
Ejecutar Pomaray
</summary> <br />

> **Nota**
> También es posible comenzar el desarrollo con GitHub Codespaces. Cuando navegue a `< > Código`, seleccione `Codespaces` en lugar de `Local`. Haga clic en el botón `+` o en el botón `Crear codespace en la rama principal`.

Pomaray está utilizando una arquitectura monorepo, alimentada por <a href="https://nx.dev">Nx Workspaces</a>, donde existen múltiples aplicaciones y bibliotec

as en un solo repositorio. Para configurar un entorno de desarrollo local, se pueden seguir los siguientes pasos:

**ANTES** de ejecutar los siguientes pasos, asegúrese de:
1. Tener TypeScript instalado localmente en su máquina ```npm install -g typescript```
2. Estar utilizando una versión compatible de Node (verifique `engines` `node` en el [package.json](./package.json))
3. Estar utilizando una versión compatible de npm (verifique `engines` `npm` en el [package.json](./package.json))
4. Tener `docker` instalado y en ejecución en su máquina


1. Clone el repositorio e instale las dependencias:
```shell
git clone https://github.com/pomaray/pomaray.git && cd pomaray && npm install
```

2. Ejecute el script de configuración, que se encarga de instalar dependencias, construir paquetes y configurar el espacio de trabajo:
```shell
npm run setup:dev
```

3. Opción 1: Ejecutar la infraestructura requerida - ver los registros de los componentes de infraestructura


```shell
npm run docker:dev
```
3. Opción 2: Ejecutar la infraestructura requerida - ejecutar los componentes de infraestructura en segundo plano
```shell
npm run docker:dev -- -d
```

4. Aplicar migraciones de base de datos
```shell
npm run db:migrate:deploy
```

5. Para comenzar a desarrollar, ejecute una o más de las aplicaciones disponibles bajo los scripts `serve:[application]` del package.json.

```shell
# ejecutando el componente del servidor
npm run serve:server

# ejecutando el componente del cliente
npm run serve:client

# ejecutando el componente del generador de servicios de datos
npm run serve:dsg

# ejecutando el componente del servicio de solicitud de extracción de git
npm run serve:git

# ejecutando el componente de la API de plugins
npm run serve:plugins
```

> **Nota**
> Para ejecutar correctamente el cliente de Pomaray, tanto el cliente como el servidor deben iniciarse con el comando `npm run serve:[application]`, así como un componente adicional para el desarrollo en un componente específico.

El entorno de desarrollo ahora debería estar configurado. Se puede encontrar información adicional sobre los diferentes componentes de la aplicación en el archivo packages/`[application]`/README.md. ¡Feliz hacking! 👾
</details>

## Recursos

- **[Sitio web](https://pomaray.com)** visión general del producto.
- **[Documentos](https://docs.pomaray.com)** para documentación completa.
- **[Blog](https://pomaray.com/blog)** para guías y comparaciones técnicas.
- **[Hoja de ruta](https://pomaray.com/#roadmap)** para ver qué características se agregarán en el futuro.
- **[Discord](https://pomaray.com/discord)** para soporte y discusiones con la comunidad y el equipo.
- **[GitHub](https://github.com/pomaray/pomaray)** para código fuente, tablero de proyectos, problemas y solicitudes de extracción.
- **[Twitter](https://twitter.com/pomaray)** para las últimas actualizaciones sobre el producto y blogs publicados.
- **[YouTube](https://www.youtube.com/c/Pomaraycom)** para guías y charlas técnicas.

<a name="contributing_anchor"></a>
## Contribuciones

Pomaray es un proyecto de código abierto. Estamos comprometidos con un proceso de desarrollo totalmente transparente y apreciamos enormemente cualquier contribución. Ya sea que nos esté ayudando a corregir errores, proponiendo nuevas características, mejorando nuestra documentación o difundiendo la palabra, nos encantaría tenerlo como parte de la comunidad de Pomaray. Consulte nuestras [pautas de contribución](./CONTRIBUTING.md) y [código de conducta](./CODE_OF_CONDUCT.md).

- Reporte de errores: Si ve un mensaje de error o encuentra un problema mientras usa Pomaray, cree un [informe de error](https://github.com/pomaray/pomaray/issues/new?assignees=&labels=type%3A+bug&template=bug.yaml&title=%F0%9F%90%9B+Reporte+de+error%3A+).

- Solicitud de función: Si tiene una idea o si hay una capacidad que falta y que facilitaría y haría más robusto el desarrollo, envíe una [solicitud de función](https://github.com/pomaray/pomaray/issues/new?assignees=&labels=type%3A+feature+request&template=feature.yml).

- Solicitud de documentación: Si está leyendo la documentación de Pomaray y siente que falta algo, envíe una [solicitud de documentación](https://github.com/pomaray/pomaray/issues/new?assignees=&labels=type%3A+docs&template=documentation-request.yaml&title=%F0%9F%93%96+Documentación%3A+).


## Contribuidores

[//]: contributor-faces
<a href="https://github.com/Aethan-oss"><img src="https://avatars.githubusercontent.com/u/147565202?v=4" title="Aethan-oss" width="50" height="50"></a>
<a href="https://github.com/Almarante12"><img src="https://avatars.githubusercontent.com/u/149071635?v=4" title="Almarante12" width="50" height="50"></a>
<a href="https://github.com/Beelexpy"><img src="https://avatars.githubusercontent.com/u/147563711?v=4" title="Beelexpy" width="50" height="50"></a>
<a href="https://github.com/Drafty237"><img src="https://avatars.githubusercontent.com/u/147564544?v=4" title="Drafty237" width="50" height="50"></a>
<a href="https://github.com/eliasdrm"><img src="https://avatars.githubusercontent.com/u/114700694?v=4" title="eliasdrm" width="50" height="50"></a>
<a href="https://github.com/katia-tsx"><img src="https://avatars.githubusercontent.com/u/123526476?v=4" title="katia-tsx" width="50" height="50"></a>
<a href="https://github.com/NombreAf"><img src="https://avatars.githubusercontent.com/u/86320830?v=4" title="NombreAf" width="50" height="50"></a>
