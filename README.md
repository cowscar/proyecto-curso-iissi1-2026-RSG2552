# Pokehub

<img width="1024" height="572" alt="image" src="https://github.com/user-attachments/assets/6d337fe9-61c0-4fb7-9b79-3c3e01ca76cc" />

## Miembros del grupo L2-ABS-8

1. Becerra Blanco, Pablo
2. Aboza Gilabert, Daniel
3. Fernández Ruiz, Óscar

## 1. Introducción al problema

El coleccionismo y comercio de cartas de Pokémon está teniendo un crecimiento exponencial, sobre todo en el mercado internacional. Este tipo de transacciones se realiza con frecuencia mediante plataformas de segunda mano o foros no especializados en el sector, donde conviven tanto usuarios interesados únicamente en explorar o consultar colecciones como usuarios interesados en la compra-venta.

<img width="500" height="750" alt="image" src="https://github.com/user-attachments/assets/90af7c1d-c6f9-4217-8247-2452137f6e73" />


Las actividades más comunes en este tipo de webs tratan desde la consulta de colecciones oficiales y la búsqueda de publicaciones individuales hasta la negociación del precio, el pago, el envio del ejemplar y el seguimiento de este.

La falta de una herramienta dedicada específicamente al ecosistema de las cartas Pokémon conlleva una serie de ineficiencias y problemas asociados, como por ejemplo:
  1) Búsqueda e identificación imprecisas: La ausencia de filtros específicos para cada expansión/colección, número de carta, rareza y otra larga lista de aspectos claves de las cartas dificultan que los compradores consulten y localicen rápidamente las ofertas deseadas dentro del catálogo.
  2) Poca fiabilidad en las características del ejemplar: En la mayoría de plataformas resulta complejo y poco fiable detallar aspectos específicos clave como el estado de conservación de la carta, el idioma o la presencia de certificaciones oficiales de autenticidad.
  3) Variabilidad de precios en la compra: Al tramitar compras, la modificación del precio por parte del vendedor antes o durante el proceso genera conflictos sobre el importe exacto acordado en la transacción.
  4) Falta de seguimiento al pedido y informes de reputación: Los compradores sufren la falta de seguimiento claro en los envíos y carecen de un sistema transparente de valoraciones que limite las reseñas únicamente a pedidos efectivamente entregados y a una sola reseña por transacción.

Nuestro sistema esta concebido como una plataforma orientada a resolver las necesidades de tres usuarios principales:
  1) Visitantes y coleccionistas: Consultarán información técnica
  2) Compradores: Gestionan el carrito de compra
  3) Vendedores: Necesitan registrar sus ejemplares así como el estado de sus envíos.
Todos estos usuarios se explicaran con más detalle en los apartados posteriores.

Nuestra plataforma Pokehub dará respuesta a estas espectativas garantizando la integridad del stock, asegurando la inmutabilidad de los precios al formalizar el pedido, aplicando códigos de certificación de las cartas gradeadas, restringiendo las autocompras, respaldando la seguridad de los datos de nuestros usuarios entre otros aspectos.

## 2. Glosario de términos

