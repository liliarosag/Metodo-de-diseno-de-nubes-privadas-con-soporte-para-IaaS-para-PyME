# Guía para la aplicación del "Método de diseño de nubes privadas con soporte para la categoría de infraestructura como servicio para pequeñas y medianas empresas"  
## Principios para la concepción del método de diseño y premisas necesarias para su aplicación exitosa  
Con el objetivo de lograr una relación suficiente entre las estrategias y procedimientos de diseño de Centros de Datos (CD) privados que implementen el paradigma de la Computación en la Nube (CN) para brindar Infraestructura como Servicio (IaaS, _Infrastructure as a Service_), y los objetivos del negocio, restricciones y requerimientos técnicos de las Pequeñas y Medianas Empresas (PyME) que los necesitan, se propone un método de diseño basado en los siguientes principios:  
* Diseño desde la perspectiva del negocio: el método debe alinear el diseño técnico de la Nube Privada (NP) con soporte para la categoría de IaaS con los objetivos del negocio de la entidad cliente, así como con sus criterios de éxito, regulaciones, políticas, preferencias, requerimientos técnicos y restricciones.  
* Facilidad de aplicación: el método debe brindar los procedimientos de diseño, instrumentos y herramientas necesarios y suficientes para la aplicación del método.
* Agilidad: el método debe contener el mínimo número de puntos de retornos e iteraciones necesario.  
* Independencia tecnológica: el método debe sustentarse en el empleo de tecnologías y soluciones de tipo Software Libre y Código Abierto (SLCA) (SW SLCA) y Hardware de tipo _Commercial Off-The-Shelf_ (COTS) (HW COTS).  
* Adaptabilidad: el método debe ser fácilmente actualizado y mantenido en el tiempo.  
* Factibilidad económica: el método debe conducir a la solución con mejor factibilidad económica posible que mejor se adecúe a las necesidades de la entidad cliente.
  
A su vez, se consideraron un conjunto de premisas para la aplicación exitosa del método:    
* La entidad debe apostar por las NP con soporte a la categoría de IaaS de tipo _on premises_, como solución económica, efectiva y segura para el soporte y aprovisionamiento de sus servicios.  
* El personal que gestiona las Tecnologías de la Información y las Comunicaciones (TIC) debe estar calificado para operar, administrar y mantener infraestructuras virtualizadas de servidores, almacenamiento y red, así como presentar disposición a asimilar nuevas tecnologías del paradigma de la CN.  
* La entidad debe incentivar la adopción de tecnologías de tipo SW SLCA y HW COTS para lograr independencia tecnológica.
## Esquema general del método de diseño  
La  [Figura 1](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/blob/main/Documentos%20complementarios/Esquema%20general%20del%20m%C3%A9todo%20de%20dise%C3%B1ov2.jpg) muestra el esquema general del método de diseño. Consta de cuatro fases, en donde tomando como referencia la filosofía de diseño _top-down_, la primera y última fase poseen un enfoque sistémico. La Fase 1 identifica los objetivos del negocio, las regulaciones, las políticas, los requerimientos técnicos y las restricciones a cumplir durante el desarrollo del proyecto; mientras la Fase 4 despliega, evalúa, entrega y cierra el proyecto.

![Figura 1](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/blob/main/Documentos%20complementarios/Esquema%20general%20del%20m%C3%A9todo%20de%20dise%C3%B1ov2.jpg)  
Figura 1. Esquema general del método de diseño de NP con soporte a la categoría de IaaS para PyME  

La Fase 2, se encuentra dividida en cinco sub-fases, que se hacen corresponder con el diseño de los subsistemas de la infraestructura de una NP. Las sub-fases son desarrolladas de forma independiente en busca de simplicidad, con un orden de precedencia establecido, aplicando en cada una la filosofía de las cuatro fases del diseño _top-down_. En consecuencia, el procedimiento presenta una organización fundamentalmente secuencial, en el que se definen puntos de retorno para propiciar la corrección de las deficiencias que identifiquen los procesos de pruebas y optimización. La Fase 3 aborda la licitación del equipamiento de nueva adquisición del proyecto a los proveedores, y la selección de la solución que mejor se adecúe al caso de uso en cuestión en función de lo identificado en la Fase 1.

