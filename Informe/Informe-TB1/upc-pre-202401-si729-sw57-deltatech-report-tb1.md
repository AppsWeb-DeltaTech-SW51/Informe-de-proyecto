---
title: "Universidad Peruana de Ciencias Aplicadas - Informe de Trabajo Final"
author: 
  - 'Startup: DeltaTech'
  - 'Producto: DiligenceTech'
  - 'Profesor: Tinoco Licas, Juan'
  - 'Integrantes:'
  - 'Ortega Huaraca, Abel: U20201B380'
  - 'Herrera Gonzalez, Luis: U202218227'
  - 'Elsner De la Torre Ugarte, Julio: U202111654'
  - 'Rivadeneyra Ramos, Joaquin: U202211846'
  - 'Mallma Espiritu, Franky: U20211C250'
date: "2024"
subject: "Markdown"
keywords: [Markdown, Report]
subtitle: 'Aplicaciones Web - SW57 - SI730'
lang: "es"
colorlinks: true
footer-left: "DeltaTech"
titlepage: true
titlepage-text-color: "FFFAFA"
titlepage-color: "DC143C"
titlepage-rule-height: 2
titlepage-rule-color: "FFFAFA"
book: true
classoption: oneside
code-block-font-size: \scriptsize
header-includes:
- |
  ```{=latex} 
  \usepackage{awesomebox}
  \usepackage{fontawesome5}
  \usepackage{tcolorbox}
 
  \newtcolorbox{info-box}{colback=cyan!5!white,arc=0pt,outer arc=0pt,colframe=cyan!60!black}
  \newtcolorbox{error-box}{colback=red!5!white,arc=0pt,outer arc=0pt,colframe=red!75!black}
  \newtcolorbox{norm-box}{colback=gray!5!white,arc=0pt,outer arc=0pt,colframe=gray!60!black}
  \newtcolorbox{warn-box}{colback=orange!5!white,arc=0pt,outer arc=0pt,colframe=orange!80!black}
  \newtcolorbox{attn-box}{colback=green!5!white,arc=0pt,outer arc=0pt,colframe=green!75!black}
  \newtcolorbox{code-box}{colback=pink!5!white,arc=0pt,outer arc=0pt,colframe=pink!80!black}
  \newtcolorbox{learn-box}{colback=blue!5!white,arc=0pt,outer arc=0pt,colframe=blue!40!black,title=\textbf{Objectives:}}
  \newtcolorbox{scenario-box}{colback=orange!5!white,arc=0pt,outer arc=0pt,colframe=orange!80!black,title=\textbf{Scenario:}}
  \newtcolorbox{outline-box}{colback=cyan!5!white,arc=0pt,outer arc=0pt,colframe=cyan!60!black,title=\textbf{Outline:}}
  \newtcolorbox{prereqs-box}{colback=red!5!white,arc=0pt,outer arc=0pt,colframe=red!60!black,title=\textbf{Prerequisites:}}
  \newtcolorbox{labtime-box}{colback=yellow!5!white,arc=0pt,outer arc=0pt,colframe=yellow!60!black,title=\textbf{Lab:}}

  ```
pandoc-latex-environment:
  tcolorbox: [box]
  info-box: [info]
  error-box: [error]
  norm-box: [norm]
  warn-box: [warn]
  attn-box: [attn]
  code-box: [code]
  learn-box: [learn]
  scenario-box: [scenario]
  outline-box: [outline]
  prereqs-box: [prereqs]
  labtime-box: [labtime]
  noteblock: [note]
  tipblock: [tip]
  warningblock: [warning]
  cautionblock: [caution]
  importantblock: [important]
---
**Registro de Versiones del Informe**

| Versión |    Fecha    | Autor                     | Descripción de Modificación                                                                |
|---------|-------------|---------------------------|--------------------------------------------------------------------------------------------|
|   tb1   | 14/04/2024  | Ortega Huaraca, Abel      | Aporté en realizar los diagramas, estructuración del informe y actividades grupales        |
|   tp    | 28/04/2024  | Ortega Huaraca, Abel      | Participé en el desarrollo de la interfaz de usuario y en la integración de componentes     |
|   tb2   | 12/05/2024  | Ortega Huaraca, Abel      | Implementé las APIs para el manejo de datos y configuré las conexiones a la base de datos   |

| Versión |    Fecha    | Autor                             | Descripción de Modificación                                                              |
|---------|-------------|-----------------------------------|------------------------------------------------------------------------------------------|
|   tb1   | 14/04/2024  | Herrera Gonzalez, Luis Eduardo    | Aporté en realizar los diagramas, landing page y actividades grupales                    |
|   tp    | 28/04/2024  | Herrera Gonzalez, Luis Eduardo    | Contribuí en la creación de componentes React y la integración de la librería de estilos CSS |
|   tb2   | 12/05/2024  | Herrera Gonzalez, Luis Eduardo    | Optimicé las consultas a la base de datos y configuré los servicios RESTful              |

| Versión |    Fecha    | Autor                          | Descripción de Modificación                                                                |
|---------|-------------|--------------------------------|--------------------------------------------------------------------------------------------|
|   tb1   | 14/04/2024  | De La Torre Ugarte, Julio      | Aporté en realizar los diagramas Lean UX, landing page y diseños de landing page y web application |
|   tp    | 28/04/2024  | De La Torre Ugarte, Julio      | Colaboré en el diseño de vistas principales y la integración con las funcionalidades del frontend |
|   tb2   | 12/05/2024  | De La Torre Ugarte, Julio      | Desarrollé la autenticación y autorización, y realicé pruebas de seguridad                  |

| Versión |    Fecha    | Autor                           | Descripción de Modificación                                                                |
|---------|-------------|---------------------------------|--------------------------------------------------------------------------------------------|
|   tb1   | 14/04/2024  | Mallma Espiritu, Franky Oswald  | Aporté en realizar los diagramas Lean UX, diseños de landing page y actividades grupales   |
|   tp    | 28/04/2024  | Mallma Espiritu, Franky Oswald  | Trabajé en la integración de las vistas con el backend y pruebas de usabilidad              |
|   tb2   | 12/05/2024  | Mallma Espiritu, Franky Oswald  | Configuré la base de datos y optimicé la interacción entre frontend y backend              |

| Versión |    Fecha    | Autor                          | Descripción de Modificación                                                                 |
|---------|-------------|--------------------------------|---------------------------------------------------------------------------------------------|
|   tb1   | 14/04/2024  | Rivadeneyra Ramos, Joaquin David| Aporté en la realización de mi entrevista                                                   |
|   tp    | 28/04/2024  | Rivadeneyra Ramos, Joaquin David| Realicé pruebas de usabilidad y la implementación de mejoras en la interfaz                 |
|   tb2   | 12/05/2024  | Rivadeneyra Ramos, Joaquin David| Desarrollé los servicios de backend y aseguré la correcta implementación de la lógica de negocios |

**Student Outcome**

El curso contribuye al cumplimiento del Student Outcome ABET: *ABET-EAC - Student Outcome 3*

* **Criterio:** *Capacidad de comunicarse efectivamente con un rango de audiencias*.

**Actividades Colaborativas (Github Roadmap)**

![](src/img/roadmap.png)

Como equipo, hemos implementado la herramienta de 'Collaborative Roadmap' para mejorar la organización de nuestros tiempos y asegurar un seguimiento claro del progreso de nuestro informe. Mediante la clasificación de tareas en estados como 'Ready', 'In progress' y 'Done', podemos visualizar fácilmente en qué etapa se encuentra cada punto del informe. Esta estructura nos permite una comunicación más fluida y una mejor coordinación entre los miembros del equipo. Asignar tareas y establecer plazos nos ayuda a fomentar la responsabilidad individual y garantizar que todos estemos alineados con los objetivos del proyecto y su avance. Esta transparencia y eficiencia en la gestión del tiempo son fundamentales para alcanzar el éxito en nuestro trabajo colaborativo.

![](src/img/roadmap-sust.png)

En cada punto, se enfatizó la necesidad de que nuestros compañeros informaran sobre cualquier cambio, con el fin de que pudiéramos discutirlo en grupo y así tomar decisiones de manera colaborativa. Esta práctica promueve la transparencia y la participación de todos los miembros del equipo en el proceso de toma de decisiones, lo que fortalece nuestra cohesión y nos permite abordar de manera efectiva los desafíos que surgen durante el desarrollo del proyecto.

En el siguiente cuadro se describe las acciones realizadas y enunciados de conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro del *ABET-EAC - Student Outcome 3*.

![](src/img/student1.jpeg)

![](src/img/student2.jpeg)

# Capítulo I: Introducción

## *Startup Profile*

### Descripción de la Startup 

**DeltaTech: Automatizando la** ***Due Diligence*** **en Línea**

DeltaTech es una startup centrada en ofrecer soluciones innovadoras para el proceso de due diligence en línea. Nos especializamos en la automatización de una variedad de procesos, desde el análisis de datos financieros de empresas hasta la revisión de sus estados de cuenta, entre otras funciones críticas.
Nuestras plataformas tecnológicas están diseñadas para proporcionar una manera eficiente y precisa de llevar a cabo una debida diligencia exhaustiva durante transacciones comerciales, como la venta de empresas. En DeltaTech, nos comprometemos a simplificar y agilizar el proceso de evaluación, permitiendo a nuestros clientes tomar decisiones informadas con confianza.
Cada solución que desarrollamos está impulsada por la búsqueda constante de la excelencia en la eficiencia operativa y la precisión en el análisis de datos. En DeltaTech, estamos transformando la forma en que se aborda la due diligence en línea, llevando la automatización al centro de las transacciones comerciales del siglo XXI.

![DeltaTech Logo](src/img/cap1/deltatech-banner.png "DeltaTech Logo")

\newpage

**Misión**

* Nuestra misión en DeltaTech es proporcionar soluciones innovadoras y eficientes para el proceso de due diligence en línea, permitiendo a nuestros clientes realizar evaluaciones exhaustivas de manera rápida y precisa durante transacciones comerciales críticas, como la venta de empresas. Nos esforzamos por automatizar y simplificar el análisis de datos financieros, brindando a los inversores las herramientas necesarias para tomar decisiones informadas y estratégicas que impulsen el éxito en sus operaciones.

**Visión**

* Nuestra visión en DeltaTech es transformar la forma en que se realiza la debida diligencia, siendo líderes en el desarrollo de plataformas tecnológicas avanzadas que agilizan el análisis de información financiera. Nos comprometemos a ofrecer una experiencia de usuario excepcional a través de interfaces intuitivas y seguras, respaldadas por algoritmos avanzados y cifrado de datos de extremo a extremo. Buscamos ser reconocidos como socios confiables y fundamentales en el éxito de las transacciones comerciales, facilitando la toma de decisiones estratégicas para nuestros clientes en todo momento.

### Perfiles de integrantes del equipo

Nuestro equipo está conformado por individuos apasionados y comprometidos, cada uno aportando sus habilidades únicas para lograr nuestros objetivos de manera efectiva y colaborativa. Aquí se muestra a nuestros miebros clave:

![](src/img/Integrantes/Abel.png) 

![](src/img/Integrantes/Joaquin.png) 

![](src/img/Integrantes/Julio.png) 

![](src/img/Integrantes/Luis.png) 

![](src/img/Integrantes/Franky.png) 

## *Solution Profile*

En el cambiante mundo empresarial actual, la debida diligencia financiera se ha convertido en un pilar fundamental para asegurar transacciones comerciales seguras y exitosas. Sin embargo, el proceso tradicional de recolección y análisis de datos financieros de empresas puede ser lento, tedioso y propenso a errores. Esta realidad ha generado una necesidad urgente de encontrar soluciones innovadoras que permitan a los inversores realizar este crucial proceso de manera más eficiente y efectiva.
En este contexto, surge una nueva era de la debida diligencia financiera, donde la tecnología y la inteligencia se unen para ofrecer soluciones ágiles y precisas. La búsqueda de métodos más inteligentes para acceder y analizar datos financieros se ha convertido en una prioridad para los profesionales que buscan tomar decisiones informadas y estratégicas en sus inversiones.

![Recurso extraído de Canva](src/img/cap1/solutionp.png) 

### Antecedentes y problemática

::: info
***What***

* El proceso tradicional de *Due Diligence* se caracteriza por ser laborioso, costoso y propenso a errores.
* Los inversores y profesionales financieros revisan una gran cantidad de documentos financieros, legales y operativos en un tiempo limitado.
* Esto puede resultar en la contratación de servicios adicionales y gastos innecesarios.
:::

::: info
***Who***

* Inversores y profesionales financieros se ven afectados por la complejidad y la carga de trabajo del proceso tradicional de *Due Diligence*.
* Propietarios de empresas enfrentan el desafío de compartir información confidencial con inversores potenciales.
:::

::: info
***Where***

Esta problemática es común en transacciones comerciales y de inversión, donde la debida diligencia es crucial.
:::

::: info
***When***

La problemática surge en cada proceso de adquisición o inversión, donde la toma de decisiones debe realizarse en un tiempo limitado.
:::

::: info
***Why***

* La falta de acceso rápido y la preocupación por la seguridad de la información sensible de la empresa dificultan la toma de decisiones.
* Existe el riesgo de que los inversores utilicen los datos sensibles con otros fines, lo que genera incertidumbre y desconfianza.
:::

::: attn
***How***

* En el estado normal, los contadores e inversores pueden requerir días o semanas para revisar y analizar manualmente los documentos financieros de una empresa. Con "DeltaTech", el proceso se acelerará significativamente, permitiendo la revisión y análisis en cuestión de horas

* El problema sigue un patrón de ineficiencia y lentitud en el proceso de *Due Diligence*. Los contadores y los inversores a menudo se ven abrumados por la cantidad de documentos y la falta de herramientas eficientes para analizarlos de manera rápida y precisa. 
:::

::: attn
***How Much***

* En un día, un inversor puede perder oportunidades de inversión valiosas debido a la demora en la obtención de informes financieros. Con "DeltaTech", estas oportunidades podrían aumentar en un 50%.

* En términos de pérdida de oportunidades de inversión, el retraso actual podría estar implicando el equivalente a 50 000 soles por mes por los participantes de la inversión. Con "DeltaTech", se podrían reducir los retrasos que se pueden presentar en el proceso de **Due Diligence**.
:::

\newpage

### *Lean UX Process*

![Recurso extraído de Canva](src/img/cap1/leanux.png)

#### *Lean UX Problem Statements*

::: note
***Problem Statement***

* El estado actual del Due Diligence para los inversionistas, y contadores que representan a sus empresas, es muy extenuante. 

* Los productos actuales no ofrecen una solución completa. Ya sea esto solo el análisis, la búsqueda de empresas, la seguridad para trabajar con archivos. Sin embargo, nunca algo que embarque todo. Debido a esto, todos los involucrados son afectados de manera negativa, perdiendo grandes oportunidades de negocio o la inversión que necesitan para poder crecer en el mercado. 

* ¿Cómo podemos mejorar la experiencia del proceso Due Diligence con el fin de agilizar y mejorar la calidad del trabajo?
:::

::: note

#### *Lean UX Assumptions*

***Business Assumptions:***

1. **Creo que mis clientes necesitan** una herramienta eficiente y confiable para realizar sus análisis financieros exhaustivos durante el proceso de *Due Diligence*. 

2. **Estas necesidades se pueden resolver con** nuestra plataforma inteligente que automatice el análisis financiero y que ofrezca acceso rápido y seguro a información relevante de las empresas objetivo.

3. **Mis clientes iniciales son** inversores y contadores financieros que trabajan en sell-side.

4. **El valor #1 que un cliente quiere de mi servicio es** una manera eficiente y precisa de realizar sus transacciones durante el proceso de *Due Diligence*. 

5. **El cliente también puede obtener estos beneficios adicionales** como una mayor confianza en el proceso de *Due Diligence*, una mayor seguridad de los datos financieros y una experiencia de usuario mejorada.
6. **Voy a adquirir la mayoría de mis clientes a través de** campañas de marketing dirigidas a empresas de capital privado, fondos de inversión y otros actores clave en el mercado de transacciones

7. **Haré dinero a través de** la venta de suscripciones a nuestra plataforma "Diligence Tech", ofreciendo diferentes niveles de acceso según las necesidades del cliente.

8. **Mi competencia principal en el mercado serán** otras plataformas de *Due Diligence* en línea, así como servicios tradicionales de consultoría que ofrecen análisis de datos financieros.

9. **Los venceremos debido a** nuestra capacidad para ofrecer una solución tecnológica más rápida, precisa y fácil de usar que nuestras competidoras, así como nuestro enfoque en la seguridad de los datos y la experiencia del usuario..

10. **El mayor riesgo del producto es** que la tecnología pueda no funcionar como se espera, lo que podría resultar en errores en los datos o brechas de seguridad.

11. **Resolveremos esto a través de la** implementación de rigurosas pruebas de calidad y seguridad, así como la rápida corrección de errores a medida que surjan.

12. **¿Qué otras suposiciones tenemos? ¿Eso, si se prueba que es falso, causará que nuestro negocio/proyecto no funcione?** Otras suposiciones que tenemos son si:
    - Existe una demanda significativa.
    - La automatización de datos financieros mejorará el proceso de *Due Diligence*. 
    - Garantizar la seguridad y privacidad de los datos financieros de las empresas objetivo a través de cifrado de extremo a extremo generará confianza entre los usuarios

***Business Outcomes:***

- Conseguir los primeros 100 usuarios registrados para la aplicación de ambos segmentos objetivos. 

- Retener el 50% de los usuarios 
durante el primer semestre.	

- Registrar 20 usuarios activos al mismo tiempo utilizando la aplicación.

- Conseguir el registro de 10 nuevos usuarios referidos a través de links compartidos.

***Users Assumptions:***


1. **¿Quién es el usuario?**

   Los usuarios son los asociados al proceso de Due Diligence, tanto los inversores que están interesados participar con empresas, como estás mismas representadas con sus contadores financieros.

2. **¿Qué problemas tiene nuestro producto? ¿Resolver?**

    * Dificultad para acceder y comparar de manera eficiente la información financiera de múltiples empresas durante el proceso de Due Diligence.
    * Riesgos asociados con la toma de decisiones basadas en datos financieros incompletos o inexactos.
    * Falta de una plataforma centralizada y fácil de usar para analizar y evaluar oportunidades de inversión de manera efectiva.
    * Dificultad para acceder y analizar rápidamente datos financieros de empresas objetivo durante el proceso de debida diligencia.
    * Riesgos asociados con la falta de seguridad y privacidad de los datos financieros sensibles.
    * Falta de eficiencia en el proceso de debida diligencia debido a la dependencia de métodos manuales y lentos.

3. **¿Qué características son importantes?**

* Interfaz de usuario intuitiva y eficiente que permita una navegación fluida y acceso rápido a la información financiera clave.
* Funcionalidades avanzadas de comparación y análisis de datos financieros para facilitar la toma de decisiones informadas.
* Seguridad de datos avanzada para garantizar la confidencialidad y protección de la información financiera sensible.
* Herramientas de visualización y generación de informes que permitan una comprensión clara y rápida de la salud financiera de las empresas objetivo.

4. **¿Dónde encaja nuestro producto en su trabajo o vida?**

   Nuestro producto se incorpora en el proceso de Due Diligence que los usuarios realizan. Estos lo utilizarían para agilizar los procesos que usualmente se realizan de manera manual o menos automatizada.

5. **¿Cuándo y cómo es usado nuestro producto?**

    * Es utilizado por los inversores y contadores desde el inicio del proceso de evaluación de una empresa objetivo hasta la toma final de decisiones de compra o inversión.
    * Los inversores utilizan nuestro producto para analizar los estados financieros, realizar comparaciones entre empresas y   evaluar los riesgos y oportunidades de inversión.
    * Los contadores lo utilizan para poder comunicarse con los inversores interesados y realizar transacciones de información de manera segura.

6. **¿Cómo debe verse nuestro producto y cómo comportarse?**

   * Debe comportarse de manera eficiente y rápida, brindando resultados precisos y actualizados de manera oportuna.
   * La seguridad y confidencialidad de los datos financieros es fundamental, por lo que el producto debe garantizar un cifrado sólido y medidas de protección avanzadas.
   * Nuestro producto debe tener una apariencia profesional y moderna, con una interfaz de usuario clara y organizada que facilite la comparación y análisis de datos.

***User outcomes:***

- Acceso de manera rápida y eficiente a la información financiera relevante de las empresas objetivo.
- Confianza en la seguridad y privacidad de los datos financieros sensibles
- Experiencia de usuario mejorada gracias a la interfaz intuitiva y fácil de usar

***Feature Assumptions***

* Herramientas avanzadas de análisis:
    - Los inversores podrán utilizar herramientas avanzadas para comparar rápidamente los datos financieros de múltiples empresas.
    - Se asume que características como gráficos interactivos, análisis comparativos y tablas dinámicas mejorarán la eficiencia del análisis.
    - Funciones especializadas para analizar estados financieros, ratios financieros, tendencias históricas y comparaciones sectoriales.
* Automatización de Procesos Repetitivos:
    - Capacidad de automatizar tareas como la extracción de datos financieros, el cálculo de ratios y la generación de informes estándar.
* Funcionalidades de Seguridad Avanzada:
    - Los inversores confiarán en la plataforma debido a las medidas de seguridad avanzada, como cifrado de extremo a extremo y autenticación de dos factores.
    - Se asume que la seguridad sólida garantizará la protección de los datos financieros confidenciales.
* Generación de Informes Personalizados:
    - Los inversores podrán crear informes personalizados basados en sus criterios de evaluación y preferencias.
    - Se asume que los informes detallados y personalizados facilitarán la toma de decisiones informadas.
* Visualización de Datos Interactiva:
    - Gráficos interactivos y tablas dinámicas para visualizar los datos financieros de manera clara y comprensible.
* Alertas y Notificaciones Relevantes: 
    - Los inversores recibirán alertas sobre cambios significativos en los datos financieros de las empresas en su lista de seguimiento.
    - Se asume que las alertas oportunas y relevantes mejorarán la capacidad de reacción a los cambios en las empresas objetivo.
:::

\newpage

#### *Lean UX Hypothesis Statements*

::: tip

* **Creemos que** los usuarios valoran la eficiencia y precisión en el análisis de datos financieros durante el proceso de *Due Diligence*. **Sabremos que** esto es cierto **cuando** observemos una disminución significativa en el tiempo dedicado al análisis manual de datos, medido por una reducción del 30% en el tiempo promedio necesario para completar una debida diligencia.

* **Creemos que** los usuarios encuentran la automatización un elemento esencial para agilizar el proceso de cDue Diligence*. **Sabremos que** esto es cierto **cuando** veamos la disminución en el tiempo que se ocupa por cada proceso, medido por una reducción en 40% en el tiempo de los procesos que tienen la capacidad de ser automatizados.

* **Creemos que** la seguridad y privacidad de los datos financieros sensibles es una preocupación clave para los usuarios durante el proceso de *Due Diligence*. **Sabremos que** esto es cierto **cuando** veamos una mayor confianza en la plataforma “DiligenceTech” por parte de los contadores, medido por una reducción del 20% en las solicitudes de soporte relacionadas con la seguridad de los datos.

* **Creemos que** la generación de informes personalizados será importante para tomar decisiones finales para los usuarios. **Sabremos que** esto es cierto **cuando** veamos un incremento en la cantidad de adquisiciones que se realicen. Medido por un aumento en un 20% de compras después de realizarse el proceso de analisis financiero.

* **Creemos que** los usuarios valoran la visualización de datos interactivos durante el proceso de *Due Diligence*. **Sabremos que** esto es cierto **cuando** observemos un aumento del 30% en la tasa de participación de los usuarios en proyectos de análisis financiero donde se ofrecen visualizaciones de datos interactivos en comparación con sesiones donde no se proporcionan

* **Creemos que** las alertas y notificaciones son una funcionalidad muy importante para todos los usuarios. **Sabremos que** esto es cierto **cuando** veamos una reducción en el tiempo de respuesta entre los usuarios y la entrega de sus partes correspondientes., medido por un 20% en la reducción de quejas por falta de respuestas a tiempo de los usuarios durante el proceso de *Due Diligence*.

:::

\newpage

#### *Lean UX Canvas*