| Término | Definición | Imagen |
|:---| :--- | :---: |
| **Carta de Catálogo (Ficha Canónica)** | Representación abstracta y oficial de una carta en el sistema, independiente de cualquier copia física. Contiene los datos inmutables definidos por el fabricante (nombre del Pokémon o entrenador, tipo elemental, puntos de salud, ilustrador, rareza y número dentro de la colección). | <img width="255" height="361" alt="Carta de catálogo" src="https://github.com/user-attachments/assets/1faa0a09-9d6d-4c12-9923-f244bfaee1b7" />|
| **Carta raw** | Carta física coleccionable que no ha sido enviada a gradear ni sellada en una cápsula rígida por ninguna empresa de gradeo. | <img width="648" height="857" alt="Carta raw" src="https://github.com/user-attachments/assets/f7792e7c-acde-4c7a-b68f-28f7394dc0c3" />|
| **Colección / Expansión (Set)** | Conjunto oficial cerrado de cartas lanzadas al mercado en una fecha concreta bajo una serie o era determinada. Define la numeración de las cartas que contiene. | <img width="1280" height="720" alt="Sets" src="https://github.com/user-attachments/assets/76418142-397a-465f-bc5d-b62b8cfbb8a1" />|
| **Empresa Certificadora / Empresa de gradeo** | Entidad externa e independiente (como PSA, Beckett/BGS o CGC) dedicada a autenticar cartas coleccionables, evaluar su estado de conservación microscópico y encapsularlas de forma permanente. | <img width="512" height="512" alt="Empresa de gradeo" src="https://github.com/user-attachments/assets/a8cda587-b4a0-44b8-89e6-a1722e2e3a27" />|
| **Estado de Conservación** | Métrica estándar utilizada en el mercado secundario para clasificar el desgaste físico de una carta no gradeada. Las categorías habituales incluyen Mint/Near Mint (NM, impecable o con desgaste casi imperceptible), Lightly Played (LP, marcas leves o micro-rozaduras), Moderately Played (MP, bordes blanqueados o pliegues menores) y Damaged/Poor (daños severos, arrugas o manchas). | <img width="47" height="98" alt="Estado" src="https://github.com/user-attachments/assets/40f0c322-dfd3-4f33-a924-c80ba4d54024" />|
| **Graduación (Grading)** | Calificación numérica (en una escala del 1 al 10) otorgada por una empresa certificadora que puntua el centrado, las esquinas, los bordes y la superficie de la carta física. | <img width="97" height="46" alt="Gradeo" src="https://github.com/user-attachments/assets/65985731-c8f6-4bce-a65a-9eb6e4ef8f58" />|
| **Idioma de Impresión** | Lenguaje en el que fue fabricada la carta. Afecta directamente al valor de mercado del artículo; las impresiones más cotizadas y comercializadas son en japonés (JP) e inglés (EN), seguidas por las ediciones en español (ES) y otros idiomas europeos. | <img width="104" height="52" alt="Idioma" src="https://github.com/user-attachments/assets/23ea6689-fc3e-4e14-88da-a3a9fcf23e0c" />|
| **Número de Carta** | Fracción impresa en la esquina inferior de la carta que indica su posición respecto al total oficial del set (por ejemplo, 025/165). | <img width="100" height="48" alt="Número de carta" src="https://github.com/user-attachments/assets/a428dea9-ffce-45fa-ba42-cc82f3de51d2" />|
| **Número de Certificación** | Código único e irrepetible emitido por la empresa certificadora e impreso en la etiqueta del slab. Sirve para validar la autenticidad del ejemplar en la base de datos pública del gradeador. | <img width="136" height="102" alt="Número certificación" src="https://github.com/user-attachments/assets/1fa75b86-4722-4209-b70d-69d22e7331e3" />|
| **Rareza** | Categorización asignada oficialmente a una carta que determina su probabilidad de aparición en sobres de cartas (Común, Infrecuente, Holo Rare, Ultra Rare, Illustration rare, Special Ilustration Rare, Hyper Rare, etc...). | <img width="60" height="42" alt="image" src="https://github.com/user-attachments/assets/41ded67c-781e-4f55-90ff-e8190993696e" />|
| **Slab** |  Estuche rígido de plástico transparente termosellado e imposible de abrir en cuyo interior queda protegida una carta gradeada junto a su etiqueta de certificación oficial. | <img width="356" height="600" alt="Slab" src="https://github.com/user-attachments/assets/81598617-2a49-4908-b8e6-c6c4c27e2ead" />|
| **Sleeve** |  Funda de plástico suave y fina ajustada para evitar arañazos. | <img width="603" height="426" alt="Sleeve" src="https://github.com/user-attachments/assets/1be07e85-a88b-4e1c-80df-64c1b24c6f91" />|
| **TCG (Trading Card Game)** |  Siglas en inglés de Juego de Cartas Coleccionables (JCC), género lúdico y de coleccionismo sobre el que opera el catálogo del sistema. | <img width="312" height="160" alt="Pokemon TCG" src="https://github.com/user-attachments/assets/256c8d1a-7407-4b5b-a3d4-fca696e2a77a" />|
| **Toploader** |  Funda de plástico rígido donde se inserta la carta previamente enfundada para impedir dobleces durante el almacenaje o el transporte. | <img width="1599" height="1284" alt="Toploader" src="https://github.com/user-attachments/assets/9e8c1d5e-b441-4674-9ea0-82f77808d5d1" />|

## 3. Visión general del sistema

### 3.1. Requisitos generales

