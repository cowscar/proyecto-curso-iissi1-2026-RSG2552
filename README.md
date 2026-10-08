# Pokehub

## Miembros del grupo L2-ABS-8

1. Becerra Blanco, Pablo
2. Aboza Gilabert, Daniel
3. Fernández Ruiz, Óscar

## 1. Introducción al problema

- Descripción del problema para poner en contexto el proyecto, incluyendo información sobre los clientes y usuarios, la situación actual, problemas, expectativas, etc. Se valorará la presencia de información multimedia (fotos, gráficos, documentos escaneados, etc.).

## 2. Glosario de términos

- Términos específicos del dominio del problema, ordenados alfabéticamente. Se valorará la presencia de información multimedia.

## 3. Visión general del sistema

### 3.1. Requisitos generales

### 3.2. Usuarios del sistema

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Buscar y filtrar cartas en el catálogo
Como usuario visitante o comprador

quiero buscar cartas aplicando filtros por nombre, expansión y rareza

para consultar rápidamente las ofertas disponibles y su precio mínimo.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### R.F.02. Publicar un ejemplar a la venta
Como vendedor

quiero crear una oferta vinculada a una carta del catálogo indicando su estado de conservación, fotos y precio

para ponerla a disposición de otros usuarios en la plataforma.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### R.F.03. Tramitar y pagar un pedido
Como comprador

quiero formalizar el pago de las cartas seleccionadas

para asegurar el precio fijado y descontar de inmediato las unidades del sto

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### R.F.04. Gestionar el seguimiento del envío
Como vendedor

quiero actualizar el estado de la compra e introducir el código de seguimiento logístico

para que el comprador pueda rastrear la entrega de su paquete.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### R.F.05. Valorar al vendedor tras la compra
Como comprador

quiero calificar con estrellas y dejar una reseña sobre un pedido entregado

para reflejar la reputación del vendedor en la plataforma.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### R.F.06. Gestionar el carrito de la compra
Como comprador

quiero añadir ejemplares a mi cesta, modificar unidades o eliminarlos

para revisar el coste total de mis artículos antes de formalizar la compra.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

#### R.I.01. Registro y perfil de usuarios
Como usuario de la plataforma

quiero que el sistema almacene mis credenciales, datos personales y dirección de entrega

para autenticarme de forma segura y recibir los pedidos en mi domicilio.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### R.I.02. Información de colecciones oficiales
Como coleccionista o visitante

quiero consultar los datos de cada expansión (nombre, serie y fecha de lanzamiento)

para explorar el catálogo agrupado por sus ediciones oficiales.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### R.I.03. Catálogo oficial de cartas
Como usuario del sistema

quiero disponer de la ficha técnica de cada carta (nombre, numeración, tipo y rareza)

para identificar inequívocamente el artículo canónico al comprar o vender.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### R.I.04. Ejemplares físicos en venta
Como vendedor

quiero registrar la información de mi carta física (estado de conservación, idioma, fotos, precio y stock)

para que los compradores conozcan las características exactas del ejemplar que pongo a la venta.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### R.I.05. Carrito de la compra
Como comprador

quiero que el sistema conserve los ejemplares seleccionados y las unidades solicitadas

para calcular el importe provisional y mantener los artículos listos antes de pagar.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### R.I.06. Pedidos y transacciones realizadas
Como comprador o vendedor

quiero registrar el desglose del pedido con los precios congelados, estado y datos de envío

para tener un justificante histórico de la transacción y gestionar su entrega logística.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

#### R.N.01. Prohibición de autocompra
Un usuario registrado no puede añadir al carrito ni adquirir ejemplares en venta publicados por él mismo; el identificador del usuario comprador debe ser estrictamente distinto al identificador del vendedor propietario de la publicación.

#### R.N.02. Inmutabilidad del precio de compra
El precio unitario registrado en una línea de pedido debe capturar y congelar el valor exacto de la publicación en el momento en que se formaliza el pago, garantizando que posteriores cambios de precio aplicados por el vendedor no alteren los importes de pedidos ya creados.

#### R.N.03. Control de stock y agotamiento de oferta
La cantidad solicitada de un artículo no puede superar el stock disponible de la publicación. Tras confirmarse el pago, el stock se reduce de forma automática según las unidades compradas; si el stock resultante es cero, la publicación pasa inmediatamente al estado de "Agotada" o "Vendida", ocultándose de las búsquedas públicas del catálogo.

#### R.N.04. Elegibilidad y unicidad de valoraciones
Únicamente el usuario que figura como comprador puede emitir una reseña sobre una transacción, siempre que el pedido se encuentre en estado "Entregado". Asimismo, el sistema solo permite registrar una única valoración por pedido, bloqueando cualquier intento de calificación duplicada.

#### R.N.05. Unicidad de códigos de certificación
En los ejemplares publicados como cartas graduadas, el número de serie asignado por la empresa certificadora oficial (como PSA, BGS o CGC) debe ser unívoco en el sistema, impidiendo la existencia de dos publicaciones activas simultáneas que compartan la misma entidad evaluadora y el mismo código de certificación.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

#### R.N.F. 01. Tiempo de respuesta en búsquedas

Como usuario visitante o comprador

quiero que las búsquedas y filtrados del catálogo respondan en menos de 2 segundos

para consultar las cartas y ofertas de forma fluida sin tiempos de espera frustrantes.

#### R.N.F. 02. Seguridad y confidencialidad de credenciales

Como usuario registrado

quiero que mis contraseñas se almacenen cifradas y la navegación web viaje cifrada por HTTPS

para proteger mis datos personales y de acceso frente a interceptaciones o accesos no autorizados.

#### R.N.F. 03. Diseño adaptable a dispositivos móviles

Como usuario móvil

quiero que la interfaz visual se ajuste automáticamente a cualquier tamaño de pantalla (móvil, tablet y escritorio)

para gestionar mis compras y ventas cómodamente desde cualquier dispositivo.

#### R.N.F. 04. Disponibilidad del servicio y copias de respaldo

Como usuario de la plataforma

quiero que la web guarde copias de seguridad de manera automática

para acceder a mis pedidos y catálogo en cualquier momento sin que estos se pierdan.

#### R.N.F. 05. Compatibilidad entre navegadores web

Como usuario del sistema

quiero que la aplicación pueda funcionar en distintos navegadores (como Chrome, Firefox, Safari, etc)

para operar con normalidad sin requerir configuraciones adicionales.

#### R.N.F. 06. Integridad transaccional del stock

Como comprador

quiero que el sistema gestione de forma atómica y segura las compras simultáneas de una misma carta

para evitar que dos usuarios adquieran el mismo ejemplar físico a la vez y prevenir incoherencias en el inventario.

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