![Artefacto creado en Figma ([URL](https://www.figma.com/file/jX7TR5fsEkgbQVH44vAmDb/Lean-UX-Canvas-2.0?type=design&node-id=0%3A1&mode=design&t=uRI0WHIdDhIsWi2g-1))](src/img/cap1/Lean-UX-Canvas.png) 

## Segmentos objetivo

![Tabla del segmento 1](src/img/cap1/segmento-1.png) 

![Tabla del segmento 2](src/img/cap1/segmento-2.png) 

# Capítulo II: *Requirements Elicitation & Analysis*

## Competidores

![](src/img/cap2/competidores-baner.png)

En el contexto de un mercado peruano en constante cambio y evolución, donde la gestión eficiente en los procesos de *Due Diligence*  se convierten en una necesidad primordial en el rubro de las inversiones. **DiligenceTech** se enfrenta a una urgente tarea: comprender y abordar a sus competidores para lograr una posición sólida y garantizar la satisfacción de sus usuarios.

**Competidores:** 

* ***Datasite Diligence:*** 
    El *virtual data room* más utilizado en el mercado. Proporcionada por la empresa Datasite, esta solución mediante aplicación web brinda un espacio de almacenamiento y edición de archivos, los cuales se esperan que sean documentos financieros para posteriormente ser enviados por correo electrónico a quien sea desee el usuario. Entre las mecánicas más resaltantes en este competidor está la posibilidad de censura mediante IA elementos de los documentos y la modalidad Q&A. Su precio es a base de páginas que contengan los archivos, costando 7 mil dólares por cada 10 mil páginas.

    ![Imagen extraída de Datasite([URL](https://www.datasite.com/es/es/products/diligence))](src/img/cap2/datasite.png)

* ***iDeals:***
    *Virtual data room online* para servicios financieros, Biotech, IT y otras especializaciones del sistema que utilizan organizaciones de muchos usuarios dentro de la aplicación, la simplificación del ingreso y uso de archivos, y la seguridad del sistema en cuidarlos. Cuenta actualmente con más de 1 millón de usuarios y destaca en el mercado por su atención al cliente rápida y constante.

    ![Imagen extraída de iDeals([URL](https://es.idealsvdr.com/))](src/img/cap2/ideals.png)

* ***Firmex:***
    *Virtual data room* para contadores financieros que permite insertar y guardar archivos al sistema con funcionalidades como Q&A y censura. Reconocido en el mercado por la seguridad que mantiene en los archivos.

    ![Imagen extraída de Firmex([URL](https://www.firmex.com/))](src/img/cap2/firmex.png)

### Análisis competitivo

![](src/img/cap2/competitive-landscape-1.png)

![](src/img/cap2/competitive-landscape-2.png)

![](src/img/cap2/competitive-landscape-3.png)

### Estrategias y tácticas frente a competidores

::: info
Según Michael Porter, la estrategia competitiva implica cómo una empresa compite en su mercado específico. Porter identificó tres estrategias generales que las empresas pueden emplear para competir con éxito: liderazgo en costos, diferenciación y enfoque. La estrategia de liderazgo en costos implica ofrecer productos o servicios a precios más bajos que los de los competidores, mientras que la diferenciación se basa en ofrecer productos y servicios únicos y distintivos. Por otro lado, una estrategia de enfoque se centra en un segmento de mercado específico. Para llevar a cabo eficazmente estas estrategias, las empresas necesitan tener un profundo conocimiento de sus mercados y competidores para desarrollar y mantener una ventaja competitiva sostenible a largo plazo.
:::

Teniendo en cuenta el análisis SWOT previamente presentado para DiligenceTech, proponemos las siguientes estrategias competitivas:

**Estrategias Competitivas para** ***DiligenceTech:***

1. **Liderazgo en Costos:**

::: norm
**Estrategia:** *DiligenceTech* puede buscar optimizar sus procesos internos para reducir costos operativos y ofrecer sus servicios a precios más competitivos que los de sus competidores.

**Tácticas:**
* Implementar tecnologías eficientes que reduzcan los gastos de infraestructura y operativos.
* Negociar acuerdos favorables con proveedores y socios para obtener mejores precios en servicios y herramientas necesarios.
* Ofrecer modelos de precios flexibles y descuentos opr volumen para atraer a clientes sensibles al costo.
:::

2. **Diferenciación a través de la Innovación:**

::: norm
**Estrategia:** *DiligenceTech* puede enfocarse en desarrollar características y funcionalidades únicas que destaquen su plataforma como líder en innovación en el proceso de *Due Diligence*.

**Tácticas:**
* Realizar investigaciones de mercado para identificar necesidades no cubiertas y oportunidades de mejora.
* Invertir en I+D para desarrollar herramientas avanzadas de análisis financiero y presentación de informes.
* Promocionar activamente las nuevas características a través de campañas de marketing destacando la vanguardia tecnológica de DiligenceTech.
:::

3. **Enfoque en segmentos específicos del mercado:**

::: norm
**Estrategia:** *DiligenceTech* puede especializarse en atender a segmentos específicos del mercado donde pueda ofrecer un valor diferenciado y adaptado.

**Tácticas:**
* Identificar sectores de la industria con necesidades únicas de debida diligencia, como startups en crecimiento, empresas de tecnología emergente, o industrias reguladas.
* Desarrollar soluciones personalizadas y paquetes de servicios adaptados a las necesidades específicas de cada segmento.
* Colaborar con asociaciones y grupos de la industria para fortalecer la presencia en estos segmentos y generar confianza.
:::

**Tácticas Específicas para** ***DiligenceTech:***

1. **Monitoreo Competitivo Continuo:**
    
::: info
**Táctica:** Realizar análisis periódicos de las estrategias, precios y ofertas de la competencia para identificar oportunidades y amenazas.

**Acciones:**
* Mantenerse al tanto de los movimientos de los competidores en cuanto a lanzamientos de productos, cambios de precios y campañas de marketing.
* Utilizar herramientas de seguimiento de competidores y análisis de mercado para obtener información valiosa.
:::

2. **Estrategias de Precios y Paquetes Competitivos:**

::: info
**Táctica:** Ajustar estratégicamente los precios y paquetes de servicios para competir de manera efectiva en el mercado.  

**Acciones:**
* Realizar análisis de precios comparativos y ajustar los precios de acuerdo con el valor percibido por los clientes.
* Ofrecer paquetes personalizados que se ajusten a las necesidades específicas de diferentes tipos de clientes, como empresas grandes, medianas y startups.
:::

3. **Inversión en Marketing Diferenciado:**

::: info
**Táctica:** Desarrollar mensajes y campañas de marketing que resalten las fortalezas únicas y la propuesta de valor de DiligenceTech.

**Acciones:**
* Crear contenido educativo y de valor que demuestre cómo DiligenceTech aborda los desafíos específicos de la debida diligencia.
* Utilizar estudios de casos y testimonios de clientes para respaldar los beneficios y resultados de la plataforma.
:::

4) **Alianzas Estratégicas y Colaboraciones:**

::: info
**Táctica:** Establecer asociaciones estratégicas con empresas complementarias o instituciones que puedan ampliar el alcance y la oferta de DiligenceTech.

**Acciones:**
* Colaborar con firmas de consultoría reconocidas para ofrecer servicios combinados de asesoramiento y tecnología.
* Formar alianzas con organizaciones financieras o legales para ofrecer paquetes completos de servicios de debida diligencia.
:::

## Entrevistas

::: note
Para acceder al video de las entrevistas, haga click en la URL: https://lc.cx/EsVmqu
:::

### Diseño de entrevistas

Entrevista a personas referentes a nuestro segmentos objetivo, las preguntas varían dependiendo del segmento debido a las diferentes situaciones:

**Segmento 1:** Contadores Financieros

**Preguntas de introducción:**

1. ¿Cuántos años tiene?
2. ¿En qué ciudad del Perú reside?
3. ¿Cuál considera que es su estatus social limitando la descripción a Clase Baja, Clase Media, Clase Media-Alta y Clase Alta?
4. ¿Cúal es su profesión?
5. ¿Cuánto tiempo lleva ejerciendo esta profesión?
6. ¿Está familiarizado con el concepto y proceso de diligencia debida?    

**Preguntas principales:**

1. ¿Cómo lleva a cabo usted su trabajo para un proceso de diligencia debida?
2. ¿Podría mencionar su participación en la diligencia debida en base a las etapas que tiene?
3. ¿Cómo son los procesos más comunes de obtener documentos financieros de las empresas investigadas y cuanto tiempo demoran?
4. ¿Cuáles son los documentos de las empresas que dan más problemas en obtener?
5. ¿Qué indicador o análisis financiero considera el más importante para calificar una empresa?
6. ¿Cual ha sido la mayor cantidad de empresas que ha consultado a la vez?
7. ¿Usted mismo realiza el análisis financiero?
8. ¿Qué tipo de problemas se encuentran a la hora de analizar los datos de la empresa?
9. ¿Qué medidas de seguridad se llevan para garantizar la confidencialidad de los datos?
10. ¿Cuáles son los procesos más importantes que usted rinde para la diligencia debida?
11. ¿Cómo se guardan y se comparten los documentos financieros en el proceso de diligencia debida?
12. ¿Usualmente cuánto demora un proceso de *Due Diligence*?
13. ¿Qué herramientas conoce o utiliza durante este proceso?
14. ¿Qué partes le parecen tediosas del proceso de diligencia debida?
15. ¿Cómo colabora con otros participantes en el proceso de diligencia debida?
16. ¿Qué problemas suelen ocurrir mediante el proceso de diligencia debida y cómo los resuelve?
17. ¿Ve factible contener los documentos financieros en un servicio de alojamiento en la web como Google Drive?
    * En caso sí, ¿Qué funcionalidades cree que vendrían útil para complementar el servicio? ¿Algo que tenga que ver con seguridad, análisis automático o edición de los documentos?
    * En caso no, ¿Qué funcionalidades cree que debería tener para que sea posible tenerlo en uno de estos sistemas?
18. En los documentos financieros se suele presentar censura de elementos que no se desea que sean revelados: ¿Le parece que le sería sencillo que en la aplicación misma sea posible hacer este proceso?
19. Para mantener la seguridad del proceso el dueño de la empresa va a agregar a diversos contadores los cuales solo tendrán acceso a subir archivos en cada request que haga el inversor. ¿Piensa que esta limitación es suficiente para mantener la integridad de la empresa a vender?
20. ¿Existen documentos financieros que obtiene, como contador, del internet? ¿Nos podría decir en donde se consiguen normalmente? ¿Me gustaría que nuestro sistema haga automáticamente la recolección de estos documentos al brindar el nombre de la compañía? ¿Tiene alguna opinión complementaria a esta funcionalidad?
21. Debido a la sensibilidad y debida discreción que deben tener los documentos privados de la empresa nuestro modelo ha implementado una vista previa de los mismos que no podrán descargarse ni apropiarse de algún modo. ¿Qué opina sobre esta funcionalidad?
22. Nuestra aplicación web usará el análisis de datos en base a lo que el contador envía y mostrará de manera intuitiva y digerible la proyección a largo plazo de la empresa. ¿Qué opina sobre esta implementación?

**Segmento 2:** Inversores

**Preguntas de introducción:**

1. ¿Cuántos años tiene?
2. ¿En qué ciudad del Perú reside?
3. ¿Cuál es su ocupación principal?
4. ¿Cuál es su nivel de experiencia en inversiones?
5. ¿Con qué frecuencia realiza inversiones?
6. ¿Cuál es su principal objetivo al invertir? (por ejemplo, crecimiento de capital, ingresos pasivos, diversificación, impacto social, etc.)
7. ¿En qué sectores o industrias prefiere invertir?
8. ¿Prefiere invertir en empresas nuevas y emergentes o en empresas establecidas?
9. ¿Ha participado anteriormente en procesos de *Due Diligence* antes de invertir en una empresa?
10. ¿Qué información financiera y empresarial considera más importante al evaluar una oportunidad de inversión?

**Preguntas principales:**

1. ¿Qué experiencia tiene en procesos de *Due Diligence* al evaluar una empresa?
2. ¿Cuáles son los aspectos clave que busca en un informe de *Due Diligence* antes de tomar una decisión de inversión?
3. ¿Qué indicadores financieros o métricas considera cruciales al evaluar la salud financiera de una empresa?
4. ¿Qué tipo de riesgos financieros le preocupan más al considerar una inversión?
5. ¿Qué papel juega la reputación y el historial de la empresa en su decisión de inversión?
6. ¿Cuál es su enfoque para diversificar su cartera de inversiones?
7. ¿Qué herramientas o plataformas utiliza para realizar análisis financiero y seguimiento de inversiones?
8. ¿Cómo es el proceso de una diligencia debida desde su experiencia? ¿Cómo participa en ella?
9. ¿En algún momento durante el proceso la empresa le ha hecho una serie de preguntas o detalles para poder llevar a cabo el proceso?
10. ¿En qué formato es el que recibe los resultados de la diligencia debida? ¿Le parece eficiente? ¿Desearía tenerlo en formato virtual?
11. ¿Ve factible contener los resultados de los documentos financieros en un servicio de alojamiento en la web como Google Drive donde se le comparte?
    * En caso sí, ¿Qué funcionalidades cree que vendrían útil para complementar el servicio? ¿Algo que tenga que ver con seguridad, análisis automático o edición de los documentos?
    * En caso no, ¿Qué funcionalidades cree que debería tener para que sea posible tenerlo en uno de estos sistemas?

**Preferencias y comportamientos de inversión:**

1. ¿Prefiere invertir en empresas locales o internacionales?
2. ¿Qué tamaño de empresa prefiere para sus inversiones? (por ejemplo, startups, PYMES, grandes corporaciones)
3. ¿Cuál es su horizonte de tiempo típico para una inversión? (corto plazo, mediano plazo, largo plazo)
4. ¿Qué factores externos (económicos, políticos, sociales) considera al tomar decisiones de inversión?
5. ¿Qué grado de involucramiento espera tener esn las empresas en las que invierte? (por ejemplo, pasivo, activo, asesoramiento)
6. ¿Cómo valora la transparencia y la comunicación de una empresa con sus inversores?
7. ¿Ha tenido experiencias previas de éxito o fracaso en inversiones que le gustaría compartir?

**Tecnología y preferencias de información:**

1. ¿Qué tipo de información financiera y empresarial prefiere recibir durante un proceso de diligencia debida?
2. ¿Cómo prefiere acceder a esta información? (documentos físicos, plataformas en línea, informes interactivos, etc.)
3. ¿Qué funcionalidades o herramientas tecnológicas le gustaría ver en una plataforma de *Due Diligence* para facilitar sus decisiones de inversión?
4. ¿Está familiarizado con el uso de análisis de datos y tecnologías de inteligencia artificial en procesos de inversión o diligencia debida?
5. ¿Qué medidas de seguridad considera esenciales al compartir información financiera y empresarial durante un proceso de inversión?

**Objetivos y desafíos:**

1. ¿Cuáles son sus principales objetivos financieros a corto, mediano y largo plazo?
2. ¿Cuáles son los desafíos más grandes que enfrenta al tomar decisiones de inversión?
3. ¿Qué información le gustaría tener disponible para tomar decisiones de inversión más informadas?
4. ¿Cómo evalúa el éxito de una inversión?

**Preferencias y comportamientos:**

1. ¿Qué factores le llevan a confiar en una empresa para invertir?
2. ¿Cuáles son sus preferencias de comunicación y cómo le gusta recibir actualizaciones sobre sus inversiones?
3. ¿Cuál es su nivel de tolerancia al riesgo en sus inversiones?
4. ¿Qué actividades o intereses adicionales tiene fuera de sus inversiones financieras?

**Tecnología y preferencias digitales:**

1. ¿Cuáles son sus hábitos de uso de tecnología y medios digitales?
2. ¿Utiliza aplicaciones o plataformas financieras para realizar transacciones o seguimiento de inversiones?
3. ¿Qué funcionalidades considera esenciales en una plataforma de inversión en línea?

### Registro de entrevistas

Para el registro de entrevistas se realizará una entrevista por segmento, dando un total de 6 entrevistas. Además, el formato de las entrevistas es mp4, cada entrevista es independiente debido a las diferentes preguntas y respuestas dadas por los entrevistados de cada segmento.

**Segmento 1: Contadores financieros trabajando en sell-side en empresas financieras con la necesidad de agilizar el proceso de análisis de debida diligencia**

| Nombre y Apellido    | James De La Torre Ugarte |
|----------------------|--------------------------|
| Edad                 | 55 años                  |
| Ubicación Geográfica | Lima, Perú               |
| Profesión            | Contador Público         |

**Resumen Entrevista:** Resumen Entrevista: James De La Torre Ugarte, un respetado contador público con una sólida trayectoria
en *Due Diligence* opina de manera favorable a nuestro diseño que consistirá en una plataforma innovadora en la nube. Esta plataforma estaría diseñada específicamente para recibir documentos empresariales relevantes, como estados financieros y otros documentos relacionados, con el objetivo de facilitar el proceso de evaluación de empresas. La propuesta sugiere que esta plataforma no solo sirva como un repositorio seguro para los documentos financieros, sino que también permita la aplicación de diversas ratios financieras los cuales van a ser de ayuda para poder determinar si es rentable o beneficioso a largo plazo para el inversor. Esto proporciona a James la capacidad de realizar análisis detallados y personalizados de la salud financiera de las empresas en consideración, lo cual es fundamental en el rol que desempeña en la *Due Diligence*. Considerando la sensibilidad y la importancia de la información financiera en el proceso de evaluación empresarial, se enfatiza la necesidad de que esta plataforma garantice altos estándares de seguridad. James comprende plenamente la importancia de proteger la confidencialidad y la integridad de los datos financieros de las empresas, por lo que sería fundamental que la plataforma implemente medidas de seguridad robustas y cumpla con las regulaciones pertinentes. Sin embargo, no descarta el uso de herramientas como Excel, Word o PowerPoint, las cuales menciona haber trabajado con ellas en los momentos que se le permitió. Además, se destaca la relevancia de que esta plataforma sea intuitiva y fácil de usar, especialmente considerando la diversidad de usuarios que podrían interactuar con ella. Dado el enfoque meticuloso y analítico que caracteriza el trabajo de James, la plataforma debería ofrecer una interfaz fluida que facilite la navegación y la extracción de datos necesarios para sus evaluaciones. Comenta que su navegador de preferencia es Safari, tiene una MacBook, un iphone y una tablet Android. Durante la entrevista el entrevistado mostró ser una persona serena y basta de conocimientos, además de mostrarse apasionado por la tecnología demostrando su conocimiento sobre el uso de base de datos empresariales.

                  [Inicio de entrevista: 0:00]
                  [Final de entrevista: 25:06]


![Imagen extraida del video de entrevistas](src/img/cap2/julio-james.png)

| Nombre y Apellido    | Guisella Brabo              |
|----------------------|-----------------------------|
| Edad                 | 51 años                     |
| Ubicación Geográfica | Lima, Perú                  |
| Profesión            | Contadora Pública Colegiada |


**Resumen Entrevista:** Guisella Bravo es contadora pública colegiada, esto quiere decir que trabaja en ámbitos financieros usualmente de una empresa, y lleva ejerciendo esta profesión por más de 25 años. Tiene experiencia con *Due Diligence* como participante Sell-side y Buy-side en su antiguo trabajo, y ha utilizado Dropbox y Excel como herramientas virtuales para rendir esta labor. Su conocimiento tecnológico se limita a la utilización de estas herramientas como otras empresariales como el correo electrónico. En su opinión, la propuesta de solución que hemos planteado es “muy buena” porque las alternativas comúnmente utilizadas en el Perú no se especializan en la interacción entre la empresa compradora y vendedora. En cuanto a como se hace un *Due Diligence* mencionó que se divide en 3 etapas: Entrega de Requerimientos de la Información, *Due Diligence* y el Informe Final. Los actores son en la primera etapa el agente de la empresa compradora que lo envía al agente de la empresa vendedora, *Due Diligence* es el proceso de entregar documentos confidenciales solicitados (.pdf y .xlsx por mayoría) a la empresa compradora mediante la separación general de estas en áreas de especialidades específicas como el área financiera, laboral, legal y tributario, que son las más comunes, y una separación particular en Ítems de Información, los cuales son una descripción completa de los documentos deseados. Esta etapa tiene como proceso intermedio el sistema de Q&A (Preguntas y Respuestas) donde, conforme se van entregando los documentos, la empresa compradora tiene la oportunidad de ordenar explicaciones a la empresa vendedora de lo que se entrega, y lo hace el agente de la empresa vendedora. *Due Diligence* termina si ambas partes confirman que cada ítem está completo. Finalmente, la empresa compradora hace un informe final con los datos entregados de la empresa vendedora. En cuanto a funcionalidades, piensa que el hecho de evitar la descarga de los archivos es innecesario, porque el punto de *Due Diligence* es entregar información confidencial a otra empresa, y opina lo mismo de la funcionalidad de censura en los documentos. Le parece que un análisis financiero hecho dentro del sistema puede ser novedoso y útil, especialmente porque son demasiados documentos. Finalmente, menciona que la herramienta de obtener información de la internet es muy útil y sería de demasiada ayuda en la recolección de documentos. En cuanto a opiniones de *Due Diligence* de carácter emocional, ella cree que no existe parte tediosa del proceso, porque demora aproximadamente un mes a un mes y medio. Adicionalmente, le interesa mucho la seguridad de estos documentos (que no se le envíe a una persona equivocada) y que existan herramientas hechas específicamente para el entorno, le gusta la eficiencia. Para concluir, también menciona que en cuanto a problemas en *Due Diligence* es importante resaltar que elegir a una empresa con intenciones maliciosas para entregar los documentos es un error que le ha pasado y provocó la creación de un competidor de su empresa. Lo cual es más un problema de la misma empresa que seleccionó a quien entregarle la información. No obstante, nos da un buen argumento en contra de nuestra posible funcionalidad de que se presente una red social que funcione como website previo a realizar un *Due Diligence*, donde un inversor encuentra a una empresa acreditada y publicada en nuestra plataforma para posteriormente iniciar un *Due Diligence* en nuestra aplicación de *Due Diligence* si ambas partes están de acuerdo en inicializarla. En el transcurrir de la entrevista la señora Guisella se mostró reservada y serena, además de una persona que prioriza la lógica y la practicidad en su trabajo. Hace mención que utiliza un celular Android, su navegador habitual es Chrome y que utiliza Windows en su ambiente laboral.

                [Inicio de entrevista: 25:07]
                [Final de entrevista: 50:39]

![Imagen extraída del video de entrevistas](src/img/cap2/luis-Guisella.png)

| Nombre y Apellido    | Patricia González           |
|----------------------|-----------------------------|
| Edad                 | 58 años                     |
| Ubicación Geográfica | Lima, Perú / Trujillo, Perú |
| Profesión            | Contadora Pública Colegiada |


**Resumen Entrevista:** Patricia González es contadora pública colegiada, lo cual significa que se dedica a ámbitos financieros de, en su caso, una empresa, que ejerce esta profesión por más de 27 años. Tiene experiencia con el proceso de *Due Diligence* como participante Sell-side en labores pasadas para una empresa trujillana. En su opinión, la propuesta de solución tiene mucho mercado interesado y mucho alcance también. Para ella el proceso de *Due Diligence* se divide en 3 etapas: Obtención de Información de Requerimientos, *Due Diligence* e Informe Final. El *Due Diligence* son Ítems de Información divido en áreas de especialización que suele restringirse a Laboral, Legal, Financiera y Tributaria. Cada Ítem es un contenedor de documentos y se reconocen por número. Cada ítem tiene como atributo el requerimiento completa y formalmente escrito. El proceso de *Due Diligence* no le parece tedioso. Opina que una herramienta para censura es una buena idea para segmentos como el RUC y razones sociales en documentos financieros. Por otro lado, no descarta el uso de herramientasque utiliza en su laptop Windows como Excel, Word hasta PowerPoint para ciertos informes que realiza habitualmente durante la *Due Diligence*. O el uso poco habitual de Drive, una herramienta de fácil acceso a través de Chrome.  Cree que el análisis financiero puede ser apoyado por la misma solución yayudaría mucho. Es favorable su opinión en cuanto a la agregación de la funcionalidad de recolección de documentos en páginas públicas específicas y acreditadas. Por último, nos mencionó que usa un iPhone.

                [Inicio de entrevista: 50:40]
               [Final de entrevista: 1:21:07]

![Imagen extraída del video de entrevistas](src/img/cap2/luis-patricia.png)


**Segmento 2: Inversores trabajando en el Buy-side de empresas que busquen agilizar sus procesos de** ***Due Diligence***

| Nombre y Apellido    | Maverick Champi      |
|----------------------|----------------------|
| Edad                 | 28 años              |
| Ubicación Geográfica | Lima, Perú           |
| Profesión            | Economista, Inversor |

**Resumen entrevista:** Maverick Champi es un Economista con 8 años de experiencia en el sector de las finanzas y las inversiones. Durante la entrevista, se exploraron diversas facetas de su experiencia en inversiones y procesos de *Due Diligence*. Maverick tiene un nivel sólido de experiencia en inversiones, realizándolas con frecuencia con el objetivo principal de lograr un crecimiento de capital, aunque también valora la diversificación y el impacto social. Prefiere invertir en empresas nuevas y emergentes, especialmente en sectores tecnológicos y de energía renovable, pero también considera empresas establecidas con potencial de crecimiento. En el proceso de *Due Diligence*, encuentra crucial la información financiera y empresarial, como los estados financieros, proyecciones futuras y el equipo de liderazgo. Maverick utiliza herramientas avanzadas de análisis financiero y plataformas en línea para un seguimiento eficiente de sus inversiones, prefiriendo acceder a la información financiera a través de plataformas en línea con funcionalidades interactivas y de generación de informes. No descarta el uso de herramientas como Google Drive o Excel, debido a que menciona que fueron sus primeras herramientas de trabajo en los momentos que recién había iniciado. Sus objetivos financieros abarcan tanto a corto como a largo plazo, buscando crecimiento y estabilidad en su cartera, y valora la transparencia y comunicación de las empresas en las que invierte. Maverick demuestra un enfoque metódico y disciplinado en sus inversiones, combinando análisis financiero con tecnología avanzada para maximizar el potencial de su cartera y gestionar los riesgos de manera cuidadosa. El entrevistado posee una PC de escritorio Windows, un celular Android y su navegador de preferencia es Chrome. El entrevistado se mostró apasionado al proceso de *Due Diligence*, se nota que le gusta de lo que habla, se expresó con naturalidad y mostró ser alegre, optimista y una persona lógica que no descarta posibilidades de mejora en su ámbito laboral.

                [Inicio de entrevista: 1:21:08]
                [Final de entrevista: 1:53:14]

![Imagen extraída del video de entrevistas](src/img/cap2/abel-maverick.png)

| Nombre y Apellido    | Manuel Flores           |
|----------------------|-------------------------|
| Edad                 | 27 años                 |
| Ubicación Geográfica | Lima, Perú              |
| Profesión            | Ing. Sistemas, Inversor |

**Resumen Entrevista:** Manuel Flores es egresado de Ing. de sistemas; sin embargo, nunca ejerció su profesión y entró al mundo de las inversiones cuando tenía 21 años. Menciona que usualmente realiza sus inversiones siempre que le parezca conveniente con todo tipo de empresas, ya sean emergentes o aquellas que ya llevan tiempo en el mercado. Da a conocer que una de sus prioridades es la seguridad y discreción. Pero siempre dejando libre la capacidad de un trabajo rápido y fluido. Aprecia en gran medida que la empresa sea clara con sus datos. Una empresa que oculte o no esté dispuesta a colaborar no está en su repertorio y prefiere ignorarlas. Algunas funciones que le gustaría ver son la capacidad de realizar búsquedas avanzadas dentro del documento, herramientas colaborativas en tiempo real y notificaciones sobre los cambios que se lleguen a realizar en el documento. Por eso es que menciona su uso cotidiano de Excel y por medio de las herramientas que proporciona Google Drive. Por otro lado, para la parte de seguridad menciona que el cifrado de datos es muy importante además de la capacidad de identificar usuarios, debido a la importancia de la información que se utiliza en estos procesos. Manuel nos comenta que usa un sistema operativo iOS, posee una MacBook Pro y un iPhone, pero su navegador de preferencia es Chrome desde hace ya varios años. Durante la entrevista fue bastante amable con nosotros y se mostró interesado por la solución, incluso realizó preguntas, el entrevistado fue bastante cálido y en ningún momento tuvimos problemas para desenvolvernos.

                [Inicio de entrevista: 2:10:44]
                [Final de entrevista: 2:35:23]

![Imagen extraída del video de entrevistas](src/img/cap2/oscar.png)

| Nombre y Apellido    | Abel Valle    |
|----------------------|---------------|
| Edad                 | 23 años       |
| Ubicación Geográfica | Lima, Perú    |
| Profesión            | Inversor      |

**Resumen entrevista:**  Abel Valle, es un joven inversionista de 24 años que vive actualmente en Lima, Perú, nos ayudó en la entrevista contándonos su experiencia en inversión y sus preocupaciones. Abel trabaja en una empresa financiera y se dedica a evaluar y recomendar oportunidades de inversión para sus clientes. El entrevistado comenta que invierte para obtener un ingreso de capital pasivo a largo plazo. Prefiere invertir en segmentos emergentes, como tecnología o salud y no tiene preferencias respecto al tiempo que lleve la empresa en el mercado. Abel nos comentó que ya conoce sobre el proceso de *Due Diligence*, incluso ha participado en este en reiteradas ocasiones. Considera que la información clave de un informe de *Due Diligence* son la salud de la empresa, su posición en el mercado y la calidad de su equipo directivo. Los riesgos financieros que más le preocupan son la volatilidad del mercado, el endeudamiento excesivo y cambios regulatorios. Suele invertir en variedad se sectores geográficos, pero principalmente invierte al extranjero. Este inversionista prefiere recibir los resultados de *Due Diligence* en formato virtual, ya sea a través de una plataforma en línea o documentos encriptados. Debido a eso es que utiliza herramientas como DropBox y en algunos casos Google Drive por las herramientas que ofrece con sus documentos y los cuadros de cálculo de fácil accesibilidad pero manteniendo una seguridad debida.  En la plataforma de *Due Diligence* le gustaría ver herramientas que faciliten el análisis de datos y la generación de informes personalizados. Considera esencial que se implementen medidas de seguridad robustas al compartir información financiera y empresarial durante el proceso de inversión. Abel menciona que le gustaría tener acceso a análisis exhaustivos y datos en tiempo real del mercado para tomar decisiones de inversión más coherentes. El entrevistado usa una computadora Windows, un celular Android y su navegador de preferencia es Chrome. Abel se mostró un poco tímido al principio, pero poco a poco fue desenvolviéndose, es bastante carismático, pero se le nota un poco abrumado por la cantidad de preguntas. Por otro lado, fue bastante conciso a la hora de dar respuestas demostrando su conocimiento práctico sobre el tema.

                [Inicio de entrevista: 1:53:15]
                [Final de entrevista: 2:10:44]

![Imagen extraída del video de entrevistas](src/img/cap2/arturo.png)

### Análisis de entrevistas

**Segmento de Contadores:**

**Perfil Demográfico**

* Edades: Promedio de 44 años.
* Ubicación Geográfica: Principalmente Lima, Perú.
* Profesión: Contadores Públicos Colegiados.
* Experiencia Laboral: Más de 25 años en promedio.

**Experiencia y Conocimientos en** ***Due Diligence***

* Todos los contadores públicos entrevistados tienen una experiencia considerable en el proceso de *Due Diligence*, con más de 25 años de experiencia en promedio.
* Algunos tienen experiencia en ambos lados de la transacción (sell-side y buy-side).

**Herramientas y Tecnologías utilizadas**

* Todos tienen experiencia con herramientas virtuales como Dropbox y Excel para Due Diligence.
* Valoran las plataformas en la nube que ofrecen seguridad y facilidad de uso para almacenar y analizar documentos financieros.

**Intereses y Necesidades en Plataformas de** ***Due Diligence***

* Consideran importante la automatización del análisis de datos financieros para agilizar el proceso.
* Valorizan la seguridad de los datos financieros sensibles, buscando cifrado de extremo a extremo y medidas de seguridad robustas.
* Prefieren una interfaz intuitiva y fácil de usar para facilitar la navegación y el acceso a la información relevante.
* Algunos encuentran útil la posibilidad de realizar análisis financieros dentro de la plataforma, especialmente al tratar con una gran cantidad de documentos.
* Opinan que la herramienta de recolección de información de la internet sería valiosa para complementar los documentos recibidos.

**Preferencias y Comportamientos**

* Tienen un enfoque meticuloso y analítico en el proceso de Due Diligence.
* Valorizan la eficiencia y la precisión en el análisis de datos financieros.
* Algunos contadores consideran que evitar la descarga de archivos durante el proceso no es necesario, ya que la confidencialidad es clave.
* Prefieren la seguridad en las plataformas de Due Diligence sobre otras funcionalidades menos relevantes.
* Reconocen la importancia de sesiones presenciales en algunos aspectos de su trabajo, aunque la tecnología como realidad virtual es vista como una herramienta complementaria.

 **Estadísticas y Porcentajes**

* El 100% de los contadores considera que nuestra propuesta de una plataforma en la nube especializada en Due Diligence es muy favorable y tiene un mercado interesante.
* El 100% valora la seguridad de los datos financieros sensibles como una prioridad.
* El proceso de Due Diligence, según el 100% de los contadores entrevistados, se divide en tres etapas: Entrega de Requerimientos de la Información, Due Diligence y el Informe Final.
* El 100% de los contadores menciona que el Due Diligence se centra en áreas específicas como laboral, legal, financiera y tributaria, dividiendo la información en ítems numerados con requerimientos formales.
* El 100% de los contadores opina que una herramienta de censura para documentos financieros sería beneficiosa, especialmente para información sensible como el RUC y razones sociales.
 Todos los contadores entrevistados consideran que la inclusión de un análisis financiero dentro de la plataforma sería una herramienta útil y novedosa.
* El 100% de los contadores está a favor de la funcionalidad de recolección de documentos desde páginas públicas específicas y acreditadas como una característica valiosa para agilizar el proceso de obtención de información clave.
 Todos los contadores destacan la importancia de la seguridad y confidencialidad de los datos financieros en el proceso de Due Diligence, enfatizando la necesidad de medidas robustas.
* El 100% de los contadores menciona que la plataforma debe ser intuitiva y fácil de usar, considerando la diversidad de usuarios que podrían interactuar con ella.
* En cuanto a los problemas más comunes atendidos durante el Due Diligence, el 100% de los contadores menciona áreas como laboral, legal, financiera y tributaria.
* El 100% los contadores consideran que la eficiencia y efectividad del proceso de Due Diligence son clave para garantizar resultados precisos y completos en las transacciones empresariales.
* El 100% mostraron ser personas racionales a lo largo de la entrevista.

::: note
Con base en estas entrevistas, se puede concluir que los contadores públicos entrevistados tienen una vasta experiencia en *Due Diligence*, valoran la eficiencia, la seguridad y la facilidad de uso en una plataforma especializada, y consideran que herramientas como el análisis financiero integrado y la recolección de documentos desde fuentes públicas serían de gran utilidad. Además, se resalta la importancia de la seguridad de los datos, la segmentación por áreas específicas en el *Due Diligence*, y la necesidad de una interfaz intuitiva para facilitar la navegación y el uso de la plataforma.
:::

**Segmento de Inversores:**

**Perfil Demográfico**

* Edades: Promedio de 25 años.
* Ubicación Geográfica: Principalmente Lima, Perú.
* Profesión: Inversores con formación en áreas como Economía, Ingeniería de Sistemas, entre otros.
* Experiencia Laboral: Alrededor de 3 a 8 años en el campo de las finanzas e inversiones.

**Objetivos e Intereses en Inversiones**

 * Todos buscan principalmente el crecimiento de capital en sus inversiones.
 * Algunos tienen interés en la diversificación de sus carteras y el impacto social de sus inversiones.
 * Prefieren empresas nuevas y emergentes, especialmente en sectores tecnológicos y de energía renovable.

 **Conocimientos y Participación en** ***Due Diligence***

 * Todos tienen experiencia en el proceso de *Due Diligence*, enfocándose en la información financiera y empresarial.
 * Participan activamente en el proceso para comprender los riesgos y oportunidades.

**Uso de Herramientas y Plataformas**

 * Utilizan herramientas avanzadas de análisis financiero y plataformas en línea para monitorear sus inversiones.
 * Valoran la seguridad de los datos financieros y aprecian funcionalidades como el análisis predictivo y simulaciones de escenarios.
 * Buscan plataformas con interfaces interactivas y generación de informes eficiente.
 * Mencionan el uso de herramientas más cotidianas como Google Drive y DropBox.

**Preferencias y Estrategias de Inversión**

 * Prefieren un enfoque activo en la inversión, buscando empresas con modelos de negocio claros y equipos directivos sólidos.
 * Su tolerancia al riesgo varía, pero buscan oportunidades con un equilibrio entre riesgo y retorno.
 * Valoran la transparencia y la comunicación de las empresas en las que invierten.

**Estadísticas y Porcentajes**

* El 100% tiene experiencia en el proceso de Due Diligence.
* El 66% ha participado en consultoría sell-side para empresas financieras.
* El 100% busca principalmente el crecimiento de capital en sus inversiones.
* El 66% tiene interés en la diversificación de sus carteras.
* El 66% valora el impacto social de sus inversiones.
* El 100% utiliza herramientas avanzadas de análisis financiero y plataformas en línea.
* El 100% valora la seguridad de los datos financieros en las plataformas de Due Diligence.
* El 100% busca interfaces interactivas y generación de informes eficiente.
* El 100% prefiere un enfoque activo en la inversión.
* El 100% busca empresas con modelos de negocio claros y equipos directivos sólidos.
* El 66% tiene una tolerancia moderada al riesgo
* El 100% de los entrevistados mostraron ser personas racionales.

::: note
Con base en estas entrevistas, se puede concluir que los inversores tienen un enfoque estratégico en sus inversiones, buscando el crecimiento de capital en empresas con potencial de crecimiento y un impacto social positivo. Valorando la seguridad y las herramientas tecnológicas en el proceso de Due Diligence, buscan plataformas que les proporcionen información clara, análisis efectivo y una gestión eficiente de sus inversiones. También, se destaca su interés en modelos de negocio sólidos y equipos directivos confiables en las empresas en las que invierten.
:::

## *Needfinding*

En el cambiante mundo de las transacciones empresariales y la diligencia debida, DiligenceTech se ha comprometido con la excelencia en el servicio a través de un enfoque dedicado para comprender las necesidades específicas de sus usuarios. Esta sección, denominada Needfinding, representa nuestra firme convicción en la importancia de escuchar y comprender a fondo las demandas de nuestros usuarios y clientes.

En DiligenceTech, creemos que el éxito de nuestra plataforma radicará en nuestra capacidad de responder de manera efectiva a las necesidades del mercado. A través de investigaciones detalladas y la recopilación de valiosas entrevistas, hemos desarrollado una profunda comprensión de las necesidades y deseos de los profesionales involucrados en el proceso de *Due Diligence*. Este conocimiento nos impulsa a ofrecer características y funcionalidades que se alinean perfectamente con las expectativas de nuestros usuarios, asegurando que DiligenceTech, se desarrolle con el objetivo de ser una herramienta esencial en la simplificación y mejora del proceso de evaluación empresarial.

En la siguiente sección de Needfinding, profundizaremos en cómo DiligenceTech se compromete a entender y abordar de manera proactiva las cambiantes necesidades de nuestros usuarios, permitiéndoles realizar el proceso de  *Due Diligence* más eficiente y preciso que nunca.

![Imagen extraída de Canva](src/img/cap2/needfind-baner.png)

### *User Personas*

Presentaremos los User Persona por cada segmento objetivo, en los cuales nos basamos en los usuarios ideales de cada segmento. A continuación, los presentamos:

User Persona 1 - Segmento de Contadores: Marta Díaz

![Artefacto creado en UXPressia](src/img/cap2/Marta-Díaz.png)

Gráfico sobre la sistema operativo mas usado:
![Creado en Excel](src/img/cap2/contador-sistema-op.png)

Gráfico sobre dispositivo movil mas usado:
![Creado en Excel](src/img/cap2/contador-disp-movil.png)

Gráfico sobre browser mas usado:
![Creado en Excel](src/img/cap2/contador-browser.png)

User Persona 2 - Segmento de Inversores: Christian Pinto

![Artefacto creado en UXPressia](src/img/cap2/Christian-Pinto.png)

Gráfico sobre la sistema operativo mas usado:
![Creado en Excel](src/img/cap2/inversor-sistema-op.png)

Gráfico sobre dispositivo movil mas usado:
![Creado en Excel](src/img/cap2/inversor-disp-movil.png)

Gráfico sobre browser mas usado:
![Creado en Excel](src/img/cap2/inversor-browser.png)

### *User Task Matrix*

User Task Matrix: Marta Díaz y Christian Pinto

![Artefacto creado en LucidChart](src/img/cap2/User-Task-Matrix.png)

### *User Journey Mapping*

User Journey Mapping: Marta Díaz 

![Artefacto creado en UXPressia](src/img/cap2/Customer-journey-Marta-Díaz.png)

User Journey Mapping: Christian Pinto

![Artefacto creado en UXPressia](src/img/cap2/Customer-journey-Christian-Pinto.png)

### *Empathy Mapping*

Empathy Mapping: Marta Díaz 

![Artefacto creado en UXPressia](src/img/cap2/empaty-map-Marta-Díaz.png)

Empathy Mapping: Christian Pinto

![Artefacto creado en UXPressia](src/img/cap2/empaty-map-Christian-Pinto.png)

### *As-is Scenario Mapping*

El As-Is Scenario Mapping es una herramienta para identificar los pensamientos que tendrán los usuarios a la hora de utilizar la aplicación actual.

***As-Is Scenario Map:*** **Contador Financiero**

![Recurso creado en Miro](src\img\cap2\AsIsSM_Cont.png)

***As-Is Scenario Map:*** **Inversor**

![Recurso creado en Miro](src\img\cap2\AsIsSM_Inv.png)

## *Ubiquitous Language*

* **M&A:** También conocido como Fusiones y Adquisiciones. El segmento de finanzas corporativas al que pertenece Due Diligence. Trata de las transacciones empresariales con el objetivo de transferir la propiedad de empresas.

* **Due Diligence:** Investigación (o proceso) hecha por una Acquiring Entity (empresa o inversor) hacia una Target Company con el objetivo de que esta averiguación de a conocer si no existen problemas financieros, tributarios, legales o de otras áreas con la Target Company para proceder con una adquisición o firma de contrato con esta. Se divide en 3 procesos centrales: Presentation of Information Requirements, Due Diligence Process y Final Report. Nuestra solución se centra en el 2do.

* **Due Diligence Project:** Identificación de un Due Diligence de una Target Company en específico y todos sus procesos, suelen tener nombres informales para evitar el reconocimiento de cualquiera de las dos empresas (Target Company y Acquiring Company) e intermediarios (por ejemplo, Proyecto Gloria, Proyecto Messi, Proyecto Bebé, Proyecto Luis).

* **Acquiring Entity:** También conocido como Acquiring Company o Inversor. Agente económico en busca de obtener el dominio parcial o completo de una empresa, o firmar acuerdos con ésta en general. Participa en Due Diligence tratando de obtener información de la empresa que desea vender su propiedad (Target Company) para formar sus conclusiones si generará problemas comprarla o no.

* **Buy-Side:** Empresa financiera dedicada a ser contratada para hacer la labor de la Acquiring Company en un proceso de Due Diligence. Normalmente, los Buy-Side Agents son en realidad trabajadores de estas empresas.

* **Buy-Side Agent:** Uno de los dos tipos de actores en un proceso de Due Diligence. Representante de la Acquiring Entity que se encarga de hacer la Presentation of Information Requirements, supervisar y confirmar el Due Diligence Process y hacer el Final Report. Suele ser un inversor, o un abogado, o un Asociado de Auditoría. Nuestra solución se centra en el caso de que sea un inversor. En un proyecto grande usualmente hay más de uno.

* **Target Company:** Empresa en busca de inversiones, la cual por convención (porque es un proceso recomendado, no obligatorio) debe participar en procesos de Due Diligence entregando información confidencial en formato de Corporate Documents en el caso que haya confiado en esta empresa previo al inicio de la investigación.

* **Sell-Side:** Empresa financiera dedicada a ser contratada para hacer la labor de la Target Company en un proceso de Due Diligence. Normalmente, los Sell-Side Agents son en realidad trabajadores de estas empresas.

* **Sell-Side Agent:** Uno de los dos tipos de actores en un proceso de Due Diligence. Representante de la Target Company que se encarga de hacer el Due Diligence Process, lo cual implica ingresar y conseguir los documentos requeridos por la Acquiring Company. Suele ser un contador público/financiero o un abogado. Nuestra solución se centra en el caso sea un contador público/financiero, el cual es el caso más común. En un proyecto grande usualmente hay más de uno.

* **Presentation of Information Requirements:** Primer proceso de Due Diligence. Los Buy-Side Agents tienen como objetivos recopilar en Information Items por Buy-Side Agents, a este conjunto se le llama Information Requirements y es enviado al Target Company para su aprobación y continuación de la investigación mediante el Due Diligence Process.

* **Due Diligence Process:** El proceso principal de nuestra solución. Se trata de, posteriormente a la obtención de Information Requirements por parte del Target Company. Los Sell-Side Agents recolectan y envían los documentos en base a cada Item obtenido. Con la ayuda de la virtualidad, este proceso suele verse ahora en un servicio de alojamiento online que permite la visualización en tiempo-real de la entrega de archivos del Target Company hacia el Acquiring Company.

* **Q&A:** Sistema complementario al Due Diligence Process. Comunicación formal y documentada en base de Questions escritas, hechas exclusivamente por cualquier Buy-Side Agent, enfocada a un Item en específico donde se puede pedir más documentos, cambio de documentos, o especificación escrita de documentos entregados. Cada Question deja espacio a un grupo de Answers escritas o presentadas con Archivos hechas exclusivamente por cualquier Sell-Side Agent. Cada Question debe especificar el Item al cual se enfoca y son identificadas por números. Al igual que un Item, estas se consideran completadas si el Status de cada equipo son “Done”.

* **Question:** Solicitud escrita centrada en un Item y hecha por un Buy-Side Agent en un Due Diligence Project solicitando más documentos, cambio de documentos, o especificación escrita de documentos entregados. El formato en el que se escribe es idéntico a un Information Item.

* **Answer:** Respuesta escrita o con documentos centrada en una Question hecha exclusivamente por un Sell-Side Agent.

* **Final Report:** Proceso final de Due Diligence donde al obtener todos los documentos deseados la Acquiring Company se encarga de producir un documento final señalando posibles riesgos al adquirir o colaborar con la Target Company. Se suele presentar en formato Office Open XML Presentation (.pptx) o PDF.

* **Area (of Specialization):** División de Information Requirements enfocado en departamentos corporativos donde puedan presentarse problemas legales o financieros. Suelen presentarse usualmente “Financial”, “Legal”, “Tax”, “Operational”, aunque no está limitado a ellos. También se presenta “IT” e “Infrastructure”.

* **Information Requirements:** Conjunto de Information Items dividido en Areas of Specialization. Suele presentarse en formato virtual Office Open XML Workbook (.xlsx).

* **Information Item:** También conocido como Information Requirement. Solicitud escrita por la Acquiring Entity en párrafos, organizada por el área al que pertenece, que debe explicitar los documentos que se desean obtener de la Target Company. La Target Company responde a cada ítem con documentos. Un Item se le considera completo cuando el Status de la Acquiring Entity y la Target Company para este sea “Done”. Están identificados por número. Pueden ser obligatorias o opcionales. Los *Information Items* poseen un sistema de jerarquía en caso exista un conjunto que pueda ser englobado por una idea general, que se escribe en un Information Item. En estos casos, cada uno del conjunto se identifica por el número del Item general y el número del Item particular. Por convención, el Item general no se escribe como una solicitud sino como una frase que represente al grupo y no puede poseer documentos, de eso se encarga cad Item particular.

* **Acquiring Status:** Opinión de la Acquiring Entity sobre la integridad del conjunto de documentos enviados por la Target Company en un ítem. Opinión limitada a “In Progress” y “Done”.
Target Status: Opinión de la Target Company sobre la integridad del conjunto de documentos enviados en un ítem. Opinión limitada a “In Progress” y “Done”.

* **(Corporate) Documents:** Una unidad de contenido escrito (usualmente un conjunto de hojas impresas en físico) que se presenta en un Item por la Target Company para ser revisado por una Acquiring Entity. Virtualmente se presenta como un archivo de los cuales los más comunes tienen como extensión “.pdf”, “.xlsx”, “.docx”.

# Capítulo III: *Requirements Specification*

En este capítulo, nos adentramos en la identificación detallada de los requisitos esenciales que permitirán a los usuarios interactuar de manera efectiva y satisfactoria con nuestra aplicación. Es fundamental comprender las necesidades y expectativas de quienes utilizarán nuestra *web application*, lo que nos guiará en la creación de una experiencia de usuario óptima.

![](src\img\cap3\requeriments-specification-baner.png)

## *To-Be Scenario Mapping*

El *To-Be Scenario Mapping* es una herramienta para identificar cómo se sentirán los usuarios con los nuevos cambios que deberían haber solucionado los problemas planteados en los *As-Is scenario maps.*

![Recurso creado en Miro](src\img\cap3\ToBeSM.png)

## *User Stories*

***Epics***

+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| EP01 (Gestión de Cuentas de Usuario) | Como usuario, quiero registrarme, iniciar sesión y mantener control sobre mi cuenta para acceder de manera segura a la aplicación y gestionar mis datos personales. |
+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US01                                 | Registro de inversor                                                                                                                                                |
+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US02                                 | Confirmación de creación de cuenta                                                                                                                                  |
+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US03                                 | Verificación de cuenta                                                                                                                                              |
+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US04                                 | Registro de empresa                                                                                                                                                 |
+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US05                                 | Verificación de cuenta empresa                                                                                                                                      |
+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US06                                 | Recuperación de cuenta                                                                                                                                              |
+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| EP02 (Gestión de Empresas y Solicitudes) | Como usuario, quiero poder gestionar empresas y solicitudes, desde su registro hasta su cierre, para realizar procesos de due diligence de manera efectiva y eficiente. |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US07                                     | Visualización de empresas                                                                                                                                               |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US08                                     | Filtro de empresas                                                                                                                                                      |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US09                                     | Ordenamiento de empresas                                                                                                                                                |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US10                                     | Interfaz de búsqueda sencilla                                                                                                                                           |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US11                                     | Visualización de solicitudes                                                                                                                                            |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US12                                     | Filtro de solicitudes                                                                                                                                                   |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US13                                     | Ordenamiento de solicitudes                                                                                                                                             |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US14                                     | Admición de solicitudes                                                                                                                                                 |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US15                                     | Creación de la solicitud                                                                                                                                                |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US16                                     | Consulta de orden de solicitud                                                                                                                                          |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US17                                     | Actualizaciones sobre la solicitud                                                                                                                                      |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US18                                     | Respuesta de solicitud                                                                                                                                                  |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US19                                     | Razón de la respuesta otorgada                                                                                                                                          |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US20                                     | Creación de queja                                                                                                                                                       |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US22                                     | Cierre de solicitud                                                                                                                                                     |
+------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| EP03 (Seguridad y Confidencialidad) | Como usuario, quiero que mis datos y la información de las empresas sean seguros y confidenciales, evitando fugas de seguridad y limitando el acceso no autorizado, para proteger la integridad de la información. |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US23                                | Seguridad de entrega                                                                                                                                                                                               |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US24                                | Limitación al entregar datos                                                                                                                                                                                       |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US25                                | Alertas de fugas de seguridad                                                                                                                                                                                      |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

+----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| EP04 (Análisis Financiero) | Como usuario, quiero realizar análisis financieros con los datos recibidos para evaluar adecuadamente las empresas y tomar decisiones informadas sobre mis inversiones. |
+----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US26                       | Visualización de análisis financieros disponibles                                                                                                                       |
+----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US27                       | Eficacia de los algoritmos de análisis financiero                                                                                                                       |
+----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US28                       | conclusión del análisis financiero                                                                                                                                      |
+----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US21                       | Visualización de datos recibidos                                                                                                                                        |
+----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| EP05 (Optimización de la API) | Como desarrollador, quiero implementar funcionalidades de paginación y filtrado en los endpoints de la API para mejorar la eficiencia en la entrega de recursos y optimizar el rendimiento del sistema. |
+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US29                          | RESTful API Registro de usuario                                                                                                                                                                         |
+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US30                          | RESTful API Inicio de sesión de usuario                                                                                                                                                                 |
+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US31                          | Autenticación basada en token JWT                                                                                                                                                                       |
+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US32                          | Recuperación de contraseña                                                                                                                                                                              |
+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US33                          | CRUD para recursos principales                                                                                                                                                                          |
+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US34                          | Paginación y filtrado de resultados                                                                                                                                                                     |
+-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| EP06 (Landing Page Optimizada) | Como usuario interesado, deseo una landing page intuitiva y optimizada que proporcione información clara y accesible sobre la aplicación, para facilitar la toma de decisiones informadas y la interacción con el equipo de la aplicación. |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US35                           | Descubrimiento intuitivo                                                                                                                                                                                                                   |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US36                           | Contenido informativo                                                                                                                                                                                                                      |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US37                           | Compatibilidad móvil                                                                                                                                                                                                                       |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US38                           | Formulario de contacto                                                                                                                                                                                                                     |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US39                           | Contenido multimedia                                                                                                                                                                                                                       |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US40                           | Call-to-action claro                                                                                                                                                                                                                       |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US41                           | Menú superior funcional                                                                                                                                                                                                                    |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| US42                           | Call to action button funcional                                                                                                                                                                                                            |
+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Criterios de Aceptación:**

![](src/img/cap3/criterios1.png)
![](src/img/cap3/criterios2.png)
![](src/img/cap3/criterios3.png)
![](src/img/cap3/criterios4.png)
![](src/img/cap3/criterios5.png)
![](src/img/cap3/criterios6.png)
![](src/img/cap3/criterios7.png)
![](src/img/cap3/criterios8.png)
![](src/img/cap3/criterios9.png)
![](src/img/cap3/criterios10.png)
![](src/img/cap3/criterios11.png)
![](src/img/cap3/criterios12.png)
![](src/img/cap3/criterios13.png)
![](src/img/cap3/criterios14.png)
![](src/img/cap3/criterios15.png)
![](src/img/cap3/criterios16.png)
![](src/img/cap3/criterios17.png)
![](src/img/cap3/criterios18.png)
![](src/img/cap3/criterios19.png)
![](src/img/cap3/criterios20.png)
![](src/img/cap3/criterios21.png)
![](src/img/cap3/criterios22.png)
![](src/img/cap3/criterios23.png)
![](src/img/cap3/criterios24.png)
![](src/img/cap3/criterios25.png)
![](src/img/cap3/criterios26.png)
![](src/img/cap3/criterios27.png)
![](src/img/cap3/criterios28.png)
![](src/img/cap3/criterios29.png)
![](src/img/cap3/criterios30.png)
![](src/img/cap3/criterios31.png)
![](src/img/cap3/criterios32.png)
![](src/img/cap3/criterios33.png)
![](src/img/cap3/criterios34.png)
![](src/img/cap3/criterios35.png)
![](src/img/cap3/criterios36.png)
![](src/img/cap3/criterios37.png)
![](src/img/cap3/criterios38.png)
![](src/img/cap3/criterios39.png)
![](src/img/cap3/criterios40.png)
![](src/img/cap3/criterios41.png)
![](src/img/cap3/criterios42.png)
![](src/img/cap3/criterios43.png)
![](src/img/cap3/criterios44.png)
![](src/img/cap3/criterios45.png)
![](src/img/cap3/criterios46.png)
![](src/img/cap3/criterios47.png)

**Redaccción de Criterios de Aceptación:** 

US01: Registro de inversor 

Como usuario inversionista, quiero crear una cuenta con el uso de mi correo electrónico para representarme en la aplicación.

Escenario 1: “Creación de cuenta"
Dado que el usuario ingresa al formulario de creación de cuenta,
cuando ingresa una dirección de correo electrónico y una contraseña,
entonces se registra con su cuenta y lo redirige a la página de inicio.

Escenario 2: “Intento de creación de cuenta sin datos"
Dado que el usuario ingresa al formulario de creación de cuenta
cuando no ingresa una dirección de correo electrónico ni contraseña
entonces se muestra un mensaje de error indicando que no se han ingresado datos.

Escenario 3: “Creación de cuenta con un correo ya usado “
Dado que el usuario ingresa al formulario de creación de cuenta
cuando ingresa una dirección de correo electrónico y una contraseña,
entonces se muestra un mensaje de error indicando que la dirección de correo ya está siendo usada.

US02: Confirmación de creación de cuenta

Como usuario, quiero recibir una confirmación de la creación de mi cuenta a través del correo electrónico que proporcioné para confirmar la creación de la cuenta.

Escenario 1: "Correo de confirmación enviado"
Dado que el usuario ha creado una cuenta,
Cuando quiere confirmar que su cuenta ha sido creada
Entonces se envía un correo electrónico de confirmación a la dirección proporcionada.

Escenario 2: "Error al enviar correo de confirmación"
Dado que el usuario ha creado una cuenta,
Cuando quiere confirmar si su cuenta ha sido creada,
Entonces no le llega ningún correo de confirmación

US03: verificación de cuenta

Como usuario, quiero llenar un formulario en la creación de mi cuenta para acreditar mi nombre y mi fiabilidad.


Escenario 1: "Formulario completado "
Dado que el usuario quiere verificar su cuenta
Cuando llena el formulario de verificación con todos sus datos,
Entonces entra al proceso de verificación de cuenta.

Escenario 2: "Error al completar el formulario"
Dado que el usuario quiere verificar su cuenta
Cuando llena el formulario de verificación sin todos sus datos,
Entonces sale un error que pide llenar todos los datos obligatorios.

US04: Registro de empresa

Como usuario contador financiero, quiero crear una cuenta con el uso de mi correo electrónico empresarial para registrar a mi empresa

Escenario 1: "Registro de empresa"
Dado que el usuario contador financiero ingresa al formulario de creación de cuenta de empresa,
Cuando ingresa la dirección de correo electrónico proporcionada por la empresa y una contraseña,
Entonces registra a su empresa y es redirigido a la página de inicio.

Escenario 2: “Registro sin datos"
Dado que el usuario contador financiero ingresa al formulario de creación de cuenta de empresa,
Cuando no ingresa la dirección de correo electrónico proporcionada por la empresa ni una contraseña,
Entonces aparece un mensaje de error que dice que ingrese los datos.

Escenario 3: “Registro con contraseña invalida"
Dado que el usuario contador financiero ingresa al formulario de creación de cuenta de empresa,
Cuando ingresa la dirección de correo electrónico proporcionada por la empresa y una contraseña,
Entonces aparece un mensaje de error que dice que su contraseña es invalida.

US05: Verificación de cuenta de empresa

Como usuario contador financiero, quiero que se me soliciten los datos de mi empresa para verificar la fiabilidad de esta.


Escenario 1: “Inicio de proceso de verificación"
Dado que el contador financiero quiere verificar la cuenta de la empresa que representa,
Cuando llena el formulario para verificar la cuenta,
Entonces entra al proceso de verificación de cuenta.

Escenario 2: “Error al completar el formulario"
Dado que el contador financiero quiere verificar la cuenta de la empresa que representa,
Cuando llena el formulario para verificar la cuenta sin todos los datos pedidos,
Entonces sale un error que le pide llenar los datos obligatorios

US06: Recuperación de cuenta

Como usuario, quiero recuperar mi contraseña por medio del correo vinculado con mi cuenta para recuperar el uso de esta.

Escenario 1: "Solicitud de recuperación de contraseña"
Dado que el usuario ingresa al formulario de recuperación de cuenta,
Cuando ingresa su correo electrónico vinculado,
Entonces se genera un enlace de restablecimiento de contraseña único y se envía por correo electrónico a la dirección proporcionada.

Escenario 2: “Solicitud de recuperación de contraseña con correo no vinculado"
Dado que el usuario ingresa al formulario de recuperación de cuenta,
Cuando ingresa un correo electrónico no vinculado,
Entonces aparece un error señalando que el correo ingresado no está vinculado con ninguna cuenta.

Escenario 3: "Error al enviar correo de recuperación “
Dado que el usuario ingresa al formulario de recuperación de cuenta,
Cuando ingresa un correo electrónico vinculado,
Entonces no le llega ningún mensaje al correo proporcionado. 

US07: Visualización de proyectos

Como usuario, quiero visualizar los proyectos creados para poder acceder a ellos cuando necesite.

Escenario 1: "Visualización de proyectos creados"
Dado que el usuario a su página principal,
Cuando se desplaza por la sección correspondiente
Entonces se muestra una lista completa y actualizada de todos los proyectos creados.

Escenario 2: “Carga de proyectos fallida"
Dado que el usuario ingresa su página principal,
Cuando se desplaza por la sección correspondiente
Entonces sale error de carga de datos.

Escenario 3: “Sin proyectos"
Dado que el usuario ingresa su página principal,
Cuando se desplaza por la sección correspondiente
Entonces sale un aviso que le indica que no hay proyectos creados.

US08: Filtro de proyectos

Como usuario, quiero filtrar la lista de proyectos disponibles para elegir los que cumplan con mis requisitos.

Escenario 1: "Filtrado de proyectos"
Dado que el usuario desea filtrar la lista de proyectos disponibles,
cuando selecciona los criterios de filtrado deseados,
entonces se muestra una lista de proyectos que cumplen con los criterios de filtrado seleccionados.

Escenario 2: "Sin resultados de filtrado"
Dado que el usuario inversionista desea filtrar la lista de proyectos disponibles
cuando selecciona los criterios de filtrado deseados,
entonces se muestra un mensaje indicando que no se encontraron proyectos que cumplan con los criterios de filtrado seleccionados

US09: Ordenamiento de proyectos

Como usuario, quiero ordenar la lista de proyectos disponibles para elegir las que cumplan con mis requisitos.


Escenario 1: "Orden por nombre"
Dado que el usuario inversionista desea ordenar la lista de proyectos disponibles,
cuando selecciona la opción de ordenar por nombre,
entonces se muestra una lista de proyectos ordenadas alfabéticamente por nombre.

Escenario 2: "Orden por sector"
Dado que el usuario inversionista desea ordenar la lista de proyectos disponibles,
cuando selecciona la opción de ordenar por sector,
entonces se muestra una lista de proyectos ordenadas alfabéticamente por sector.

Escenario 3: "Error de ordenación"
Dado que el usuario inversionista desea ordenar la lista de proyectos disponibles,
cuando intenta ordenarlas, 
entonces se muestra un mensaje de error indicando que no se pudo completar la ordenación de los proyectos.

US10: Barra de búsqueda.

Como usuario, quiero una barra de búsqueda para realizar búsquedas más específicas.


Escenario 1: “búsqueda de proyectos"
Dado que el usuario desea encontrar un proyecto en específico,
Cuando se ingresa el nombre del proyecto en la barra de búsqueda,
Entonces aparece el proyecto que estaba buscando.

Escenario 2: “Proyecto no encontrado"
Dado que el usuario desea encontrar un proyecto en especifico,
Cuando se ingresa el nombre del proyecto en la barra de búsqueda,
Entonces aparece un mensaje que menciona que no hay proyectos con el nombre ingresado.

Escenario 3: “Error de carga"
Dado que el usuario desea encontrar un proyecto en específico,
Cuando se ingresa el nombre del proyecto en la barra de búsqueda,
Entonces aparece un mensaje de error que menciona que no se pudo acceder a la base de datos.

US11: Visualización de solicitudes

Como usuario contador financiero, quiero visualizar las solicitudes que me han llegado para acceder a ellas.


Escenario 1: "Visualización exitosa de solicitudes"
Dado que el usuario contador financiero ingresa al área de solicitudes,
cuando es dirigido al área,
entonces se muestra una lista de las solicitudes recibidas por el contador financiero.

Escenario 2: "Error al cargar solicitudes"
Dado que el usuario contador financiero ingresa al área de solicitudes,
cuando es dirigido al área,
entonces se muestra un mensaje de error indicando que no se pueden cargar las solicitudes recibidas en este momento.

US12: Filtrado de solicitudes

Como usuario contador financiero, quiero filtrar las solicitudes recibidas según diferentes criterios para mantener un mayor orden.


Escenario 1: "Filtrado de solicitudes"
Dado que el usuario contador financiero ingresa al área de solicitudes,
cuando selecciona los criterios de filtrado deseados,
entonces se muestra una lista de solicitudes que cumplen con los criterios de filtrado seleccionados.

Escenario 2: "Sin resultados de filtrado"
Dado que el usuario contador financiero ingresa al área de solicitudes,
cuando selecciona criterios de filtrado que no coinciden con ninguna solicitud en la base de datos,
entonces se muestra un mensaje indicando que no se encontraron solicitudes que cumplan con los criterios de filtrado seleccionados.

US13: Ordenamiento de solicitudes

Como usuario contador financiero, quiero ordenar las solicitudes recibidas según diferentes criterios para mantener un mayor orden.


Escenario 1: "Ordenación exitosa de solicitudes"
Dado que el usuario contador financiero ingresa al área de solicitudes,
cuando selecciona un criterio de ordenamiento,
entonces se muestra una lista de solicitudes ordenadas según el criterio seleccionado.

Escenario 2: "Error de ordenación"
Dado que el usuario contador financiero ingresa al área de solicitudes
cuando selecciona el criterio de ordenamiento,
entonces se muestra un mensaje de error indicando que no se pudo completar la ordenación de las solicitudes.

US14: Admisión de solicitudes

Como usuario contador financiero, quiero aceptar o rechazar solicitudes que reciba para mantener un control de los datos que estoy permitido entregar.


Escenario 1: “Admisión de solicitud"
Dado que el usuario contador financiero desea aceptar una solicitud recibida,
cuando selecciona la solicitud correspondiente y elige aceptar
entonces se procesa la solicitud y actualiza su estado como aceptada.

Escenario 2: "Rechazo de solicitud"
Dado que el usuario contador financiero desea rechazar una solicitud recibida,
cuando selecciona la solicitud correspondiente y elige rechazar,
entonces se procesa la solicitud y actualiza su estado como rechazada

US15: Creación de solicitud

Como usuario inversionista, quiero solicitar los datos que quiero conocer sobre la empresa que elegí para realizar los análisis necesarios.


Escenario 1: "Solicitud de datos"
Dado que el usuario inversionista pide datos a una empresa,
cuando selecciona la empresa deseada y especifica los datos que desea obtener,
entonces se registra la solicitud y la envía al contador financiero correspondiente para su procesamiento.

Escenario 2: "Error al enviar la solicitud"
Dado que el usuario inversionista pide datos a una empresa,
cuando selecciona la empresa deseada y especifica los datos que desea obtener,
entonces se muestra un mensaje de error indicando que no se pudo procesar la solicitud en este momento.

US16: Actualizaciones sobre la solicitud 
Como usuario inversionista, quiero recibir notificaciones sobre el estado de mi solicitud para mantenerme informado sobre el comportamiento de la empresa.


Escenario 1: "Notificación de actualización de estado"
Dado que el usuario inversionista ha realizado una solicitud,
cuando hay un cambio en el estado de su solicitud,
entonces se envía una notificación al usuario informándole sobre el nuevo estado de su solicitud.

Escenario 2: "Falta de notificaciones de estado"
Dado que el usuario inversionista que ha realizado una solicitud,
cuando hay un cambio en el estado de su solicitud, 
entonces no se envía ninguna notificación sobre estado de solicitudes.

US17: Respuesta de solicitud
Como usuario inversionista, quiero recibir la respuesta sobre mi solicitud realizada para conocer si fue aprobada o no.


Escenario 1: "Recepción de respuesta sobre solicitud"
Dado que el usuario inversionista ha realizado una solicitud,
cuando la solicitud ha sido procesada y se ha tomado una decisión de aceptarla o no,
entonces se envía una notificación al usuario informándole sobre el resultado de su solicitud.

Escenario 2: "Falta de respuesta sobre solicitud"
Dado que el usuario inversionista que ha realizado una solicitud,
cuando la solicitud ha sido procesada y se ha tomado una decisión de aceptarla o no,
entonces no se envía una respuesta a pesar de haberse decidido.

US18: Creación de queja
Como usuario, quiero realizar quejas para expresarme sobre mi molestia por cualquier motivo


Escenario 1: "Presentación de queja"
Dado que el usuario ingresa a la zona de quejas,
cuando presenta una queja,
entonces se registra la queja y notifica al equipo responsable para atenderlo.

Escenario 2: "Problemas al presentar la queja"
Dado que el usuario ingresa a la zona de quejas,
cuando presenta una queja,
entonces se no registra la queja.

US19: Visualización de datos recibidos
Como usuario inversionista, quiero visualizar los archivos recibidos para acceder a los datos que contienen.


Escenario 1: "Visualización de datos recibidos"
Dado que el usuario inversionista tiene los archivos de datos,
Cuando accede a la sección designada de la aplicación para visualizar los archivos de datos,
Entonces se abre un visualizador para el formato del archivo correspondiente.

Escenario 2: “Error al abrir archivo"
Dado que el usuario inversionista tiene los archivos de datos,
Cuando accede a la sección designada de la aplicación para visualizar los archivos de datos,
Entonces aparece un mensaje de error que menciona que no se pudo abrir el archivo. 

US20: Cierre de solicitud
Como usuario inversionista, quiero visualizar los datos obtenidos hasta cerrar y marcar como completada la solicitud para tener el tiempo necesario con los datos sin comprometer a la empresa a la cual solicité.


Escenario 1: “Confirmación de cierre de solicitud"
Dado que el usuario inversionista ha terminado su uso con los datos de la empresa,
Cuando decide cerrar la solicitud,
Entonces los datos y archivos se borran y no puede volver a visualizarlos.

Escenario 2: "Error al cerrar la solicitud"
Dado que el usuario inversionista ha terminado su uso con los datos de la empresa,
Cuando decide cerrar la solicitud,
Entonces aparece un mensaje de error que menciona que no se pudo cerrar la solicitud.

Escenario 3: "Error al eliminar datos"
Dado que el usuario inversionista ha terminado su uso con los datos de la empresa,
Cuando decide cerrar la solicitud,
Entonces se marca como cerrada pero no desaparecen los datos.

US21: Recepción de solicitud
Como usuario inversionista, quiero recibir los datos solicitados para verificar que sean los correctos y trabajar con ellos.


Escenario 1: “Entrega de solicitud"
Dado que el usuario inversionista ha realizado una solicitud y ha sido aprobada,
Cuando accede a la sección designada en la aplicación para ver sus solicitudes,
Entonces accede a los documentos que se hayan enviado.

Escenario 2: “Error de acceso a la entrega de solicitud"
Dado que el usuario inversionista ha realizado una solicitud y ha sido aprobada,
Cuando accede a la sección designada en la aplicación para ver sus solicitudes,
Entonces sale un error que menciona que la entrega no se puede abrir.
Escenario 3: “Entrega vacía"
Dado que el usuario inversionista ha realizado una solicitud y ha sido aprobada,
Cuando accede a la sección designada en la aplicación para ver sus solicitudes,
Entonces encuentra que la entrega se encuentra vacía.

US22: Cifrado de datos
Como usuario contador financiero, quiero la presencia de un sistema de cifrado de datos para garantizar la confidencialidad de la compañía que represento.


Escenario 1: "Entrega segura con cifrado"
Dado que el usuario contador financiero desea entregar los datos solicitados,
cuando procede con la entrega de los datos a través del canal designado por la aplicación,
entonces se entregan los datos con un método de cifrado.

Escenario 2: “Error de cifrado"
Dado que el usuario contador financiero desea entregar los datos solicitados,
cuando procede con la entrega de los datos a través del canal designado por la aplicación,
entonces aparece un error mencionando que no se pudo realizar el cifrado de datos.

Escenario 3: “Error de cifrado"
Dado que el usuario contador financiero desea entregar los datos solicitados,
cuando procede con la entrega de los datos a través del canal designado por la aplicación,
entonces se envían los datos sin el cifrado sin que el contador se entere.

US23: Confidencialidad de la entrega
Como usuario contador financiero, quiero que no se permita descargar ni tomar captura de pantalla de los datos compartidos para mantener la confidencialidad de la empresa.


Escenario 1: "Restricción de descarga de datos"
Dado que el usuario contador financiero desea mantener la confidencialidad de los datos compartidos,
Cuando envía los archivos solicitados por algún usuario inversor
Entonces se implementa medidas de seguridad que impiden la descarga de los archivos abiertos.

Escenario 2: "Restricción de captura de pantalla"
Dado que el usuario contador financiero desea mantener la confidencialidad de los datos compartidos,
Cuando envía los archivos solicitados por algún usuario inversor
Entonces se implementa medidas de seguridad que impiden la captura de pantalla de los archivos abiertos.

Escenario 3: “Error de descarga no restringida"
Dado que el usuario contador financiero desea mantener la confidencialidad de los datos compartidos,
Cuando envía los archivos solicitados por algún usuario inversor
Entonces no se implementan medidas de seguridad que impidan la descarga de los archivos abiertos.

Escenario 4: “Error de captura de pantalla habilitada"
Dado que el usuario contador financiero desea mantener la confidencialidad de los datos compartidos,
Cuando envía los archivos solicitados por algún usuario inversor
Entonces no se implementan medidas de seguridad que impidan la captura de pantalla de los archivos abiertos.

US24: Alertas de fugas de seguridad
Como usuario contador financiero, quiero recibir alertas de violaciones de seguridad para informar a la empresa sobre el problema.


Escenario 1: "Recepción de alerta de violación de seguridad"
Dado que el usuario contador financiero desea estar al tanto de posibles violaciones de seguridad,
cuando se detecta una actividad sospechosa o una violación de seguridad en la aplicación,
entonces se envía una alerta inmediata al usuario contador financiero, notificándole sobre el problema y proporcionando detalles pertinentes para que pueda informar rápidamente a la empresa y tomar las medidas necesarias para abordar la situación.

Escenario 2: "Falta de alertas de violaciones de seguridad"
Dado que el usuario contador financiero desea estar al tanto de posibles violaciones de seguridad,
cuando ocurre una violación de seguridad, pero se no envía ninguna alerta al usuario,
entonces no es consciente del incidente y la empresa puede no ser informada oportunamente, lo que aumenta el riesgo de daños adicionales o pérdida de datos.

US25: Visualización de analisis financieros disponibles
Como usuario inversionista, quiero disponer de una gama de análisis financieros para realizar el proceso de Due Diligence sin problemas.


Escenario 1: “Analisis financieros"
Dado que el usuario inversionista desea utilizar los análisis financieros disponibles,
cuando accede a la sección correspondiente en la aplicación,
entonces se muestra una lista completa de los análisis financieros disponibles.

Escenario 2: “Error al mostrar analisis financieros"
Dado que el usuario inversionista desea revisar los análisis financieros disponibles,
cuando accede a la sección correspondiente en la aplicación,
entonces no se muestra ningún analisis financiero.

Escenario 3: “Error al seleccionar analisis financiero"
Dado que el usuario inversionista desea seleccionar algún análisis financiero disponible,
cuando intenta ingresar a alguno de los disponibles
entonces aparece un mensaje de error que menciona que no se puede ingresar al analisis seleccionado.


US26: Eficacia de los algoritmos de análisis financiero
Como usuario inversionista, quiero realizar cualquier análisis financiero disponible de manera rápida y sencilla para agilizar el proceso de evaluación.


Escenario 1: “Eficacia de analisis financiero"
Dado que el usuario inversionista desea realizar un análisis financiero,
cuando accede a la herramienta de análisis financiero disponible en la aplicación,
entonces se ejecuta de acuerdo con las expectativas sin demorarse ni dar resultados erróneos.

Escenario 2: "Problemas de eficacia en la herramienta de análisis financiero"
Dado que el usuario inversionista desea realizar un análisis financiero,
cuando intenta utilizar la herramienta de análisis financiero
entonces se ejecuta con problemas tardándose y dando resultados erróneos.

Escenario 3: “Error de ejecución "
Dado que el usuario inversionista desea realizar un análisis financiero,
cuando intenta utilizar la herramienta de análisis financiero
entonces no se ejecuta y da error.

US27: Informe de análisis financiero
Como usuario inversionista, quiero recibir un informe en base a los análisis que se realizaron para tener una segunda opinión o utilizarlo como un informe final.


Escenario 1: "Veredicto claro y fundamentado"
Dado que el usuario inversionista ha realizado análisis utilizando la aplicación,
cuando finaliza los análisis financieros,
entonces se proporciona un veredicto claro y fundamentado basado en los resultados de los análisis.

Escenario 2: "Falta de veredicto o información insuficiente"
Dado que el usuario inversionista ha realizado análisis utilizando la aplicación,
cuando finaliza los análisis financieros,
entonces se entrega un informe con información vaga y sin sentido.

Escenario 3: “Error al generar el informe"
Dado que el usuario inversionista ha realizado análisis utilizando la aplicación,
cuando finaliza los análisis financieros,
entonces produce un error y no se genera ningún informe.

US28: RESTful API – Registro de usuario
Como desarrollador, quiero implementar un endpoint de registro de usuario para permitir que los usuarios se registren en la aplicación mediante la API RESTful.


Escenario 1: "Registro exitoso"
Dado que el usuario que desea registrarse en la aplicación a través de la API RESTful,
cuando envía una solicitud de registro con la información requerida al endpoint correspondiente,
entonces se procesa la solicitud y se crea la cuenta 

Escenario 2: "Fallo en el registro"
Dado que el usuario que intenta registrarse en la aplicación a través de la API RESTful,
cuando envía una solicitud de registro al endpoint correspondiente, entonces no se registra la solicitud y regresa un mensaje de error.

US29: RESTful API – Inicio de sesión de usuario
Como desarrollador, quiero implementar un endpoint de inicio de sesión para permitir que los usuarios accedan a sus cuentas mediante la API RESTful.

Escenario 1: "Inicio de sesión exitoso"
Dado que el usuario que desea iniciar,
cuando envía una solicitud de inicio de sesión con las credenciales al endpoint correspondiente,
entonces se autentica al usuario, genera un token de acceso válido y devuelve una respuesta junto con el token de acceso para la sesión.

Escenario 2: "Fallo en el inicio de sesión"
Dado que el usuario que intenta iniciar sesión en la aplicación a través de la API RESTful,
cuando envía una solicitud de inicio de sesión al endpoint correspondiente con credenciales incorrectas
entonces se devuelve un mensaje de error indicando que el inicio de sesión ha fallado.

US30: Autenticación basada en token JWT
Como desarrollador, quiero implementar la funcionalidad de autenticación basada en el token JWT para mejorar la seguridad de la API.


Escenario 1: "Generación de token JWT"
Dado que el usuario autenticado desea acceder a recursos protegidos en la API RESTful,
cuando se valida las credenciales,
entonces se genera un token JWT válido que contiene la información de autenticación y tiene una fecha de expiración adecuada.
Escenario 2: "Token JWT inválido"
Dado que el usuario que intenta acceder a recursos protegidos en la API RESTful,
cuando incluye un token JWT inválido en el encabezado de autorización de la solicitud,
entonces se rechaza la solicitud indicando que la autenticación ha fallado.


US31: Recuperación de contraseña
Como desarrollador, quiero implementar un endpoint de recuperación de contraseña para permitir que los usuarios restablezcan sus contraseñas mediante la API RESTful.


Escenario 1: "Solicitud de restablecimiento de contraseña"
Dado que el usuario olvidó su contraseña y desea restablecerla,
cuando envía una solicitud POST al endpoint de recuperación de contraseña con su dirección de correo electrónico registrada,
entonces se verifica la existencia del correo electrónico en la base de datos, genera un token de restablecimiento de contraseña único asociado a la cuenta y lo envía al correo asociado de la cuenta.

Escenario 2: “Error en solicitud de restablecimiento de contraseña"
Dado que el usuario olvidó su contraseña y desea restablecerla,
cuando envía una solicitud POST al endpoint de recuperación de contraseña con su dirección de correo electrónico registrada,
entonces se verifica la existencia del correo electrónico en la base de datos, pero no obtiene respuesta.

US32: CRUD para recursos principales
Como desarrollador, quiero implementar endpoint CRUD para la gestión de recursos principales de la aplicación.


Escenario 1: "Creación de recursos"
Dado que el usuario que desea crear un nuevo recurso en la aplicación,
cuando envía una solicitud POST al endpoint correspondiente con los datos del nuevo recurso,
entonces se procesa la solicitud y crea el recurso en la base de datos.

Escenario 2: “Error en la creación de recursos"
Dado que el usuario que desea crear un nuevo recurso en la aplicación,
cuando envía una solicitud POST al endpoint correspondiente con los datos del nuevo recurso,
entonces no se crea el recurso solicitado.

Escenario 3: “Eliminación de recursos"
Dado que el usuario que desea eliminar un nuevo recurso en la aplicación,
cuando envía una solicitud POST al endpoint correspondiente con los datos del recurso,
entonces se procesa la solicitud y elimina el recurso en la base de datos.

Escenario 4: “Error en la eliminación de recursos"
Dado que el usuario que desea crear un nuevo recurso en la aplicación,
cuando envía una solicitud POST al endpoint correspondiente con los datos del nuevo recurso,
entonces no se elimina el recurso solicitado.

US33: Landing page organizada

Como visitante de la landing page, quiero encontrar una navegación intuitiva que me permita acceder fácilmente a la información para informarme sobre sus características.

Escenario 1: "Organización correcta e intuitiva"
Dado que el visitante se encuentra en la landing page,
cuando accedo a la página principal,
entonces encuentro todas las funcionalidades y servicios que ofrece sin problemas.

Escenario 2: "Organización no intuitiva"
Dado que el visitante se encuentra en la landing page,
cuando accedo a la página principal no entiendo nada.
entonces me siento frustrado y es menos probable que continúe explorando la página o considere utilizar la aplicación.

US34: Contenido de la landing page

Como visitante de la landing page, quiero encontrar contenido detallado y fácil de entender sobre las funcionalidades y beneficios de la aplicación para tomar una decisión informada sobre su uso.

Escenario 1: "Contenido claro"
Dado que el visitante se encuentra en la landing page,
cuando navega por la landing page
entonces encuentra contenido detallado y fácil de entender que describe claramente las funcionalidades y beneficios de la aplicación.

Escenario 2: "Contenido confuso o insuficiente"
Dado que el visitante se encuentra en la landing page,
cuando navega por la landing page,
entonces no encuentra información relevante o suficiente.

US35: Landing page - Compatibilidad móvil
Como visitante de la landing page, quiero que sea responsiva para utilizarla en cualquier dispositivo.


Escenario 1: "Compatibilidad con
dispositivos móviles"
Dado que el visitante se encuentra en la landing page,
cuando visita la landing page de la aplicación desde su dispositivo móvil,
entonces navega la landing page sin problemas.

Escenario 2: "Problemas de visualización o navegación"
Dado que el visitante se encuentra en la landing page,
cuando visita la landing page de la aplicación desde su dispositivo móvil, 
entonces encuentra problemas de visualización o navegación.

US36: Landing page - Formulario de contacto
Como visitante de la landing page, quiero encontrar un formulario de contacto en la landing page para poder comunicarme con el equipo de la aplicación.


Escenario 1: "Acceso al formulario de contacto"
Dado que el visitante se encuentra en la landing page,
cuando quiera contactarse con el equipo de la aplicación,
entonces encuentra un formulario de contacto.

Escenario 2: "Falta de formulario de contacto"
Dado que el visitante se encuentra en la landing page,
cuando quiera contactarse con el equipo de la aplicación,
entonces no encuentra un formulario de contacto o cualquier medio claro para comunicarme con el equipo de la aplicación.

US37: Landing page - Contenido multimedia

Como visitante de la landing page, quiero encontrar contenido multimedia para obtener más información.


Escenario 1: "Contenido multimedia disponible"
Dado que el visitante se encuentra en la landing page,
cuando navega por la página,
entonces encuentra contenido multimedia que ilustran las características y beneficios de la aplicación.

Escenario 2: "Falta de contenido multimedia"
Dado que el visitante se encuentra en la landing page,
cuando navega por la página,
entonces no encuentra ningún contenido multimedia.

US38: Landing page - Call-to-action

Como visitante de la landing page, quiero encontrar call-to-action´s para solicitar una demo.


Escenario 1: "call-to-action presente"
Dado que el visitante se encuentra en la landing page,
cuando quiera descargar la demo de la aplicación,
entonces encuentra el call-to-action  visible.

Escenario 2: "Falta de call-to-action´s"
Dado que el visitante se encuentra en la landing page,
cuando quiera descargar la demo de la aplicación,
entonces no encuentra ningun call-to-action.

US39: Landing page - menú superior 

Como visitante de la landing page, quiero un menú superior, para desplazarme rápidamente a través de la landing page.


Escenario 1: “Menú superior”
Dado que el visitante se encuentra en la landing page.
Cuando quiere visitar otros segmentos de la página y utiliza el menú superior.
Entonces se desplaza a otros segmentos.

Escenario 2: “Error de vinculo menú superior”
Dado que el visitante se encuentra en la landing page.
Cuando quiere visitar otros segmentos de la página y utiliza el menú superior.
Entonces no ocurre nada.

Escenario 3: “Vinculo equivocado en menú superior”
Dado que el visitante se encuentra en la landing page.
Cuando quiere visitar otros segmentos de la página y utiliza el menú superior.
Entonces lo lleva a un segmento incorrecto.

US40: Ingresar proyecto

Como usuario, quiero ingresar a los proyectos creados para acceder a su contenido.

Escenario 1: “Ingreso de proyecto”
Dado que el usuario selecciona un proyecto existente.
Cuando intenta ingresar a su contenido.
Entonces ingresa al proyecto.

Escenario 2: “Error en ingreso”
Dado que el usuario selecciona un proyecto existente.
Cuando intenta ingresar a su contenido.
Entonces un error impide que ingrese al proyecto.


US41: Explorar information ítems

Como usuario, quiero visualizar los information ítems que contengan los proyectos para ingresar a su contenido.

Escenario 1: “Visualizar information item”
Dado que el usuario ingresa a un proyecto.
Cuando quiere visualizar los information item que contiene el proyecto.
Entonces se cargan y los puede vizualizar.

Escenario 1: “Error de carga de information item”
Dado que el usuario ingresa a un proyecto.
Cuando quiere visualizar los information item que contiene el proyecto.
Entonces se produce un error de carga y no logra ver los information items.

Escenario 3: “Proyecto vacío”
Dado que el usuario ingresa a un proyecto.
Cuando quiere visualizar los information item que contiene el proyecto.
Entonces no encuentra ningún information item debido a que no se ha creado ninguno aún.

US42: Crear documento en information item como Sell Side Agent
Como usuario contador financiero quiero crear documentos dentro de los information ítems para compartirlos con el Buy Side.

Escenario 1: “Creación de documento”
Dado que el usuario contador financiero crea un documento en el information item.
Cuando ingresa los inputs que corresponden.
Entonces se crea un documento.

Escenario 2: “Error en la creación de documento”
Dado que el usuario contador financiero crea un documento en el information item.
Cuando ingresa los inputs que corresponden.
Entonces se produce un error y no se crea un documento.


US43: Crear information item como Buy Side Agent
Como usuario inversionista quiero crear information ítems para compartirlos con el Sell Side.

Escenario 1: “Creación de information item”
Dado que el usuario inversionista crea un un information item.
Cuando ingresa los inputs que corresponden.
Entonces se crea el information item.

Escenario 2: “Error en la creación de information item”
Dado que el usuario inversionista crea un information item.
Cuando ingresa los inputs que corresponden.
Entonces se produce un error y no se crea el information item.


US44: Visualizar preguntas de proyecto
Como usuario, quiero visualizar las preguntas del proyecto para interactuar e ingresar a ellas.


Escenario 1: “Visualizar preguntas”
Dado que el usuario se encuentra en la zona de preguntas de proyecto.
Cuando quiere visualizar las preguntas que se encuentren.
Entonces aparecen las preguntas anteriormente realizadas.

Escenario 2: “Error de carga”
Dado que el usuario se encuentra en la zona de preguntas de proyecto.
Cuando quiere visualizar las preguntas que se encuentren.
Entonces aparece un mensaje de error de carga de datos.

Escenario 3: “Sin preguntas previas”
Dado que el usuario se encuentra en la zona de preguntas de proyecto.
Cuando quiere visualizar las preguntas que se encuentren.
Entonces no aparece ninguna pregunta pues no se han creado aún.




US45: Crear pregunta como Buy Side Agent
Como usuario inversor, quiero crear preguntas para intercambiar dudas con el Sell Side.

Escenario 1: “Creación de pregunta”
Dado que el usuario inversor crea una nueva pregunta.
Cuando ingresa todos los inputs requeridos.
Entonces se sube su pregunta.

Escenario 2: “Error en la creación de pregunta”
Dado que el usuario inversor crea una nueva pregunta.
Cuando ingresa todos los inputs requeridos.
Entonces ocurre un error y no se sube la pregunta.

Escenario 3: “Pregunta vacía”
Dado que el usuario inversor crea una nueva pregunta.
Cuando ingresa todos los inputs requeridos, pero no pone ningún contenido.
Entonces se le pide ingresar una cantidad de texto mínimo en la pregunta.



US46: Crear respuesta como Sell Side Agent
Como usuario contador financiero, quiero responder a las preguntas recibidas por el lado Buy Side para resolver cualquiera de sus dudas.

Escenario 1: “Creación de respuesta”
Dado que el usuario contador financiero responde una nueva pregunta.
Cuando ingresa todos los inputs requeridos.
Entonces se sube su respuesta

Escenario 2: “Error en la creación de respuesta”
Dado que el usuario contador financiero responde una nueva pregunta.
Cuando ingresa todos los inputs requeridos.
Entonces ocurre un error y no se sube la respuesta.

Escenario 3: “Respuesta vacía”
Dado que el usuario contador financiero responde una nueva pregunta.
Cuando ingresa todos los inputs requeridos, pero no pone ningún contenido.
Entonces se le pide ingresar una cantidad de texto mínimo en la pregunta.

## *Impact Mapping*

El impact map es una herramienta estratégica que permite identificar de manera precisa las características de una aplicación que pueden ser utilizadas o mejoradas para cumplir con un objetivo empresarial específico. Al partir del objetivo clave, se desglosan los comportamientos necesarios de los usuarios, se definen las acciones que deben realizar en la aplicación, se identifican las características necesarias para habilitar esas acciones, se evalúa el impacto potencial de cada característica en el logro del objetivo, y finalmente se crea un plan de acción detallado que guía el desarrollo y mejora continua de la aplicación, alineando así las acciones de los usuarios con los objetivos estratégicos de la empresa.

![Artefacto creado en UXPressia](src/img/cap3/impact-map.png)

## *Product Backlog*

![](src/img/cap3/productbacklog1.png)

![](src/img/cap3/productbacklog2.png)

![](src/img/cap3/productbacklog3.png)

![](src/img/cap3/productbacklog4.png)

![](src/img/cap3/productbacklog5.png)

![](src/img/cap3/productbacklog6.png)

![](src/img/cap3/productbacklog7.png)

![](src/img/cap3/productbacklog8.png)

![](src/img/cap3/productbacklog9.png)

![](src/img/cap3/productbacklog10.png)

![](src/img/cap3/productbacklog11.png)

![](src/img/cap3/productbacklog12.png)

![](src/img/cap3/productbacklog13.png)

![](src/img/cap3/productbacklog14.png)

![](src/img/cap3/productbacklog15.png)

![](src/img/cap3/productbacklog16.png)

![](src/img/cap3/productbacklog17.png)

![](src/img/cap3/productbacklog18.png)

![](src/img/cap3/productbacklog19.png)

![](src/img/cap3/productbacklog20.png)

![](src/img/cap3/productbacklog21.png)

![](src/img/cap3/productbacklog22.png)

![](src/img/cap3/productbacklog23.png)

# Capítulo IV: *Product Design*

## *Style Guidelines*

### *General Style Guidelines*

Es fundamental considerar las decisiones y elementos visuales que respaldan los principios generales de diseño para *DiligenceTech*. Por esta razón, resulta esencial definir aspectos clave como la identidad de marca, la paleta de colores y la tipografía. Además, es necesario establecer el tono de comunicación y el lenguaje utilizado, que abarcan características como divertido o serio, formal o casual, respetuoso o irreverente, y entusiasta o sereno.

**Branding:** 

*DiligenceTech* encarna la eficiencia, la confianza y la innovación en el campo de la debida diligencia en línea. Nuestra esencia se basa en proporcionar soluciones tecnológicas avanzadas que simplifican y agilizan el proceso de análisis de datos financieros de empresas para transacciones comerciales. Nuestra marca es sinónimo de precisión, seguridad y resultados confiables en un mundo impulsado por la tecnología.

**Logotipo:**

El logo de *DiligenceTech* refleja la esencia de la marca como una empresa innovadora y confiable en el campo de la debida diligencia en línea. Con una combinación de colores vibrantes y un diseño moderno, el logo representa la eficiencia, elegancia, la precisión y la tecnología avanzada que caracterizan a *DiligenceTech*.

![Imagen creada en Figma](src/img/Logo/diligencetech-logo.png)

**Colores:**

Se ha utilizado los naranja y negro como colores principales para el diseño de nuestro producto.

**Naranja (#FFA500):** El color naranja se utiliza como color principal del logo, aportando vitalidad, energía y optimismo. Representa la creatividad y la innovación que caracterizan a *DiligenceTech* en su enfoque hacia soluciones tecnológicas avanzadas.

![Imagen extraída de Figma](src/img/cap4/color-naranja.png)

**Negro (#000000):** El negro se emplea como color secundario, brindando elegancia, sofisticación y profesionalismo al logo. Se combina con el naranja para crear un contraste visual efectivo y destacar la modernidad de la marca.

![Imagen extraída de Figma](src/img/cap4/color-negro.png)

**Tipografía:**

La tipografía utilizada para *DiligenceTech* es moderna y legible, con líneas limpias y claras. Se ha elegido una fuente que refleje la tecnología y la seriedad de la marca, mientras mantiene un aspecto actual y contemporáneo.

![Imagen extraída de Figma](src/img/cap4/tipografia.jpg)

![Imagen extraída de Figma](src/img/cap4/montserrat-typography.png)

**Tonos de Comunicación:**

* **Formal/Confianza:** En *DiligenceTech* adoptamos un enfoque formal que refleja nuestra seriedad en la seguridad de los datos, sin embargo, mantenemos un toque de accesibilidad y cercanía en nuestra comunicación con los usuarios.

* **Respetuoso/Irreverente:** Nos caracterizamos por ser siempre respetuosos y considerados en nuestra comunicación, mostrando empatía hacia las necesidades y preocupaciones de nuestros usuarios.

* **Entusiasta/Sereno:** En *DiligenceTech* transmitimos entusiasmo al ofrecer soluciones innovadoras, al mismo tiempo que mantenemos un tono sereno para transmitir confianza y estabilidad en la gestión de datos.

### *Web Style Guidelines*

**Fuentes:**
Se hizo uso de la fuente Monserrat con variantes en el tamaño:

Para el *Heading* se usó: 

![](src/img/cap4/Heading.png)

![](src/img/cap4/Heading1.png)

![](src/img/cap4/Heading2.png)

![](src/img/cap4/Heading3.png)

![](src/img/cap4/Heading4.png)

Para el *Title* se usó: 

![](src/img/cap4/Title.png)

![](src/img/cap4/Title1.png)

![](src/img/cap4/Title2.png)

Para el *Body* se usó: 

![](src/img/cap4/Body.png)

![](src/img/cap4/Body1.png)

![](src/img/cap4/Body2.png)

**Colores:**

![Imagen creada en Figma](src/img/cap4/colors-orange.png)

![Imagen creada en Figma](src/img/cap4/colors-black.png)

Los colores principales para el diseño web y Mobile son utilizados para lo siguiente: el negro es empleado para el fondo, el naranja es aplicado para los botones. Además, el color de los títulos y textos son de color negro y blanco.

**Gráficos:**

* Logo de la aplicación 
* Funcionalidades esenciales
* Imágenes de características
* Imágenes de los planes 
* Iconos de redes sociales

**Componentes:**

* Botones  
* Deslizador Desplegables 
* Campos de texto 
* Cuadro de Planes 
* Botón de redes sociales 

## *Information Architecture*

### *Organization Systems*

Los usuarios podrán percibir la interfaz de forma lógica e intuitiva gracias a la estructura organizativa prevista para DiligenceTech.

![](src/img/cap4/organization.png)

### *Labeling Systems*

El conjunto de información *DiligenceTech* será representado por el sistema mediante las siguientes etiquetas.

![](src/img/cap4/labeling.png)

### *SEO Tags and Meta Tags*

A continuación, presentaremos las etiquetas que erpresentarán el contenido persentado en nuestra *web application* como en nuestra *landing page*. Con esto, se podrá encontrar *DiligenceTech* rápidamente en cualquier navegador.

Para la *landing page*:
* ***Title:*** *DiligenceTech | Revolutionize your Due Diligece*.
* ***Description:*** *DiligenceTech - DeltaTech Official Landing Page*.
* ***keywords:*** *Finances, investments, companies, due diligence*.
* ***Author:*** *DeltaTech*
* ***Canonical:*** *https://diligencetech.com/*

Para la *web application*:
* ***Title:*** *DiligenceTech | Revolutionize your Due Diligence*.
* ***Description:*** *DiligenceTech - DeltaTech Official Web Application*.
* ***keywords:*** *Finances, investments, companies, due diligence*.
* ***Author:*** *DeltaTech*
* ***Canonical:*** *https://diligencetech.app.io/*

### *Searching Systems*

Este sistema de búsqueda agilizará el tiempo con el objetivo de ofrecer una mejor experiencia para *DiligenceTech*.

![](src/img/cap4/searching.png)

### *Navigation Systems*

Los procedimientos técnicos permitirán a los usuarios de " DiligenceTech " elegir cualquier detalle que deseen sobre un producto o aplicación en una ventana web.

![](src/img/cap4/navigation.png)

## *Landing Page UI Design*

### *Landing Page Wireframe*

::: note
Para acceder a los Wireframe creados por el equipo, haga click en la URL: https://lc.cx/ATxkeR
:::

![Hero wireframe, Imagen creada en Figma](src/img/cap4/wireframes/header-wireframe.png)

![About Us wireframe, Imagen creada en Figma](src/img/cap4/wireframes/about-us-wireframe.png)

![Essential Features wireframe, Imagen creada en Figma](src/img/cap4/wireframes/essential-feature-wireframe.png)

![Plans wireframe, Imagen creada en Figma](src/img/cap4/wireframes/plans-wireframe.png)

![Why Us wireframe, Imagen creada en Figma](src/img/cap4/wireframes/why-us-wireframe.png)

![Features wireframe, Imagen creada en Figma](src/img/cap4/wireframes/features-wireframe.png)

![FAQS wireframe, Imagen creada en Figma](src/img/cap4/wireframes/faqs-wireframe.png)

![Request Demo wireframe, Imagen creada en Figma](src/img/cap4/wireframes/reques-demo-wireframe.png)

![Footer wireframe, Imagen creada en Figma](src/img/cap4/wireframes/footer-wireframe.png)

### *Landing Page Mock-up*

::: note
Para acceder a los Mock-up creados por el equipo, haga click en la URL: https://lc.cx/ATxkeR
:::

![Design Mock-up](src/img/cap4/mockups/design-mockup1.png)

![Design Mock-up](src/img/cap4/mockups/design-mockup2.png)

***Mock-ups concept:***

![Mock-up concept](src/img/cap4/mockups/mockup1.png)

![Mock-up concept](src/img/cap4/mockups/mockup2.png)

![Mock-up concept](src/img/cap4/mockups/mockup3.png)

![Mock-up concept](src/img/cap4/mockups/mockup4.png)

## *Web Applications UX/UI Design*

### *Web Applications Wireframes*

::: note
Para acceder a los wireframes creados por el equipo, haga click en la URL: https://lc.cx/zYHzk4
:::

**Inicio de sesión:**

![Login wireframe, imagen creada en Figma](src/img/cap4/wireframes/wa-login-wireframe.png)

**Registro de cuenta:**

![Signup wireframe, imagen creada en Figma](src/img/cap4/wireframes/wa-signup-wireframe.png)

**Pantalla de inicio:**

![Home wireframe, imagen creada en Figma](src/img/cap4/wireframes/wa-main-wireframe.png)

**Herraminetas de la** ***Web Application***

**Proyecto solicitado:**

![Requested projects wireframe, imagen creada en Figma](src/img/cap4/wireframes/wa-request-wireframe.png)

**Filtro de información:**

![Filter wireframe, imagen creada en Figma](src/img/cap4/wireframes/wa-filter-wireframe.png)

**Generación de pregunta:**

![Question wireframe, imagen creada en Figma](src/img/cap4/wireframes/wa-questions-wireframe.png)

### *Web Applications Wireflow Diagrams*

* **Inicio de sesión, registro y cambio de contraseña (Para ambos segmentos):**

![Wireflow 1, imagen creada en Figma](src/img/cap4/wireflows/wireflow1.png)

**Descripción:** Cualquiera de nuestros usuarios inicia sesión, sino tiene cuenta se registra, o tambien puede cambiar su contraseña en caso lo requiera. Si es inversor o no lo dirigirá a la pantalla de su segmento.

* **Herramientas principales:**

![Wireflow 2, imagen creada en Figma](src/img/cap4/wireflows/wireflow2.png)

**Descripción:** En la página de inicio se podrá ver los proyectos solicitados con toda su información. Así también los segmentos pueden usar la opción de configuración para configurar la aplicación,y por último, “reportar” para reportar fallos entre otros.

* **Visualizar proyecto y cambiar el estado de** ***sell side*** **de un ítem:**

![Wireflow 3, imagen creada en Figma](src/img/cap4/wireflows/wireflow3.png)

**Descripción:** El contador podrá elegir un proyecto y entrar a un item y cambiar el estado de *sell side*, luego podrá remover o confirmar cambios.

* **Responder preguntas de** ***Q&A*** **del inversor:**

![Wireflow 4, imagen creada en Figma](src/img/cap4/wireflows/wireflow4.png)

**Descripción:**  El contador podrá acceder al Q & A de un proyecto y podrá responder las preguntas dadas por el inversor , también cambia el estado del equipo a “HECHO” y confirma y con posibilidad de remover lo respondido.

* **Insertar documentos en los ítems:**

![Wireflow 5, imagen creada en Figma](src/img/cap4/wireflows/wireflow5.png)

**Descripción:** El contador podrá desde el apartado de insertar documentos desde su explorador de archivos y tendrá una pantalla de confirmación exitosa.

**Wireflows específicos para el segmento del Inversor**

* **Crear un nuevo proyecto para** ***buy side*** **y** ***sell side:***

![Wireflow 6, imagen creada en Figma](src/img/cap4/wireflows/wireflow6.png)

**Descripción:**  El inversor podrá crear un nuevo de proyecto de  bull side y sell side asignando un nombre de equipo, agregar a cada team  los miembros involucrados por correo y pulsa “agregar”.

* **Seleccionar un proyecto y cambiar el estado** ***buy side:***

![Wireflow 7, imagen creada en Figma](src/img/cap4/wireflows/wireflow7.png)

**Descripción:** El inversor podrá ingresar a un proyecto y seleccionar un item , por ende mostrará los documentos contenidos en ese ítem y podrá cambiar el estado de Buy side de “pendiente” a “hecho”

* **Añadir un nuevo ítem a un proyecto:**

![Wireflow 8, imagen creada en Figma](src/img/cap4/wireflows/wireflow8.png)

**Descripción:** El inversor podrá añadir un nuevo item en un proyecto elegido ingresando el lugar de alojo o  un  posible  sub-item , añadiendo descripción y tipo de prioridad. Luego le dará una confirmación exitosa y  podrá agregar contenido en este ítem como su descripción.

* **Crear preguntas en** ***Q&A:***

![Wireflow 9, imagen creada en Figma](src/img/cap4/wireflows/wireflow9.png)

**Descripción:** El inversor podrá crear una pregunta ingresando el área  de proyecto y su item . Escribira una pregunta y dara en “agregar pregunta”, luego recibirá un mensaje de confirmación exitoso.

* **Insertar lote:**

![Wireflow 10, imagen creada en Figma](src/img/cap4/wireflows/wireflow10.png)

**Descripción:** El inversor podrá insertar un nuevo lote en un proyecto , recibirá el mensaje confirmacion y finalmente podrá añadir contenido en el lote.

**Filtración de información y de documentos:**

![Wireflow 11, imagen creada en Figma](src/img/cap4/wireflows/wireflow11.png)

**Descripción:** Ambos segmentos podrán usar el filtrado para búsqueda ya sea fecha de creación, estado, cantidad de documentos,etc.

### *Web Applications Mock-ups*

::: note
Para acceder a los Mock-ups creados por el equipo, haga click en la URL: https://lc.cx/zYHzk4
:::

![Login Mock-up](src/img/cap4/mockups/wa-Login-mockup.png)

![Register Mock-up](src/img/cap4/mockups/wa-register-mockup.png)

![Home Mock-up](src/img/cap4/mockups/wa-main-mockup.png)

![Requested Projects Mock-up](src/img/cap4/mockups/wa-requested-mockup.png)

![Barch Insertion Mock-up](src/img/cap4/mockups/wa-barch-mockup.png)

***Mock-ups concept:***

![Mock-up concept](src/img/cap4/mockups/login-mockup.png)

![Mock-up concept](src/img/cap4/mockups/register-mockup.png)

![Mock-up concept](src/img/cap4/mockups/home-mockup.png)

![Mock-up concept](src/img/cap4/mockups/barch-mockup.png)

![Mock-up concept](src/img/cap4/mockups/requested-mockup.png)

### *Web Applications User Flow Diagrams*

* **Inicio de sesión, registro y cambio de contraseña:**

![Wireflow 1, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow1.png)

**Descripción:** El segmento inicia sesión, sino tiene cuenta se registra, o también cambia su contraseña.si es inversor o no lo dirigirá a la pantalla de su segmento.

* **Herramientas Principales:**

![Wireflow 2, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow2.png)

**Descripción:** En la página de inicio se podrá ver los proyectos solicitados con toda su información. Así también los segmentos pueden usar la opción de configuración para configurar la aplicación,y por último, “reportar” para reportar fallos entre otros.

* **Visualizar proyecto y cambiar el estado de** ***sell side*** **de un ítem:**

![Wireflow 3, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow3.png)

**Descripción:** El contador podra elegir un proyecto y entrar a un item y cambiar el estado de sell side, luego podrá remover o confirmar cambios.

* **Responder preguntas de** ***Q&A*** **del inversor:**

![Wireflow 4, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow4.png)

**Descripción:**  El contador podrá acceder al Q & A de un proyecto y podrá responder las preguntas dadas por el inversor , también cambia el estado del equipo a “HECHO” y confirma y con posibilidad de remover lo respondido.

* **Insertar documentos en los ítems:**

![Wireflow 5, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow5.png)

**Descripción:** El contador podrá desde el apartado de insertar documentos desde su explorador de archivos y tendrá una pantalla de confirmación exitosa.

***Wireflows*** **enfocados en el segmento de Inversor:**

* **Crear un nuevo proyecto para** ***buy side*** **y** ***sell side:***

![Wireflow 6, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow6.png)

**Descripción:**  El inversor podrá crear un nuevo de proyecto de  bull side y sell side asignando un nombre de equipo, agregar a cada team  los miembros involucrados por correo y pulsa “agregar”.

* **Seleccionar proyecto y cambiar el estado** ***buy side:***

![Wireflow 7, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow7.png)

**Descripción:** El inversor podrá ingresar a un proyecto y seleccionar un item , por ende mostrará los documentos contenidos en ese ítem y podrá cambiar el estado de Buy side de “pendiente” a “hecho”

* **Añadir un nuevo ítem a un proyecto:**

![Wireflow 8, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow8.png)

**Descripción:** El inversor podrá añadir un nuevo item en un proyecto elegido ingresando el lugar de alojo o  un  posible  sub-item , añadiendo descripción y tipo de prioridad. Luego le dará una confirmación exitosa y  podrá agregar contenido en este ítem como su descripción.

* **Crear pregunta en** ***Q&A:***

![Wireflow 9, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow9.png)

**Descripción:** El inversor podrá crear una pregunta ingresando el área  de proyecto y su item . Escribira una pregunta y dara en “agregar pregunta”, luego recibirá un mensaje de confirmación exitoso.

* **Insertar lote:**

![Wireflow 10, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow10.png)

**Descripción:** El inversor podrá insertar un nuevo lote en un proyecto , recibirá el mensaje confirmacion y finalmente podrá añadir contenido en el lote.

**Filtración de información y documentos:**

![Wireflow 11, imagen creada en Figma](src/img/cap4/wireflows/wa-wireflow11.png)

**Descripción:** Ambos segmentos podrán usar el filtrado para búsqueda ya sea fecha de creación, estado, cantidad de documentos,etc.

## *Web Applications Prototyping*

![Video del prototipo de la Web Application](src/img/cap4/prototyping-figma-appsweb.png)

::: note
Para acceder y visualizar el contenido del video, haga click en la URL: https://lc.cx/o_VByz
:::

## *Domain-Driven Software Architecture*

### *Software Architecture Context Diagram*

![Context Diagram, elaboración hecha en Structurizr](src/img/cap4/ddd-diagrams/diagrama-contexto.png)

### *Software Architecture Container Diagrams*

![Container Diagram, elaboración hecha en Structurizr](src/img/cap4/ddd-diagrams/diagrama-contenedores.png)

### *Software Architecture Components Diagrams*

![Component Diagram, elaboración hecha en Structurizr](src/img/cap4/ddd-diagrams/diagrama-componentes.png)

## *Software Object-Oriented Design*

### *Class Diagrams*

Nuestro dominio es *(Sell-Side and Buy-Side)* *Due Diligence* y se divide en 4 *Bounded Contexts:*

1. ***Due Diligence Bounded Context:*** Centrado en los actores/usuarios de la solución y el estado general del proyecto de *Due Diligence* (*Due Diligence Project*).
2. ***Information Requirements Bounded Context:*** Centrado en los cambios de estado de Information Requirements de cada *Due Diligence Project*, su organización y los documentos que el *Sell-Side Agent* inserta en ellos.
3. ***QandA Bounded Context:*** Centrado en los cambios de estado de la evidencia de *QandA*.
4. ***Project Creation Bounded Context:*** Centrado en la transformación de un *Pending Project* a un proyecto manejable (*Due Diligence Project*).

* ***Due Diligence Bounded Context:***

![Class diagram Due Diligence, imagen creada en StartUML](src/img/cap4/ddd-diagrams/class-diagram-1.png)

* ***Information Requirements Bounded Context:***

![Class diagram Information Requirements, imagen creada en StartUML](src/img/cap4/ddd-diagrams/class-diagram-2.png)

* ***QandA Bounded Context:***

![Class diagram Q&A, imagen creada en StartUML](src/img/cap4/ddd-diagrams/class-diagram-3.png)

* ***Project Creation Bounded Context:***

![Class diagram Project Creation, imagen creada en StartUML](src/img/cap4/ddd-diagrams/class-diagram-4.png)

### *Class Dictionary*

***Due Diligence Bounded Context:***

* ***Agent:*** *Aggregate Root* y representa a los usuarios de nuestra solución.
* ***Due Diligence Project:*** *Aggregate Root* y representa a los proyectos de *Due Diligence* de nuestra solución. Casi todos los métodos en el modelo se basan en cambiar el estado de *Due Diligence Project.*
* ***AcquiringEntity:*** Entidad que representa a la compañía que está vendiendo.
* ***BuySideAgent:*** *Value Object* proveniente del *AcquiringEntity.*
* ***SellSideAgent:*** *Value Object* proveniente de *TarjetCompany.*
* ***TarjetCompany:*** Entidad que representa a la compañía que está comprando

***Information Requirements Bounded Context:***

* ***Information Requirements:*** *Aggregate Root* y representa a los *Information Requirements* presentes en nuestra solución.
* ***Document:*** *Value object* que representan los documentos del usuario.
* ***Area:*** *Value object* que representa las áreas legales, operacionales, impuestos y finanzas.
* ***InformationItem:*** *Aggregate Root* y representa a los *Information Items* presentes en nuestra solución.
* ***InformationItemInfo:*** *Value object* que representa a los *Information Items*.

***QandA Bounded Context:***

* ***QandA:*** *Aggregate Root* que representa las preguntas para los usuarios.
* ***BuySideQuestion:*** *Value Object* que representa la interacción de preguntas y respuestas de compras entre los agentes y los proyectos de *Due Diligence*. 
* ***SellSlideAnswer:*** *Value Object* que representa la interacción de preguntas y respuestas de ventas entre los agentes y los proyectos de *Due Diligence.* 

***Project Creation Bounded Context:***

* ***PendingProjects:*** *Aggregate Root* que representa los diferentes agentes y se encargará de la creación, configuración inicial de los proyectos de *Due Diligence*.
* ***AgentProjectInvitation:*** *Value Object* que representa la asignación de agentes y configuración de información requerida.

## *Database Design*

![Class diagram Due Diligence, imagen generada en ERD editor](src/img/cap4/db-diagrams/diseno-base.png)

### *Database Diagram*

![Class diagram Due Diligence, imagen generada en ERD editor](src/img/cap4/db-diagrams/diagrama-base.png)

# Capítulo V: *Product Implementation, Validation & Deployment*

## *Software Configuration Management*

En esta sección se resume toda la información recopilada y se analizan que pasos se realizarán en el trayecto del proyecto:

### *Software Development Environment Configuration*

En la siguiente sección se describe la ruta de referencia de cada uno de los productos desoftware para que cualquier miembro del equipo pueda desarrollarcada punto del trabajo. 

* **UXPressia:** Plataforma colaborativa que nos permitirá crear user personas e integrados con los múltiples mapas para evaluar sus prioridades.

* **Figma:** Herramienta colaborativa que nos permitirá desarrollar wireframes y mockups.

* **Vertabelo:** Plataforma colaborativa que nos permitirá crear nuestro diagrama de base de datos.

* **LucidChard:** Aplicación web destinada a la elaboración de Wireflows, Users Flows y diagramas de clases.

* **StartUML:** Aplicación de escritorio que nos permitirá crear diagramas de clases.

* **WebStorm:** IDE que utilizaremos para trabajar con javascript y desarrollar la *landing page* y *web application*.

### *Source Code Management*

Este proyecto se trabajó en base a 6 ramas:

* **Main:** Rama principal del proyecto, el cual contienen publicaciones oficiales y actualizadas del proyecto.

* **Rama de integrante del equipo:** Con un total de 5 integrantes, cada miembro del equipo de DeltaTech trabajó por separado sus respectivas asignaciones. Asimismo, también se colaboró en grupo para los puntos que lo requirieron.

::: note
Para acceder al flujo de trabajo del equipo, haga click en la URL: https://github.com/OpenSource-DeltaTech-SW57
:::

### *Source Code Style Guide & Conventions*

Para desarrollar nuestro proyecto hemos requerido de algunas nomenclaturas, referencias y lenguajes para esta solución:

* **Tecnologías:** Utilizamos algunas de estas tecnologías praa el desarrollo de nuestra palicación como: HTML5, CSS, JS.

* **Herramientas:** Nos apoyamos de las tecnologías más utilizadas y recomendadas para el desarrollo de nuestra aplicación como: WebStorm, Github, Git, Fimga, LucidChard.

* **Convenciones de idioma:** Uso del idioma inglés para elaborar nuestro código, incluyendo la parte de la *landing page*..

* Utilizamos el lenguaje Gherkin para realizar los diseños de prueba de cada historia de usuario, contando con su estructura básica. 


**Convenciones de Commits:**
Nuestro equipo de desarrollo sigue las Convenciones de Commits, adoptando el formato de los “Conventional Commits” en su versión 1.0.0 (disponible en URL: https://www.conventionalcommits.org/en/v1.0.0/))) para garantizar una fácil comprensión de nuestros registros. Por lo tanto, nos regimos por la siguiente estructura:
 
Donde:

::: code 
```
<type>[scope opcional]: <description>
```
:::

* **type:** Indica el tipo de modificación realizada, limitado a opciones como feat, fix, docs, etc.
* **scope:** Define el alcance del cambio realizado en nuestro código.
* **descripción:** Ofrece un resumen conciso de los cambios implementados.

**Convenciones de versionado de lanzamientos**

Para la gestión de versiones, seguimos el estándar *“Semantic Versioning 2.0.0”*. En este formato las versiones se presentan como (X.Y.Z), con las siguientes interpretaciones: 

* X: Indica una versión principal que incorpora cambios incompatibles con versiones anteriores. Iniciamos en 0 durante la etapa de desarrollo inicial y traicionamos a 1 cuando la versión esté lista para su lanzamiento público. Por convención, Y y Z se reinician a 0 cuando X aumenta.

* Y: Representa una versión secundaria, que abarca cambios compatibles con versiones anteriores. Además, esta incluye los commits provenientes de las “release branches” cada vez que se agregan nuevas funcionalidades. Convencionalmente, Z se reinicia a 0 cuando Y aumenta.

* Z: Refleja parches y correcciones de errores menores, integrando commits realizados en la “rama de corrección” y fusionados con la rama principal.

### *Software Deployment Configuration*

Ingresar a los repositorios de la organización de Github a través del URL: https://github.com/orgs/OpenSource-DeltaTech-SW57/repositories

![Organización DeltaTech, imagen extraída de Github](src/img/cap5/github1.png)

Seleccionar el repositorio *DiligenceTech* el cual contiene la *landing page*:

![Repositorio de la Organización, imagen extraída de Github](src/img/cap5/github2.png)

Abrir, descarga y ejecutar el index.html en VSCode o WebsTorm:

![Index de la landing page, imagen extraída de Github](src/img/cap5/github3.png)

![Landing page - DiligenceTech, imagen extraída de Github](src/img/cap5/github4.png)

## *Landing Page, Services & Applications Implementation*

Realizamos  la landing page mediante el uso del lenguaje de programación estructurado HTML5, Css y uso de Bootstrap para su diseño.
La primera sección de la landing page se puede evidenciar el header con un menú de navegación haciendo referencia a cada parte de la landing page.  Añadido a esto, podemos apreciar nuestro logo de la StartUp y un fondo dando alusión al servicio que estamos realizando.

![Landing page DiligenceTech, imagen extraída del localhost](src/img/cap5/land1.png)

En la sección About Us mostramos una imagen de gran tamaño haciendo referencia a cómo está constituido nuestro StartUp en base a nuestro producto y además damos una breve descripción, de esta manera el cliente puede conocer de manera más simple y resumida acerca de nosotros.

![About Us DiligenceTech, imagen extraída del localhost](src/img/cap5/land2.png)

En la sección Features damos a conocer las diversas funcionalidades y versatilidad de nuestro producto mediante el uso de animaciones el usuario puede conocer más sobre estas, de esta forma podrá estructurar los diversos procesos que conforma una due diligence y su acoplamiento con nuestro producto.

![Essential Features DiligenceTech, imagen extraída del localhost](src/img/cap5/land3.png)

En la sección Plans damos a conocer los planes de pago que constituyen nuestro servicio, puede elegir entre pago Mensual, Trimestral y Anual. El plan anual te da el beneficio de un solo pago además del ahorro significativo a comparación de los demás planes.

![Plans DiligenceTech, imagen extraída del localhost](src/img/cap5/land4.png)

En esta sección mostramos porque deben elegirnos a nosotros de entre toda la competencia. Además de explicar las ventajas de nuestra plataforma y cómo nosotros podemos acortar costos gracias a la tecnología actual manteniendo la simpleza y el orden. Además de darles a conocer que el pago del servicio es 100% seguro ya que puede tanto usar TPV o pagar mediante su banco en línea de preferencia.

![Mockup DiligenceTech, imagen extraída de Figma](src/img/cap5/land5.png)

![Mockup DiligenceTech, imagen extraída de Figma](src/img/cap5/land6.png)

En la sección de Frequently Asked Questions (FAQs) nosotros mostramos las preguntas que más nos hacen para así las personas no pierdan tiempo en contactar con nosotros, ya que, la mayoría de preguntas ya están en la landing page.

![FAQs DiligenceTech, imagen extraída de Figma](src/img/cap5/land7.png)

Por último, en la sección Request a Demo el cliente digita sus datos personales, seguido a esto se le enviará un correo con las indicaciones a seguir para que un especialista pueda asesorarle y guiarle durante todo el proceso de la due diligence de manera gratis y de demostración. Gracias a esto el cliente podrá tener una idea de cuán rentable es pagar por nuestro servicio y conocer todas los beneficios que este trae.

![Request Demo DiligenceTech, imagen extraída de Figma](src/img/cap5/land8.png)

### *Sprint 1*

Para este primer *Sprint* nos enfocaremos en los task para la elaboración de la *landing page*. Nos dividiremos entre nosotros cada una de las tareas identificadas para el sprint.

#### *Sprint Planning 1*

![](src/img/cap5/sprint1.png)

#### *Sprint Backlog 1*

![](src/img/cap3/productbacklog1.png)

![](src/img/cap3/productbacklog2.png)

![](src/img/cap3/productbacklog3.png)

#### *Development Evidence for Sprint Review*

![](src/img/cap5/team-colaboration1.png)

#### *Testing Suite Evidence for Sprint Review*

Para este sprint 1 no se han generado Unit Tests ni integration test, debido a la falta de clases y la relación entre ellas. Sin embargo, si se podrá realizar Acceptance Tests para los requerimientos planteados.

**US36 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US36: Contenido informativo
#
#   Como usuario interesado, 
#   quiero encontrar contenido detallado y fácil de entender sobre las funcionalidades y beneficios de la aplicación en la landing page 
#   para tomar una decisión informada sobre su uso.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: informative content

    As a user
    I want to find informative content that makes easy to understand the funtionalities and benefits of the application
    So that I can make a good use of the application

  Scenario: Valid information
    Given I am on the landing page
    When I scroll through the page
    And I read the content
    Then I should understand the goal of the application

      Examples:

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I read the content
    Then I dont understand the goal of the application

      Examples:
      .
```
![Imagen creada extraida de VSC](src/img/cap5/testing1.png)

**US37 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US37: Compatibilidad móvil
#
#   Como usuario que accede desde dispositivos móviles,
#   quiero que la landing page esté optimizada para dispositivos móviles
#   para garantizar una experiencia de navegación fluida y accessible.
#
#---------------------------------------------------------------------------------------------------------------------------------------

Feature: mobile compatibility

    As a user
    I want the landing page to be available through mobile devices
    So that I can have an accessible and easy going experience

  Scenario: working comptibility
    Given I am on my mobile device
    When I enter the landing page
    Then the landing page adapts to the device size and format

        Examples:

  Scenario: no comptibility
    Given I am on my mobile device
    When I enter the landing page
    Then the landing page does not adapts to the device size and format at all

        Examples:
#---------------------------------------------------------------------------------------------------------------------------------------
#-------------------------------
```

![Imagen creada extraida de VSC](src/img/cap5/testing2.png)

**US38 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US38: Formulario de contacto
#
#   Como usuario interesado,
#   quiero encontrar un formulario de contacto en la landing page
#   para poder comunicarme con el equipo de la aplicación y obtener respuestas a mis preguntas de manera rápida y sencilla.
#
#---------------------------------------------------------------------------------------------------------------------------------------

Feature: contact form

    As a user
    I want to find a contact form in the landing page
    So that I can contact with the page team and ask questions in an easy way
    
  Scenario: working contact form
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then a message of confirmation pops up

      Examples:

  Scenario: not working contact form
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then nothing happens

      Examples:

  Scenario: unkown error
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then I should see and error message

      Examples:


  Scenario: invalid email
    Given I am on the landing page contact form section
    When I enter the form answers
    And use a wrong "<email>"
    And push the send button
    Then I should see and error message

        Examples:
        | email |
        | aadds | 
        | 12344 |

#---------------------------------------------------------------------------------------------------------------------------------------
#-------------------
```

![Imagen creada extraida de VSC](src/img/cap5/testing3.png)

**US39 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US39: Contenido multimedia
#
#   Como visitante de la landing page,
#   quiero encontrar contenido multimedia, como imágenes y videos, que ilustren las características y beneficios de la aplicación de manera visualmente atractiva
#   para ayudarme a entender mejor el propósito de la aplicación.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: multimedia content

    As a user
    I want to find multimedia content such as images, videos, that represent the benefits and characteristics of the application in a visually appealing way
    So that I can make myself a good understanding of the purpose of the application

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I see multiple multimedia content
    Then I should be able to get a better idea of the goal of the application

      Examples:

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I dont see any multimedia content
    Then I still dont get the goal of the application

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing4.png)

**US40 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US40: Call-to-action claro
#
#   Como usuario potencial,
#   quiero encontrar llamadas claras a la acción en la landing page, como botones de registro o descarga
#   para que me guíen hacia el siguiente paso en mi interacción con la aplicación.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: clear Call-to-action 

    As a user
    I want to find clear call-to-action buttons such as sign-in or download buttons in the landing page
    So that they gide me in the next step in order to get the application.

  Scenario: easy to see call-to-action
    Given I am on the landing page
    When I scroll through the page
    And I easily see the call-to-action
    Then I should be able to get to the next step in order to get the application

      Examples:

  Scenario: unclear call-to-action
    Given I am on the landing page
    When I scroll through the page
    And I dont see any call-to-action
    Then I still dont know how to get the application

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing5.png)

**US41 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US41:  Menú superior funcional
#
#   Como visitante de la landing page,
#   quisiera que el menú superior funcione correctamente
#   para desplazarme rápidamente a través de la landing page.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: working upper menu 

    As a user
    I want upper menu to work properly
    So that I can quickly navigate through the landing page

  Scenario: working upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then I should be redirected to the corresponding section of the landing page

      Examples:

  Scenario: malfunctioning upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then I am redirected to the wrong section of the landing page

      Examples:

  Scenario: not working upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then nothing happens

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing6.png)

**US42 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US42: Call-to-action funcional
#
#   Como visitante de la landing page,
#   quisiera que el call to action button del inicio funcione correctamente
#   para que me lleve a donde dice.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: working Call-to-action 

    As a user
    I want the call-to-action buttons to work properly
    So that they take wherever they said

  Scenario: working call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then I it takes me to the place it said it should take me to

      Examples:

  Scenario: not working call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then nothing happens

      Examples:

  Scenario: malfunctioning call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then it takes to the wrong place

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing7.png)

![Imagen creada extraida de VSC](src/img/cap5/testing8.png)

![](src/img/cap5/testing-suite-table.png)

#### *Execution Evidence for Sprint Review*

Durante este primer sprint se realizó la implementación del landing page incluyendo sus features. Estos siendo un menú superior para mayor alcance de sus secciones, además de un botón para poder ingresar a la cuenta del usuario pero sin uso por el momento.  Por otro lado, cada sección cuenta con partes funcionales dependiendo de la funcionalidad deseada. En las imágenes y video que se presentarán se apreciará de mejor manera lo mencionado.

![Imagen extraída del navegador](src/img/cap5/execution1.png)

![Imagen extraída del navegador](src/img/cap5/land5.png)

![Imagen extraída del navegador](src/img/cap5/execution2.png)

::: note
Puede visualizar un video de demostración en el URL: https://lc.cx/3UYtuQ
:::

#### *Services Documentation Evidence for Sprint Review*

::: warning
No aplica para esta entrega.
:::

#### *Software Deployment Evidence for Sprint Review*

Para el despliegue de la Landing Page primero creamos el repositiorio indicado:

![Imagen extraída de Github](src/img/cap5/github2.png)

Luego de ello, cada uno aporto con sus respectivas partes al proyecto de la *landing page:*

![Imagen extraída de Github](src/img/cap5/github3.png)

Por último, utilizando la herramienta Github Pages, completamos la inforamción que nos piden como la fuente y rama de donde desplegaremos el trabajo. Luego de ello, *Pages* brinda un link de nuestro sitio web desplegado:

#### *Team Collaboration Insights during Sprint*

Para este sprint se ha realizado la implementación del landing page, para esto los integrantes del grupo realizaron su aporte a través de commits en la herramienta Git Hub.

![Imagen extraída de Github](src/img/cap5/team-colaboration1.png)

Utilizando GitHub se creó una organización llamada DeltaTech, en la cual creamos repositorios para nuestro trabajo. Para este punto solo mencionaremos el repositorio de la landing page, ya que el otro presente por el momento es el del informe.

![Imagen extraída de Github](src/img/cap5/team-colaboration2.png)

Dentro del repositorio se encuentran los archivos necesarios para el proyecto. Estos están siendo actualizados en ramas independientes en primer lugar, y cuando sea necesario se realiza un push a la rama main.

Commits realizados por los integrantes: 

![Imagen extraída de Github](src/img/cap5/team-colaboration3.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration4.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration5.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration6.png)

### *Sprint 2*

Para este primer *Sprint* nos enfocaremos en los task para la elaboración de la *Web Application*. Nos dividiremos entre nosotros cada una de las tareas identificadas para el sprint.

#### *Sprint Planning 2*

![](src/img/cap5/sprint2.png)

#### *Sprint Backlog 2*

![](src/img/cap3/productbacklog12.png)

![](src/img/cap3/productbacklog13.png)

#### *Development Evidence for Sprint Review*

![](src/img/cap5/team-colaboration1.png)

#### *Testing Suite Evidence for Sprint Review*

Para este sprint 1 no se han generado Unit Tests ni integration test, debido a la falta de clases y la relación entre ellas. Sin embargo, si se podrá realizar Acceptance Tests para los requerimientos planteados.

**US36 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US36: Contenido informativo
#
#   Como usuario interesado, 
#   quiero encontrar contenido detallado y fácil de entender sobre las funcionalidades y beneficios de la aplicación en la landing page 
#   para tomar una decisión informada sobre su uso.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: informative content

    As a user
    I want to find informative content that makes easy to understand the funtionalities and benefits of the application
    So that I can make a good use of the application

  Scenario: Valid information
    Given I am on the landing page
    When I scroll through the page
    And I read the content
    Then I should understand the goal of the application

      Examples:

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I read the content
    Then I dont understand the goal of the application

      Examples:
      .
```
![Imagen creada extraida de VSC](src/img/cap5/testing1.png)

**US37 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US37: Compatibilidad móvil
#
#   Como usuario que accede desde dispositivos móviles,
#   quiero que la landing page esté optimizada para dispositivos móviles
#   para garantizar una experiencia de navegación fluida y accessible.
#
#---------------------------------------------------------------------------------------------------------------------------------------

Feature: mobile compatibility

    As a user
    I want the landing page to be available through mobile devices
    So that I can have an accessible and easy going experience

  Scenario: working comptibility
    Given I am on my mobile device
    When I enter the landing page
    Then the landing page adapts to the device size and format

        Examples:

  Scenario: no comptibility
    Given I am on my mobile device
    When I enter the landing page
    Then the landing page does not adapts to the device size and format at all

        Examples:
#---------------------------------------------------------------------------------------------------------------------------------------
#-------------------------------
```

![Imagen creada extraida de VSC](src/img/cap5/testing2.png)

**US38 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US38: Formulario de contacto
#
#   Como usuario interesado,
#   quiero encontrar un formulario de contacto en la landing page
#   para poder comunicarme con el equipo de la aplicación y obtener respuestas a mis preguntas de manera rápida y sencilla.
#
#---------------------------------------------------------------------------------------------------------------------------------------

Feature: contact form

    As a user
    I want to find a contact form in the landing page
    So that I can contact with the page team and ask questions in an easy way
    
  Scenario: working contact form
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then a message of confirmation pops up

      Examples:

  Scenario: not working contact form
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then nothing happens

      Examples:

  Scenario: unkown error
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then I should see and error message

      Examples:


  Scenario: invalid email
    Given I am on the landing page contact form section
    When I enter the form answers
    And use a wrong "<email>"
    And push the send button
    Then I should see and error message

        Examples:
        | email |
        | aadds | 
        | 12344 |

#---------------------------------------------------------------------------------------------------------------------------------------
#-------------------
```

![Imagen creada extraida de VSC](src/img/cap5/testing3.png)

**US39 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US39: Contenido multimedia
#
#   Como visitante de la landing page,
#   quiero encontrar contenido multimedia, como imágenes y videos, que ilustren las características y beneficios de la aplicación de manera visualmente atractiva
#   para ayudarme a entender mejor el propósito de la aplicación.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: multimedia content

    As a user
    I want to find multimedia content such as images, videos, that represent the benefits and characteristics of the application in a visually appealing way
    So that I can make myself a good understanding of the purpose of the application

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I see multiple multimedia content
    Then I should be able to get a better idea of the goal of the application

      Examples:

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I dont see any multimedia content
    Then I still dont get the goal of the application

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing4.png)

**US40 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US40: Call-to-action claro
#
#   Como usuario potencial,
#   quiero encontrar llamadas claras a la acción en la landing page, como botones de registro o descarga
#   para que me guíen hacia el siguiente paso en mi interacción con la aplicación.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: clear Call-to-action 

    As a user
    I want to find clear call-to-action buttons such as sign-in or download buttons in the landing page
    So that they gide me in the next step in order to get the application.

  Scenario: easy to see call-to-action
    Given I am on the landing page
    When I scroll through the page
    And I easily see the call-to-action
    Then I should be able to get to the next step in order to get the application

      Examples:

  Scenario: unclear call-to-action
    Given I am on the landing page
    When I scroll through the page
    And I dont see any call-to-action
    Then I still dont know how to get the application

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing5.png)

**US41 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US41:  Menú superior funcional
#
#   Como visitante de la landing page,
#   quisiera que el menú superior funcione correctamente
#   para desplazarme rápidamente a través de la landing page.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: working upper menu 

    As a user
    I want upper menu to work properly
    So that I can quickly navigate through the landing page

  Scenario: working upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then I should be redirected to the corresponding section of the landing page

      Examples:

  Scenario: malfunctioning upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then I am redirected to the wrong section of the landing page

      Examples:

  Scenario: not working upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then nothing happens

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing6.png)

**US42 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US42: Call-to-action funcional
#
#   Como visitante de la landing page,
#   quisiera que el call to action button del inicio funcione correctamente
#   para que me lleve a donde dice.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: working Call-to-action 

    As a user
    I want the call-to-action buttons to work properly
    So that they take wherever they said

  Scenario: working call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then I it takes me to the place it said it should take me to

      Examples:

  Scenario: not working call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then nothing happens

      Examples:

  Scenario: malfunctioning call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then it takes to the wrong place

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing7.png)

![Imagen creada extraida de VSC](src/img/cap5/testing8.png)

![](src/img/cap5/testing-suite-table.png)

#### *Execution Evidence for Sprint Review*

Durante este primer sprint se realizó la implementación del landing page incluyendo sus features. Estos siendo un menú superior para mayor alcance de sus secciones, además de un botón para poder ingresar a la cuenta del usuario pero sin uso por el momento.  Por otro lado, cada sección cuenta con partes funcionales dependiendo de la funcionalidad deseada. En las imágenes y video que se presentarán se apreciará de mejor manera lo mencionado.

![Imagen extraída del navegador](src/img/cap5/execution1.png)

![Imagen extraída del navegador](src/img/cap5/land5.png)

![Imagen extraída del navegador](src/img/cap5/execution2.png)

::: note
Puede visualizar un video de demostración en el URL: https://lc.cx/3UYtuQ
:::

#### *Services Documentation Evidence for Sprint Review*

::: warning
No aplica para esta entrega.
:::

#### *Software Deployment Evidence for Sprint Review*

Para el despliegue de la Landing Page primero creamos el repositiorio indicado:

![Imagen extraída de Github](src/img/cap5/github2.png)

Luego de ello, cada uno aporto con sus respectivas partes al proyecto de la *landing page:*

![Imagen extraída de Github](src/img/cap5/github3.png)

Por último, utilizando la herramienta Github Pages, completamos la inforamción que nos piden como la fuente y rama de donde desplegaremos el trabajo. Luego de ello, *Pages* brinda un link de nuestro sitio web desplegado:

#### *Team Collaboration Insights during Sprint*

Para este sprint se ha realizado la implementación del landing page, para esto los integrantes del grupo realizaron su aporte a través de commits en la herramienta Git Hub.

![Imagen extraída de Github](src/img/cap5/team-colaboration1.png)

Utilizando GitHub se creó una organización llamada DeltaTech, en la cual creamos repositorios para nuestro trabajo. Para este punto solo mencionaremos el repositorio de la landing page, ya que el otro presente por el momento es el del informe.

![Imagen extraída de Github](src/img/cap5/team-colaboration2.png)

Dentro del repositorio se encuentran los archivos necesarios para el proyecto. Estos están siendo actualizados en ramas independientes en primer lugar, y cuando sea necesario se realiza un push a la rama main.

Commits realizados por los integrantes: 

![Imagen extraída de Github](src/img/cap5/team-colaboration3.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration4.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration5.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration6.png)

### *Sprint 3*

Para este primer *Sprint* nos enfocaremos en los task para la elaboración del *Backend*. Nos dividiremos entre nosotros cada una de las tareas identificadas para el sprint.

#### *Sprint Planning 3*

![](src/img/cap5/sprint3.png)

#### *Sprint Backlog 3*

![](src/img/cap3/productbacklog14.png)

![](src/img/cap3/productbacklog15.png)

![](src/img/cap3/productbacklog16.png)

![](src/img/cap3/productbacklog17.png)

![](src/img/cap3/productbacklog18.png)

![](src/img/cap3/productbacklog19.png)

![](src/img/cap3/productbacklog20.png)

![](src/img/cap3/productbacklog21.png)

![](src/img/cap3/productbacklog22.png)

![](src/img/cap3/productbacklog23.png)

#### *Development Evidence for Sprint Review*

Link del deployment - version estable
- https://diligencetech-platform-api.azurewebsites.net/

Link del Deployment Backend: 
- https://webapp-240608171515.azurewebsites.net/
- https://diligencetech-platform.azurewebsites.net/
- https://webapp-240608171515.azurewebsites.net/swagger/index.html

![](src/img/cap5/team-colaboration1.png)

#### *Testing Suite Evidence for Sprint Review*

Para este sprint 1 no se han generado Unit Tests ni integration test, debido a la falta de clases y la relación entre ellas. Sin embargo, si se podrá realizar Acceptance Tests para los requerimientos planteados.

**US36 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US36: Contenido informativo
#
#   Como usuario interesado, 
#   quiero encontrar contenido detallado y fácil de entender sobre las funcionalidades y beneficios de la aplicación en la landing page 
#   para tomar una decisión informada sobre su uso.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: informative content

    As a user
    I want to find informative content that makes easy to understand the funtionalities and benefits of the application
    So that I can make a good use of the application

  Scenario: Valid information
    Given I am on the landing page
    When I scroll through the page
    And I read the content
    Then I should understand the goal of the application

      Examples:

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I read the content
    Then I dont understand the goal of the application

      Examples:
      .
```
![Imagen creada extraida de VSC](src/img/cap5/testing1.png)

**US37 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US37: Compatibilidad móvil
#
#   Como usuario que accede desde dispositivos móviles,
#   quiero que la landing page esté optimizada para dispositivos móviles
#   para garantizar una experiencia de navegación fluida y accessible.
#
#---------------------------------------------------------------------------------------------------------------------------------------

Feature: mobile compatibility

    As a user
    I want the landing page to be available through mobile devices
    So that I can have an accessible and easy going experience

  Scenario: working comptibility
    Given I am on my mobile device
    When I enter the landing page
    Then the landing page adapts to the device size and format

        Examples:

  Scenario: no comptibility
    Given I am on my mobile device
    When I enter the landing page
    Then the landing page does not adapts to the device size and format at all

        Examples:
#---------------------------------------------------------------------------------------------------------------------------------------
#-------------------------------
```

![Imagen creada extraida de VSC](src/img/cap5/testing2.png)

**US38 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US38: Formulario de contacto
#
#   Como usuario interesado,
#   quiero encontrar un formulario de contacto en la landing page
#   para poder comunicarme con el equipo de la aplicación y obtener respuestas a mis preguntas de manera rápida y sencilla.
#
#---------------------------------------------------------------------------------------------------------------------------------------

Feature: contact form

    As a user
    I want to find a contact form in the landing page
    So that I can contact with the page team and ask questions in an easy way
    
  Scenario: working contact form
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then a message of confirmation pops up

      Examples:

  Scenario: not working contact form
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then nothing happens

      Examples:

  Scenario: unkown error
    Given I am on the landing page contact form section
    When I enter the form answers
    And push the send button
    Then I should see and error message

      Examples:


  Scenario: invalid email
    Given I am on the landing page contact form section
    When I enter the form answers
    And use a wrong "<email>"
    And push the send button
    Then I should see and error message

        Examples:
        | email |
        | aadds | 
        | 12344 |

#---------------------------------------------------------------------------------------------------------------------------------------
#-------------------
```

![Imagen creada extraida de VSC](src/img/cap5/testing3.png)

**US39 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US39: Contenido multimedia
#
#   Como visitante de la landing page,
#   quiero encontrar contenido multimedia, como imágenes y videos, que ilustren las características y beneficios de la aplicación de manera visualmente atractiva
#   para ayudarme a entender mejor el propósito de la aplicación.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: multimedia content

    As a user
    I want to find multimedia content such as images, videos, that represent the benefits and characteristics of the application in a visually appealing way
    So that I can make myself a good understanding of the purpose of the application

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I see multiple multimedia content
    Then I should be able to get a better idea of the goal of the application

      Examples:

  Scenario: Invalid information
    Given I am on the landing page
    When I scroll through the page
    And I dont see any multimedia content
    Then I still dont get the goal of the application

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing4.png)

**US40 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US40: Call-to-action claro
#
#   Como usuario potencial,
#   quiero encontrar llamadas claras a la acción en la landing page, como botones de registro o descarga
#   para que me guíen hacia el siguiente paso en mi interacción con la aplicación.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: clear Call-to-action 

    As a user
    I want to find clear call-to-action buttons such as sign-in or download buttons in the landing page
    So that they gide me in the next step in order to get the application.

  Scenario: easy to see call-to-action
    Given I am on the landing page
    When I scroll through the page
    And I easily see the call-to-action
    Then I should be able to get to the next step in order to get the application

      Examples:

  Scenario: unclear call-to-action
    Given I am on the landing page
    When I scroll through the page
    And I dont see any call-to-action
    Then I still dont know how to get the application

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing5.png)

**US41 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US41:  Menú superior funcional
#
#   Como visitante de la landing page,
#   quisiera que el menú superior funcione correctamente
#   para desplazarme rápidamente a través de la landing page.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: working upper menu 

    As a user
    I want upper menu to work properly
    So that I can quickly navigate through the landing page

  Scenario: working upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then I should be redirected to the corresponding section of the landing page

      Examples:

  Scenario: malfunctioning upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then I am redirected to the wrong section of the landing page

      Examples:

  Scenario: not working upper menu
    Given I am on the landing page
    When I go to the upper menu
    And I select any of the options there
    Then nothing happens

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing6.png)

**US42 - Gherkin**

```gherkin
#---------------------------------------------------------------------------------------------------------------------------------------
#---------------------------------------------------------------------------------------------------------------------------------------
#   US42: Call-to-action funcional
#
#   Como visitante de la landing page,
#   quisiera que el call to action button del inicio funcione correctamente
#   para que me lleve a donde dice.
#
#---------------------------------------------------------------------------------------------------------------------------------------
Feature: working Call-to-action 

    As a user
    I want the call-to-action buttons to work properly
    So that they take wherever they said

  Scenario: working call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then I it takes me to the place it said it should take me to

      Examples:

  Scenario: not working call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then nothing happens

      Examples:

  Scenario: malfunctioning call-to-action button
    Given I am on the landing page
    When I press the call-to-action button
    Then it takes to the wrong place

      Examples:
```

![Imagen creada extraida de VSC](src/img/cap5/testing7.png)

![Imagen creada extraida de VSC](src/img/cap5/testing8.png)

![](src/img/cap5/testing-suite-table.png)

#### *Execution Evidence for Sprint Review*

Durante este primer sprint se realizó la implementación del landing page incluyendo sus features. Estos siendo un menú superior para mayor alcance de sus secciones, además de un botón para poder ingresar a la cuenta del usuario pero sin uso por el momento.  Por otro lado, cada sección cuenta con partes funcionales dependiendo de la funcionalidad deseada. En las imágenes y video que se presentarán se apreciará de mejor manera lo mencionado.

![Imagen extraída del navegador](src/img/cap5/execution1.png)

![Imagen extraída del navegador](src/img/cap5/land5.png)

![Imagen extraída del navegador](src/img/cap5/execution2.png)

::: note
Puede visualizar un video de demostración en el URL: https://lc.cx/3UYtuQ
:::

#### *Services Documentation Evidence for Sprint Review*

| Endpoint         | Acción Implementada         | HTTP  | Sintaxis de Llamada               | Parámetros                | Ejemplo de Response                                                                                             |
|------------------|-----------------------------|-------|-----------------------------------|---------------------------|---------------------------------------------------------------------------------------------------------------|
| /agents        | Obtener todos los agentes   | GET   | /api/v1/agents                  | Ninguno                   | [{"id":1, "name":"John Doe", "email":"john.doe@example.com", "status":"active"}]                             |
| /agents/{id}   | Obtener agente por Id       | GET   | /api/v1/agents/{id}             | id (Path)                 | {"id":1, "name":"John Doe", "email":"john.doe@example.com", "status":"active"}                               |
| /agents        | Crear nuevo agente          | POST  | /api/v1/agents                  | name, email, status       | {"message":"Agente creado exitosamente"}                                                                     |
| /folders       | Obtener todas las carpetas  | GET   | /api/v1/folders                 | Ninguno                   | [{"id":1, "name":"Financial Reports", "created_at":"2023-01-01T12:00:00Z"}]                                  |
| /folders/{id}  | Obtener carpeta por Id      | GET   | /api/v1/folders/{id}            | id (Path)                 | {"id":1, "name":"Financial Reports", "created_at":"2023-01-01T12:00:00Z"}                                    |
| /folders       | Crear nueva carpeta         | POST  | /api/v1/folders                 | name, created_at          | {"message":"Carpeta creada exitosamente"}                                                                    |
| /qa            | Obtener todas las QA        | GET   | /api/v1/qa                      | Ninguno                   | [{"id":1, "question":"What is due diligence?", "answer":"A comprehensive appraisal of a business."}]         |
| /qa/{id}       | Obtener QA por Id           | GET   | /api/v1/qa/{id}                 | id (Path)                 | {"id":1, "question":"What is due diligence?", "answer":"A comprehensive appraisal of a business."}           |
| /qa            | Crear nueva QA              | POST  | /api/v1/qa                      | question, answer          | {"message":"QA creada exitosamente"}                                                                         |
| /projects      | Obtener todos los proyectos | GET   | /api/v1/projects                | Ninguno                   | [{"id":1, "name":"Project Alpha", "description":"A top-secret project", "status":"ongoing"}]                 |
| /projects/{id} | Obtener proyecto por Id     | GET   | /api/v1/projects/{id}           | id (Path)                 | {"id":1, "name":"Project Alpha", "description":"A top-secret project", "status":"ongoing"}                   |
| /projects      | Crear nuevo proyecto        | POST  | /api/v1/projects                | name, description, status | {"message":"Proyecto creado exitosamente"}                                                                   |

#### *Software Deployment Evidence for Sprint Review*

Para el despliegue de la Landing Page primero creamos el repositiorio indicado:

![Imagen extraída de Github](src/img/cap5/github2.png)

Luego de ello, cada uno aporto con sus respectivas partes al proyecto de la *landing page:*

![Imagen extraída de Github](src/img/cap5/github3.png)

Por último, utilizando la herramienta Github Pages, completamos la inforamción que nos piden como la fuente y rama de donde desplegaremos el trabajo. Luego de ello, *Pages* brinda un link de nuestro sitio web desplegado:

#### *Team Collaboration Insights during Sprint*

Para este sprint se ha realizado la implementación del landing page, para esto los integrantes del grupo realizaron su aporte a través de commits en la herramienta Git Hub.

![Imagen extraída de Github](src/img/cap5/team-colaboration1.png)

Utilizando GitHub se creó una organización llamada DeltaTech, en la cual creamos repositorios para nuestro trabajo. Para este punto solo mencionaremos el repositorio de la landing page, ya que el otro presente por el momento es el del informe.

![Imagen extraída de Github](src/img/cap5/team-colaboration2.png)

Dentro del repositorio se encuentran los archivos necesarios para el proyecto. Estos están siendo actualizados en ramas independientes en primer lugar, y cuando sea necesario se realiza un push a la rama main.

Commits realizados por los integrantes: 

![Imagen extraída de Github](src/img/cap5/team-colaboration3.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration4.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration5.png)

![Imagen extraída de Github](src/img/cap5/team-colaboration6.png)

Para una mejor organización, se realizó la organización de todas las pendientes de esta entrega en un tablero Kanvan. En donde, se detallan los puntos específicos a abordar, los participantes de cada punto, las *labels* que describen en forma de etiquetas cada Issue y el uso de Milestones para organizar las fechas de entrega del proyecto y sus respectivos entregables.

![Tablero Kanvan del equipo, imagen extraída de Github](src/img/cap5/tablero-kanvan.png)


## Validation Interviews

Para la validación de la solución empleada se producen entrevistas a candidatos de los segmentos objetivos para verificar su conformidad con el futuro producto.

::: note
Para acceder al video de las entrevistas, haga click en la URL: https://lc.cx/3UYtuQ
:::

### Diseño de Entrevistas

Entrevista a personas referentes a nuestro segmentos objetivo, las preguntas varí­an dependiendo del segmento debido a las diferentes situaciones:

**Segmento 1:** Contadores Financieros

**Preguntas de introducción:**

1. ¿Cuál es su nombre completo?
2. ¿Cuál es su edad?
3. ¿En qué ciudad y/o distrito reside?
4. ¿Cúal es su profesión?
5. ¿Cuánto tiempo lleva ejerciendo esta profesión?
6. ¿Está familiarizado con el concepto y proceso de diligencia debida?

**Preguntas principales:**

1.	¿Cómo describirías tu impresión general después de ver la aplicación de DiligenceTech?
2.	¿Qué aspectos de la aplicación te parecieron más útiles para tu trabajo diario?
3.	¿Hubo alguna funcionalidad específica que te sorprendiera o impresionara?
4.	¿Notaste alguna dificultad potencial al navegar por la aplicación?
5.	¿Qué tan fácil crees que sería acceder a los análisis de datos o a los documentos del proyecto?
6.	¿Consideras que la aplicación podría mejorar la eficiencia en la realización de due diligence? ¿Por qué?
7.	¿Qué elementos de la interfaz de usuario te parecen más intuitivos?
8.	¿Qué elementos de la interfaz de usuario crees que podrían mejorarse?
9.	¿La velocidad de procesamiento de datos mostrada te parece adecuada para tus necesidades?
10.	¿Cómo calificarías la precisión de los análisis financieros presentados?
11.	¿Crees que la aplicación facilita la colaboración con otros contadores o miembros del equipo?
12.	¿La aplicación cubre todas tus necesidades actuales de Due Diligence? Si no, ¿qué le falta?
13.	¿Qué características adicionales te gustaría ver en futuras versiones de la aplicación?
14.	¿Consideras que la información presentada en los informes es clara y comprensible?
15.	¿Qué tan útil te parece la automatización de las funciones para tu trabajo?
16.	¿La aplicación ofrece suficientes recursos y soporte para resolver dudas o problemas técnicos?
17.	¿Cómo calificarías el diseño visual de la aplicación?
18.	¿Recomendarías esta aplicación a otros contadores? ¿Por qué?
19.	¿Qué mejoras sugieres para incrementar la usabilidad de la aplicación?
20.	¿Algún comentario adicional sobre tu experiencia con DiligenceTech?

**Segmento 2:** Inversores

**Preguntas de introducción:**

1. ¿Cuál es su nombre completo?
2. ¿Cuál es su edad?
3. ¿En qué ciudad y/o distrito reside?
4. ¿Cúal es su profesión?
5. ¿Cuánto tiempo lleva ejerciendo esta profesión?
6. ¿Está familiarizado con el concepto y proceso de diligencia debida?

**Preguntas principales:**

1.	¿Cuál fue tu impresión inicial después de ver la aplicación de DeltaTech?
2.	¿Qué aspectos de la aplicación te parecieron más valiosos para tus decisiones de inversión?
3.	¿Hubo alguna característica que te resultara especialmente innovadora o útil?
4.	¿Te pareció fácil navegar por la aplicación y encontrar la información que necesitabas?
5.	¿Qué tan bien crees que la aplicación ayuda a evaluar el riesgo financiero?
6.	¿Cómo describirías la calidad y precisión de los informes generados por la aplicación?
7.	¿Qué tan rápido crees que podrías obtener la información necesaria para tus evaluaciones?
8.	¿La aplicación facilita la comprensión de los datos financieros para la toma de decisiones?
9.	¿Qué elementos de la aplicación te resultaron más intuitivos?
10.	¿Qué aspectos de la interfaz de usuario crees que podrían mejorarse?
11.	¿Consideras que la aplicación podría mejorar la eficiencia en la realización de due diligence? ¿Por qué?
12.	¿Te parece útil la función de automatización para tus análisis financieros?
13.	¿En qué medida crees que la aplicación permitiría colaborar con otros inversores o asesores financieros?
14.	¿Qué funcionalidades adicionales te gustaría ver en futuras versiones de la aplicación?
15.	¿La aplicación cubre todas tus necesidades actuales de due diligence? Si no, ¿qué le falta?
16.	¿Cómo calificarías el soporte y los recursos disponibles para resolver dudas o problemas técnicos?
17.	¿Qué tan clara y comprensible encuentras la presentación de los datos en la aplicación?
18.	¿Recomendarías esta aplicación a otros inversores? ¿Por qué?
19.	¿Qué mejoras sugieres para incrementar la usabilidad de la aplicación?
20.	¿Algún comentario adicional sobre tu experiencia con DeltaTech?

### Registro de Entrevistas

Para el registro de entrevistas se realizarán 3 entrevistas por segmento, dando un total de 6 entrevistas. Además, el formato de las entrevistas es .mp4, cada entrevista es independiente debido a las diferentes preguntas y respuestas dadas por los entrevistados de cada segmento.

**Segmento 1: Contadores financieros**

| Nombre               | Patricia González                   |
|----------------------|-------------------------------------|
| Edad                 | 58 años                             |
| Ubicación Geográfica | Lima, Perú (Surco) / Trujillo, Perú |
| Profesión            | Contadora pública colegiada         |
| Timing Entrevista    | [0:00 - 08:59]                      |

**Resumen de Entrevista:**

Patricia González, de 58 años, contadora pública colegiada con residencia en Lima y Trujillo, Perú, describió su impresión general de la aplicación DiligenceTech como positiva, destacando su facilidad de uso y utilidad. Los análisis automatizados y la rapidez en la generación de informes fueron los aspectos más útiles para su trabajo diario. Quedó impresionada por la precisión y claridad de los análisis financieros. No notó dificultades significativas al navegar por la aplicación, considerando que es muy fácil acceder a los análisis de datos y documentos del proyecto. Cree que la aplicación puede mejorar la eficiencia en la diligencia debida debido a la automatización y la reducción del tiempo necesario para generar informes. Destacó los menús desplegables y la organización lógica de las funciones como elementos intuitivos, aunque sugirió mejorar la visibilidad de ciertas opciones avanzadas. La velocidad de procesamiento de datos le parece adecuada y calificó la precisión de los análisis financieros como alta. Considera que la aplicación facilita la colaboración al permitir compartir fácilmente los informes y análisis. La aplicación cubre sus necesidades actuales de due diligence, aunque mencionó que siempre hay espacio para mejoras y actualizaciones. Le gustaría ver una integración más profunda con otras herramientas contables y financieras. Encuentra que los informes son claros y comprensibles, incluso para no expertos en contabilidad. La automatización de funciones le resulta muy útil, reduciendo la carga de trabajo manual. La aplicación ofrece suficientes recursos y soporte para resolver dudas o problemas técnicos. Calificó el diseño visual como moderno y atractivo. Recomendaría la aplicación por su eficiencia y precisión en el análisis de datos financieros. Sugirió implementar tutoriales interactivos para nuevos usuarios y mejorar la visibilidad de las funciones avanzadas, reafirmando su satisfacción general con la aplicación.

![Imagen extraída de Microsoft Video](src/img/cap5/imagen1.png)

| Nombre               | Guisella Díaz               |
|----------------------|-----------------------------|
| Edad                 | 51 años                     |
| Ubicación Geográfica | Lima, Perú (Surco)          |
| Profesión            | Contadora pública colegiada |
| Timing Entrevista    | [08:59 - 20:35]             |

**Resumen de Entrevista:**

Guisella Díaz, de 51 años y contadora pública colegiada residente en Lima, Perú (Surco), tuvo una impresión general positiva de la aplicación DiligenceTech, resaltando su facilidad de uso y la utilidad de las funcionalidades. Consideró los análisis automatizados y la rapidez en la generación de informes como los aspectos más útiles para su trabajo diario. La precisión y claridad de los análisis financieros la sorprendieron gratamente. No encontró dificultades significativas al navegar por la aplicación y mencionó que es muy fácil acceder a los análisis de datos y documentos del proyecto. Cree que la aplicación podría mejorar la eficiencia en la diligencia debida gracias a la automatización y a la reducción del tiempo necesario para generar informes. Destacó la organización lógica de las funciones como elementos intuitivos y sugirió mejorar la visibilidad de ciertas opciones avanzadas. La velocidad de procesamiento de datos le pareció adecuada y calificó la precisión de los análisis financieros como alta. Considera que la aplicación facilita la colaboración al permitir compartir informes y análisis con otros miembros del equipo. Aunque la aplicación cubre sus necesidades actuales de due diligence, cree que siempre hay espacio para mejoras y actualizaciones. Le gustaría ver una integración más profunda con otras herramientas contables y financieras que utiliza en su trabajo diario. Encuentra que los informes son claros y comprensibles, incluso para aquellos que no son expertos en contabilidad. La automatización de funciones le resulta muy útil, reduciendo la carga de trabajo manual. La aplicación ofrece suficientes recursos y soporte para resolver dudas o problemas técnicos. Calificó el diseño visual como moderno y atractivo. Recomendaría la aplicación por su eficiencia y precisión en el análisis de datos financieros. Sugirió implementar tutoriales interactivos para nuevos usuarios y mejorar la visibilidad de las funciones avanzadas, reafirmando su satisfacción general con la aplicación.

![Imagen extraída de Microsoft Video](src/img/cap5/imagen2.png)

| Nombre               | James De La Torre Ugarte |
|----------------------|--------------------------|
| Edad                 | 55 años                  |
| Ubicación Geográfica | Lima, Perú (La Molina)   |
| Profesión            | Contador público         |
| Timing Entrevista    | [20:35 - 36:16]          |

**Resumen de Entrevista:**

James De La Torre Ugarte, de 55 años, contador público residente en Lima, Perú (La Molina), tuvo una impresión general muy positiva de la aplicación DiligenceTech, destacando su facilidad de uso y la eficiencia de sus funcionalidades. Los análisis automatizados y la rapidez en la generación de informes fueron los aspectos más útiles para su trabajo diario. La precisión y claridad de los análisis financieros le impresionaron particularmente. No encontró dificultades significativas al navegar por la aplicación, señalando que es muy fácil acceder a los análisis de datos y documentos del proyecto. James cree que la aplicación mejorará significativamente la eficiencia en la diligencia debida debido a la automatización y a la reducción del tiempo necesario para generar informes. Destacó la organización lógica de las funciones y los menús desplegables como elementos intuitivos, aunque sugirió mejorar la visibilidad de ciertas opciones avanzadas. La velocidad de procesamiento de datos le parece adecuada y calificó la precisión de los análisis financieros como alta. Considera que la aplicación facilita la colaboración al permitir compartir fácilmente los informes y análisis con otros miembros del equipo. Cree que la aplicación cubre sus necesidades actuales de due diligence, aunque siempre hay espacio para mejoras y actualizaciones. Le gustaría ver una integración más profunda con otras herramientas contables y financieras que utiliza en su trabajo diario. Encuentra que los informes son claros y comprensibles, incluso para aquellos que no son expertos en contabilidad. La automatización de funciones le resulta muy útil, reduciendo la carga de trabajo manual. La aplicación ofrece suficientes recursos y soporte para resolver dudas o problemas técnicos. Calificó el diseño visual como moderno y atractivo. Recomendaría la aplicación por su eficiencia y precisión en el análisis de datos financieros. Sugirió implementar tutoriales interactivos para nuevos usuarios y mejorar la visibilidad de las funciones avanzadas, reafirmando su satisfacción general con la aplicación.

![Imagen extraída de Microsoft Video](src/img/cap5/imagen3.png)

**Segmento 2: Inversores**

| Nombre               | Piero Delgado Bracamonte |
|----------------------|--------------------------|
| Edad                 | 25 años                  |
| Ubicación Geográfica | Lima, Perú (San Borja)   |
| Profesión            | Inversor                 |
| Timing Entrevista    | [36:16 - 42:42]          |

**Resumen de Entrevista:**

Piero Delgado Bracamonte, de 25 años, inversor residente en Lima, Perú (San Borja), tuvo una impresión inicial positiva de la aplicación DeltaTech, resaltando su facilidad de uso y la claridad de la información presentada. Consideró que los aspectos más valiosos para sus decisiones de inversión fueron los análisis detallados y la rapidez en la generación de informes. Le resultaron especialmente innovadoras las herramientas de evaluación de riesgos financieros. No encontró dificultades significativas al navegar por la aplicación, señalando que es muy fácil acceder a la información necesaria. Piero cree que la aplicación ayuda efectivamente a evaluar el riesgo financiero y describió la calidad y precisión de los informes generados como alta. Mencionó que puede obtener la información necesaria para sus evaluaciones de manera rápida. Considera que la aplicación facilita la comprensión de los datos financieros para la toma de decisiones y destacó la organización de las funciones como muy intuitiva. Sugirió mejorar algunos aspectos de la interfaz de usuario para hacerla aún más accesible. Cree que la aplicación puede mejorar la eficiencia en la diligencia debida gracias a la automatización y a la reducción del tiempo necesario para realizar análisis. Encuentra útil la función de automatización para sus análisis financieros y mencionó que la aplicación permite colaborar fácilmente con otros inversores o asesores financieros. Le gustaría ver funcionalidades adicionales, como más herramientas de predicción y análisis de tendencias, en futuras versiones de la aplicación. Considera que la aplicación cubre sus necesidades actuales de due diligence, aunque siempre hay espacio para mejoras. Calificó el soporte y los recursos disponibles para resolver dudas o problemas técnicos como adecuados. Encuentra la presentación de los datos clara y comprensible. Recomendaría la aplicación a otros inversores por su eficiencia y precisión en el análisis de datos financieros. Sugirió implementar tutoriales interactivos para nuevos usuarios y mejorar algunos aspectos de la interfaz de usuario para incrementar la usabilidad, reafirmando su satisfacción general con la aplicación.

![Imagen extraída de Microsoft Video](src/img/cap5/imagen4.png)

| Nombre               | Alex Martinez            |
|----------------------|--------------------------|
| Edad                 | 24 años                  |
| Ubicación Geográfica | Lima, Perú (Santa Anita) |
| Profesión            | Inversor                 |
| Timing Entrevista    | [42:42 - 47:11]          |

**Resumen de Entrevista:**

Alex Martinez, de 24 años, inversor residente en Lima, Perú (Santa Anita), tuvo una impresión inicial muy positiva de la aplicación DeltaTech, destacando su facilidad de uso y la claridad de la información presentada. Los aspectos más valiosos para sus decisiones de inversión fueron los análisis detallados y la rapidez con la que se generan los informes. Encontró especialmente innovadora y útil la herramienta de evaluación de riesgos financieros. No experimentó dificultades significativas al navegar por la aplicación, señalando que es fácil encontrar la información necesaria. Alex cree que la aplicación ayuda a evaluar el riesgo financiero de manera efectiva y describió la calidad y precisión de los informes generados como alta. Mencionó que puede obtener la información necesaria para sus evaluaciones de manera rápida. Considera que la aplicación facilita la comprensión de los datos financieros para la toma de decisiones y destacó la organización de las funciones como muy intuitiva. Sugirió mejorar algunos aspectos de la interfaz de usuario para hacerla aún más accesible. Cree que la aplicación podría mejorar la eficiencia en la diligencia debida gracias a la automatización y la reducción del tiempo necesario para realizar análisis. Encuentra útil la función de automatización para sus análisis financieros y mencionó que la aplicación permite colaborar fácilmente con otros inversores o asesores financieros. Le gustaría ver funcionalidades adicionales, como herramientas de predicción y análisis de tendencias, en futuras versiones de la aplicación. Considera que la aplicación cubre sus necesidades actuales de due diligence, aunque siempre hay espacio para mejoras. Calificó el soporte y los recursos disponibles para resolver dudas o problemas técnicos como adecuados. Encuentra la presentación de los datos clara y comprensible. Recomendaría la aplicación a otros inversores por su eficiencia y precisión en el análisis de datos financieros. Sugirió implementar tutoriales interactivos para nuevos usuarios y mejorar algunos aspectos de la interfaz de usuario para incrementar la usabilidad, reafirmando su satisfacción general con la aplicación.

![Imagen extraída de Microsoft Video](src/img/cap5/imagen5.png)


| Nombre               | Marco Gutierrez          |
|----------------------|--------------------------|
| Edad                 | 25 años                  |
| Ubicación Geográfica | Lima, Perú (Lince) |
| Profesión            | Inversor                 |
| Timing Entrevista    | [47:11 - 55:04]          |

**Resumen de Entrevista:**

Marco Gutierrez, de 25 años, inversor residente en Lima, Perú (Lince), participó en una entrevista sobre la aplicación DeltaTech. Marco expresó una impresión inicial muy positiva de la aplicación, elogiando su facilidad de uso y la claridad de la información presentada. Destacó la utilidad de los análisis detallados y la rapidez en la generación de informes para tomar decisiones de inversión informadas. Marco consideró innovadoras y útiles las herramientas de evaluación de riesgos financieros proporcionadas por la aplicación. Durante la entrevista, señaló que no encontró dificultades significativas al navegar por la aplicación y que pudo acceder fácilmente a la información necesaria. Marco opinó que la aplicación facilita la comprensión de los datos financieros y destacó la organización intuitiva de las funciones. Sugirió algunas mejoras en la interfaz de usuario para hacerla aún más accesible. Además, cree que la aplicación podría mejorar la eficiencia en la diligencia debida gracias a la automatización de ciertos procesos. Marco encontró útil la función de automatización para sus análisis financieros y mencionó que la aplicación permite una colaboración fluida con otros inversores o asesores financieros. Expresó interés en ver funcionalidades adicionales, como herramientas de predicción y análisis de tendencias, en futuras versiones de la aplicación. En general, Marco considera que la aplicación cubre sus necesidades actuales de due diligence, aunque siempre hay margen para mejoras. Calificó el soporte y los recursos disponibles como adecuados y recomendó la aplicación a otros inversores por su eficiencia y precisión en el análisis de datos financieros. Sugirió implementar tutoriales interactivos para nuevos usuarios y mejorar algunos aspectos de la interfaz de usuario para incrementar la usabilidad.

![Imagen extraída de Microsoft Video](src/img/imagen123.png)

### Evaluaciones según heurísticas

**TAREAS A EVALUAR**

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Registro de un usuario
2. Visualización de proyectos
3. Creación de solicitud
4. Admisión de solicitudes
5. Visualización de solicitudes
6. Respuesta de solicitud
7. Visualización de archivos recibidos
8. Crear documentos
9. Crear preguntas
10. Crear respuestas
11. Visualizar preguntas

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Análisis financiero
2. Alerta de fugas de seguridad
3. Cifrado de datos
4. Creación de queja
5. Barra de búsqueda

**ESCALA DE SEVERIDAD:**
Los errores serán puntuados tomando en cuenta la siguiente escala de severidad

![Imagen extraída de PPT](src/img/cap5/tabla4.png)


**TABLA RESUMEN  SEGMENTO 1 SELL-SIDE:**
Web application

![Imagen extraída de PPT](src/img/cap5/tabla3.png)

**DESCRIPCIÓN DE PROBLEMAS:**

**PROBLEMA #1: Los botones del sidebar están desalineados**
Severidad: 2

Heurística violada: IA - Is it clear?

Problema:

En la parte izquierda del sidebar, se encuentran los botones para visualizar cada sección de la aplicación, sin embargo, los botones no se pueden apreciar de forma ordenada y clara.

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas6.png)

Recomendación:

Ajustar el tamaño y ordenar de los botones de forma alinead

**PROBLEMA #2: Los botones de la sección settings carecen de funcionalidad**

Severidad: 1

Heurística violada: IA - Is it usable?

Problema:

Se presentan botones para realizar ajustes y configuraciones en la aplicación, sin embargo estas etiquetas no realizan ninguna funcionalidad 

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas7.png)

**PROBLEMA #3: Botones que no tienen relación a la vista Due Diligence**

Severidad: 1

Heurística violada: Usability - Consistency and standards

Problema:

La existencia de un botón “New Question” no tiene relación con la vista seleccionada,por lo que el usuario estará desorientado.

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas8.png)


Recomendación:

Desarrollar una funcionalidad para omitir el botón o quitarlo,para que el usuario no pueda confundirse y desorientarse .


**TABLA RESUMEN SEGMENTO OBJETIVO 2 BUY SIDE:**

Web Application

![Imagen extraída de PPT](src/img/cap5/tabla2.png)


DESCRIPCIÓN DE PROBLEMAS:

**PROBLEMA #1: Los botones del sidebar están desalineados**
Severidad: 2

Heurística violada: IA - Is it clear?

Problema:

En la parte izquierda del sidebar, se encuentran los botones para visualizar cada sección de la aplicación, sin embargo, los botones no se pueden apreciar de forma ordenada y clara.

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas4.png)

Recomendación: 

Ajustar el tamaño y ordenar de los botones de forma alineada


**PROBLEMA #2: Los botones de la sección settings carecen de funcionalidad**

Severidad: 1

Heurística violada: IA - Is it usable?

Problema:

Se presentan botones para realizar ajustes y configuraciones en la aplicación, sin embargo estas etiquetas no realizan ninguna funcionalidad 

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas1.png)

Recomendación:

Desarrollar la funcionalidad de los botones para que el cliente pueda personalizar en la aplicación .


**PROBLEMA #3: El formulario para crear nueva área en la vista Project carece de funcionalidad**

Severidad: 3

Heurística violada: Usability - Consistency and standards

Problema:

Al seleccionar el botón new area proporciona un formulario no editable ,por lo que el usuario no podrá crear nuevas áreas y se frustrará.

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas9.png)

Recomendación:

Desarrollar una funcionalidad para que el formulario pueda permitir ingresar información y crear área, para que el usuario pueda continuar con el proceso due diligence.

DESCRIPCIÓN TABLA Landing page AMBOS SEGMENTOS : 

![Imagen extraída de PPT](src/img/cap5/tabla1.png)

**PROBLEMA #1: Las cards de la sección Features se encuentran desalineados**

Severidad: 1

Heurística violada: IA - Is it clear?

Problema:

En la parte inferior de la sección Essential features, se encuentran las cards de información de la aplicación, sin embargo, las cards no se pueden apreciar de forma ordenada .

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas3.png)

Recomendación:

Ajustar el tamaño y ordenar de los botones de forma alineada

**PROBLEMA #2: El botón de envío de información de la sección  Request a Demo carece de funcionalidad**

Severidad: 1

Heurística violada: Usability - Consistency and standards

Problema:

Dentro de la sección Request a Demo se presenta un cuadro para ingresar información de contacto en la aplicación, pero el botón de enviar carece de funcionalidad, lo cual puede generar disconformidad en el usuario. 

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas2.png)


Recomendación: 

Ingresar una funcionalidad para poder enviar al cliente un correo para poder coordinar un presupuesto en nuestra aplicación.


**PROBLEMA #3: Los botones de footer de contacto no funcionan**

Severidad: 1

Heurística violada: IA - Is it usable?

Problema:

En el footer, existen botones para ver las redes sociales, pero no se dirigen a lo que el cliente desea ver de la startup de la aplicación.

![Imagen extraída de DiligenceTech](src/img/cap5/heuristicas5.png)

Recomendación:
Añadir una dirección de link de cada red social de la startup.

## Video About-the-Product

Video About-the-Product, imagen extraída de Microsoft Stream: https://lc.cx/oFjvUE

# Conclusiones

## Conclusiones y recomendaciones

El proyecto de solución en aplicación web para un servicio de alojamiento especializado en Due Diligence ha demostrado ser una respuesta acertada a una necesidad creciente en el mercado. Desde la fase inicial de investigación, se confirmó la demanda y se validó la pertinencia del servicio. El diseño centrado en el usuario garantizó que las interfaces fueran intuitivas y funcionales, alineadas con los procesos de Due Diligence. La implementación por sprints permitió una adaptación ágil a medida que surgían nuevos requisitos, con una colaboración estrecha entre el equipo de desarrollo y los stakeholders. Se aplicaron altos estándares de calidad y seguridad en todas las etapas, asegurando la protección de los datos sensibles. Con la conclusión del primer sprint, se establece una base sólida para futuras iteraciones, marcando el inicio de un viaje continuo de mejora y expansión para mantener la competitividad y la relevancia del servicio en el mercado.

## Video *About-the-Team*

Video About-the-Team, imagen extraída de Microsoft Stream: https://lc.cx/D-1Svi

# Anexos

::: note
Video de exposición, para acceder hagla click en la URL: https://lc.cx/98woy_
:::