#### R.G.01. Plataforma de compraventa con catálogo desacoplado
El sistema debe proporcionar un punto de encuentro web seguro para compradores y vendedores particulares de cartas de Pokémon TCG, manteniendo una separación estricta entre el catálogo oficial canónico (referencia abstracta de colecciones, numeración y rarezas) y los ejemplares físicos puestos a la venta (artículos reales definidos por su estado de conservación, idioma, fotografías y precio fijado por el vendedor).

#### R.G.02. Gestión integral de transacciones y sistema de confianza
La aplicación debe cubrir todo el flujo comercial (carrito de compra temporal, formalización de pedidos con precios congelados, seguimiento logístico y confirmación de entrega) e integrar mecanismos antifraude basados en un sistema público de valoraciones y en la verificación de códigos únicos de certificación para cartas gradeadas.

#### R.G.03. Accesibilidad web multiplataforma y privacidad como norma
El sistema debe operar como cliente ligero accesible desde navegadores web (en móvil, tablet y escritorio) sin requerir instalaciones locales, garantizando en todo momento el cumplimiento de la normativa de protección de datos, el cifrado de credenciales y la confidencialidad de los datos personales entre las partes de cada pedido.

### 3.2. Usuarios del sistema
**Usuario visitante**
Es cualquier persona que accede a la plataforma web sin haber iniciado sesión o sin disponer de una cuenta. Solo tiene acceso a la información pública.

**Usuario Registrado**
Es un usuario que ha completado el proceso de registro e inicio de sesión en la plataforma. Sobre este usuario se construirán las entidades según el rol que tengan como comprador/vendedor.
Este usuario tendrá acceso a la gestión de sus datos personales aparte de la información pública.

**Comprador** 
Es cualquier usuario registrado que utiliza la plataforma con el propósito de adquirir ejemplares de cartas físicas ofertados por otros usuarios. Tendrá acceso a herramientas de gestión de compras, carrito y recepción de productos.
Restricción: No puede añadir al carrito ni adquirir ejemplares creados por él mismo.

**Vendedor**
Es cualquier usuario registrado que pone a disposición del mercado ejemplares físicos de sus cartas Pokémon para su venta. Tiene acceso a herramientas de publicación, gestión de inventario/stock y logística de envíos.
Restricción: El vendedor no puede comprar sus propias publicaciones.

**Administrador**
Es el responsable de velar por la seguridad de la información y la continuidad del servicio. Tiene acceso administrativo a nivel de datos e infraestructura.

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Consultar y filtrar cartas del catálogo oficial

Como usuario visitante o comprador  
quiero consultar el listado de cartas del catálogo filtrando por nombre, colección, rareza o tipo elemental  
para localizar la ficha técnica oficial de las cartas que me interesan.

#### R.F.02. Consultar el listado de colecciones y expansiones

Como coleccionista o visitante  
quiero consultar todas las colecciones registradas ordenadas por serie y fecha de lanzamiento  
para conocer las ediciones oficiales disponibles en el sistema y el tamaño de cada set.

#### R.F.03. Consultar ofertas activas de una carta concreta

Como comprador  
quiero consultar todos los ejemplares en estado "Activo" asociados a una carta del catálogo, pudiendo filtrar por idioma, estado de conservación y rango de precio  
para comparar las distintas opciones de compra y elegir la oferta que mejor se adapte a mi presupuesto.

#### R.F.04. Consultar el detalle completo de un ejemplar y su certificación

Como comprador  
quiero consultar la vista detallada de una publicación (incluyendo fotografías reales, stock, vendedor y datos de graduación/código de certificado si es un *slab*)  
para verificar el estado físico y la autenticidad de la carta antes de añadirla al carrito.

#### R.F.05. Consultar el contenido y subtotal del carrito de la compra

Como comprador  
quiero consultar los ejemplares que tengo guardados actualmente en mi carrito junto con las unidades seleccionadas y el importe total acumulado  
para revisar el coste provisional de mi cesta antes de tramitar el pedido.

#### R.F.06. Consultar el inventario de publicaciones propias

Como vendedor  
quiero consultar el listado de todos los ejemplares que he puesto a la venta filtrando por su estado (Activa, Agotada o Retirada)  
para llevar el control de mi stock disponible y de las cartas que ya se han vendido.

#### R.F.07. Consultar el historial de pedidos realizados y su seguimiento

Como comprador  
quiero consultar mis pedidos históricos y en curso junto con su estado actual y código de seguimiento logístico (*tracking*)  
para rastrear el envío de mis paquetes y saber cuándo han sido entregados.

