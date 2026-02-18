

# Índice

1. [Objetivo principal de tu proyecto](#1-objetivo-principal-de-tu-proyecto)
  - [Herramientas a usar](#11-herramientas-a-usar)
2. [Descripción del proyecto](#2-descripción-del-proyecto)
3. [Descripción del Entorno de Desarrollo y Despliegue](#3-descripción-del-entorno-de-desarrollo-y-despliegue)
  - [Entorno de desarrollo](#31-entorno-de-desarrollo)
  - [Entorno de Despliegue](#32-entorno-de-despliegue)
4. [Estudio de Necesidades y Requisitos Funcionales](#4--estudio-de-necesidades-y-requisitos-funcionales)
  - [Requisitos Funcionales](#41-requisitos-funcionales)
  - [Requisitos No Funcionales](#42-requisitos-no-funcionales)
5. [Recursos y Planificación](#5-recursos-y-planificación)
  - [Planificación aproximada](#51-planificación-aproximada)
  - [Identificación y gestión de riesgos](#52-identificación-y-gestión-de-riesgos)
  - [Control de Versiones y Estrategia Modular](#53-control-de-versiones-y-estrategia-modular)
6. [Propuesta técnica](#6-propuesta-técnica)
  - [Capa de Percepción (Entrada)](#61-capa-de-percepción-entrada)
  - [Capa Cognitiva (Procesamiento)](#62-capa-cognitiva-procesamiento)
  - [Capa de acción y gestión (salidas)](#63-capa-de-acción-y-gestión-salidas)
  - [Stack tecnologico](#64-stack-tecnologico)
7. [Justificación de la propuesta](#7-justificación-de-la-propuesta)
8. [Implantación](#8-implantación)
  - [Requisitos de despliegue](#81-requisitos-de-despliegue)
  - [Proceso de instalación](#82-proceso-de-instalación)
9. [Viabilidad y Aspectos Económicos](#9viabilidad-y-aspectos-económicos)
  - [Empresa: MacedonIA Solutions](#91-empresa-macedonia-solutions)
  - [Presupuesto](#92-presupuesto)
    - [Hardware](#921-hardware)
    - [Software](#922-software)
    - [Total](#923-total)

# ANEXOS

- [ANEXO I: Manual de Usuario y Administración](#anexo-i-manual-de-usuario-y-administración)
  - [INSTALACIÓN Y DESPLIEGUE](#1-instalación-y-despliegue)
    - [Requisitos del sistema](#11-requisitos-del-sistema)
    - [Preparación del entorno](#12-preparación-del-entorno)
    - [Proceso de Instalación Automatizada](#13-proceso-de-instalación-automatizada)
    - [Verificación de la instalación](#14-verificación-de-la-instalación)
    - [Configuración del Modo Kiosk](#15-configuración-del-modo-kiosk)
  - [CONFIGURACIÓN DEL SISTEMA](#2-configuración-del-sistema)
  - [MANUAL DE USUARIO](#3-manual-de-usuario)
  - [MANUAL DE ADMINISTRACIÓN](#4-manual-de-administración)
  - [CONFIGURACION AVANZADA](#5-configuracion-avanzada)

- [ANEXO II: Manual Técnico de Despliegue](#anexo-ii-manual-técnico-de-despliegue)
  - [INTRODUCCIÓN TÉCNICA](#1-introducción-técnica)
  - [ARQUITECTURA INTERNA Y FLUJO DE DATOS](#2-arquitectura-interna-y-flujo-de-datos)
  - [INSTALACIÓN DE BAJO NIVEL](#3-instalación-de-bajo-nivel)
  - [RETOQUES Y OPTIMIZACIÓN DEL KERNEL](#4-retoques-y-optimización-del-kernel)
  - [SEGURIDAD AVANZADA](#5-seguridad-avanzada)
  - [ANEXOS TECNICOS](#8-anexos-tecnicos)

- [ANEXO III: Arquitectura Interna e Inteligencia Artificial](#anexo-iii-arquitectura-interna-e-inteligencia-artificial)
  - [INTRODUCCIÓN A LA COGNICIÓN ARTIFICIAL](#1-introducción-a-la-cognición-artificial)
  - [ARQUITECTURA COGNITIVA](#2-arquitectura-cognitiva)
  - [COMPRENSIÓN DEL LENGUAJE NATURAL (NLU)](#3-comprensión-del-lenguaje-natural-nlu)
  - [EL "CEREBRO" (SISTEMAS DE MEMORIA)](#4-el-cerebro-sistemas-de-memoria)
  - [INTELIGENCIA GENERATIVA (LLM)](#5-inteligencia-generativa-llm)
  - [PROCESAMIENTO DE SEÑALES (LOS SENTIDOS)](#6-procesamiento-de-señales-los-sentidos)
  - [COGNICIÓN MULTI-AGENTE](#7-cognición-multi-agente)
  - [CASOS DE ESTUDIO DE INTERACCIÓN](#8-casos-de-estudio-de-interacción)
  - [REFERENCIA DE API INTERNA (AI MODULES)](#9-referencia-de-api-interna-ai-modules)
  - [REFERENCIA DE CONFIGURACIÓN (AI)](#9-referencia-de-configuración-ai)
  - [HOJA DE RUTA DE IA](#10-hoja-de-ruta-de-ia)

- [ANEXO IV: Resolución de Problemas](#anexo-iv-resolución-de-problemas)
  - [PROBLEMAS DEL USUARIO FINAL](#1-problemas-del-usuario-final)
  - [PROBLEMAS DE INGENIERÍA Y DESPLIEGUE](#2-problemas-de-ingeniería-y-despliegue)
  - [PROBLEMAS DEL SISTEMA DE IA Y LOGICA](#3-problemas-del-sistema-de-ia-y-logica)
  - [CÓDIGOS DE ERROR INTERNOS](#4-códigos-de-error-internos)

- [ANEXO V: Programación y Creación de Skills](#anexo-v-programación-y-creación-de-skills)
  - [INTRODUCCIÓN](#1-introducción)
  - [ARQUITECTURA DEL SISTEMA DE SKILLS](#2-arquitectura-del-sistema-de-skills)
  - [CREACIÓN DE UNA NUEVA SKILL](#3-creación-de-una-nueva-skill)
  - [ACCESO AL NÚCLEO (NEOCORE)](#4-acceso-al-núcleo-neocore)
  - [BUENAS PRÁCTICAS DE DESARROLLO](#5-buenas-prácticas-de-desarrollo)
  - [SKILLS EXISTENTES](#6-skills-existentes)
  - [DESARROLLO COMUNITARIO (Watermelon-extras)](#7-desarrollo-comunitario-watermelon-extras)

- [ANEXO VI: Pruebas de Validación y Rendimiento](#anexo-vi-pruebas-de-validación-y-rendimiento)
  - [INTRODUCCIÓN](#1-introducción)
  - [PRUEBAS UNITARIAS Y DE COMPONENTES](#2-pruebas-unitarias-y-de-componentes)
  - [PRUEBAS DE INTEGRACIÓN (FLUJO COMPLETO)](#3-pruebas-de-integración-flujo-completo)
  - [PRUEBAS DE RENDIMIENTO Y ESTRÉS](#4-pruebas-de-rendimiento-y-estrés)
  - [CONCLUSIONES DE LAS PRUEBAS](#5-conclusiones-de-las-pruebas)

- [ANEXO VII: Retos de Desarrollo y Soluciones Adoptadas](#anexo-vii-retos-de-desarrollo-y-soluciones-adoptadas)
  - [INTRODUCCIÓN](#1-introducción)
  - [RETOS DE AUDIO Y LATENCIA](#2-retos-de-audio-y-latencia)
  - [RETOS DE INTELIGENCIA ARTIFICIAL (LLM)](#3-retos-de-inteligencia-artificial-llm)
  - [CONCLUSIÓN](#5-conclusión)

- [ANEXO VIII: Despliegue](#anexo-viii-despliegue)
  - [INTRODUCCIÓN](#1-introducción)
  - [PREPARACIÓN DEL HARDWARE](#2-preparación-del-hardware)
  - [DESPLIEGUE DE DEBIAN](#3-despliegue-de-debian)
    - [Instalación del Sistema](#31-instalación-del-sistema)
    - [Despliegue del Servicio](#32-despliegue-del-servicio)
    - [Instalacion Automatizada](#321-instalacion-automatizada)
    - [Personalizacion](#322-personalizacion)
    - [Configuración de la base de datos](#323-configuración-de-la-base-de-datos)
    - [Systemd, HTTPS y sudoers](#324-systemd-https-y-sudoers)
  - [INTERFAZ WEB](#4-interfaz-web)
    - [La "Cara"](#41-la-cara)
    - [WebUI](#42-webui)
    - [Dashboard](#421-dashboard)
    - [Monitor del sistema](#422-monitor-del-sistema)
    - [Herramientas de red](#423-herramientas-de-red)
    - [Terminal del sistema](#424-terminal-del-sistema)
    - [Logs](#425-logs)
    - [Acciones](#426-acciones)
    - [Gestor de tareas (Cron)](#427-gestor-de-tareas-cron)
    - [Explorador de archivos](#428-explorador-de-archivos)
    - [Gestor de extensiones](#429-gestor-de-extensiones)
    - [NLU](#4210-nlu)
    - [MQTT](#4211-mqtt)

- [ANEXO IX: Documentación de Modelos Personalizados Grape](#anexo-ix-documentación-de-modelos-personalizados-grape)
  - [GRAPE ROUTER (Router Clasificador)](#1-grape-router-router-clasificador)
  - [MODELOS GRAPE (Modelos T5 de Ejecución)](#2-modelos-grape-modelos-t5-de-ejecución)

- [ANEXO X: Referencias y Bibliografía](#anexo-x-referencias-y-bibliografía)
  - [LIBRERÍAS Y SOFTWARE OPEN SOURCE](#1-librerías-y-software-open-source)
  - [DOCUMENTACION USADA](#2-documentacion-usada)
  - [RECURSOS ADICIONALES](#3-recursos-adicionales)

- [GLOSARIO DE TÉRMINOS TÉCNICOS](#glosario-de-términos-técnicos)

---

**Anteproyecto:**
# 1. Objetivo principal de tu proyecto

   La creación de  un asistente de voz inteligente con un  bajo consumo de recursos, diseñado para ayudar a los administradores de sistemas en sus tareas de administración y gestión de sistemas, funcionando al completo de manera local para garantizar la propiedad de los datos.

   Este proyecto busca cubrir la necesidad de un asistente capaz de hacer tareas de administración así como de ejecutar comandos que el  usuario pida usando lenguaje natural, sin depender de una conexión a internet ni servicios de terceros. A diferencia de un asistente normal, con OpenMacedonIA se busca:

* **Inteligencia Híbrida:** Haciendo uso de una arquitectura de varios modelos con un router que categoriza la entrada de audio en las diferentes opciones que el sistema es capaz de manejar, permitiendo tener varios modelos cada uno especializado en un tema sin saturar el sistema y manteniendo una buena velocidad en las respuestas
* **Seguridad proactiva:** El sistema es capaz de detectar intrusiones y anomalías en el sistema en tiempo real por medio de un sistema IDS e informar al usuario de ello
* **Eficiente:** Se ha optimizado para funcionar en hardware modesto y de hace unos años (Procesador de 2 nuceos y 8Gb de ram), para permitir el despliegue en servidores de bajos recursos o estaciones de trabajo

## 1.1. Herramientas a usar

* **Lenguajes de Programación:**
  * **Python 3.10:** Lenguaje principal del sistema y los módulos, se ha elegido una versión más antigua porque ofrece más compatibilidad con librerías antiguas de python
  * **ShellScript:** Para los scripts de despliegue y automatización, así como para los datasheet de entrenamiento de la IA
  * **HTML/CSS/JS:** Para la interfaz web
* **Inteligencia Artificial:**
  * **Conversaciones:** Gemma 2B mediante llama-cpp-python, usada para responder preguntas avanzadas o de temas ajenos a generar comandos (Modulo **BrainNut**)
  * **Comandos:** Grape-models (creados para este proyecto) mediante transformers, para traducir de lenguaje natural a Bash
  * **Voz:** Vosk y Piper, para la entrada y salida de voz
* **Frameworks:**
  * **Web:** Flask, como servidor web ejecutado desde python
  * **Visión Artificial:** OpenCV para la detección de presencia (desactivado por defecto)
  * **Sistema:** systemd, para la gestión de procesos del sistema

# 2. Descripción del proyecto

OpenMacedonIA nace de la necesidad de un asistente personal, privado y autónomo, centrado en la administración de sistemas. La idea principal de su diseño es que no tuviera ninguna dependencia de la nube, para así garantizar el principio de que son nuestros datos y no de las empresas.

El desarrollo se basa en tres pilares:

* **Privacidad y soberanía de datos**, a diferencia de asistentes comerciales OpenMacedonIA está diseñado para ser ejecutado en local, permitiendo adaptarse al hardware, desde el más modesto hasta servidores muy potentes. Todo el procesamiento se realiza de manera local y no depende de internet para funcionar.
* **Eficiente,** una de las ideas principales era que pudiera ejecutarse de una manera fluida en hardware modesto, esto es ya que hay administradores de sistemas con acceso a hardware potente pero hay otros más aficionados con hardware más modesto, la optimización de OpenMacedonIA permite ejecutarse en sistemas de recursos limitados
* **Modular,** otra función clave es su capacidad de ampliación, el uso de python y librerías código abierto permiten que cualquiera expanda las funciones del sisrema con módulos adaptados a sus necesidades

**Evolución del proyecto:**

En los inicios este proyecto se llamó OpenKompaiNano, diseñado para ser un asistente proactivo que acompañase a las personas mayores este disponía de una interfaz grafica de botones que fue eliminada para centrar los recursos en otras partes del sistema , después se renombró a Neo Nano, mantiene la base de código de su antecesor pero se enfoca en la administración de sistemas, no era inteligente solo comparaba la entrada de voz del usuario con una serie de respuestas predefinidas, finalmente el proyecto se terminó de llamar COLEGA y posteriormente OpenMacedonIA, este ultimo se plantea ya que los componentes tienen nombre de fruta y todos juntos hacen una Macedonia, Open es por que el proyecto es codigo abierto (y por que macedonIA ya estaba cogido en Github).

# 3. Descripción del Entorno de Desarrollo y Despliegue

## 3.1 Entorno de desarrollo

En un primer momento se probó a usar como sistema operativo base Fedora Linux, pero al ser una distribución con las ultimas novedades en cuanto a software, muchas de las dependencias y librerías entraban en conflicto entre sí, por eso finalmente se ha optado por Debian, que usa versiones más antiguas pero más estables. Podemos resumir que el sistema operativo de **despliegue es Debian** pero podría ser instalada en Ubuntu o Fedora.

Para el desarrollo se ha usado principalmente Python 3.10, una versión algo más vieja a la actual python 3.14, pero con mayor compatibilidad con las librerias de IA y estabilidad

**Principales utilidades usadas:**

* **Gestión de dependencias:** *pip*, *uv* y *venv* este último para el aislamiento de paquetes
* **Control de versiones:** *Git* y *Github*
* **Librerías de Python Principales:** *torch,* para la IA, *vosk,* para la voz a texto, *flask,* para el servidor Web

## 3.2 Entorno de Despliegue

Para desplegar el proyecto, se están usando tres dispositivos diferentes cada uno con un uso final diferente:

* **Nodo Principal:** Lenovo Yoga 530-14IKB
> Este dispositivo ha muerto, se esta usando una maquina virtual que replica sus caracteristicas
	
* **Procesador:** Intel Core I3-7020U (2 núcleos / 4 hilos)
* **RAM:** 8Gb DDR4
* **Almacenamiento:** 128Gb Nvme
* **Uso:** Ejecuta el Núcleo principal (**NeoCore**), los modelos Gemma y Mango y el servidor Web (**TangerineUI**).

* **Agente Satélite:** Raspberry Pi 4B
	* **Procesador:** Broadcom BCM2711
	* **RAM:** 4Gb
	* **Almacenamiento:** 32Gb MicroSD
	* **Uso:** Se va a usar como agente, depende del procesamiento del núcleo principal.
	
* **Sensor IoT:** ESP32-WROOM-32E
	* **Procesador:** Xtensa dual-core
	* **RAM:** 520KB + 16Kb
	* **Almacenamiento:** 448Kb
	* **Uso:** Va a ser el segundo agente, se va a usar como sensor simplemente para demostrar las capacidades del protocolo MQTT.

# 4.  Estudio de Necesidades y Requisitos Funcionales

El proyecto como se ha comentado en puntos anteriores, busca cubrir las necesidades de los administradores de sistemas (no sustituir), es un compañero, trabaja en colaboracion con ellos. El ejemplo más fácil para esto es, mientras el administrador de sistemas hace una tarea (arreglar un servidor, o desplegar un kubernetes), el asistente OpenMacedonIA, puede ayudar en el proceso, por ejemplo dándole datos del estado de servicios, espacio en disco incluso el mismo podrá desplegar ese kubernetes. Algunas de las necesidades de mercado que cubre son:

* **No depende de una nube** para funcionar, en un corte de red el asistente sigue funcionando, aparte de dar control total al usuario o empresa sobre sus datos
* **Capacidades técnicas**, mientras que los asistentes de hoy en día están diseñados, para el consumo diario, este está diseñado para interactuar de manera nativa tanto con las herramientas como con los tecnicismos de los administradores.
* **Personalización ilimitada**, su naturaleza código abierto, la documentación y el uso de python permiten a cualquiera expandir las capacidades del proyecto y adaptarlas a sus necesidades
* **“Manos Libres”:** Permite consultar el estado de un servicio o ejecutar un script mientras se está haciendo un mantenimiento físico al sistema

## 4.1 Requisitos Funcionales

1. **Interaccion y comunicacion**:
	   - **Reconocimiento de Voz:** El sistema debe ser capaz de transcribir audio a texto en tiempo real sin depender de servidores externos
	   - **Síntesis de Voz:** El sistema debe generar respuestas de audio inteligentes con una voz casi natural
2. **Inteligencia y Razonamiento:**
	   - **Procesamiento de lenguaje natural:** Debe ser capaz de entender que quiere hacer el usuario, basándose en los módulos que ya tiene predefinidos
	   - **Generación de Respuestas:** Debe integrar un modelo de LLM que pueda mantener conversaciones fluidas (limitado al hardware)
	   - **Memoria:** Debe tener una memoria que recuerde datos y que le permita responder a preguntas específicas sobre un equipo o proyecto
3. **Control y Administración:**
	   - **Gestión del Sistema Operativo:** El asistente será capaz de ejecutar comandos en el sistema
	   - **Herramientas de red:** El asistente será capaz de usar herramientas de red (ping, dig, whois, nmap, etc)
	   - **Control IoT:** El asistente será capaz de integrarse con el protocolo MQTT para usar dispositivos IoT
	   - **Gestión básica:** Debe ser capaz de ejecutar funciones básicas (temporizador, alarmas, recordatorios)
	   - **Seguridad:** Debe ser capaz de detectar anomalías e intentos de intrusión

## 4.2 Requisitos No Funcionales

Son requisitos que le pongo para lograr el objetivo pero que no agregan funcionalidades al sistema.

1. **Privacidad Total:** Ningún dato de ningún tipo saldrá nunca del asistente, si no es capaz de funcionar en local, no sirve.
2. **Eficiencia:** El sistema completo debe ser capaz de funcionar en hardware de recursos limitados sin bloquearse (6-8Gb de ram)
3. **Tiempo de respuesta:** El tiempo de respuesta del sistema debe ser, para comandos definidos en los módulos (< 1s), para interacciones con Grape (<1 - 2s) para interacciones con el LLM (< 5 -10s)
4. **Modularidad:** La arquitectura debe permitir agregar módulos o cambiar componentes sin tener que reescribir todo el código
5. **Disponibilidad sin red:** El sistema mantendrá una funcionalidad mínima incluso sin tener conexión a la red, pudiendo mantener comunicación con dispositivos IoT
6. **Resiliencia:** Capacidad de recuperarse de manera automática ante fallos

# 5. Recursos y Planificación

Los recursos de hardware a usar se han descrito en el apartado 3.2. Si hablamos de otros recursos nos encontramos que este proyecto ha sido desarrollado en conjunto con un agente de Inteligencia Artificial, podríamos definir que del total de código del proyecto alrededor del 40% ha sido desarrollado en exclusiva por un modelo de inteligencia artificial, siendo usado este en el desarrollo de la interfaz web y sus animaciones, el módulo NeoGuard, el protocolo BCP (no soy ingeniero como para desarollar un protocolo entero), el despliegue de algoritmos avanzados y las optimizaciones y resolución de problemas. El otro total de código ha sido desarrollado por una única persona apoyándose en librerías de código abierto, documentación online, foros de internet y conocimientos que se tenían de antes

## 5.1 Planificación aproximada:

1. **Fase 1 (Completada):** Primer prototipo funcional, reconocimiento de voz y ejecución de comando básica
2. **Fase 2 (Completada):** Desarrollo de la arquitectura modular, integración con Gemma y primera interfaz web
3. **Fase 3 (Completada):** Implementación de Nut, desarrollo y despliegue de NeoGuard y optimización del sistema
4. **Fase 4 (Completada):** Soporte de nodos de red, implementación de la visión por ordenador
5. **Fase 5 (En Pruebas):** Protocolo BCP, integracion con MQTT

## 5.2. Identificación y gestión de riesgos

Dado el poco tiempo que hay para el proyecto y los desafíos técnicos que conlleva, estos son algunos de los riesgos que pueden surgir:

- Incompatibilidad de las dependencias
- Fallos en el reconocimiento de voz
- Dificultad para entender tecnologías nuevas
- Cuellos de botella en el rendimiento
- Alucinaciones del LLM

## 5.3 Control de Versiones y Estrategia Modular

Para garantizar el mantenimiento y escalabilidad del proyecto OpenMacedonIA, se ha adoptado una estrategia de desarrollo modular, separando componentes críticos en repositorios independientes. Esto permite actualizaciones granulares y facilita la colaboración.

* **WatermelonD (Core):** Repositorio principal que contiene el nucleo principal `NeoCore`, el gestor de audio y la integración básica.
* **BrainNut:** Módulo de Inteligencia Artificial que gestiona los modelos LLM (Gemma y Grape) y la lógica de razonamiento. Se mantiene separado para permitir actualizaciones de su logica sin tocar el núcleo.
* **TangerineUI:** Interfaz Web moderna y reactiva. Permite actualizarse sin romper el backend
* **BlueberrySkills:** Repositorio de habilidades. Permite agregar funcionalidades extra al sistema sin tocar el nucleo
* **WatermelonExtras:** Extensiones que no son esenciales para que el sistema funcione y se pueden instalar como añadidos

# 6. Propuesta técnica

El sistema denominado OpenMacedonIA esta basado en la arquitectura de OVOS pero modificado para usar una arquitectura modular que se ha diseñado para ejecutar varios LLM segun la necesidad del usuario

A diferencia de los asistentes  tradicionales, el sistema se estructura sobre un orquestador **NeoCore** que gestiona la comunicación entre módulos independientes. La arquitectura del sistema se dividen en tres capas:

## 6.1 Capa de Percepción (Entrada):

* **Lime-Voice (Voice Manager):** RResponsable de convertir de audio a texto (STT). Hace uso de Vosk o Sherpa-ONNX, que funciona de manera completamente offline, implementa un sistema de gramáticas dinámicas para restringir el vocabulario a lo que el sistema debe reconocer y asi aumentar la precisión, incorpora un VAD (Detector de actividad de voz), para solo procesar cuando detecta la palabra de activacion
* **Visión Manager:** (Opcional) Detección de presencia y reconocimiento facial mediante OpenCV.

## 6.2 Capa Cognitiva (Procesamiento):

* **Grape-Route (Decision Router):** Un modelo de clasificacion basado en **Transformers (BERT)** que analiza la entrada de voz y la enruta al módulo adecuado (Sistema, Conversación, IoT, etc.), reemplazando los sistemas de coincidencia difusa.
* **BrainNut (AI Engine):** El núcleo que se encraga de la inteligencia. Integra:
	  * **Gemma 2B (LLM):** Para razonamiento complejo y conversación general.
	  * **BrainNut-T5 (antes Mango):** Modelos entrenados para la traducción de lenguaje natural a comandos Bash (nl2bash)
* **Memoria (RAG):** Sistema basado en ChromaDB/SQLite para almacenamiento de documentación y contexto

## 6.3 Capa de acción y gestión (salidas):

* **BlueberrySkills:** Colección de habilidades (SysAdmin, Network, Docker) que ejecutan las acciones finales.
* **Altavoz (TTS):** Motor de síntesis de voz basado en Pipper, genera una voz casi humana
* **TangerineUI:** Interfaz Web y panel de control visual para administración remota.

## 6.4 Stack tecnologico

El stack tecnológico busca en su totalidad apoyarse en tecnologías código abierto y que permiten la fácil escalabilidad del sistema:

- **Lenguajes de programación:** El lenguaje principal es Python 3.10, debido que es el lenguaje predominante a la hora de trabajar con Inteligencia Artificial y tiene una capacidad nativa para trabajar con sistemas Linux. En cuanto a lenguajes secundarios, usamos Shell Script para la automatización de la instalación, SQL para la gestión de la base de datos, HTML y CSS para la interfaz web
- **Hardware Base:** En principio se optó por una raspberry pi por su bajo consumo y pequeño tamaño, pero al final se está usando un viejo PC Lenovo Yoga 530-14ikb. Finalmente debido a que el pc no ha podido mas se esta usando una maquina virtual con dos nucleo y 7Gb de ram
- **Backend Web:** Se usa un servidor flask desplegado desde python
- **Gestión de procesos:** Para la gestión pocesos del sistema y del asistente se usa systemd integrado en sistemas Linux
- **Frameworks de IA:** Pytorch y Llama.cpp
- **Entrenamiento de modelos**: Google Colab Pro, con los kernels T4 y L4

# 7. Justificación de la propuesta

Este sistema solventa tres necesidades críticas en la Administración de sistemas:

1. **Soberanía de Datos y Seguridad:** En entornos donde los datos son criticos, el uso de asistente comerciales (Alexa, Google Assistant), pone en riesgo la seguridad de los mismos, con WatermelonD se garantiza que todos los datos sean procesados de manera local.
2. **Manos libres en entornos técnicos:** Un administrador de sistemas a menudo realiza tareas físicas donde el acceso a un teclado puede ser difícil. Con WatermelonD pueden hacer consultas sobre el estado de un sistema, recibir información de red o desplegar contenedores, optimziando las tareas que realiza
3. **Código Abierto:** Su código abierto y su arquitectura modular permiten que se agreguen plugins y nuevas características con solo un par de líneas de código, esto permite a los administradores, personalizar el sistema a sus necesidades

# 8. Implantación

## 8.1 Requisitos de despliegue

El despliegue del sistema requiere de un entorno Linux compatible con una arquitectura x86_64. Los requisitos mínimos son los siguientes:

- **Sistema Operativo:** Debian 11/12
- **Hardware:**
	  - **RAM:** Mínimo 6Gb (LLM Ligero Phi3 o TinyLlama ). Recomendado 8GB
	  - **CPU:** Procesador x86_64 compatible con el set de instrucciones AVX2
	  - **Disco Duro:** SSD o Nvme 64Gb mínimo
	- **Conectividad:** Para la primera instalación se requiere una conexión a internet estable ya que hay que descargar una gran cantidad de datos

## 8.2 Proceso de instalación

El proceso de instalación se ha simplificado mediante un script grafico (install.sh) que hace uso de whiptail para mostrar una interfaz mas amigable, que automatiza todo el despliegue del sistema:

1. **Detección y preparación:** El script detecta la distribución Linux (Debian/Ubuntu u Otro) y procede segun lo que detecte
2. **Entorno aislado:** Se configura un entorno virtual de python (venv) para evitar conflictos con librerías del sistema.
3. **Descarga de modelos:** Se obtienen y verifican mediante hash los modelos de inteligencia artificial, modelos acústicos y voces.
4. **Demonización:** Se genera una archivo de systemd, para que el asistente se inicie automáticamente con el sistema

# 9.Viabilidad y Aspectos Económicos

## 9.1 Empresa: MacedonIA Solutions

Somos una empresa tecnológica enfocada en el uso de la inteligencia artificial para Pymes y departamentos de IT buscamos crear herramientas seguras y fáciles de usar que reduzcan la carga de trabajo en los administradores de sistemas.
**Modelo de Negocio:**

- **Consultoría:** Despliegue de asistentes OpenMacedonIA personalizados en la infraestructura del cliente
- **Soporte Técnico:** Mantenimiento, actualización de modelos y resolución de incidencias
- **Personalización:** Desarrollo de skills personalizadas a medida para integrar sistemas y herramientas en OpenMacedonIA

## 9.2 Presupuesto

A continuación se detallan el coste aproximado del desarrollo del prototipo funcional de este proyecto.

### 9.2.1 Hardware

| Concepto                   | Modelo                    | Coste     | Notas       |
| :------------------------- | :------------------------ | :-------- | :---------- |
| **Nodo Central**     | Lenovo Yoga 530           | 0,00 eur  | Reutilizado |
| **Agente Satélite** | Raspberry pi 4B           | 60,00 eur |             |
| **Sensor IoT**       | ESP32                     | 4,00 eur  |             |
| **Tarjeta SD**       | Samsung 64Gb              | 12,00 eur |             |
| **Varios**           | Cables, periféricos, etc | 20,00eur  |             |
| **Total**            |                           | 96,00 eur |             |

### 9.2.2 Software

| Concepto                      | Descripción     | Coste     | Notas        |
| :---------------------------- | :--------------- | :-------- | :----------- |
| **Entrenamiento de IA** | Google Colab Pro | 11,99 eur | 100 unidades |
| **DataSheets**          | HugguinFace Pro  | 9,00 eur  |              |
| **Total**               |                  | 20,99 eur |              |

### 9.2.3 Total

| Concepto           | Coste      |
| :----------------- | :--------- |
| **Hardware** | 96,00 eur  |
| **Software** | 20,99 eur  |
| **Total**    | 116,99 eur |

# ANEXO I: Manual de Usuario y Administración

## 1. INSTALACIÓN Y DESPLIEGUE

## 1.1 Requisitos del sistema

Para garantizar que todo funcione de manera fluida, especialmente el modelo LLM Gemma, se deben cumplir una serie de requisitos

### 1.1.1 Hardware

* **Procesador:**
	* *Arquitectura*: x86_64 (PC/Portátil)
	* *Instrucciones*: Se recomienda un procesador con soporte para **AVX2**
	* *Nucleos*: Minimo 2 nucleos fisicos
* **Memoria Ram:**
	* *Mínimo*: 6Gb (El sistema irá lento y se necesitaría usar un modelos mas ligero como Phi3)
	* *Recomendado*: **8Gb** o más
* **Almacenamiento:**
	 * **SSD** (SATA o NVMe)
	 * *Espacio*: Mínimo 32Gb. Se recomienda 64Gb o más
* **Periféricos:**
	 * Micrófono
	 * Altavoces
	 * Cámara (Opcional)
	 * Pantalla (Opcional)

### 1.1.2 Software

* **Sistema Operativo:**
	* **Debían 11/12** (Recomendado para la mayor estabilidad)
	* **Ubuntu 22.04/24.04 LTS** (Soportado)
	* **Raspberry Pi OS (64-Bit)** (El soporte de ARM es experimental)
	* **Fedora 40+** (Soporte experimental)
* **Dependencias base:** curl wget git python3
> Se recomienda un sistema operativo sin interfaz grafica



## 1.2 Preparación del entorno

Antes de comenzar la instalación, debemos:

> Esta guía asume un sistema Debian para la instalación

1. **Actualizar el sistema:**
```bash
sudo apt update && sudo apt upgrade -y  
```

2. **Instalar las dependencias base:**
```bash
sudo apt install curl python3 -y  
```

3. **Clonar el repositorio:** (Se recomienda clonar el repositorio en el directorio del usuario y no clonarlo en root).
```bash
cd ~
git clone https://github.com/OpenMacedonIA/WatermelonD.git
cd WatermelonD
```
## 1.3 Proceso de Instalación Automatizada

El repositorio de Git incluye un script de instalación **install.sh**, que automatiza la configuración. Este script realiza lo siguiente:

1. Detecta la distribución Linux (Sistemas Debian o sistemas no Debian)
	- Si no es un sistema debian, instala y configura un distrobox con una imagen de debian y procede con la instalación (Experimental)
	- Si es debian procede con la instalación normal
2. Instala todas las dependencias del sistema
3. Instala y configura **Pyenv**
4. Instala **Python 3.10**
5. Crea un entorno virtual (venv) e instala las dependencias desde el requirements.txt
6. Descarga los modelos:
   * Vosk (Reconocimiento de voz),
   * Sherpa-ONNX (Si el usuario lo selecciona)
   * Piper (síntesis de voz),
   * Gemma 2B (LLM).
   * Grape-Models
   * lemon-route
7. Configura el servicio **systemd** para ejecutar el servicio al arranque del sistema

**Ejecución del script:**
```bash
chmod x install.sh && .install.sh
```

> El script solicitara la contraseña de administrador cuando sea necesario
## 1.4 Verificación de la instalación

Para comprobar que todo se ha instalado correctamente, podemos usar estos comandos:

* **Comprobar el servicio:**
```bash
systemctl –user status neo.service  #Debería aparecer como active (running).  
```

* **Verificar Logs en tiempo real:**
```bash
journalctl –user -u neo.service -f #Buscar "Neo Core iniciado"
```

> Después de la instalación debemos reiniciar el sistema.

## 1.5 Configuración del Modo Kiosk

Si se dispone de una pantalla conectada, el instalador  puede configurar un modo “Kiosco” para mostrar la UI del asistente al inicio del sistema

El script configura:
* Auto-login en la terminal ``tty1``
* Inicio automático del servidor gráfico (``startx``)
* Lanzamiento de chromium en pantalla completa apuntando a ``http://localhost:5000/face``

> Podemos desactivar esto desde el fichero `~/.xinitrc`.

## 2. CONFIGURACIÓN DEL SISTEMA

### 2.1 Archivo de configuración Principal (`config.json`)

Toda la configuración se almacena en `config/config.json`.Este archivo se genera automáticamente en la instalación y se puede modificar para personalizar el sistema

**Estructura básica:**
```json
{
    "decision_router": { 
        "enabled": true,
        "model_path": "models/lemon-route", 
        "confidence_threshold": 0.6
    },
    "wake_words": [
        "neo",
        "tio",
        "bro",
        "melon"
    ],
    "secret_key": "", //Dejar vacio el sistema la genera
    "stt": {
        "engine": "vosk",
        "input_device_index": null
    },
    "web_admin": {
        "host": "0.0.0.0",
        "port": 5000, // Aunque este aqui para cambiarse el puerto, se recomienda no hacerlo
        "debug": false
    },
    "audio": {
        "jack_no_start_server": "1",
        "driver": "alsa"
    },
    "ai_model_path": "models/gemma-2b-it-q4_k_m.gguf", // Desde aqui podemos cambiar el modelo LLM 
    "vision_enabled": false, // Aqui podemos activar la vision por ordenador
    "experimental": {
        "voice_auth_enabled": false // La autenticacion por huella de voz es experimental y falla bastante
    },
    "admin_pass": "admin"
}
```

### 2.2 Personalización de la Palabra de Activación
Para cambiar el nombre al que responde el asistente:

1. Editamos `config/config.json`
2. Modificamos el valor de “wake word”. Puede ser una lista de palabras
```json
"wake_word": ["colega", "tío", "juan","wamd"]
```
3. Reiniciamos el servicio:
```bash
systemctl –user restart neo.service
```

### 2.3 Configuración de Modelos de IA
* **LLM (Gemma):** La ruta al modelo *.gguf* se define en `ai_model_path`. Si se quiere cambiar el modelo, se descargaría uno diferente en la ruta `models/` y se actualizará la ruta en el json
* **Voz (Piper):** Los modelos de voz se encuentran en `piper/`. Para cambiar la voz se debe descargar el modelo *.onnx* y su *.json* correspondiente, y actualizar todas las referencias en el código (Actualmente no se permite cambiar la voz de manera fácil)

### 2.4 Configuración de Red y MQTT
El proyecto, utiliza MQTT para comunicarse con otros dispositivos (BerryConnect)

* **Broker** usa por defecto `localhost`. Si ya se tiene un broker central en la red, cambia `"broker": "IP_DEL_BROKER"`.
* **Topic Base:** Los agentes publican en `home/agents/{hostname}/...`.

### 2.5 Gestión de Usuarios y Permisos
El asistente se ejecuta en modo usuario. Esto lo hace más seguro que ejecutarlo como root. Algunas acciones pueden requerir permisos de administracio . Se puede usar la utilidad ` polkit`  para gestionar estos permisos

## 3. MANUAL DE USUARIO

### 3.1 Interacción por Voz
La forma principal de interactuar es mediante la voz (aunque se puede también por texto mediante la UI), haciendo uso de la palabra de activación seguido de lo que le queramos pedir

#### 3.1.1 Comandos de Sistema
* **Apagar / Reiniciar**: "Wamd, apaga el sistema”, “Wamd, reinicia el ordenador”
* **Estado:** “Wamd, ¿como estas?”, “Wamd, dame un diagnóstico del sistema”
* **Volumen:** "Wamd, sube el volumen", "Wamd, silencio".

#### 3.1.2 Comandos de Red y SSH
* **IP Pública:**  "Wamd, ¿cuál es mi IP pública?"
* **Escaneo de Red:** "wamd, escanea la red en busca de intrusos"
* **Ping:** "wamd, haz un ping a [google.com](http://google.com)"
* **SSH:** "wamd, conéctate al servidor de pruebas", "wamd, ejecuta 'ls -la' en el servidor produccion"

#### 3.1.3 Comandos de Organización
* **Alarmas:** “Wamd, pon una alarma a las 8 de la mañana”
* **Temporizador:** “Wamd, pon un temporizador de 10 minutos”
* **Calendario:** “Wamd, que hay en mi agenda”

#### 3.1.4 Comandos de contenedores (Docker)
* **Estado**: "Wamd, ¿Que contenedores hay?", "Wamd, dime los dockers activos", " wamd, lista de contendores".
* **Gestion**: "wamd, reinicia el contendor Apache", "wamd, para el contenedor de base de datos"

> Comandos críticos requerirán confirmación por parte del usuario ("¿Seguro que quieres eliminar...?").

#### 3.1.5 Otros Comandos (Grape-Models)
* **Busqueda**: "Wamd, búscame el archivo imagen.png"
* **Directorios y archivos**: "Wamd, muevete al directorio /etc", "wamd, listame los archivos en /home"
* **Red**: "Wamd, haz ping a google", "Wamd, bloquea el trafico en el puerto 20"
* **SSH (Cuando este disponible):** "Wamd, conectate a produccion", "Wamd, copia el archivo notas.txt a nextcloud" 
#### 3.1.6 Filtrado Inteligente de Salida
WamtermelonD procesa algunos comandos de manera inteligente para no saturar la salida de voz, estos son:

* **Listas (`ls`)**: Si hay muchos archivos anunciara el total de las lineas y lee los tres primeros
* **Logs**: Lee solo las dos ultimas lineas
* **Salidas extensas**: Si el resultado supera los 400 caracteres, lo guardara de manera automática en un archivo de texto y nos dira la ubicacion del mismo

### 3.2 Interacción Conversacional (Gemma 2B)
Si el comando no coincide con una de las instrucciones predefinida o el router lo clasifica como `[gemma]`:

* **Preguntas Generales:** “wamd, ¿Quien fue Nikola Tesla?”, “wamd, ¿Cual es la capital de España?”
* **Conversación:** “wamd, cuéntame un chiste”, “wamd, cuéntame un dato curioso”.
* **Razonamiento:** “wamd, tengo tres manzanas y me como una ¿Cuantas me quedan?”

> Las respuestas generativas pueden tardar unos segundos dependiendo del hardware.

### 3.3 Interfaz Visual (TangerineUI)
Podemos acceder a la interfaz web en `localhost:5000` y a la interfaz visual (face) en `localhost:5000/face`

#### 3.3.1 Caracteristicas de la WebUI
* **Tema adaptable**: Podemos cambiar entre el modo claro o oscuro
* **Vistazo Rapido**: En el inicio podemos ver el estado del sistema de manera rapida
* **Terminal**: Acceso a un terminal del sistema (limitada)
* **Visor de logs**: Visor de logs tanto del sistema como del servicio
* **Entrenamiento NLU**: Permite ver intentos pasados sin respuesta y asignarles una accion

### 3.4 Uso del explorador de archivos
El sistema permite buscar archivos en el sistema local, haciendo uso de uno de los modelos Grape para la generación del comando y una skill para la ejecución en el sistema

* **Búsqueda:** “Wamd, buscame el archivo apuntes.pdf”
* **Lectura:** “Wamd, muéstrame el archivo notas.txt”

> Esta funcion se encuentra en fase experimental y va cuando quiere, el mostrar archivo requiere de una pantalla

### 4.5 Gestión del conocimiento
WatermelonD tiene la capacidad de aprender de documentos del usuario, esto permite que el sistema tenga conocimientos de manuales del usuario o documentación de sistemas usados (Actualmente solo soporta PDF, TXT y MD)

> Esta función puede hacer que el modelo LLM alucine generando respuestas poco coherentes

## 4. MANUAL DE ADMINISTRACIÓN
### 4.1 Gestión del Servicio (systemd)
El servicio se llama `neo.service` y se ejecuta al nivel del usuario `--user`

* **Iniciarlo:** `systemctl --user start neo.service`
* **Detenerlo:** `systemctl --user stop neo.service`
* **Reiniciarlo:** `systemctl --user restart neo.service`
* **Ver su estado:** `systemctl --user status neo.service`
* **Habilitarlo al inicio del sistema:** `systemctl --user enable neo.service`

### 4.2 Monitorización y Logs
Podemos monitorizar el estado del sistema de dos maneras, mediante el uso de los logs, o mediante la consola de administración web:

* **Logs de servicio:**
	* Almacenados en `logs/`
	* Podemos verlos con el comando `cat`
* **Logs de sistema:**
	* Los gestiona `systemd`
	* Para verlos en vivo usamos `journalctl -u neo.service -f`
* **Administración Web: `http://localhost:5000`**
	* Pestaña Logs
	* Pestaña Monitorización

### 4.3 Administración remota (SSH Manager)
> Esta función está en fase experimental y hace uso de un modelo de IA

OpenMacedonIA permite conexiones SSH usando la voz gracias a una skill, esta puede:
* **Añadir Servidores:** Actualemnente se agregan con la primera configuracion del sistema o mediante la interfaz web
* **Conexión:** Conectarse a un servidor por ssh
* **Gestion:** Permite copiar archivos entre sistemas con el comando `scp`

### 4.4 Seguridad y “Guard”
El módulo “Guard”, monitorea logs del sistema, en busca de accesos no autorizados, las alertas se anuncia por voz y por notificacion web

### 4.5 Mantenimiento y Actualizaciones
Para actualizar OpenMacedonIA tenemos dos opciones:

**Manual**
1. Nos situamos en el directorio `cd ~/WatermelonD`
2. Descargamos los cambios `git pull`
3. Ejecutamos, `source venv/bin/activate && pip install -r requirements.txt` (por si hubiera cambios de dependencias).
4. Reiniciamos el servicio `systemctl --user restart neo.service`

**Desde la Web:**
1. En la pestaña **Acciones**
2. En acciones > **Actualizar NEO**

## 5. CONFIGURACION AVANZADA
### 5.1 Ajuste Fino de Vosk
El reconocimiento de voz de Vosk. Se puede modificar en *modules/voice_manager.py.*

* **Sample Rate:** Por defecto usa 16000Hz
* **Gramática:** Se puede ampliar la lista de palabras restringidas para que sea mas preciso

### 5.2 Personalización de la UI Web
La interfaz web se encuentra en *web/templates/face.html* y *web/static/*.

* **CSS:** Se pueden modificar los colores y animaciones, se puede aplicar un css personalizado desde la consola de administracion
* **Imágenes:** Se pueden modificar los iconos o avatares

### 5.3 Parámetros Ocultos
Algunos parámetros no están en *config.json* por defecto pero pueden añadirse:

* `“debug_mode": true`: Habilita logs más extendidos
* `“tts_engine: "espeak"`: Fuerza el sistema a usar espeak-ng (Si piper falla)

# ANEXO II: Manual Técnico de Despliegue
## 1. INTRODUCCIÓN TÉCNICA
### 1.1 Propósito
A diferencia del Manual de Usuario y Administración (Anexo I), que se centra en el uso y la instalación simplificada, este detalla toda la ingeniería del sistema al detalle, explicado para ingenieros y desarrolladores que quieran entender a fondo el funcionamiento a fondo y despliegue del sistema.

### 1.2 Stack Tecnológico Detallado
El sistema se ha construido sobre un tecnologias modernas y eficientes, siempre priorizando el rendimiento en hardware modesto

* **Lenguaje Principal:** Python 3.10
* **Interfaz LLM:** *llama.cpp* (haciendo uso de *llama-cpp-python*) con soporte para instrucciones AVX2/AVX512 y aceleración Metal (MacOS) o CUDA (Nvidia)
* **E/S de Audio:** *Pyaudio* interactuando directamente con la capa ALSA de Linux para disminuir la latencia, evitando servidores de sonido como PulseAudio
* **Motor STT (Voz a texto):**
	* *Vosk*: Utiliza modelos de grafos FST, es muy robusto pero el reconocimiento algo pobre si hablas rapido
	* *Sherpa-ONNX*: Motor de nueva generación, basado en Whisper, optimizado para sistemas de recursos limitados
* **Motor TTS (Texto a voz):** *Piper*, usa modelos neuronales, es rápido y está altamente optimizado para usarse en CPU
* **Bus de Eventos:** MQTT v3.1.1 (*Mosquito*), para la comunicación entre dispositivos
* **Base de Datos:** SQLite 3
* **Base de datos de vectores**: *ChromaDB* para el sistema de memoria documental (RAG)
* **NL2BASH (Lenguaje Natural a Bash)**: *Grape-models*, para traducir comandos complejos

### 1.3 Filosofía de diseño
OpenMacedonIA sigue una filosofía “primero-local”, en la que todo se ejecuta de manera local, se sacrifica algo de velocidad de procesamiento y capacidad de razonamiento pero se consigue:

* **Privacidad:** Ningún dato de voz o texto sale de la red local
* **Latencia:** Se elimina la latencia de red hacia la nube
* **Resiliencia:** EL sistema funciona 100% offline

## 2. ARQUITECTURA INTERNA Y FLUJO DE DATOS
### 2.1 Diagrama de Componentes (Nivel de Kernel)
El nucleo del sistema *NeoCore* actua como un bucle de eventos (EventLoop), que ejecura una serie de hilos bloqueantes (Audio, E/S) y no bloqueantes (MQTT, Servidor Web)

### 2.2 Esquema de Mensajeria MQTT (Network Bros)
El protocolo de comunicación entre agentes sigue una estructura jerárquica estricta para garantizar el correcto funcionamiento y el descubrimiento automático de otros agentes

**Dirección Base:** *wamd/agents/{hostname}/{type}*

| Nivel | Valor                          | Descripción                 |
| :---- | :----------------------------- | :--------------------------- |
| Root  | *wamd*                       | Nombre global del proyecto   |
| Grupo | *agents*                     | Subgrupo para los agentes    |
| ID    | *{hostname}*                 | Identificador de dispositivo |
| Tipo  | *telemetry* (telemetría)    | Datos de estado              |
| Tipo  | *alerts* (alertas)           | Eventos críticos            |
| Tipo  | *commands* (comandos)        | Comandos remotos             |
| Tipo  | *discovery* (descubrimiento) | Aviso de conexión           |

**Datos en  JSON que pueden transferirse:**
1. **Telemetría (*.../telemetry*):** Se envía cada 60 segundos, dando información del estado del sistema,
```json
{
 "cpu_usage": 15.4, // Porcentaje de uso de CPU
 "ram_usage": 42.1, // Porcentaje de uso de RAM
 "temperature": 45.0, // Temperatura del chip en celsius
 "uptime": 3600, // Tiempo de actividad en segundos
 "status": "idle", // Estados: boot, idle, listening, thinking, speaking, error
 "ip_address": "192.168.1.50"
}
```

2. **Alertas (*.../alerts*):** Se envían inmediatamente al ocurrir un evento, intrusión en el sistema, intento de inicio de sesión,etc
```json
{
 "level": "critical", // info, warning, critical
 "code": "AUTH_FAIL", // Código de error interno estandarizado
 "msg": "Intento de acceso SSH fallido desde 192.168.1.50",
 "source": "GuardModule",
 "timestamp": 1701620000 
}
```

3. **Comandos (*.../comands*):** Para control remoto (solo para agentes que ejecuten Linux)
```json
{
 "action": "reboot", // Accion: reboot, poweroff, halt, shutdown
 "force": true,
 "auth_token": "token_si_aplica"
}
```

### 2.3 Proceso de Audio (ALSA -> VAD -> STT)
Se evita el uso de PulseAudio/PipeWire para evitar latencias innecesarias y el alto consumo de CPU.

1. **Captura:** *PyAudio* abre un canal de audio directo al dispositivo *hw:X,Y* (donde X es la tarjeta e Y el dispositivo). Se usa tamaño de fragmento de audio de 1024 segmentos (64ms de 16kHz)
2. **VAD (Detector de Actividad de Voz):**
	1. **RMS (Volumen):** Se calcula el volumen del audio
	2. **Lógica:** Si el volumen, supera un umbral durante un tiempo predefinido se considera audio.
	3. **Silencio:** Si el nivel de volumen cae por debajo del umbral durante un tiempo predefinido, se corta la transmisión y se manda a procesar.
	4. **Wake-Word**: El sistema debe detectar la palabra de activacion para iniciar el procesamiento del comando
	5. **Buffer:** Los segmentos de audio se acumulan en un buffer, antes de enviarse al STT para evitar sobrecargas si la CPU está ocupada.

### 2.4 Gestión de Memoria y Ciclo de Vida
* **Carga Perezosa (Lazy Loading):** Los modelos pesados (Gemma) no se cargan en RAM hasta el primer uso o solicitud.
* **Descarga Automática:** Si el sistema se encuentra en estado de memoria crítica (se queda sin ram), el sistema descargara el modelo después de un tiempo de inactividad.
* **Carga según el uso:** Los modelos grape, se cargan en cada uso, y solo se mantienen cargados los mas usados

## 3. INSTALACIÓN DE BAJO NIVEL
### 3.1 Compilación de Dependencias Críticas
Algunas librerías requieren ser compiladas de una forma específica para utilizar al máximo la capacidad del sistema de destino. Instalar las versiones genéricas de estas librerías usando el gestor de paquetes pip o uv puede causar grandes pérdidas de rendimiento (50-150%).

**FANN (Fast Artificial Neural Network):** Utilizada por *Padatius* para la clasificación de intentos mediante redes neuronales simples.

```bash
# Dependencias de compilación
sudo apt install libfann-dev swig
# Instalación con pip forzando compilación desde fuente
pip install fann2 --no-binary :all:
```

**Llama-cpp-python:** El motor de LLM, debe compilarse con los parámetros específicos para cada hardware,

* Para CPU x86 moderna (Intel/AMD con AVX2):
```bash
CMAKE_ARGS="-DGGML_AVX2=on" pip install llama-cpp-python --force-reinstall --no-cache-dir
```

* Para Nvidia GPU (CUDA):
```bash
CMAKE_ARGS="-DGGML_CUDA=on" pip install llama-cpp-python --force-reinstall --no-cache-dir
```

### 3.2 Configuración del Entorno Python
Se recomienda el uso de entornos virtuales (*venv*) para aislar los paquetes de python de los del sistema.

* **Ruta:** */home/usuario/COLEGA/venv*
* **Pip.conf:** Para despliegues repetitivos se puede configurar *global.index_url* para usar un sistema de caché local.

### 3.3 Despliegue de modelos (GGUF & ONNX)
El sistema soporta carga dinámica, pero se recomienda una pre-carga de los modelos durante el despliegue.

* **GGUF (Gemma):** Para el mapeado en memoria, se requiere que el archivo no esté fragmentado en el disco. Se recomienda usar sistemas de archivos como `EXT4`  o `XFS`.
* **ONNX (Sherpa/Piper):** Se ejecuta mediante *onnxruntime*
	* **Optimización:** Si tenemos  una GPU Nvidia podemos usar *onnxruntime-gpu,* para CPUs podemos usar *onnxruntime-openvino*

## 4. RETOQUES Y OPTIMIZACIÓN DEL KERNEL
### 4.1 Parametros `systcl.d` para Baja Latencia

Para un asistente de voz, la latencia de audio es crítica. Por lo que se recomienda añadir lo siguiente a */etc/sysctl.d/99-wamd-latency*
```bash
# Aumentar la frecuencia máxima de interrupciones RTC (para temporizadores precisos)
dev.hpet.max-user-freq = 2048

# Swappiness bajo para evitar paginación de los modelos de IA al disco
vm.swappiness = 10
# Preferir mantener inodos en caché
vm.vfs_cache_pressure = 50

# Aumentar buffers de red para MQTT/WebSockets 
net.core.rmem_max = 16777216
net.core.wmem_max = 16777216

# Optimización de TCP
net.ipv4.tcp_fastopen = 3
net.ipv4.tcp_slow_start_after_idle = 0
```

Después aplicamos los cambios con `sudo sysctl -p /etc/sysctl.d/99-wamd-latency.conf`

### 4.2 Configuración de Prioridad de Procesos

El servicio debe tener prioridad sobre los procesos, pero no tanta como para bloquear el kernel. En `neo.service`
```bash
[Service]
# Usamos la política Round Robin
CPUSchedulingPolicy=rr
CPUSchedulingPriority=50
# Nice negativo para mayor prioridad 
Nice=-10
```

> Nota: Requiere permisos de Real-Time (RT) configurados en `/etc/security/limits.conf` para el usuario

### 4.3 Gestión de Memoria
Para evitar que el kernel mate el proceso *python* durante un pico de uso:

1. **OOM Score:** Ajustar en systemd `OOMScoreAdjust=-500` Esto reduce la posibilidad de que el OOM Killer mate el proceso si se queda sin memoria
2. **ZRAM:** Configurar la compresión *zstd* o *lz4* para la swap en RAM. Esto duplica la RAM disponible para datos comprimibles (logs, texto, JSONs).

### 4.4 Gobernanza de CPU
En dispositivos ARM (Raspberry Pi), el cambio de frecuencia de CPU puede introducir latencia de procesamiento de audio. Se recomienda fijar el gobernador en el modo *performance*

```bash
echo performance | sudo tee /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor
```

## 5. SEGURIDAD AVANZADA

Si se ejecuta el proceso con systemd podemos usar directivas para aislar el proceso en modo sandbox
```bash
[Service]
# Solo permitir acceso a red, no a /home 
ProtectHome=read-only
ReadWritePaths=/home/usuario/COLEGA/database /home/usuario/COLEGA/logs
# Aislar /tmp (crea un directorio /tmp privado para el proceso)
PrivateTmp=true
# Prohibir escalada de privilegios (sudo, suid)
NoNewPrivileges=true
# Restringir acceso a dispositivos (solo permitir sonido y null/zero/random)
DeviceAllow=/dev/snd/* rw
DeviceAllow=/dev/null rw
DeviceAllow=/dev/zero rw
DeviceAllow=/dev/urandom r
DevicePolicy=closed
# Si queremos darle acceso a la camara debemos especificarlo aqui
```

### 5.1. Políticas de AppArmor/SELinux
Para entornos de alta seguridad, se debe generar un perfil de AppArmor que restrinja el proceso Python.
**Perfil AppArmor Básico (`/etc/apparmor.d/usr.bin.neo`):**

```apparmor
#include <tunables/global>

profile neo /home/usuario/WatermelonD/venv/bin/python3 {
#include <abstractions/base>
#include <abstractions/python>
#include <abstractions/audio>

# Network access
 network inet tcp,
 network inet udp,

# Read project files
 /home/usuario/WatermelonD/** r,
 
# Write logs and db
 /home/usuario/WatermelonD/logs/** rw,
 /home/usuario/WatermelonD/database/** rw,
 
# Deny execution of other binaries
 deny /bin/bash x,
 deny /usr/bin/curl x,
}
```

> Cambiar *usuario* por el nombre del usuario del sistema

### 5.2. Protección contra Fuerza Bruta
Si se expone SSH o la Web UI a internet, se recomienda configurar el servicio Fail2Ban.

**Jail para SSH (`/etc/fail2ban/jail.local`):**

```bash
[sshd]
enabled = true
port = ssh
filter = sshd
logpath = /var/log/auth.log
maxretry = 3
bantime = 3600
```

### 5.3. Gestión de Secretos y Certificados SSL
**SSL/TLS:** Generar un certificado autofirmado para pruebas o usar Let's Encrypt para un entorno de produccion

**Generar Certificado Autofirmado:**
```bash
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365 -nodes
```

Configurar Flask para usar estos certificados (`ssl_context=('cert.pem', 'key.pem')`).

> Por defecto el instalador genera los certificados de manera automatica

## 8. ANEXOS TECNICOS
### 8.1 Mapa de Memoria

**Estimación** de consumo en reposo vs carga máxima.

| Componente       | RAM (Reposo)     | RAM (Carga)      | Notas                                |
| :--------------- | :--------------- | :--------------- | :----------------------------------- |
| Kernel + OS      | 150 Mb           | 200 Mb           | Debian Minimizado                    |
| NeoCore (Python) | 1 Gb             | 2 Gb             | Servicio Base                        |
| Vosk             | 600 Mb           | 800 Mb           | Modelos small (es)                   |
| Gemma 2B         | 0 Mb             | 3 Gb             | —----                               |
| TTS              | 0 Mb             | 1 Gb             |                                      |
| ChromaDB         | 50Mb             | 200Mb            | Depende del numero de documentos     |
| Grape-Models     | 0Mb              | 300Mb            |                                      |
| **TOTAL**  | **~2,5Gb** | **~7,5Gb** | **En RPI requiere swap (2Gb)** |

# ANEXO III: ARQUITECTURA INTERNA E INTELIGENCIA ARTIFICIAL

## 1. INTRODUCCIÓN A LA COGNICIÓN ARTIFICIAL

### 1.1. Filosofía de Diseño: Híbrido Determinista-Generativo
OpenMacedonIa es un cambio de  respecto a los asistentes virtuales tradicionales. No es un chatbot basado en reglas predefinidas ni una "caja negra" que solo genera texto. Su arquitectura implementa un enfoque **híbrido** que combina la precisión de los modelos T5 (Text-to-Text) con la flexibilidad creativa de los Modelos de Lenguaje Grande (LLM)

* **Capa Determinista:** Se encargada de las acciones críticas, comandos del sistema y respuestas inmediatas. Prioriza la velocidad, la seguridad y la exactitud. Si el usuario dice "Apagar sistema", el sistema debe apagar el sistema, sin generar respuestas alucionadas, una respuesta filosófica o dudar. Esta capa opera en el orden de los milisegundos (<50ms)
* **Capa Generativa:** Responsable de la interfaccion, el razonamiento complejo, saber información y el manejo de consultas no estructuradas. Utiliza modelos cuantizados como Gemma-2B o Llama-3-8B para generar respuestas creativas y contextuales. Esta capa opera en el orden de los segundos (1-10s).

### 1.2. El Bucle Cognitivo (Percepción-Acción)
El sistema opera en un ciclo continuo inspirado en el bucle OODA (Observe, Orient, Decide, Act), adaptado para la latencia y los recursos de un sistema modesto:

1. **Percibir:** Captura de los datos del entorno
	* Audio (Micrófono).
	* Video (Cámara, si activa).
	* Telemetría de Red (MQTT).
	* Estado del Sistema (CPU, RAM, Temperatura)
2. **Procesar:** Transforma los datos en información útil.
	* VAD (Voice Activity Detetion) para aislar la voz del ruido
	* STT (Speech-to-Text) para pasar la voz a texto
	* Normalización de texto (pone todo en minusculas y elimina las tildes)
3. **Comprender:** Extracción de la accion
	* Clasificación de Intención (NLU).
	* Extracción de Entidades (NER).
4. **Decidir:** Selección de la mejor acción, se encarga el router de ello
	* Categoriza la entrada de voz en categorias segun el modelo a ejecutar
	* Contiene una categoria `[null]`, para comandos no entendidos
	* Contiene la categoria `[gemma]`, que ejecuta un segundo comparador antes de cargar el modelo LLM
5. **Actuar:** Ejecución física o digital.
	* Ejecución de script Python.
	* Carga de un modelo LLM o SLM
	* Generación de respuesta de voz (TTS).
	* Cambio de expresión facial (UI).
	* Envío de comando IoT (MQTT).
6. **Aprender:** Retroalimentación del usuario (opcional).
	* Corrección de alias.
	* Ajuste de preferencias.

### 1.3. Principios de Diseño Ético y de Seguridad
Dado que el sistema tiene capacidades de administración (SSH, ejecución de comandos), la arquitectura incorpora "salvadidas":

* **Mínima Sorpresa:** El sistema siempre debe confirmar acciones destructivas.
* **Privacidad por Diseño:** El procesamiento de voz y texto es 100% local. No se envían datos a la nube por defecto.

---

## 2. ARQUITECTURA COGNITIVA

### 2.1. Diagrama de Bloques Funcionales

```mermaid
graph TD
    subgraph "Percepción"
        Input[Entrada Sensorial] -->|Audio/Texto| Preproc[Pre-procesamiento]
        Preproc -->|Texto Normalizado| Router[Router Cognitivo]
    end
  
    subgraph "Razonamiento"
        Router -->|Alta Confianza| IntentEngine[Motor de Intenciones]
        Router -->|Baja Confianza| LLMEngine[Motor Generativo ]
      
        IntentEngine -->|Match| SkillExec[Ejecutor de Skills]
        LLMEngine -->|Prompt| Context[Gestor de Contexto]
        Context -->|History + Prompt| Inference[Inferencia Local]
    end
  
    subgraph "Acción"
        SkillExec -->|Resultado| ResponseGen[Generador de Respuesta]
        Inference -->|Texto| ResponseGen
      
        ResponseGen -->|Texto Final| TTS[Síntesis de Voz]
        ResponseGen -->|Estado| FaceUI[Interfaz Emocional]
    end
```

### 2.2. Ruta del  Procesamiento de Señales
El flujo de datos no es lineal; es asíncrono y basado en eventos para maximizar la reactividad.

* **Hilo de Escucha:** Dedicado exclusivamente a capturar audio y detectar la voz (VAD).
* **Hilo de Pensamiento:** Procesa la lógica pesada (LLM/SLM/Skills).
* **Interrupciones:** El sistema está diseñado para permitir que el usuario pueda interrumpir al asistente mientras habla. Si el VAD detecta voz durante el estado de `SPEAKING`, el sistema detiene inmediatamente el TTS y pasa al estado de `LISTENING`.

### 2.3. Gestión de Prioridades y Atención
El sistema implementa un mecanismo de atención básico:

1. **Foco Principal:** La interacción de voz actual.
2. **Interrupciones:** Alertas críticas de sistema (ej. "Temperatura CPU Crítica") pueden interrumpir cualquier estado.
3. **Timeout:** Si el sistema espera una entrada y no lo recibe en un tiempo predefinido, vuelve al estado de espera.

---

## 3. COMPRENSIÓN DEL LENGUAJE NATURAL (NLU)

### 3.1. Enfoque Híbrido: Fuzzy Logic vs Neural Networks
OpenMacedonIA utiliza dos sistemas en paralelo pero que se complementan.

1. **RapidFuzz (Lógica Difusa):**
	* **Uso:** Comandos de sistema, control de hardware.
	* **Mecánica:** Comparar parecido de las palabras.
	* **Ventaja:** Rápido (<5ms), determinista.
	* **Desventaja:** Poca generalización semántica.
2. **Padatious (Redes Neuronales):**
	* **Uso:** Comandos complejos, frases naturales.
	* **Mecánica:** Redes neuronales superficiales (FANN).
	* **Ventaja:** Generaliza variaciones gramaticales.
	* **Desventaja:** Requiere reentrenarse en el incio del sistema o cada X tiempo.

### 3.2. Algoritmo de Clasificación de Intenciones (RapidFuzz)
El `IntentManager` implementa un algoritmo de puntuación:

1. **Token Sort Ratio:** Compara las palabras sin importar el orden.
2. **Partial Ratio:** Busca si la frase de activacion está en la entrada. No le importa el orden

### 3.3. Redes Neuronales Superficiales (FANN/Padatious)
Padatious utiliza la librería FANN (Fast Artificial Neural Network).

* **Arquitectura:** Perceptrón Multicapa (MLP).
* **Input:** Bag of Words (BoW) o n-gramas de la frase de entrada.
* **Hidden Layers:** Generalmente 1 capa oculta pequeña (16-32 neuronas).
* **Output:** Probabilidad para cada Intent registrado.
* **Entrenamiento:** Backpropagation rápido. Al ser una red pequeña, se entrena en segundos en la CPU.

### 3.4. Router Semántico: DecisionRouter (lime-router)
El **DecisionRouter** es un modelo de clasificación que analiza el texto del usuario y lo enruta en una de las categorías predefinidas. Utiliza un modelo Transformer de clasificación cargado mediante HuggingFace:

```python
from transformers import pipeline

self.classifier = pipeline(
    "text-classification",
    model="models/lime-router",
    top_k=1
)
```

#### 3.4.1. Categorías de Clasificación

| Categoría            | Dominio                  | Ejemplo                                           |
| :-------------------- | :----------------------- | :------------------------------------------------ |
| **malbec**      | Docker / Contenedores    | "Muéstrame los logs de nginx"                    |
| **syrah**       | Red / Network            | "Escanea la red local"                            |
| **tempranillo** | Administracion / Sistema | "Reinicia el servicio ssh"                        |
| **pinot**       | Búsqueda                | "Buscame el archivo imagen.png"                   |
| **chardonnay**  | Gestión de Archivos     | "Lista los archivos en /home"                     |
| **cabernet**    | SSH / Remoto             | "Conecta al servidor web"                         |
| **gemma**       | Chat / General / Skills  | "Cuéntame un chiste"                             |
| **null**        | Fuera de dominio         | Reinicia el bucle anunciando "No te he entendido" |

#### 3.4.2. Posición en el flujo de las Decisiones

![[User Input Processing-2026-02-18-191019.png]]

### 3.5. Motor de Traducción de Comandos: Grape-models
Para comandos mas avanzados del sistema que requieren una traducción precisa a Bash (ej. Docker), se utiliza un modelo **Encoder-Decoder (T5)** ajustado (Fine-Tuned). La implementación se encuentra en `modules/BrainNut/engine.py`

#### 3.5.1. Arquitectura del Modelo
Se seleccionó `salesforce/codet5-base` (~770M parámetros) frente a modelos solo-decoder por su arquitectura encoder-decoder, ideal para traducción de lenguaje natural a código.

* **Pre-entrenamiento:** Incluye datasets generados para este proyecto con pares de `{"instruction": "Contexto: [] | Mata el proceso con ID 1234.", "cmd": "kill 1234"}`, permitiendo entender comandos avanzados
* **Eficiencia:** Con 770M  de parámetros, es ligero y eficiente.

#### 3.5.2. Flujo de Inferencia
![[User Input Processing-2026-02-18-191527.png]]

#### 3.5.3. Sistema de Semáforo de Seguridad
Tras generar un comando, NeoCore aplica un semáforo de seguridad, para evitar romper el sistema:

| Color    | Confianza | Acción                                          |
| :------- | :-------- | :----------------------------------------------- |
| Verde    | ≥ 0.85   | Ejecución directa (lectura segura: ls, cat, df) |
| Amarillo | 0.50-0.85 | Solicita confirmación de voz                    |
| Rojo     | < 0.50    | Se descarta y se avisa al usurio                 |

## 4. EL "CEREBRO" (SISTEMAS DE MEMORIA)

### 4.1. Memoria a Corto Plazo (Context Window)
El LLM (Gemma) tiene una ventana de contexto muy limitada (2048 tokens)

* **Gestión de Turnos:** Lista FIFO para los mensajes.
* **Limpieza:** Se eliminan los mensajes más antiguos para ahorrar recursos, preservando la peticion hecha por el usuario.

Los modelos *Grape-Models*, no disponen de ningún tipo de memoria, debido a su arquitectura basica.
### 4.2. Memoria a Largo Plazo (Persistencia SQLite)
Almacenada en `database/brain.db`, gestionada por `DatabaseManager`

### 4.3. Esquema Completo de Base de Datos

| Tabla               | Campos clave                                                               | Propósito                                             |
| :------------------ | :------------------------------------------------------------------------- | :----------------------------------------------------- |
| `history`         | `user_input`, `assistant_response`, `intent_detected`, `timestamp` | Registro histórico de todas las interacciones         |
| `facts`           | `key` (UNIQUE), `value`, `confidence`                                | Memoria semántica — hechos enseñados por el usuario |
| `aliases`         | `user_phrase` (UNIQUE), `canonical_command`                            | Alias aprendidos (one-shot learning)                   |
| `episodic_events` | `event_type`, `details`, `sentiment`, `context_snapshot`           | Eventos con contexto (snapshot del sistema)            |
| `concepts`        | `word` (PK), `frequency`, `avg_sentiment`                            | Knowledge Graph — nodos                               |
| `relations`       | `source`, `target`, `relation_type`, `weight`                      | Knowledge Graph — aristas                             |
| `surprises`       | `topic`, `message`, `timestamp`                                      | Anomalías detectadas                                  |
| `daily_summaries` | `date` (UNIQUE), `summary`                                             | Resúmenes diarios de consolidación                   |
| `file_index`      | `path` (PK), `name`, `extension`, `size`, `mtime`                | Índice de archivos del sistema                        |

### 4.4. Aprendizaje Adaptativo (Alias y Preferencias)
Sistema de aprendizaje simple. Si el usuario corrige al asistente, se crea un alias 

### 4.5. Estructura de Embeddings Vectoriales (RAG)
Implementado mediante **ChromaDB**.

* **Modelo de Embedding:** `sentence-transformers/all-MiniLM-L6-v2` (rápido, 384 dim).
* **Almacenamiento:** Base de datos persistente en local.
* **Proceso de Ingesta:**
	1. Escaneo de carpeta `docs/`.
	2. Chunking (segmentación) de ficheros `.md`, `.txt`, `.pdf`.
	3. Generación de vectores y almacenamiento.
* **Recuperación:** Al preguntar, se buscan los 3 fragmentos más similares y se inyectan en el prompt del LLM ("Contexto Técnico").

### 4.8. Consolidación de Memoria (Resúmenes Diarios)
El modulo BrainNut implementa un sistema de resumenes automáticos

1. Se ejecuta una vez al día (al inicio o a medianoche).
2. Obtiene todas las interacciones del día anterior.
3. Solicita al LLM un resumen narrativo en tercera persona.
4. Almacena el resumen en `daily_summaries`.

**Prompt de ejemplo:**
> "Resume brevemente las siguientes interacciones del día {fecha}. Destaca los temas principales, comandos ejecutados y datos aprendidos"

### 4.9. Motor Conversacional (`modules/chat.py`)
El `ChatManager` gestiona el historial de las conversaciones con el LLM:

* **Historial**: Lista de mensajes que se pasa como contexto al modelo.
* **System Prompt**: Personalidad del asistente, inyectado en cada turno.
* **Pruning**: Se eliminan los mensajes más antiguos para no saturar la ventana de contexto.
* **Formateo**: Adapta el historial al formato requerido por el modelo.

---

## 5. INTELIGENCIA GENERATIVA (LLM)

### 5.1. Integración de Llama.cpp
Uso de `llama-cpp-python` con modelos GGUF y `mmap` para una carga mas rápida.

### 5.2. Estrategias de Muestreo (Sampling)
* **Temperatura (0.7):** Balance creatividad/coherencia.
* **Top-P (0.9):** Nucleus sampling.
* **Repeat Penalty (1.1):** Evita bucles.

### 5.3. Optimización de Inferencia (KV Cache & Batching)
* **KV Cache:** Reutiliza cálculos y salidas generadas con anterioridad.

### 5.4. Ajuste Fino (Fine-Tuning) y LoRA
Uso de Low-Rank Adaptation (LoRA) para adaptar el modelo base a la jerga de administración de sistemas sin reentrenarlo entero.

---

## 6. PROCESAMIENTO DE SEÑALES (LOS SENTIDOS)

### 6.1. Secuencia de Audio: VAD y Normalización
1. **Captura:** Captura el audio en mono (PyAudio lo captura y lo manda a ALSA directo).
2. **VAD Energético:** Si el RMS supera el umbral dinámico, se activa el reconocimiento de voz.
3. **Normalización:** Se ajusta la ganancia del audio.
4. **Wake Word**: Hilo dedicado para el reconocimiento de la palabra de activación con Vosk (vocabulario restringido).

#### 6.1.1. Sistema Multi-Motor STT
El `VoiceManager` soporta tres motores diferentes de reconocimiento de voz, por defecto se usa Vosk o Sherpa-ONNX y Whisper requeire que el usuario lo configure de manera manual:

| Motor                    | Latencia | Precisión | Hardware mínimo      | Uso ideal                  |
| :----------------------- | :------- | :--------- | :-------------------- | :------------------------- |
| **Vosk**           | ~50ms    | Media-Baja | i3                    | Wake word, comandos cortos |
| **Faster-Whisper** | 200ms-2s | Alta       | i3 (tiny), i5 (base+) | Transcripción precisa     |
| **Sherpa-ONNX**    | ~100ms   | Alta       | i3                    | Tiempo real en CPU (int8)  |

**Historial de migración:**

| Versión | Motor STT              | Estado                                        |
| :------ | :--------------------- | :-------------------------------------------- |
| v1.0    | Google Speech (online) | Se elimino por que dependia de la nube        |
| v2.0    | Vosk (offline)         | Soportado, si hablas rapido no es muy preciso |
| v2.5    | Vosk + Faster-Whisper  | Se soporta Whisper pero en el i3 es muy lento |
| v3.0    | Vosk + Sherpa-ONNX     | Actual                                        |

---

## 7. COGNICIÓN MULTI-AGENTE

### 7.1. Protocolo de Consenso
Evita el "efecto coro" cuando varios agentes detectan la palabra de activación al avez.

1. **Detección:** Todos detectan la palabra de activacion.
2. **Evaluación:** Se calcula un score basado en la relacion señal ruido y la proximidad al usuario.
3. **Inhibición:** El agente con mayor score publica `wamd/consensus/claim`.
4. **Silencio:** Los agentes con menor score abortan.

### 7.2. Resolución de Conflictos
* **Jerarquía:** El nodo principal tiene prioridad sobre los nodos secundarios.
* **Timestamp:** El ultimo agente en publicar tiene prioridad.

---

## 8. CASOS DE ESTUDIO DE INTERACCIÓN

### 8.1. Caso 1: Resolución de Ambigüedad (Si hay dispoitivos IoT)
**Escenario:** El usuario dice "Apaga".
**Problema:** Hay múltiples dispositivos (Luz Salón, Luz Cocina, PC).
**Proceso Cognitivo:**

1. **NLU:** Detecta intent `turn_off` pero falta la entidad `device`.
2. **Decisión:** Puntuacion de confianza baja para una ejecución directa.
3. **Acción:** El sistema pregunta "¿Qué quieres que apague?".
4. **Usuario:** "La luz del salón".
5. **NLU:** Fusiona la entrada anterior ("Apaga") con la nueva ("Luz salón").
6. **Ejecución:** Apaga la luz del salón.

### 8.2. Caso 2: Cambio de Contexto (Context Switching)
**Escenario:** Usuario pide parar el contenedor apache y, a mitad de la respuesta, interrumpe.
**Proceso Cognitivo:**

1. **Estado:** `THINKING`.
2. **Evento:** VAD detecta voz nueva entrada ("Espera, ¿Que contenedores hay activo?").
3. **Interrupción:** El hilo de audio detiene el TTS inmediatamente (`stop_speaking()`).
4. **Nuevo Proceso:** Se descarta el procesamiendo.
5. **NLU:** Procesa "¿Que contenedores hay activos?".
6. **Ejecución:** Dice los contenedores activos.

---

## 9. REFERENCIA DE API INTERNA (AI MODULES)

### 9.1. Módulo `AIEngine`
Clase responsable de comunicarse con el LLM/SLM.

* `__init__(model_path: str)`: Inicializa el modelo LLM/SLM
* `generate_response(prompt: str, max_tokens: int) -> str`: Genera una respuesta
* `generate_stream(prompt: str) -> Iterator[str]`: Genera los tokens uno a uno para el streaming
* `reload_model(new_path: str)`: Cambia el modelo en caliente sin reiniciar el servicio.

### 9.2. Módulo `IntentManager`
Clase responsable del NLU y del enrutamiento

* `register_skill(skill: BaseSkill)`: Registra una nueva habilidad y sus activadores.
* `parse_command(text: str) -> IntentResult`: Procesa texto y devuelve la mejor coincidencia con una puntuacion
* `learn_alias(user_phrase: str, command: str)`: Añade una entrada a la base de datos de los alias.

### 9.3. Módulo `VoiceManager`
Clase responsable de la entrada/salida de audio.

* `start_listening()`: Inicia el hilo de captura de voz y el VAD.
* `stop_listening()`: Pausa la captura (ej. mientras habla).
* `speak(text: str)`: Sintetiza voz usando el motor TTS configurado (Piper/Espeak).

---

## 9. REFERENCIA DE CONFIGURACIÓN (AI)

### 9.1. Bloque `ai_engine`
Parámetros en `config.json`:
```json
"ai_engine": {
  "model_path": "models/gemma-2b-it-q4_k_m.gguf", //El modelo LLM a usar, se almacenan en "/models"
  "context_window": 2048, 
  "temperature": 0.7,
  "top_p": 0.9,
  "n_threads": 3
}
```

### 9.2. Bloque `voice`
```json
"voice": {
  "stt_engine": "vosk",
  "tts_engine": "piper",
  "vad_sensitivity": 2,  // 0-3 (3 es más sensible)
  "wake_word": "wamd" // Aqui definimos las palabras de activacion
}
```

### 9.3. Bloque `intents`
```json
"intents": {
  "confidence_threshold": 70,
  "fuzzy_matching": true,
}
```

---

## 10. HOJA DE RUTA DE IA

### 10.1. Multimodalidad
* Integración de un modelo basado en  LLaVA (Large Language-and-Vision Assistant) para permitir que el asistente pueda ver y describit imágenes en tiempo real (Requiere de una camara)

### 10.2 Optimizacion
* Extender los pares de datos de los modelos Grape, para hacerlos mas fiables a la entrada del usuario
* Hacer un FineTuning al modelo Gemma para personalizarlo al sistema final (Actualmente usamos el modelos base sin modificar)

# ANEXO IV: RESOLUCIÓN DE PROBLEMAS

En este apartado se detalla toda la información sobre como solucionar los problemas que puedan surgir durante el despliegue del sistema

## 1. PROBLEMAS DEL USUARIO FINAL

### 1.1 Problemas de Audio
* **Problema:** El asistente no escucha o no habla
* **Solución:**
	1. Verificar dispositivos: `aplay -l` (altavoces), `arecord -l` (microfono)
	2. Verificar los niveles de volumen con `alsamixer`
	3. Verificar logs: Buscar errores relacionados con `PyAudio` o `ALSA`

### 1.2 Problemas de Reconocimiento de Voz
* **Problema:** El asistente entiende mal los comandos o no responde
* **Solución:**
	1. Rudio, moverse a un lugar con menos ruido
	2. Cambiar el modelo de vosk a sherpa-onnx, y usar uno mas grande (si el hardware lo permite)
	3. Ajustar la sensibilidad del micrófono en `config.json`

### 1.3 Problemas de Conectividad
* **Problema:** No se detecta la red o los pings fallan
* **Solución:**
	1. Verificar la conexión Ethernet/WiFi usando `ip a`
	2. Verificar los servidores DNS con `cat /etc/resolv.conf`
	3. Si falla el MQTT, verificar que el servicio *mosquitto* este activo y funcionando con `sudo systemctl status mosquitto`

### 1.4 Problemas del Modelo LLM
* **Problema:** Respuestas lentas (+10s), incoherentes o el servicio se reinicia al hablar
* **Solución:**
	1. No hay suficiente memoria RAM, si estamos en un sistema con menos de 6GB de ram los modelos no funcionaran de manera correcta, podemos intentar aumentar la Swap o usar un modelo más pequeño

## 2. PROBLEMAS DE INGENIERÍA Y DESPLIEGUE

### 2.1 Resolución de errores en la compilación
* **Error: missing Python.h**: Falta `python3`
* **Error gcc: error: ....**: Falta `build-essential`
* **Error portaudio.h not found**: Falta `portaudio19-dev`
* **Error illegal Instruction** (SIGILL): Se compiló con parámetros que la CPU no soporta

## 3. PROBLEMAS DEL SISTEMA DE IA Y LOGICA

### 3.1 Diagnostico de NLU (Falsos Positivos/Negativos)
* **Problema**: El sistema no entiende un comando
* **Solucion**:
	1. **Revisar Logs**: Busca `IntentManager: Match Score`
	2. **Puntuacion Baja (<60)**: El activador no se parece lo suficiente. Añadir variaciones en `intents.json`
	3. **Falso Positivo**: El sistema se activa con ruido. Aumentar `confidence:threshold`

### 3.2 Depuracion de Alucionaciones del LLM
* **Problema**: Si el LLM inventa respuestas
* **Solucion**:
	1. **Bajar La Temperatura**: Reducir de 0.7 a 0.2 en `config.json`

### 3.3 Problemas de Latencia de Interferencia
* **Problema**: Si el sistema tarda >5s en responder
* **Solucion**:
	1. **Hardware**: Verificar que no haya extrangulamiento termico del procesador
	2. **Modelo**: Cambiar el modelo a una cuantizacion menor (ej. Q4_K_M a Q2_K).

## 4. CÓDIGOS DE ERROR INTERNOS

Códigos estandarizados para logs y alertas MQTT.

| Código | Significado                        | Corrección                         |
| ------- | :--------------------------------- | :---------------------------------- |
| E001    | Dispositivo de audio no encontrado | Verificar `arecord -l` y permisos |
| E002    | Conexión con MQTT perdida         | Revisar el estado de Mosquito       |
| E002    | LLM sin ram                        | Aumentar la Swap                    |
| W001    | Alta temperatura de CPU            | Revisar la ventilación             |
| S001    | Error de autenticación            | Posible intrusión, revisar logs    |

# ANEXO V: PROGRAMACIÓN Y CREACIÓN DE SKILLS

## 1. INTRODUCCIÓN

Este documento es una guía destallada para desarrolladores que buscan extender las funcionalidades de WatermelonD mediante la creación de nuevos módulos o "Skills". El sistema de habilidades se llama **BlueberrySkills**.

## 2. ARQUITECTURA DEL SISTEMA DE SKILLS

### 2.1. Ubicación
Las Skills se almacenan en el directorio `modules/BlueberrySkills/`. Es un **submódulo de Git** independiente con su propio repositorio.

### 2.2. Estructura del Directorio

```
modules/BlueberrySkills/
├── __init__.py          # Registro central de skills y funciones
├── system.py            # Control del sistema (apagar, reiniciar, estado)
├── docker.py            # Gestión de contenedores Docker
├── files.py             # Búsqueda y gestión de archivos
├── finder.py            # Buscador avanzado de archivos
├── ssh.py               # Gestión SSH por voz
├── network.py           # Herramientas de red
├── media.py             # Control multimedia
├── content.py           # Chistes, frases célebres, datos curiosos
├── time_date.py         # Hora y fecha
├── diagnosis.py         # Diagnóstico del sistema (Sherlock)
├── organizer.py         # Organizador de archivos
├── visual.py            # Interfaz visual
└── README.md            # Documentación del submódulo
```

### 2.3. Registro de Skills
El archivo `__init__.py` actúa como registrador cental, este exporta un diccionario de funciones que NeoCore usa para mapear intenciones a acciones:

```python
# modules/BlueberrySkills/__init__.py
from .system import get_system_status, shutdown_system, reboot_system
from .docker import list_containers, restart_container
from .files import search_files, create_file
from .ssh import connect_ssh, list_servers
# ... más imports

SKILLS_REGISTRY = {
    "system_status": get_system_status,
    "shutdown": shutdown_system,
    "docker_list": list_containers,
    "docker_restart": restart_container,
    "file_search": search_files,
    "ssh_connect": connect_ssh,
    # ... más mappings
}
```

## 3. CREACIÓN DE UNA NUEVA SKILL

### 3.1. Paso 1: Crear el archivo Python
Creamos un nuevo fichero `.py` en `modules/BlueberrySkills/`:

```python
# modules/BlueberrySkills/my_skill.py

import logging
import subprocess

logger = logging.getLogger("my_skill")

def mi_funcion(core, params=None):
    """
    Ejecuta una acción personalizada.
  
    Args:
        core: Referencia al nucleo, con acceso a todos los subsistemas.
        params: Extra los parametros desde la peticion del usuario.
  
    Returns:
        str: Respuesta para el usuario.
    """
    try:
        resultado = subprocess.run(
            ["whoami"],
            capture_output=True, text=True, timeout=10
        )
        respuesta = f"El usuario actual es {resultado.stdout.strip()}"
        logger.info(f"Skill ejecutada: {respuesta}")
        return respuesta
    except Exception as e:
        logger.error(f"Error en mi_skill: {e}")
        return "Error al ejecutar la skill"
```

### 3.2. Paso 2: Registramos la skill en `__init__.py`
```python
from .my_skill import my_function

SKILLS_REGISTRY = {
    # ... skills existentes
    "my_action": my_function,
}
```

### 3.3. Paso 3: Creamos la intención en el fichero `intents.json`
```json
{
    "name": "my_action",
    "triggers": [
        "ejecuta mi acción personalizada",
        "haz mi acción",
        "activa la skill personalizada"
    ],
    "action": "my_action",
    "response": "Ejecutando tu acción personalizada...",
    "confidence": 0.75
}
```

## 4. ACCESO AL NÚCLEO (NEOCORE)

El parámetro `core` proporciona acceso a todos los subsistemas:

| Acceso                   | Código                                    | Propósito                      |
| :----------------------- | :----------------------------------------- | :------------------------------ |
| **TTS (Hablar)**   | `core.speaker.speak("Texto")`            | Anunciar por el altavoz         |
| **Configuración** | `core.config_manager.get("clave")`       | Leer configuración del sistema |
| **MQTT**           | `core.mqtt_manager.publish(topic, data)` | Publicar en MQTT                |
| **SSH**            | `core.ssh_manager.execute(host, cmd)`    | Ejecutar en un servidor remoto  |
| **Memoria**        | `core.brain.store_fact(key, value)`      | Guardar informaicon             |
| **RAG**            | `core.knowledge_base.query(text)`        | Consultar base de conocimiento  |
| **Base de datos**  | `core.db.add_interaction(...)`           | Interacción dire               |
| cta con SQLite           |                                            |                                 |

## 5. BUENAS PRÁCTICAS DE DESARROLLO

1. **No bloquear el hilo principal:**
   Si la Skill realiza una operación larga, se recomienda ejecutarla en un hilo separado (`threading.Thread`):

   ```python
   import threading
   def mi_funcion_larga(core, params=None):
       threading.Thread(target=_heavy_lifting, args=(core,)).start()
       return "Iniciando tarea en segundo plano..."
   ```
2. **Manejo de Errores:**
   Se recomienda envolver el código en bloques `try-except` para evitar que un error detenga todo el servicio
3. **Logging:**
   Se recomienda usar `logging.getLogger()` para registrar logs, nunca `print()`.
4. **Timeouts:**
   Se recomienda usar `timeout` en `subprocess.run()` para evitar que comandos colgados bloqueen el sistema

## 6. SKILLS EXISTENTES

| Skill                  | Archivo          | Funciones principales                                                                                  |
| :--------------------- | :--------------- | :----------------------------------------------------------------------------------------------------- |
| **Sistema**      | `system.py`    | Control del sistema (apagar, reiniciar, info del hardware)                                             |
| **Docker**       | `docker.py`    | Control de contenedores (docker / podman)                                                              |
| **Archivos**     | `files.py`     | Buscar, crear, eliminar archivos                                                                       |
| **Buscador**     | `finder.py`    | Búsqueda avanzada por nombre, extensión, contenido (A diferencia del anterior este usa grep y pipes) |
| **SSH**          | `ssh.py`       | Conectar, ejecutar, listar servidores                                                                  |
| **Red**          | `network.py`   | Ping, escaneo, WHOIS, puertos abiertos                                                                 |
| **Hora/Fecha**   | `time_date.py` | Hora actual, fecha, temporizadores                                                                     |
| **Diagnóstico** | `diagnosis.py` | Test de internet, disco, RAM, CPU vía Sherlock                                                        |
| **Organizador**  | `organizer.py` | Organizar archivos por tipo/fecha                                                                      |
| **Visual**       | `visual.py`    | Muestra archivos en la interfaz gráfica (experimental)                                                |

> Muchas de estas skills se estan eliminando ya que los Grape-Models hacen sus funciones de manera mas eficiente por lo que se fusionaran unas con otras o se eliminaran

## 7. DESARROLLO COMUNITARIO (Watermelon-extras)
El submódulo `modules/Watermelon-extras/` aloja skills que no son esenciales para el funcionamiento del sistema:

```
modules/Watermelon-extras/
├── alarms.py          # Alarmas con audio
├── content.py         # Contenido extra
├── hello_world.py     # Ejemplo mínimo de skill
├── sys_control.py     # Control del sistema extra
├── weather.py         # Clima (API externa)
└── setup.sh           # Instalador de dependencias extra
```


# ANEXO VI: PRUEBAS DE VALIDACIÓN Y RENDIMIENTO

## 1. INTRODUCCIÓN

Este documento detalla las pruebas realizadas para verificar el coreccto funcionamiento del sistema. Se incluyen pruebas individuales a componentes críticos, pruebas de integración del flujo de datos completo y pruebas de estrés/rendimiento en el hardware final.

## 2. PRUEBAS UNITARIAS Y DE COMPONENTES

### 2.1. Validación del Sistema RAG (Retrieval-Augmented Generation)
**Objetivo:** Verificar que el sistema puede analizar documentos locales y sacar datos relevantes de ellos ante una consulta.
* **Script de Prueba:** `test_rag_temp.py`
* **Funcionamiento:**
	1. Se inicializa el `KnowledgeBase` con una base de datos temporal.
	2. Se fuerza el escaneo de documentos del directorio `docs/`.
	3. Ejecutamos una consulta de prueba: "Wamd, arquitectura cognitiva".
	4. Verificamos que el resultado contiene palabras clave relacionadas con la búsqueda.
* **Resultados:**
	* **Analisis:** Correcto 
	* **Búsqueda:** Recuperación de trozos del `ANEXO_III` con alta similitud.
	   **Tiempo de Respuesta:** < 2s para búsqueda en base de datos local.

### 2.2. Pruebas del Bus de Eventos (MQTT)
**Objetivo:** Asegurar la comunicación entre módulos.
* **Herramienta:** `mosquitto_sub` / `mosquitto_pub`
* **Casos de Prueba:**
	1. **Publicación de Telemetría:** Verificar que `home/agents/{hostname}/telemetry` recibe datos cada 60s.
	2. **Recepción de Comandos:** Enviar JSON a `home/agents/{hostname}/commands` y verificar respuesta.
* **Resultados:**
	* **Latencia de los mensajes** < 10ms en la red local

## 3. PRUEBAS DE INTEGRACIÓN (FLUJO COMPLETO)

### 3.1. Prueba del flujo de Voz
**Objetivo:** Validar el flujo de voz enterio: Audio -> STT -> NLU -> Lógica -> TTS.
* **Script de Prueba:** `test_pipeline.py`
* **Funcionamiento:**
	1. Inyección simulada de texto ("qué hora es") en el bus MQTT (`recognizer_loop:utterance`), saltando el reconocimiento de voz.
	2. Escucha del evento `speak` en el bus.
	3. Medición del tiempo total.
* **Resultados:**
	* **NLU:** Se detecta la intención `time_query` correctamente con la puntuacion > 0.8
	* **Respuesta:** El sistema genera el evento `speak` y devuelve la hora del sistema
	* **Tiempo de Ejecución:** ~0.5s

### 3.2. Pruebas de Interrupción (Barge-in)
**Objetivo:** Verificar que el usuario puede interrumpir al asistente mientras habla
* **Escenario:**
	1. El asistente comienza a leer un texto largo.
	2. El usuario dice "wamd, para".
* **Resultados:**
	* El módulo de audio detecta sonido (VAD) durante el estado `SPEAKING`
	* Se envía una señal `tts:stop`.
	* El audio se detiene en menos de 300ms

## 4. PRUEBAS DE RENDIMIENTO Y ESTRÉS

### 4.1. Consumo durante el procesamiento
**Modelo:** Gemma-2B-IT (Quantized q4_k_m).

| Métrica         | Valor Medido  | Notas                                   |
| :-------------- | :------------ | :-------------------------------------- |
| **CPU**         | 89% (2 cores) | El sistema da un pico de consumo.       |
| **RAM (Pico)**  | 3.8 GB        | Dentro del margen de los 4Gb            |
| **Tokens/seg**  | ~2-5 t/s      | Algo lento para conversaciones seguidas |
| **Temperatura** | 68-75°C       | Un disipador no le iria mal             |

### 4.3. Latencia al realizar una consulta
Desglose del tiempo de respuesta para una consulta simple ("Hola").

| Componente             | Tiempo Estimado  |
| :--------------------- | :--------------- |
| **VAD + Grabación**    | 500ms            |
| **STT (Whisper/Vosk)** | 800ms - 1.5s     |
| **SLM (Router)**       | 500ms            |
| **SLM (Grape-Models)** | 600ms - 800ms    |
| **LLM (Gemma)**        | 5s - 10s         |
| **TTS (Generación)**   | 200ms            |
| **Total (Sin Gemma)**  | **~3.5s - 5.0s** |


## 5. CONCLUSIONES DE LAS PRUEBAS

1. **Estabilidad:** El sistema es estable para interacciones cortas. En interacciones mas extensas puede sufrir de cuelgues
2. **Cuello de Botella:** El principal cuello de botella es la CPU durante la ejecucion del LLM/SLM y el STT.

# ANEXO VII: RETOS DE DESARROLLO Y SOLUCIONES ADOPTADAS

## 1. INTRODUCCIÓN

Este anexo documenta los principales problemas técnicos que me he encontrado durante la creacion del proyecto WatermelonD, y las soluciones y apaños que he implementado. A diferencia del *Anexo IV (Troubleshooting)*, que se centra en el usuario final, este documento se centra en los arreglos hechos para que el sistema funcione de manera semi estable

## 2. RETOS DE AUDIO Y LATENCIA

### 2.1. El Problema de PulseAudio/PipeWire en Headless
**Problema:** Inicialmente, el sistema utilizaba las capas intermedias de audio estándar de Linux como PulseAudio. En el equipo usado, esto introducía una latencia variable de 200ms a 500ms y un consumo de CPU del 5-10% solo por mantener el servidor de audio activo, lo cual se comía los recursos.
**Solución:**
* Migramos a **ALSA** nativo `PyAudio`.
* Se implementó un acceso  al dispositivo de hardware (`hw:X,Y`), eliminando servicios intermedios.
* **Resultado:** Se redujo la latencia de la captura de audio a < 50ms

### 2.2. Cancelación de Eco
**Problema:** El micrófono captaba la propia voz del asistente (TTS), creando un bucle de retroalimentación infinito donde el asistente se escuchaba a sí mismo y se respondía.
**Solución:**
* Implementación de un mecanismo de **"Semáforo de Audio"**. Cuando el estado del sistema es `SPEAKING`, se suspende temporalmente la escucha de audio (El sistema sigue detectando la Wake-word)

## 3. RETOS DE INTELIGENCIA ARTIFICIAL (LLM)

### 3.1. Inferencia Lenta en CPU
**Problema:** Ejecutar modelos de 7B parámetros (como Gemma-7B) resulto en que los resultados tardaban mas de 10 segundos por token, haciendo el sistema inusable.
**Solución:**
* **Cambio de Modelo:** Migración a **Gemma-2B**, un modelo más pequeño.
* **Cuantización:** Uso del formato **GGUF** (Q4_K_M) mediante `llama.cpp`. Esto reduce el uso de memoria y aprovecha las instrucciones AVX2 del procesador
* **Resultado:** Velocidad de 2-5 tokens/segundo, suficiente para responder datos en momentos puntuales

### 3.2. Alucinaciones y "Verborrea"
**Problema:** Los modelos pequeños tienden a perder el hilo de la conversacion o generar respuestas excesivamente largas y creativas en peticiones simples (ej. "¿Qué hora es?" -> "El tiempo es una construcción relativa...").
**Solución:**
* **Ingeniería de Prompts :** Se le inyecta un prompt  que define la "personalidad" del asistente como concisa, servicial y directa.
* **Stop Tokens:** Se confiigura un limite de tokens maximo que puede generar para que no se vuelva demasiado creativo.

## 5. CONCLUSIÓN

La creacion del proyecto OpenMacedonia ha demostrado que es posible ejecutar IA generativa moderna en hardware muy modesto y de hace unos años, siempre y cuando se apliquen algunas optimizaciones a nivel de sistema operativo y se elijan las arquitecturas de modelos adecuadas (SLMs vs LLMs). Esto nos indica que no se necesitan equipos de ultima generacion para poder usar estas tecnologias y solo se necesita optimizar bien el sistema.

# ANEXO VIII: DESPLIEGUE
## 1. INTRODUCCIÓN
Este anexo documenta el proceso de despliegue de OpenMacedonia en un entorno "real".

## 2. PREPARACIÓN DEL HARDWARE

El hardware inicial de este proyecto iba a ser un portátil Lenovo Yoga 530-14IKB que no ha podido mas, algunas capturas están hechas desde el portátil y ya el resto desde una maquina virtual, ya que el despliegue se ha hecho por fases. Por lo que para salir del paso mientras lo arreglo usare una maquina virtual que replique las características del portátil, 2 núcleos y 8 Gb de ram.


## 3. DESPLIEGUE DE DEBIAN

Como imagen de debian usaremos el archivo ISO: `debian-13.3.0-amd64-DVD-1.iso`, este se puede descargar desde la pagina oficial de [Debian](https://www.debian.org/CD/http-ftp//). Elegimos la imagen *CD* y no *netinst* por que esta incluye todas las herramientas necesarias para hacer el despliegue mas rápido sin depender de internet, pero si esta no la tuviéramos disponible, podemos usar la imagen *netinst*.

### 3.1. Instalación del Sistema

Debemos elegir la opción de **Instalar**. (La segunda)
![alt text](image/PXL_20260207_164926514.jpg)

Las primeras opciones están relacionadas con el *Idioma*, *Región* y *Distribución del teclado*. Esto es a gusto del usuario final, pero en este caso usaremos **Español**
![alt text](image/PXL_20260207_164941481.jpg)
![alt text](image/PXL_20260207_164944937.jpg)
![alt text](image/PXL_20260207_164948940.jpg)

Para el nombre de la maquina, dejare el por defecto, ya que esto no afecta al sistema final
![alt text](image/PXL_20260207_171803920.jpg)

Ahora nos pregunta la contraseña del usuario administrador (root), este no es necesario habilitarlo, ya que el servicio funciona en la capa de usuario.
![alt text](image/PXL_20260207_171811803.jpg)

Ahora en el nombre del usuario yo pondré *user*, pero podemos poner otra cosa, no afecta al sistema final
![alt text](image/PXL_20260207_171821971.jpg)

Como contraseña se recomienda algo seguro (mínimo 8 caracteres y mezclar letras y numero), no el *1234* que yo he puesto
![alt text](image/PXL_20260207_171829622.MP.jpg)
![alt text](image/PXL_20260207_171836023.jpg)

En el particionado del disco, seleccionamos *Guiado - Utilizar todo el disco* (Segunda opcion) y despues seleccionamos el disco
![alt text](image/PXL_20260207_171909395.jpg)
![alt text](image/PXL_20260207_171916643.jpg)

Al estar en una maquina virtual con espacio limitado, no veo necesario hacer particiones, en un sistema real no habría problema si el usuario quiere partcionar el disco siempre que tenga suficiente espacio luego para el despliegue (~65Gb).Por ello usamos *Todos los ficheros en una partición (Recomendado para novatos)* y confirmamos los cambios
![alt text](image/PXL_20260207_171921564.jpg)
![alt text](image/PXL_20260207_171930862.jpg)
![alt text](image/PXL_20260207_171935739.jpg)

Seleccionamos en la lista la región de nuestra replica
![alt text](image/PXL_20260207_172045392.jpg)

Ahora en la lista de replicas, se recomienda la primera o la segunda opción, ya que son las mas rápidas y estables.
![alt text](image/PXL_20260207_172053178.jpg)

La encuesta de uso de paquetes es algo opcional, por costumbre doy que si ya que el software de gratis no esta de mas ceder algunos datos de uso.
![alt text](image/PXL_20260207_172245163.jpg)

Ahora viene el paso clave, que es la diferencia entre un sistema optimizado y un sistema que come recursos sin limites. Tenemos que desmarcar todas las opciones y dejar solo **SSH Server** y **Utilidades estándar del sistema**
![alt text](image/PXL_20260207_172302808.jpg)

Elegiremos continuar para reiniciar el sitema.
![alt text](image/PXL_20260207_172438641.MP.jpg)

Ahora iniciamos sesión en el sistema, verificamos que tengamos conexión de red, apuntamos la *dirección IP* y activamos el servicio *SHH* en el arranque (`systemctl enable ssh`) y en el momento (`systemctl start ssh`)
![alt text](image/PXL_20260207_173523644.jpg)

### 3.2 Despliegue del Servicio

> Desde aquí todo lo demás es en maquina virtual, pero el despliegue y los pasos serian 1:1 a una maquina real
> Las imágenes de a continuación, se van a ver todas desde una terminal ssh, por comodidad a la hora de copiar comandos, ademas que se asemeja bastante a la realidad ya que lo administradores solemos conectarnos por SHH.
> Para el primer paso, nos desplazamos a la pagina de Github del [proyecto](https://github.com/OpenMacedonIA/WatermelonD), en ella nos desplazamos hasta que nos aparezca el campo con el comando para la instalacion automatizada
> 

![alt text](image/image-22.png)

Copiaremos el contenido de ese campo y lo pegaremos en la consola SSH que tenemos abierta, una vez pulsemos enter empezara una instalación automatizada, que nos hará una serie de preguntas durante la misma para personalizar un poco la instalación
![alt text](image/image-23.png)

#### 3.2.1 Instalacion Automatizada

> El instalador hace uso de whiptail, que es una utilidad para mostrar interfaces gráficas simples desde la propia consola, los sistemas debian la llevan instalada por defecto
> La primera pregunta que tenemos es el directorio de instalación, se recomienda dejar el por defecto que es `~/watermelonD` pero podemos cambiarlo a uno de nuestra preferencia.

![alt text](image/image-24.png)
![alt text](image/image-25.png)

Actualmente la rama main y rc son la misma ya que se fusionaron debido a que el proyecto ya es "semi-estable", por lo que no hay diferencia entre elegir una o otra. Para la instalación cogeremos **main**
![alt text](image/image-26.png)
![alt text](image/image-27.png)

Si el instalador detectara que ya esta clonado  en la carpeta de destino, nos avisaría de ello, dándonos la opción de seguir y actualizar si *hay cambios*.
![alt text](image/image-28.png)

Se cerrara whiptail, y el instalador empezara a descargar de manera automática el *repositorio principal*y *los submodulos*
![alt text](image/image-29.png)

Para continuar se nos abrirá un menu con diferentes opciones que nos permite elegir el tipo de instalación, estas son:
* **Instalacion ESTANDAR**: Instala todo el sistema y todas las funciones, aunque algunas nos las pregunta
* **Cliente Web Remoto**: Solo instalaria la WebUI, es una opcion si queremos desplegar un cliente y ya tenemos el servidor
* **Satelite**: Configura dispositivos MQTT (Esta funcion se ha movido, pero se me olvido quitarla)
* **Configuracion Developer**: Solo descarga los repositorios para trabajar en el codigo
* **Herramientas / Mantenimiento**: Incluye herramientas que he ido usando durante el desarollo para arreglar pequeños error (La mayoria obsoletas)
* **Salir**: Sale de la instalacion
  **Aqui usaremos la primera opcion**
  ![alt text](image/image-30.png)![alt text](image/image-31.png)

El instalador detectara el sistema en el que estamos, siendo las opciones *Debian/Ubuntu* o *Otros*, y en base a ello procede, nos pide la clave del usuario que la requiere para instalar los paquetes del sistema necesarios
![alt text](image/image-32.png)

Nos pregunta si queremos instalar el *modo kiosko*, esto *solo* se debe instalar si tenemos una *pantalla* en el equipo, ya sea por que es un portátil (consume recursos innecesarios si no hay pantalla). Después si queremos *optimizar el sistema*, aquí cambiamos el nombre de hostname, agregamos unas entradas en el `/etc/hosts` y quita basura preinstalada (si la hay)

Vamos a decir *Si* a todo para hacer la instalación completa
![alt text](image/image-33.png)
Ahora comenzara una de las partes que *mas tiempo* toma, descargar los paquetes del sistema, dependiendo de la velocidad de internet puede tardar entre *5 - 15 minutos*
![alt text](image/image-34.png)

En el proceso de descarga de paquetes, se instala *Tripwire*, esta es una utilidad para evitar modificaciones no autorizadas de fichero del sistema, *el configurarlo o no , no afecta al sistema final*, esto añade una capa de seguridad si el sistema esta expuesto a internet impidiendo que se modifiquen los ficheros.

Para este despliegue lo vamos a usar, pulsamos *Si* para crear las claves de sitio y local y para crear la base de datos
![alt text](image/image-35.png)
![alt text](image/image-36.png)
![alt text](image/image-37.png)

Después de un rato de descarga de paquetes, nos pedirá las claves de sitio y local, siguiendo el despliegue voy a  *1234* (esto no se debe hacer no es seguro).
![alt text](image/image-38.png)
![alt text](image/image-39.png)

Para continuar, descargara la versión de *python* requerida, ya que no usa la que viene con el sistema por defecto usa una algo mas vieja, junto a ella se descarga *uv* que es un gestor de paquetes mas rápido de el integrado PIP.  Después crea el entorno virtual para que no haya conflictos con paquetes del sistema y para terminar con esta parte clona *FANN C* y lo compila, esto es para optimizar esta librería al sistema de destino
![alt text](image/image-40.png)

Después *uv*, descargara e instalara las *librerías de python* requeridas para funcionar, igual que la instalación de paquetes del sistema, la velocidad de esta requiere de nuestro Internet tardando entre 5 - 10 minutos
![alt text](image/image-41.png)

#### 3.2.2 Personalizacion
Para continuar, el instalador nos preguntara si queremos personalizar el sistema, aquí se genera el fichero `config.json` en caso de pulsar *No*, se genera un fichero genérico.
Para el despliegue usaremos *Si*
![alt text](image/image-42.png)

Se dispone de dos modos, que son los siguientes:
* **Simple**: Configura cosas esenciales (el nombre de usuario y las palabras de activación)
* **Avanzado**: Configura lo anterior y le sumamos el puerto de la webUI, alias de servidores y equipos SSH.
  Seleccionamos el *Avanzado*
  ![alt text](image/image-43.png)
![alt text](image/image-44.png)
Ahora nos permite añadir mas palabras de activacion, aparte de las incluidas.

> Recomendación si queremos añadir una palabra por ejemplo *wamd* seria ideal añadir como se escribiría foneticamente *guamde*

![alt text](image/image-47.png)


 Aqui podemos agregar servidores ssh para que el sistema pueda conectarse a ellos.
> Esta función usa un modelo que no esta disponible todavía dado que es mas complejo de entrenar que el resto

![alt text](image/image-48.png)

Esta opción nos pide las siguientes opciones a la hora de agregar un servidor:
* **Alias del servidor**: Este es el nombre que usamos para referirnos a el a la hora de hacer peticiones al asistente
  ![alt text](image/image-49.png)
* **Host o direccion IP**: La direccion del servidor
  ![alt text](image/image-50.png)
* **Usuario SSH:** El usuario con el que se inicia sesion por ssh en ese servidor
  ![alt text](image/image-51.png)
* **Puerto:** Normalmente es el 22 pero hay gente que lo cambia
  ![alt text](image/image-52.png)
* **Autenticacion:** Aqui nos da las dos opciones si es por medio de una clave o una contraseña, de ambas formas el sistema las almacena de forma segura las contraseñas van encriptadas
  ![alt text](image/image-53.png)
  * **Si cojemos autenticacion por clave:** Debemos copiar la clave privada previamente en el servidor o generarla desde el mismo
    ![alt text](image/image-54.png)
  * **Si cojemos autenticacion por contraseña**: El sistema nos pedirá la clave
    ![[Captura desde 2026-02-07 19-03-40.png]]
    ![alt text](image/image-55.png)
    Y nos da la opción de agregar mas
    ![alt text](image/image-56.png)
    ![alt text](image/image-57.png)

Ahora configuramos los alias de red, por defecto esta configurado `google=8.8.8.8` y `router=192.168.1.1`. 
Con esta opción podemos usar utilidades de red sin recordar la IP, lo que permite decirle al asistente `haz ping a google` y que sepa donde esta *google*.
![alt text](image/image-58.png)
![alt text](image/image-59.png)
![alt text](image/image-60.png)

Primero nos pide el nombre del alias
![alt text](image/image-61.png)
Y despues su direccion IP
![alt text](image/image-62.png)
![alt text](image/image-63.png)
Y nos pregunta si queremos agregar mas
![alt text](image/image-64.png)

Aunque se permite cambiar el puerto de la interfaz web, no se recomienda, por dos razones:
1. Habría que hacer ajustes manuales en diferentes archivos como el `.xinitrc` para cambiar la dirección a la que apunta chromiun en modo kiosko
2. Implemente esto por que pensé que funcionaria. Cuando lo probé dejo de funcionar todo (se me olvida quitarlo).
   ![alt text](image/image-65.png)

Las preferencias de voz no ha dado tiempo a que se puedan editar desde aquí, pero el sistema informa de donde pueden cambiarse
![alt text](image/image-66.png)
![alt text](image/image-67.png)
![alt text](image/image-68.png)

#### 3.2.3 Configuración de la base de datos
Para continuar con el despliegue, el sistema creara la base de datos
![alt text](image/image-70.png)

#### Descarga de los modelos LLM/SLM
Despues comenzara con la descarga de los modelos, estos modelos son:

- *Sherpa-ONNX-Whisper-Small*
![alt text](image/image-71.png)
- *Gemma2B*
![alt text](image/image-72.png)
- *Grape-models*
![alt text](image/image-73.png)

#### 3.2.4 Systemd, HTTPS y sudoers
Tras la descarga creara los servicios *systemd* para el arranque del servicio en el sistema y configurara algunos permisos necesarios para que algunas utilidades funcionen

> Esto requiere contraseña del usuario administrador

![alt text](image/image-74.png)

Después genera el certificado autofirmado HTTPS y nos explica como se configura en los clientes
![alt text](image/image-75.png)

Para finalizar configurara un fichero `sudoers` para dar al sistema ciertos permisos
![alt text](image/image-76.png)

Para finalizar y que el sistema arranque, reiniciamos el sistema
![alt text](image/image-77.png)

Con el comando `systemctl status --user neo.service`, podemos ver si todo ha salido bien y el servicio arranca
![alt text](image/image-78.png)

## 4. INTERFAZ WEB

> Todo el código Web (frontend) ha sido desarrollado por un agente de IA, en base a dibujos que le he ido pasando de lo que quería.  Pongo esto por que se nota a distancia que he usado herramientas para hacerlo.

 Por defecto a la interfaz web se accede con las credenciales *admin/1234*, esta contraseña se puede cambiar desde el archivo `config/config.json`

### 4.1 La "Cara"

Para acceder a la cara no se requieren credenciales
Le llamo la cara pero ya no lo, al principio empezo siendo una cara como la de la siguiente imagen:

![[Captura desde 2026-01-17 21-55-59.png]]

Se basaba en el sphere de las vegas para que tuviera apariencia amigable, se tuvo que cambiar por que consumía  el 60% de los recursos mover esos ojos. 

Actualmente esta lo siguiente;  un orbe que hace como un efecto de respiración mientras el sistema habla y al lado una terminal en tiempo real en la que el usuario puede ver la ejecución de los comandos en tiempo real, es decir se vería: 
- La entrada de voz
- Lo el STT transcribe a texto.
- Lo que el router categoriza
- La generación del comando por los grape-models 
- La salida del comando  
También muestra el consumo de recursos, pero hay que remarcar este consumo de recursos no es del servidor es del sistema en el que se ejecuta la ventana web. Podemos acceder a esta ventana en `http://localhost:5000/face`
![alt text](image/image-79.png)

### 4.2 WebUI
La WebUI esta dividida en varios menús cada una con una función. Esta un poco desactualizada y hay cosas que no van, pero da una idea de lo que se busca y el uso que tiene.
La WebUI tiene tanto un modo claro como uno oscuro (aunque el claro te quema los ojos).

Cuando el sistema se desconecta la interfaz web muestra un mensaje de *Conectando con WatermelonD*.
![alt text](image/image-81.png)

#### 4.2.1 Dashboard
Este panel muestra de un vistazo rápido:
- El estado del sistema
- También permite enviar comandos por medio de texto directamente al bus de escucha (para pruebas).
- Un botón para silenciar el micrófono 
- Una zona que indica si el sistema esta o no activo
![alt text](image/image-82.png)

#### 4.2.2 Monitor del sistema
Aquí nos encontramos con un monitor de recursos, y procesos. 
Podemos ver los procesos activos (aquí si es en el servidor) con: 
- **El PID**.
- **El usuario que lo ejecuta**.
- **El consumo de CPU** (aquí vemos el consumo del modo kiosko que es bastante alto) 
- **El uso de ram**. 
En cuanto al monitor de recursos es en tiempo real haciendo uso de *graphana* para almacenar un pequeño margen del historial de consumo desde el inicio del sistema.
![alt text](image/image-83.png)

#### 4.2.3 Herramientas de red
Ahora nos encontramos la pestaña de herramientas de red. 
Nos permite : 
- Ver las **interfaces de red** del sistema
- Hacer un **test de velocidad** usando *speedtest-cli* 
- Un **ping** al *8.8.8.8* 
- **Escanear Wifi** para  conectar el sistema a Internet. (Conectar por wifi no va en la maquina virtual)
![alt text](image/image-84.png)

#### 4.2.4 Terminal del sistema
Aqui tenemos una terminal (no interactiva) para **ejecutar comandos simples**, esta se encuentra *enjaulada* en el directorio del usuario y no puede acceder a otros.

> Cuando decimos que no es interactiva nos referimos a que no permite comandos que requieran una entrada por parte del usuario. Ej: sudo apt update

![alt text](image/image-85.png)

#### 4.2.5 Logs
Desde aquí podemos ver los logs del servicio.
Esta pantalla visualiza los logs que se almacenan en `/logs/` del directorio en el que se encuentra el sistema (`WatermelonD/logs`).
Con los cambios que se han hecho en el sistema de logs a lo largo del proyecto, actualmente solo van las pestañas de *All*, *Web* y *System*

> Se que en este log no va el sistema de audio, lleva asi como un mesy espero que este arreglado para la defensa de este proyecto

![alt text](image/image-86.png)

#### 4.2.6 Acciones
Desde este menu se pueden hacer acciones rápidas en el sistema, entre ellas tenemos:

* **Actualizar WatermelonD**: Esto se hace por medio de `git pull`, si detecta cambios entre el *origin* (carpeta local) y el *remote* (github), los descarga y reinicia el servicio
* **Actualizar Grape/Lime**: Funciona igual que el anterior pero en este caso itera en las carpetas de cada uno de los modelos (`/models`) y comprueba los cambios desde *HugguinFace* que es la pagina web donde se almacenan los modelos.
* **Actualizar Pkgs**: Actualiza el sistema, ejecuta un `apt update`.
* **Limpiar cache**: Elimina la carpeta `.cache` del sistema
* **Crear Backup**: Crea una copia de seguridad de la configuracion `config/config.json`
* **Reiniciar red**: Reinicia el servicio de red usando systemctl
  En la consola de debajo se visualiza la salida de estos comandos
  ![alt text](image/image-87.png)

#### 4.2.7 Gestor de tareas (Cron)
Esto es una interfaz para el cron, por si el usuario quiere ejecutar tareas, lo que se escribe aquí se almacena en el cron a nivel de usuario
![alt text](image/image-88.png)
![alt text](image/image-89.png)

#### 4.2.8 Explorador de archivos
Esta ventana al principio funcionaba un día toque algo y no volvió a funcionar, sigue aquí por que se me olvida quitarla, pero aquí tendríamos un explorador de archivos que permite visualizarlos.
![alt text](image/image-90.png)

#### 4.2.9 Gestor de extensiones
Desde aquí podemos ver las skills instaladas en el sistema, por desgracia no todas.
Requiere referenciar la skill en los archivos de la web (no he conseguido que al meter una skill personalizada salga aquí su nombre automáticamente).
![alt text](image/image-91.png)
Algunas de las skills que hay aquí permiten configuración,  esas son las siguientes: 

* **Archivos**: Esta skill pre-escanea el sistema de archivos en cada inicio del sistema o 24 horas, desde aquí podemos configurar cada cuanto tiempo, archivos a escanear y las rutas. Tambien podemos ejecutar un escaneo
  ![alt text](image/image-92.png)
* **SSH**: Aquí podemos agregar servidores ssh al sistema de la misma forma que desde el instalador
  ![alt text](image/image-93.png)
* **Red**: Desde aquí agregamos servidores y sus alias igual que en el instalador
  ![alt text](image/image-94.png)
* **Otras Skills**: Las skills sin configuración por interfaz gráfica tienen un editor json para editarlas por medio de código.
  ![alt text](image/image-95.png)

#### 4.2.10 NLU
Aquí nos aparecen las frases que el sistema no ha entendido.
Se les puede asignar o una función o una skill. 
Al pulsar en *Reiniciar WatermelonD*, lo hacemos es reentrenar la pequeña red neuronal agregando estos nuevos datos.
![alt text](image/image-96.png)

#### 4.2.11 MQTT
Esta es la ultima función agregada. Permite ver el estado de los agentes que usan el protocolo MQTT, desde aquí podemos: 
- Ver los que están *conectados* y su *estado*. 
- *Generar un script* personalizado para el despliegue en dispositivos **RaspberryPi**.
![alt text](image/image-97.png)

> La ultima pestaña Ajustes un día dejo de funcionar y no he conseguido como repararla, se que esta relacionado con la libreria socket.io pero si la quito deja de funcionar toda la webUI

# ANEXO IX: DOCUMENTACIÓN DE MODELOS PERSONALIZADOS GRAPE

## 1. GRAPE ROUTER (Router Clasificador)

### 1.1. Propósito
El modelo **grape-router** es un modelo de clasificación de texto que actúa como un router clasificador. El modelo se encarga de clasificar el texto que entra al sistema (petición del usuario en lenguaje natural) y clarificarlo en una de las categorías predefinidas,  después esta entrada se enruta al modelo SLM correspondiente. 

### 1.2. Especificaciones

| Aspecto     | Detalle                                                                  |
| :---------- | :----------------------------------------------------------------------- |
| Nombre      | `minilm-l12-grape-route`                                                 |
| Ubicación   | `models/grape-route/`                                                    |
| Framework   | HuggingFace Transformers (`pipeline("text-classification")`)             |
| Formato     | PyTorch estándar                                                         |
| Categorías  | 8 (malbec, syrah, tempranillo, pinot, chardonnay, cabernet, gemma, null) |
| Umbral      | 0.4 (configurable en `config.json`)                                      |
| Caché       | LRU (128 entradas)                                                       |
| Enlace      | https://huggingface.co/jrodriiguezg/minilm-l12-grape-route               |
| Modelo base | `microsoft/Multilingual-MiniLM-L12-H384`                                 |

### 1.3. Categorías de Enrutamiento

El modelo Lime clasifica la petición del usuario en una de las siguientes categorías, cada una asociada a una función del sistema en específico:

| Categoría       | Funcion                    | Descripción                                                                                                                                                           | Ejemplo de entrada                                         |
| :-------------- | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------- |
| **malbec**      | Docker / Contenedores      | Gestión de contenedores Docker y Podman: listar, reiniciar, ver logs, crear y eliminar contenedores                                                                   | "Muéstrame los logs del contenedor nginx"                  |
| **syrah**       | Red / Network              | Herramientas de red: escaneo de red local, ping, WHOIS, consulta de IP, puertos abiertos y diagnóstico de conectividad                                                | "Escanea la red local", "¿Cuál es mi IP?"                  |
| **tempranillo** | Administracion del Sistema | Administración del sistema: reiniciar servicios, actualizar paquetes, gestión de procesos, monitorización de hardware y estado del sistema                            | "Reinicia el servicio ssh", "Actualiza el sistema"         |
| **pinot**       | Búsqueda de Archivos       | Búsqueda y localización de archivos en el sistema: buscar por nombre, extensión, contenido o fecha de modificación usando herramientas como `find`, `grep` y `locate` | "Busca archivos .log", "Encuentra el archivo config.json"  |
| **chardonnay**  | Gestión de Archivos        | Operaciones con archivos y directorios: listar, crear, mover, copiar, eliminar y organizar archivos en el sistema de ficheros                                         | "Lista los archivos en /home", "Borra el archivo temp.txt" |
| **cabernet**    | SSH / Remoto               | Gestión de conexiones SSH: conectar a servidores remotos, ejecutar comandos remotos, listar servidores configurados y transferir archivos                             | "Conecta al servidor web", "Ejecuta top en el servidor"    |
| **gemma**       | Chat / General             | Conversación general: preguntas generales, chistes, saludos . Se redirige al LLM o a una Skill (Gemma 2B)                                                             | "Cuéntame un chiste", "¿Quién  fue Cristobal Colon?"       |
| **null**        | Fuera de dominio           | Se reinicia el bucle e informa al usuario "No he entendido"                                                                                                           | —                                                          |

## 2. MODELOS GRAPE (Modelos T5 de Ejecución)

### 2.1. Propósito
Los modelos **Grape** son 6 modelos especializados, basados en la arquitectura T5 (Text-to-Text Transfer Transformer). 
Cada modelo está reentrenado (fine-tuned) para una función específica y se encargan de traducir las peticiones del usuario en *lenguaje natural* a *comandos ejecutables* (bash, docker, etc.) dentro de su categoría.
Después de que el router le asigne una categoría a la entrada, el sistema redirige la petición al modelo Grape que le corresponda. Todos los modelos usan la misma arquitectura base, lo único diferente es el grupo de datos que se han usado para re entrenarlos.

### 2.2. Especificaciones

| Aspecto          | Detalle                                                      |
| :--------------- | :----------------------------------------------------------- |
| Modelo Base      | salesforce/codet5-small                                      |
| Cantidad         | 7 modelos (uno por categoría técnica)                        |
| Framework        | HuggingFace Transformers                                     |
| Formato original | ONNX (onnxruntime)                                           |
| Función          | Traducción Lenguaje Natural a Comando ejecutable             |
| Gestor           | `MangoManager` (`modules/BrainNut/engine.py`)                |


### 2.3. Modelos por Categoría

| Modelo            | Categoría Lime | Dominio               | Enlace                                                |
| :---------------- | :-------------- | :-------------------- | :---------------------------------------------------- |
| Grape-Malbec      | `malbec`      | Docker / Contenedores | https://huggingface.co/jrodriiguezg/grape-malbec      |
| Grape-Syrah       | `syrah`       | Red / Network         | https://huggingface.co/jrodriiguezg/grape-syrah       |
| Grape-Tempranillo | `tempranillo` | SysAdmin / Sistema    | https://huggingface.co/jrodriiguezg/grape-tempranillo |
| Grape-Pinot       | `pinot`       | Búsqueda de Archivos | https://huggingface.co/jrodriiguezg/grape-pinot       |
| Grape-Chardonnay  | `chardonnay`  | Gestión de Archivos  | https://huggingface.co/jrodriiguezg/grape-chardonnay  |
| Grape-Cabernet    | `cabernet`    | SSH / Remoto          | -                                                     |

> El modelo Grape-Cabernet no esta disponible para descargar ya que entrenar este modelo requiere mas tiempo, esta pendiente. 

### 2.4. Funcionamiento

El flujo de la ejecución es el siguiente:

1. El usuario inicia una solictud al asistente 
2. El sistema transforma el audio a texto.
3. El modelo **grape-route** clasifica la intención y devuelve una categoría junto a un porcentaje de confianza.
4. Si la categoría existe y la confianza es mayor al umbral establecido, el `MangoManager` carga el modelo T5 correspondiente.
5. El modelo Grape seleccionado traduce la petición en lenguaje natural a un comando ejecutable.
6. El sistema ejecuta el comando y devuelve el resultado al usuario.
7. Si la categoría no existe o la confianza es menor al umbral establecido, el sistema devuelve un error.

# ANEXO X: REFERENCIAS Y BIBLIOGRAFÍA

## 1. LIBRERÍAS Y SOFTWARE OPEN SOURCE

El proyecto OpenMacedonIA se construye sobre librerias codigo abierto.

### 1.1. Inteligencia Artificial y Procesamiento

* **Llama.cpp:** Inferencia de LLMs optimizada para CPU. [GitHub](https://github.com/ggerganov/llama.cpp)
* **Vosk API:** Reconocimiento de voz offline ligero. [Web](https://alphacephei.com/vosk/)
* **Faster-Whisper:** Implementación optimizada de Whisper de OpenAI. [GitHub](https://github.com/SYSTRAN/faster-whisper)
* **Padatious:** Motor de intenciones basado en redes neuronales (Mycroft AI). [GitHub](https://github.com/MycroftAI/padatious)
* **FANN (Fast Artificial Neural Network):** Librería de redes neuronales en C. [SourceForge](http://leenissen.dk/fann/wp/)
* **Pytorch**: Para entrenamiento de modelos [Web](https://docs.pytorch.org/docs/stable/index.html)

### 1.2. Infraestructura y Sistema

* **Mosquitto:** Broker MQTT ligero. [Web](https://mosquitto.org/)
* **PyAudio:** Conectores de Python para PortAudio. [Web](https://people.csail.mit.edu/hubert/pyaudio/)
* **ChromaDB:** Base de datos vectorial para RAG. [Web](https://www.trychroma.com/)
* **Debian**: Documentación del sistema [Web](https://wiki.debian.org/es/FrontPage?action=show&redirect=P%C3%A1ginaInicial)
* **SystemD**: Documentación de SystemD desde [Arch Wiki](https://wiki.archlinux.org/title/Systemd_(Espa%C3%B1ol))
* **AppArmor**: Modulo de seguridad de Linux [Web](https://apparmor.net/)
* **Fail2Ban**: Modulo de seguridad [Wiki](https://github.com/fail2ban/fail2ban/wiki)
* **Piper TTS**: Sistema de síntesis de voz offline [GitHub](https://github.com/rhasspy/piper)
- **Flask**: Framework web usado para el backend y la API [Web](https://flask.palletsprojects.com/)
- - **OpenCV**: Biblioteca para visión artificial y detección de presencia [OpenCV](https://opencv.org/)
- 

## 2. DOCUMENTACION USADA 

* **GGUF**: Formato de modelos de IA [Hugguin Face](https://huggingface.co/docs/hub/gguf)
* **KV Cache**: Para optimizar modelos [Reddit](https://www.reddit.com/r/LocalLLaMA/comments/1p1uuf2/help_me_understand_kv_caching/?tl=es-es) y [Hugguin Face](https://huggingface.co/blog/not-lain/kv-caching)
* **NLU**: Entender que era [Web](https://www.datacamp.com/es/blog/natural-language-understanding-nlu)
* **Cuantizacion**: Ayuda a hacer los modelos mas ligeros [Hugguin Face](https://huggingface.co/docs/optimum/llm_quantization/usage_guides/quantization)
* **Sherpa-ONNX**: Ejecutor de modelos [GitHub](https://k2-fsa.github.io/sherpa/onnx/index.html)
* **ReAct**: Técnica de optimizacion [Web](https://www.promptingguide.ai/techniques/react)
* **Guía de Modelos T5**: Una guía bastante extensa sobre como funcionan los modelos T5 [Web](https://medium.com/@gagangupta_82781/understanding-the-t5-model-a-comprehensive-guide-b4d5c02c234b)
* **Documentacion de Hugguin Face**: Incluye todo sobre los modelos de LLM/SLM y su entrenamiento y uso [Hugguin Face](https://huggingface.co/docs/hub/index)
* **Github Docs**: Para entender el control de versiones [Github](https://docs.github.com/es)
* **Reddit**: Navegando en foros para resolver dudas (No tengo todos los enlaces).

## 3. RECURSOS ADICIONALES

* **Repositorio del Proyecto:** [Github](https://github.com/OpenMacedonIA) | [HuggingFace](https://huggingface.co/jrodriiguezg)

# GLOSARIO DE TÉRMINOS TÉCNICOS

Este documento recopila y define todos los términos técnicos y conceptos avanzados utilizados en la documentación del sistema OpenMacedonIA, abarcando administración de sistemas, DevOps, arquitectura de software e Inteligencia Artificial. (Me puedo haber dejado algo).

> La fuente de estos terminos es principalmente la Wikipedia

## A

### ALSA (Advanced Linux Sound Architecture)

Componente del núcleo Linux, introducido en la versión 2.6, que proporciona una interfaz de programación de aplicaciones (API) para controladores de dispositivos de tarjetas de sonido. Fue diseñado para reemplazar al sistema Open Sound System (OSS), ofreciendo soporte para síntesis MIDI por hardware, mezcla multicanal y operación full-dúplex. En OpenMacedonIA se utiliza para la captura de audio de baja latencia, accediendo directamente al hardware sin capas intermedias como PulseAudio.

### AppArmor

Módulo de seguridad del núcleo Linux que restringe las capacidades de los programas individuales mediante perfiles de seguridad. Permite al administrador del sistema asociar a cada programa un perfil que limita sus capacidades, incluyendo el acceso a la red, al sistema de archivos y a operaciones privilegiadas del sistema.

### Artifact (Artefacto)

En el contexto de la integración y entrega continuas (CI/CD), un artefacto es cualquier archivo producido durante el proceso de compilación o pruebas de software, como binarios compilados, informes de test o paquetes de distribución, que se conserva para su uso posterior o su descarga.

## B

### Backpropagation (Retropropagación)

Algoritmo utilizado en el entrenamiento de redes neuronales artificiales supervisadas que calcula el gradiente de la función de pérdida con respecto a cada peso de la red, propagando el error desde la capa de salida hacia las capas anteriores mediante la regla de la cadena del cálculo diferencial. Permite ajustar los pesos de forma iterativa para minimizar el error de predicción del modelo.

### BLE (Bluetooth Low Energy)

Tecnología de red inalámbrica de área personal diseñada y comercializada por el Bluetooth Special Interest Group (SIG), orientada a aplicaciones del Internet de las cosas (IoT). A diferencia del Bluetooth clásico, BLE fue diseñado para proporcionar un consumo de energía considerablemente reducido manteniendo un alcance de comunicación similar.

### Barge-in

En sistemas de diálogo hablado, capacidad que permite al usuario interrumpir al sistema mientras este está generando una respuesta de voz (TTS), deteniendo la reproducción actual para atender la nueva solicitud del usuario.

### Batching

Técnica de procesamiento por lotes en la que múltiples solicitudes o datos se agrupan y procesan simultáneamente en lugar de secuencialmente, mejorando la eficiencia computacional y el rendimiento general del sistema.

## C

### Chain-of-Thought (CoT)

Técnica de ingeniería de prompts en la que se induce a un modelo de lenguaje a generar una cadena de razonamiento paso a paso antes de producir una respuesta final. Investigaciones han demostrado que esta técnica mejora significativamente el rendimiento en tareas que requieren razonamiento aritmético, lógico y de sentido común.

### CI/CD (Continuous Integration / Continuous Deployment)

Conjunto de prácticas de ingeniería de software que combinan la integración continua (CI), donde los cambios de código se integran y verifican automáticamente mediante compilación y pruebas, con el despliegue continuo (CD), donde el software validado se entrega automáticamente a los entornos de producción.

### ChromaDB

Base de datos vectorial de código abierto diseñada para almacenar y consultar embeddings de forma eficiente. Permite realizar búsquedas por similitud semántica sobre grandes colecciones de documentos transformados en representaciones vectoriales.

### Context Window (Ventana de Contexto)

Número máximo de tokens que un modelo de lenguaje puede procesar en una sola interacción, incluyendo tanto la entrada (prompt) como la salida generada. Determina la cantidad de información contextual que el modelo puede considerar simultáneamente durante la inferencia.

## E

### Embedding

En aprendizaje automático y procesamiento del lenguaje natural, representación de objetos discretos (como palabras, frases o documentos) como vectores de números reales en un espacio de dimensión reducida. Los embeddings capturan relaciones semánticas, de modo que objetos con significados similares se representan mediante vectores cercanos en el espacio vectorial.

### Epoch (Época)

En aprendizaje automático, una pasada completa del conjunto de datos de entrenamiento a través del algoritmo de aprendizaje. El entrenamiento de un modelo típicamente requiere múltiples épocas para que los pesos de la red converjan hacia valores óptimos.

## F

### Fail2Ban

Framework de prevención de intrusiones escrito en Python que analiza los archivos de registro del sistema y ejecuta acciones predefinidas, como el bloqueo de direcciones IP, cuando detecta patrones que indican intentos de acceso maliciosos, como múltiples fallos de autenticación.

### FANN (Fast Artificial Neural Network)

Biblioteca de software libre escrita en C que implementa redes neuronales artificiales multicapa. Soporta tanto redes completamente conectadas como redes de conexión dispersa, con ejecución tanto en punto fijo como en punto flotante.

### FFT (Fast Fourier Transform)

Algoritmo eficiente para calcular la transformada discreta de Fourier (DFT) y su inversa. Convierte una señal del dominio del tiempo al dominio de la frecuencia, descomponiéndola en sus componentes frecuenciales. Es fundamental en el procesamiento digital de señales de audio para la extracción de características como los MFCC.

### Fine-Tuning (Ajuste Fino)

En el contexto del aprendizaje por transferencia, proceso de tomar un modelo previamente entrenado en un gran conjunto de datos general y continuar su entrenamiento con un conjunto de datos más pequeño y específico de un dominio concreto, con el objetivo de adaptar el modelo a una tarea particular.

### Fernet

Esquema de cifrado simétrico autenticado incluido en la biblioteca `cryptography` de Python. Garantiza que un mensaje cifrado no pueda ser manipulado ni leído sin la clave, utilizando AES en modo CBC con un HMAC SHA256 para autenticación.

### Fuzzy Logic (Lógica Difusa)

Sistema de lógica matemática basado en el concepto de grado de verdad, en el que los valores de verdad de las variables pueden ser cualquier número real entre 0 y 1, a diferencia de la lógica booleana clásica donde solo existen verdadero o falso. En procesamiento de texto, se aplica a algoritmos de coincidencia aproximada de cadenas (como la distancia de Levenshtein).

## G

### GGUF (GPT-Generated Unified Format)

Formato de archivo binario desarrollado por el proyecto `llama.cpp` para almacenar modelos de lenguaje cuantizados. Está optimizado para la carga rápida, el mapeo de memoria (mmap) y la ejecución eficiente de modelos en CPU y GPU.

## H

### Hallucination (Alucinación)

En el contexto de la inteligencia artificial generativa, fenómeno por el cual un modelo de lenguaje genera información que parece factual y coherente pero que es incorrecta, inventada o no respaldada por los datos de entrenamiento. Es uno de los principales desafíos de los LLMs actuales.

## I

### IaC (Infrastructure as Code)

Proceso de gestión y aprovisionamiento de infraestructura informática mediante archivos de definición legibles por máquina, en lugar de la configuración manual de hardware o el uso de herramientas de configuración interactivas. Permite versionar, reutilizar y automatizar la infraestructura de la misma forma que el código fuente.

### In-Context Learning

Capacidad de los modelos de lenguaje grandes para realizar nuevas tareas a partir de ejemplos proporcionados directamente en el prompt de entrada (few-shot learning), sin necesidad de modificar ni reentrenar los parámetros del modelo.

### Intent (Intención)

En el procesamiento del lenguaje natural (NLU), una intención representa el objetivo o la acción que un usuario desea realizar al emitir una frase. Los sistemas de comprensión del lenguaje clasifican las expresiones del usuario en intenciones predefinidas para determinar la acción apropiada.

## K


### KV Cache (Key-Value Cache)

Técnica de optimización utilizada durante la inferencia en modelos basados en la arquitectura Transformer, que almacena los vectores de claves (Keys) y valores (Values) calculados para tokens anteriores, evitando su recálculo en cada paso de generación autoregresiva y acelerando significativamente el proceso de inferencia.

## L

### Latency (Latencia)

En informática y telecomunicaciones, intervalo de tiempo que transcurre entre el envío de una solicitud y la recepción de la respuesta correspondiente. En sistemas de reconocimiento de voz, una latencia baja (<500ms) es crítica para mantener una experiencia de interacción natural.

### LLM (Large Language Model)

Modelo de lenguaje basado en redes neuronales de aprendizaje profundo, entrenado con grandes cantidades de datos textuales, capaz de generar, comprender, resumir y traducir texto en lenguaje natural. Los LLMs utilizan la arquitectura Transformer y contienen típicamente miles de millones de parámetros.

### LoRA (Low-Rank Adaptation)

Técnica de ajuste fino eficiente para modelos de lenguaje grandes que congela los pesos del modelo preentrenado e introduce matrices de bajo rango entrenables en las capas del Transformer. Reduce drásticamente el número de parámetros entrenables y los requisitos de memoria, manteniendo un rendimiento comparable al ajuste fino completo.

## M

### MQTT (Message Queuing Telemetry Transport)

Protocolo de red ligero de publicación-suscripción que transporta mensajes entre dispositivos. Fue diseñado en 1999 por Andy Stanford-Clark (IBM) y Arlen Nipper para la monitorización remota de oleoductos por satélite. Es un estándar OASIS y una recomendación ISO (ISO/IEC 20922), ampliamente utilizado en aplicaciones de Internet de las cosas (IoT) por su bajo consumo de ancho de banda y recursos.

## N

### NER (Named Entity Recognition)

Subtarea del procesamiento del lenguaje natural que busca localizar y clasificar entidades nombradas mencionadas en texto no estructurado en categorías predefinidas como nombres de personas, organizaciones, ubicaciones, expresiones temporales, cantidades monetarias y porcentajes.

### NLU (Natural Language Understanding)

Subcampo de la inteligencia artificial y la lingüística computacional que se ocupa de la comprensión automática del lenguaje humano por parte de las máquinas. Incluye tareas como la clasificación de intenciones, la extracción de entidades y el análisis semántico.

## O

### OOM Killer (Out of Memory Killer)

Mecanismo del núcleo Linux que se activa cuando el sistema se queda sin memoria disponible. Selecciona y termina uno o más procesos para liberar memoria y evitar el colapso completo del sistema, utilizando una heurística que asigna una puntuación (oom_score) a cada proceso.

## P

### PCM (Pulse Code Modulation)

Método utilizado para representar digitalmente señales analógicas muestreadas. La amplitud de la señal analógica se muestrea a intervalos regulares y cada muestra se cuantifica al valor más cercano dentro de un rango de valores discretos. Es el formato estándar de audio digital sin compresión.

### Perplexity (Perplejidad)

En teoría de la información y procesamiento del lenguaje natural, medida de qué tan bien un modelo probabilístico predice una muestra de datos. Una perplejidad más baja indica una mejor capacidad predictiva del modelo. Se utiliza comúnmente para evaluar y comparar modelos de lenguaje.

### Prompt Engineering (Ingeniería de Prompts)

Disciplina dentro de la inteligencia artificial que se ocupa del diseño y optimización de las entradas textuales (prompts) proporcionadas a modelos de lenguaje grandes para obtener respuestas precisas, relevantes y útiles. Incluye técnicas como few-shot prompting, chain-of-thought y role prompting.

## Q

### Quantization (Cuantización)

En el contexto de modelos de aprendizaje automático, proceso de reducción de la precisión numérica de los pesos y activaciones de un modelo, por ejemplo de punto flotante de 32 bits (FP32) a enteros de 4 bits (INT4). Reduce significativamente el tamaño del modelo y los requisitos de memoria, con una pérdida mínima de precisión en la mayoría de los casos.

## R

### RAG (Retrieval-Augmented Generation)

Técnica que combina la generación de texto mediante modelos de lenguaje con la recuperación de información de fuentes externas. Ante una consulta, el sistema primero recupera documentos relevantes de una base de conocimiento y luego los utiliza como contexto adicional para generar una respuesta más precisa y fundamentada.

### ReAct (Reasoning + Acting)

Paradigma de agentes de IA en el que un modelo de lenguaje genera de forma alternada trazas de razonamiento verbal y acciones concretas. Permite al modelo interactuar con herramientas externas (APIs, bases de datos, motores de búsqueda) y utilizar las observaciones obtenidas para refinar su razonamiento.

## S

### Sherpa-ONNX

Runtime de inferencia de código abierto desarrollado por el proyecto k2-fsa (Next-gen Kaldi), optimizado para la ejecución de modelos de procesamiento de voz (STT/TTS/VAD) en formato ONNX. Permite ejecutar modelos de reconocimiento de voz cuantizados con alto rendimiento en CPU, sin necesidad de GPU.

### STT (Speech-to-Text) / ASR (Automatic Speech Recognition)

Tecnología interdisciplinar del subcampo de la lingüística computacional que permite el reconocimiento y la traducción del lenguaje hablado a texto por parte de un sistema informático. Los sistemas modernos de ASR utilizan técnicas de aprendizaje profundo y modelos basados en la arquitectura Transformer.

### Swappiness

Parámetro configurable del núcleo Linux (valor entre 0 y 100) que controla la tendencia relativa del kernel a reclamar páginas de memoria de los procesos frente a descartar páginas de la caché. Un valor alto favorece el uso del espacio de intercambio (swap), mientras que un valor bajo prioriza mantener los procesos en memoria RAM.

### System Prompt

Instrucción inicial proporcionada a un modelo de lenguaje que define su comportamiento, personalidad, restricciones y formato de respuesta antes de que comience la interacción con el usuario. No es visible para el usuario final y actúa como configuración base del modelo.

## T

### Temperature (Temperatura)

Hiperparámetro utilizado durante la generación de texto en modelos de lenguaje que controla la aleatoriedad de la distribución de probabilidad sobre el vocabulario. Una temperatura cercana a 0 produce salidas más deterministas y conservadoras, mientras que valores más altos (>1.0) aumentan la diversidad y creatividad de las respuestas generadas.

### Token

Unidad básica de procesamiento de texto en modelos de lenguaje. Un token puede representar una palabra completa, un fragmento de palabra (subword) o un carácter individual, dependiendo del algoritmo de tokenización utilizado (BPE, WordPiece, SentencePiece, etc.).

### Transformer

Arquitectura de red neuronal propuesta en el artículo «Attention Is All You Need» (Vaswani et al., 2017). Se basa en mecanismos de auto-atención (self-attention) que permiten procesar secuencias completas de datos en paralelo, a diferencia de las redes recurrentes. Es la arquitectura base de la mayoría de los modelos de lenguaje modernos (GPT, BERT, T5, Gemma, etc.).

### TTS (Text-to-Speech)

Tecnología de síntesis de voz que convierte texto escrito en habla artificial. Los sistemas modernos de TTS utilizan modelos neuronales que generan audio con una calidad cercana a la voz humana natural.

## V

### VAD (Voice Activity Detection)

Técnica utilizada en el procesamiento del habla cuyo objetivo es detectar la presencia o ausencia de voz humana en una señal de audio. Se emplea para determinar cuándo un usuario comienza y termina de hablar, optimizando el uso de recursos al procesar únicamente los segmentos que contienen habla.

### Vector Database (Base de Datos Vectorial)

Sistema de gestión de bases de datos optimizado para almacenar, indexar y consultar datos en forma de vectores de alta dimensión (embeddings). Utiliza algoritmos de búsqueda de vecinos más cercanos aproximados (ANN) para realizar consultas de similitud semántica de forma eficiente.

## W

### Wake Word (Palabra de Activación)

Palabra o frase clave predefinida que activa un asistente de voz desde un estado de reposo de bajo consumo a un estado de escucha activa. Ejemplos conocidos incluyen «Hey Siri», «OK Google» y «Alexa».

### WER (Word Error Rate)

Métrica estándar para evaluar el rendimiento de sistemas de reconocimiento automático del habla y traducción automática. Se calcula como la proporción de errores a nivel de palabra: (Sustituciones + Inserciones + Eliminaciones) / Número total de palabras de referencia.

### AppArmor

Módulo de seguridad del kernel de Linux que permite al administrador restringir las capacidades de un programa mediante perfiles. Se utiliza para "enjaular" los procesos del asistente, limitando su acceso al sistema de archivos y red.

### Artifact (Artefacto)

En el contexto de CI/CD (GitHub Actions), se refiere a los archivos generados por un paso del pipeline (ej. binarios compilados, logs de test) que se guardan para ser usados en pasos posteriores o para su descarga.




