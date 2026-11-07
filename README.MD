# Práctica 3 – Interacción VR

## Descripción del proyecto

Proyecto desarrollado en Unreal Engine utilizando la plantilla XR, cuyo objetivo es implementar diferentes minijuegos y elementos interactivos mediante realidad virtual, sistemas de agarre y físicas.

## Funcionalidades implementadas

### 1. Bolos

- Implementación de una bola con un componente de agarre (`BP_GrabComponent`) para que el jugador pueda cogerla y manipularla.
- Los bolos cuentan con físicas que permiten que sean derribados al recibir el impacto de la bola.
- Interacción basada en el comportamiento físico de los objetos.

### 2. Mr. Potato

- Incorporación de las diferentes piezas del personaje: ojos, orejas, nariz y demás componentes.
- Implementación de un collider en el cuerpo de Mr. Potato que permite detectar cuándo se introducen las piezas en su zona de interacción.
- Cuando el jugador suelta una pieza dentro de dicho collider, esta queda unida al cuerpo mediante el sistema de agarre y acoplamiento de componentes (`Attach Actor To Component`).
- Posibilidad de colocar y reorganizar las diferentes partes del personaje mediante interacción VR.

### 3. Wreck-It Ralph

- Implementación de objetos destructibles mediante el sistema de fractura de Unreal Engine (Chaos Destruction).
- Utilización de Geometry Collections para dividir los objetos en diferentes fragmentos.
- Configuración de la fractura mediante el método Uniform Voronoi.
- Incorporación de una estatua y una piñata como elementos destructibles.
- **Piñata:** se fractura correctamente al recibir un impacto, generando numerosos fragmentos.
- **Estatua:** aunque se ha configurado su fractura y se generan los fragmentos, al recibir un impacto el objeto desaparece visualmente en lugar de mostrar correctamente la rotura. No he conseguido solucionar este comportamiento durante el desarrollo. Como la piñata se fractura bien, asumo que es un problema relacionado con la estatua.

### 4. Diana y dardos

- Incorporación de dos dianas con diferentes disposiciones dentro del escenario.
- Sistema de detección de impactos mediante `On Component Hit`.
- Los dardos quedan fijados a la diana al entrar en contacto con ella.
- Sistema de puntuación acumulativa que aumenta 10 puntos por cada impacto.
- Visualización de la puntuación directamente en la diana mediante un componente `TextRender`.

Se han implementado dos situaciones:

- **Diana horizontal:** un dardo cae automáticamente al comenzar la experiencia, mostrando el funcionamiento del impacto y la actualización de la puntuación.
- **Diana vertical:** el jugador puede agarrar los dardos colocados en el suelo, acercarlos a la diana y soltarlos para que queden clavados y se contabilice la puntuación.

## Controles e interacción

La interacción con los diferentes elementos se realiza mediante los sistemas de agarre de la plantilla XR, permitiendo recoger, manipular y soltar objetos dentro del entorno virtual.