#### R.F.08. Consultar el desglose y factura de un pedido

Como comprador o vendedor  
quiero consultar las líneas de detalle de un pedido específico mostrando las cartas adquiridas, cantidades y los precios unitarios congelados en el momento de la compra  
para disponer del justificante económico exacto de la transacción sin que afecten cambios posteriores de precio.

#### R.F.09. Consultar los pedidos pendientes de envío

Como vendedor  
quiero consultar la lista de pedidos pagados que contienen ejemplares míos y que aún se encuentran pendientes de envío  
para conocer la dirección de entrega de los compradores y preparar los paquetes correspondientes.

#### R.F.10. Consultar el perfil de reputación y valoraciones de un vendedor

Como comprador  
quiero consultar la puntuación media de un vendedor y el listado histórico de reseñas y comentarios dejados por otros compradores en sus pedidos entregados  
para evaluar su fiabilidad antes de comprarle una carta.

#### 4.1.1. Requisitos de información

##### R.I.01. Registro y perfil de usuarios

Como usuario de la plataforma  
quiero que el sistema almacene mis credenciales, datos personales y dirección de entrega  
para autenticarme de forma segura y recibir los pedidos en mi domicilio.

* **Atributos asociados:**
  * `idUsuario`: Identificador único del usuario.
  * `nickname`: Nombre de usuario.
  * `nombreCompleto`: Nombre y apellidos reales del usuario.
  * `email`: Dirección de correo electrónico.
  * `passwordHash`: Contraseña cifrada de acceso.
  * `direccionPostal`: Calle, número, piso, ciudad, código postal y país.
  * `fechaRegistro`: Fecha de alta en la plataforma.
  * `reputacionMedia`: Valoración media calculada como vendedor (1 a 5).

##### R.I.02. Información de colecciones oficiales

Como coleccionista o visitante  
quiero consultar los datos de cada expansión (nombre, serie y fecha de lanzamiento)  
para explorar el catálogo agrupado por sus ediciones oficiales.

* **Atributos asociados:**
  * `idColeccion`: Código o identificador único de la colección.
  * `nombreColeccion`: Nombre oficial del set.
  * `serie`: Era o bloque al que pertenece.
  * `fechaLanzamiento`: Fecha oficial de salida al mercado.
  * `totalCartasOficiales`: Número base de cartas que componen el set estándar.

##### R.I.03. Catálogo oficial de cartas

Como usuario del sistema  
quiero disponer de la ficha técnica de cada carta (nombre, numeración, tipo y rareza)  
para identificar inequívocamente el artículo canónico al comprar o vender.

* **Atributos asociados:**
  * `idCarta`: Identificador único de la carta en el catálogo.
  * `nombreCarta`: Nombre oficial del Pokémon, Entrenador o Energía.
  * `numeroCarta`: Numeración secuencial dentro de su colección.
  * `rareza`: Nivel de escasez oficial.
  * `tipoCategoria`: Tipo elemental o subcategoría.
  * `urlImagenOficial`: Enlace a la imagen de referencia del catálogo.

##### R.I.04. Ejemplares físicos en venta

Como vendedor  
quiero registrar la información de mi carta física (estado de conservación, idioma, fotos, precio y stock)  
para que los compradores conozcan las características exactas del ejemplar que pongo a la venta.

* **Atributos asociados:**
  * `idPublicacion`: Identificador único de la oferta o ejemplar en venta.
  * `estadoConservacion`: Estado físico de la carta.
  * `idioma`: Idioma de impresión.
  * `precioUnitario`: Importe de venta fijado por el vendedor.
  * `stockDisponible`: Cantidad de unidades físicas iguales disponibles.
  * `urlFotografiasReales`: Imagen o imágenes reales del ejemplar subidas por el vendedor.
  * `estadoPublicacion`: Disponibilidad de la oferta.
  * `esGraduada`: Indicador booleano de si la carta está certificada.
  * `empresaCertificadora`: Entidad evaluadora si está graduada.
  * `codigoCertificacion`: Código del certificado oficial.
  * `notaGraduacion`: Calificación numérica oficial del 1 al 10 (si está graduada).

##### R.I.05. Carrito de la compra

Como comprador  
quiero que el sistema conserve los ejemplares seleccionados y las unidades solicitadas  
para calcular el importe provisional y mantener los artículos listos antes de pagar.

