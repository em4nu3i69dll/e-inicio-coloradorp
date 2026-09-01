<div align="center">

# e-inicio · Colorado RP

### Una experiencia de bienvenida completa para servidores FiveM

[![FiveM](https://img.shields.io/badge/FiveM-Cerulean-f7931e?style=for-the-badge&logo=fivem&logoColor=white)](#)
[![QBCore](https://img.shields.io/badge/Framework-QBCore-7657ff?style=for-the-badge)](#)
[![Showcase](https://img.shields.io/badge/Repositorio-Showcase-ff9800?style=for-the-badge)](#)
[![Estado](https://img.shields.io/badge/Estado-En%20desarrollo-17141f?style=for-the-badge)](#)

Este repositorio presenta visualmente **e-inicio**, un sistema de onboarding, recompensas y administración creado para Colorado RP.

> **Showcase público:** el código fuente no está incluido ni se distribuye desde este repositorio.

</div>

<a href="./3-%20Inicio.png">
  <img src="./3-%20Inicio.png" alt="Pantalla principal de e-inicio" width="100%">
</a>

<div align="center">

### [▶ Ver demostración completa en YouTube](https://youtu.be/rxNliFkgf94)

<sub>Recorrido en video por la experiencia del jugador y el panel administrativo.</sub>

</div>

## El primer contacto con la ciudad

`e-inicio` reúne en una sola experiencia todo lo que un jugador necesita para comenzar. El recorrido nace en un NPC de bienvenida, continúa con una interfaz inmersiva y permite reclamar beneficios, utilizar códigos de creador, conocer puntos importantes y encontrar trabajos iniciales.

<table>
  <tr>
    <td width="50%" align="center"><strong>NPC de bienvenida</strong></td>
    <td width="50%" align="center"><strong>Carga integrada</strong></td>
  </tr>
  <tr>
    <td width="50%">
      <a href="./1-%20NPC.png"><img src="./1-%20NPC.png" alt="NPC interactivo de bienvenida" width="100%"></a>
    </td>
    <td width="50%">
      <a href="./2-%20Carga.png"><img src="./2-%20Carga.png" alt="Pantalla de carga de e-inicio" width="100%"></a>
    </td>
  </tr>
  <tr>
    <td>Interacción contextual dentro del mundo para acceder a la información inicial.</td>
    <td>Transición visual mientras se recuperan los datos persistentes del personaje.</td>
  </tr>
</table>

## Experiencia del jugador

- Kit inicial único por personaje.
- Recompensas con artículos, dinero y vehículos.
- Canje de códigos de creador con control de usos.
- Destinos importantes con marcado directo en el GPS.
- Trabajos recomendados para comenzar a progresar.
- Navegación visual, rápida y completamente en español.
- Identidad, colores, imágenes y contenido configurables.

<table>
  <tr>
    <td width="50%" align="center"><strong>Exploración de la ciudad</strong></td>
    <td width="50%" align="center"><strong>Trabajos recomendados</strong></td>
  </tr>
  <tr>
    <td width="50%">
      <a href="./4-%20Ciudades.png"><img src="./4-%20Ciudades.png" alt="Ubicaciones importantes de la ciudad" width="100%"></a>
    </td>
    <td width="50%">
      <a href="./5-%20Trabajos.png"><img src="./5-%20Trabajos.png" alt="Trabajos iniciales recomendados" width="100%"></a>
    </td>
  </tr>
  <tr>
    <td>Catálogo de lugares relevantes con información, imágenes y acceso al GPS.</td>
    <td>Actividades iniciales presentadas de forma clara para orientar a nuevos jugadores.</td>
  </tr>
</table>

## Administración en tiempo real

El panel administrativo permite gestionar el sistema sin modificar archivos durante el juego. Toda la configuración dinámica se persiste en la base de datos y las operaciones sensibles se validan desde el servidor.

<a href="./6-%20PanelInicio.png">
  <img src="./6-%20PanelInicio.png" alt="Resumen del panel administrativo" width="100%">
</a>

<div align="center">
  <sub>Resumen de personajes registrados, kits entregados, canjes, códigos activos y actividad reciente.</sub>
</div>

### Configuración de recompensas

Los administradores pueden definir exactamente qué recibe cada personaje: artículos, cantidades, saldo inicial, cuenta de destino y vehículo de bienvenida.

<a href="./7-%20Kit%20Inicial%20Edit.png">
  <img src="./7-%20Kit%20Inicial%20Edit.png" alt="Editor administrativo del kit inicial" width="100%">
</a>

### Catálogos visuales

Los selectores integrados evitan trabajar con nombres internos de memoria. El panel consulta los artículos disponibles en `ox_inventory` y ofrece un catálogo visual de vehículos con búsqueda y categorías.

<table>
  <tr>
    <td width="50%" align="center"><strong>Catálogo de vehículos</strong></td>
    <td width="50%" align="center"><strong>Catálogo de artículos</strong></td>
  </tr>
  <tr>
    <td width="50%">
      <a href="./8-%20Carrusel%20autos.png"><img src="./8-%20Carrusel%20autos.png" alt="Selector visual de vehículos" width="100%"></a>
    </td>
    <td width="50%">
      <a href="./9-%20Carrusel%20items.png"><img src="./9-%20Carrusel%20items.png" alt="Selector visual de artículos de ox_inventory" width="100%"></a>
    </td>
  </tr>
</table>

### Códigos de creador

Cada código puede tener su propia combinación de artículos, dinero y vehículo, además de estado y límite de usos. El sistema admite códigos ilimitados o promociones con disponibilidad controlada.

<a href="./10-%20Crear%20codigo.png">
  <img src="./10-%20Crear%20codigo.png" alt="Creación y configuración de códigos de creador" width="100%">
</a>

### Seguimiento de canjes

El historial permite buscar personajes por nombre, `citizenid` o código, aplicar filtros y restablecer reclamos cuando sea necesario.

<a href="./11-%20Estado%20de%20canjes.png">
  <img src="./11-%20Estado%20de%20canjes.png" alt="Seguimiento administrativo de canjes" width="100%">
</a>

## Funciones principales

| Jugadores | Administración | Integraciones |
| --- | --- | --- |
| NPC interactivo | Métricas generales | QBCore |
| Kit inicial único | Editor del kit | oxmysql |
| Códigos promocionales | Gestión de códigos | ox_inventory |
| Ubicaciones con GPS | Historial de canjes | prism_uipack |
| Trabajos recomendados | Catálogos visuales | Esquemas JG/QBCore |
| Vehículo de bienvenida | Registros administrativos | qb-vehiclekeys opcional |

## Diseño adaptable

La interfaz puede personalizarse para cada servidor mediante:

- Nombre e identidad visual.
- Colores principal y secundario.
- Logo, fondos y personajes.
- NPC, ubicación y distancia de interacción.
- Destinos y trabajos recomendados.
- Contenido del kit y códigos de creador.
- Vehículos, garaje y formato de matrículas.

## Disponibilidad

`e-inicio` es un proyecto propietario. Este repositorio funciona exclusivamente como **expositor visual** y no contiene archivos ejecutables, configuraciones, SQL ni código fuente.

## Autor

<div align="center">

Diseñado y desarrollado por **EM4NU3L69dll**.

Todos los derechos reservados. No se autoriza la copia, redistribución, reventa o reproducción del proyecto ni de sus recursos visuales sin permiso expreso.

</div>