El orden de precedencia en el diseño de los subsistemas en la Fase 2 fue definido en base a que: 
* **Sub-fase 2.1:** La Plataforma de Gestión de Nube (CMP, _Cloud Management Platform_) es el elemento que integra a los subsistemas que conforman la infraestructura TIC, logrando su orquestación y gestión como un todo. Por consiguiente, las diferentes tecnologías y soluciones a seleccionar para desplegar la NP, tienen que ser soportadas eficaz y eficientemente por el gestor, de lo contrario se complejizaría la Operación, Administración y Mantenimiento (OAM) del sistema y los servicios. A su vez, el gestor incide directamente en los diseños lógico y físico de la infraestructura TIC, como, por ejemplo, en el soporte de una infraestructura convergente o no, o en el soporte de diferentes tecnologías de virtualización en un mismo nodo, incidiendo directamente en el diseño de los subsistemas de cómputo y de almacenamiento.  
* **Sub-fase 2.2:** El par CMP-solución de virtualización determina las Agrupaciones de Recursos de Cómputo (ARC) que tendrá la NP/Centro de Datos Virtualizado (CDV). Una ARC es el conjunto de nodos de cómputo configurados con la misma solución(es) de virtualización, la que soportará un conjunto de aplicaciones/servicios. En  consecuencia, su definición influye directamente en el diseño del subsistema de los nodos de cómputo, y su dimensionamiento. A su vez, la compatibilidad del par CMP-solución de virtualización con el Almacenamiento Definido por Software (SDS, _Software-Defined Storage_) a seleccionar en el diseño del Sistema de Almacenamiento (SA) debe ser considerada y comprobada. El proceso de selección y de puesta a punto de una solución de virtualización es más simple, que el diseño y despliegue de un SA.  
* **Sub-fase 2.3:** el SA alberga los discos de las instancias virtuales. En consecuencia, ante el despliegue de un prototipo de pruebas lo más cercano posible al diseño de la NP/CDV que esté siendo concebida, una migración paulatina a esta durante el desarrollo del proyecto, e inclusive su puesta a punto, el SA debe estar diseñado y desplegado ante que los nodos de cómputo, para poder almacenar los datos de las aplicaciones/servicios a soportar.  Su compatibilidad con el par CMP-solución de virtualización de servidores debe ser garantizado, así como su correcto desempeño.  
* **Sub-fase 2.4:** El dimensionamiento de los nodos de cómputo se encuentra determinado por la demanda de las aplicaciones/servicios a soportar, el _overhead_ que imponen las soluciones de virtualización de servidores, el CMP, la solución del SA; y los requerimientos de HW que imponga el SA en caso de la posibilidad de una infraestructura convergente.  
* **Sub-fase 2.5:** la Red del Centro de Datos (DCN, _Data Center Network_) es dimensionada en función de: la red del SA diseñada y el número de nodos de cómputo concebido, junto al número y tipo de Tarjetas de Interfaces de Red (NIC, _Network Interface Card_) por servidor físico. 

Se propone que el diseño de los subsistemas de: CMP, SA y recursos de cómputo sea proyectado táctica y estratégicamente. El diseño táctico, es el que será desplegado de forma inmediata en la puesta a punto del proyecto, y el estratégico será contemplado para garantizar la Escalabilidad Horizontal (EH) de la infraestructura de la NP. 

La proyección estratégica no debe superar los tres años, debido a que es el tiempo de obsolescencia tecnológica actual del equipamiento correspondiente a las TIC. Adquirir equipamiento a explotar con una proyección superior a los tres años, puede acarrear impactos económicos negativos como por ejemplo que: el Retorno de la Inversión (RoI, _Return of Investment_) sea lento, debido a una baja utilización de los recursos, no cumpliéndose lo estimado táctica y estratégicamente; y/o que el RoI del equipamiento comprado se vea afectado por la rápida depreciación. Siguiendo esta línea se propone en consecuencia dimensionar tácticamente para un 100% de Escalabilidad Vertical (EV), y escalar horizontalmente en caso necesario.

Los recursos facilitadores de la NP de: construcción física de las instalaciones, distribución de _racks_ y cableado estructurado, el subsistema de Calefacción, Ventilación y Aire Acondicionado (HVAC, _Heating, Ventilation and Air Conditioning_), el subsistema de protección ante incendios, y el subsistema de seguridad física, sí se propone que sean  diseñados bajo requerimientos y objetivos estratégicos, debido a los grandes esfuerzos económicos y de tiempo de obra que implican su montaje y rediseño, los que pueden acarrear la interrupción de los servicios. En consecuencia, para mantener la EH, se calcula el Factor de Crecimiento de la NP/CDV a Largo Plazo (FCLP) como variable de entrada del diseño estratégico de los recursos facilitadores.

A su vez, se propone que como mínimo una vez al año se analice la Calidad de servicio (QoS, _Quality of Service_) de los servicios e infraestructura de la NP, con el objetivo de identificar nuevos requerimientos de capacidad. Además, se considera que el reaprovisionamiento del HW se debe hacer de forma escalonada y bajo un ciclo que comience a partir de transcurrida la mitad del tiempo de vida declarado por el fabricante del equipamiento.

## Estructura de los documentos e instrumentos para la aplicación del método de diseño
La ejecución del método de diseño debe ser secuencial como indica el esquema general mostrado en la [Figura 1](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/blob/main/Documentos%20complementarios/Esquema%20general%20del%20m%C3%A9todo%20de%20dise%C3%B1ov2.jpg). La estructura de los documentos e instrumentos para la aplicación del método de diseño es:
* [Documentos complementarios](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/tree/main/Documentos%20complementarios):  
  * [Figura](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/blob/main/Documentos%20complementarios/Esquema%20general%20del%20m%C3%A9todo%20de%20dise%C3%B1ov2.jpg): Esquema general del método de diseño.
  * [Documento](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/blob/main/Documentos%20complementarios/ARF%20Nube%20Privada%20IaaS.pdf): Arquitectura de Referencia Funcional (ARF) de la NP con soporte a la categoría de IaaS.
  * [Documento](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/blob/main/Documentos%20complementarios/RNF%20pruebas%20evaluaci%C3%B3n.pdf): Requerimientos no Funcionales (RNF) y pruebas que permiten evaluar las capacidades de la NP.
* [Fase 1](https://github.com/liliarosag/Metodo-de-diseno-de-nubes-privadas-con-soporte-para-IaaS-para-PyME/tree/main/Fase%201): Contiene el procedimiento y los instrumentos para el desarrollo de la Fase 1 del método de diseño: 
  * Documento: Procedimiento Fase 1.
  * Documentos complementarios:  
    * Figura: Esquema general del procedimiento de la Fase 1.