* **Atributos asociados:**
  * `idItemCarrito`: Identificador de la línea o elemento dentro del carrito.
  * `cantidadSeleccionada`: Número de unidades del ejemplar que se desean comprar.
  * `fechaAgregado`: Fecha y hora en que se introdujo el artículo en la cesta.

##### R.I.06. Pedidos y transacciones realizadas

Como comprador o vendedor  
quiero registrar el desglose del pedido con los precios congelados, estado y datos de envío  
para tener un justificante histórico de la transacción y gestionar su entrega logística.

* **Atributos asociados a la cabecera del Pedido:**
  * `idPedido`: Identificador único de la transacción.
  * `fechaHoraCompra`: Instante exacto de formalización del pago.
  * `importeTotal`: Suma económica total del pedido.
  * `estadoPedido`: Fase logística (*Pagado*, *Enviado*, *Entregado*, *Cancelado*).
  * `direccionEntrega`: Dirección postal donde se envía el paquete.
  * `codigoSeguimiento`: Código único proporcionado por la empresa de mensajería.
* **Atributos asociados a la Línea de Pedido:**
  * `idLineaPedido`: Identificador único de cada línea dentro del pedido.
  * `cantidadComprada`: Unidades adquiridas de ese ejemplar concreto.
  * `precioUnitarioCongelado`: Precio exacto al que se pagó la unidad en el momento de la compra.
* **Atributos asociados a la Valoración del Pedido:**
  * `puntuacion`: Calificación de 1 a 5 estrellas emitida por el comprador tras la entrega.
  * `comentarioResena`: Texto sobre el trato, envío y estado de la carta.
  * `fechaValoracion`: Fecha de emisión de la reseña.
    
#### 4.1.2. Reglas de negocio

#### R.N.01. Prohibición de autocompra
Un usuario registrado no puede añadir al carrito ni adquirir ejemplares en venta publicados por él mismo; el identificador del usuario comprador debe ser estrictamente distinto al identificador del vendedor propietario de la publicación.

#### R.N.02. Inmutabilidad del precio de compra
El precio unitario registrado en una línea de pedido debe capturar y congelar el valor exacto de la publicación en el momento en que se formaliza el pago, así, si el vendedor modifica el precio original, el de la línea de pedido ya creada no se ve afectado.

#### R.N.03. Control de stock y agotamiento de oferta
La cantidad solicitada de un artículo no puede superar el stock disponible de la publicación. Tras confirmarse el pago, el stock se reduce de forma automática según las unidades compradas; si el stock resultante es cero, la publicación pasa inmediatamente al estado de "Agotada", ocultándose del catálogo.

#### R.N.04. Elegibilidad y unicidad de valoraciones
Únicamente el usuario que figura como comprador puede emitir una reseña sobre una transacción, siempre que el pedido se encuentre en estado "Entregado". Además, el sistema solo permite registrar una única valoración por pedido.

#### R.N.05. Unicidad de códigos de certificación
En los ejemplares publicados como cartas gradeada, el código de certificación asignado por la empresa certificadora oficial (como PSA, BGS o CGC) debe ser único en el sistema, por lo que no pueden existir dos publicaciones activas simultáneas que compartan la misma empresa y el mismo código de certificación.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

#### R.N.F. 01. Tiempo de respuesta en búsquedas

Como usuario visitante o comprador

quiero que las búsquedas y filtrados del catálogo respondan en menos de 2 segundos

para consultar las cartas y ofertas de forma fluida sin tiempos de espera frustrantes.

#### R.N.F. 02. Seguridad y confidencialidad de credenciales

Como usuario registrado

quiero que mis contraseñas estén cifradas y la navegación web sea segura,

para proteger mis datos personales y de acceso frente accesos no autorizados.

#### R.N.F. 03. Disponibilidad del servicio y copias de respaldo

Como usuario de la plataforma

quiero que la web guarde copias de seguridad de manera automática

para acceder a mis pedidos y catálogo en cualquier momento sin que estos se pierdan.

#### R.N.F. 04. Compatibilidad entre navegadores web

Como usuario del sistema

quiero que la aplicación pueda funcionar en distintos navegadores (como Chrome, Firefox, Safari, etc)

para operar con normalidad sin requerir configuraciones adicionales.

#### R.N.F. 05. Integridad transaccional del stock

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


