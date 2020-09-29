---
title: Otras métricas importantes para la capacidad de entrega
description: Una de las mejores maneras de identificar un problema de reputación de envío es a través de las métricas. Veamos algunas métricas clave de entregabilidad para monitorearlas y cómo utilizarlas para identificar un problema de reputación.
feature: null
topics: Deliverability
kt: 5256
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: 7aa32d583ac2ea756945a17634fb477d7b94cb7f
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 1%

---


# Otras métricas importantes para la capacidad de entrega

Una de las mejores maneras de identificar un problema de reputación de envío es a través de las métricas. Veamos algunas métricas clave de entregabilidad para monitorearlas y cómo utilizarlas para identificar un problema de reputación.

## Devoluciones

Las devoluciones son el resultado de un intento de envío y un error en el que el ISP proporciona notificaciones de error de devolución. El procesamiento de la manipulación de rebotes es es una parte fundamental de la higiene de la lista. Después de que un correo electrónico dado haya rebotado varias veces seguidas, este proceso lo marca para la supresión. El número y el tipo de devoluciones necesarios para desencadenar la supresión varían de un sistema a otro. Este proceso impide que los sistemas continúen enviando direcciones de correo electrónico no válidas. Las devoluciones son uno de los datos clave que utilizan los ISP para determinar la reputación de la IP. Es muy importante tener en cuenta esta métrica. &quot;Enviado&quot; versus &quot;devuelto&quot; es probablemente la forma más común de medir el envío de los mensajes de mercadotecnia: cuanto mayor sea el porcentaje entregado, mejor. Exploraremos dos tipos diferentes de devoluciones.

## Rechazos graves

Las devoluciones en firme son errores permanentes generados después de que un ISP determine que un intento de correo a una dirección de suscriptor no es posible entregar. Dentro de Adobe Campaign, las devoluciones duras que se categorizan como no entregables se agregan a la cuarentena, lo que significa que no se volverían a tentar. Hay algunos casos en los que se ignoraría una devolución forzada si se desconoce la causa del error. Estos son algunos ejemplos comunes de rebotes duros:

* La dirección no existe
* Cuenta deshabilitada
* Sintaxis incorrecta
* Dominio incorrecto

## Rechazos leves

Las devoluciones en software son errores temporales que los ISP generan cuando tienen dificultades para enviar correo. Los errores de software se reintentarán varias veces (con varianza según el uso de la configuración de envío de Adobe Campaign personalizada o predeterminada) para intentar un envío correcto. Las direcciones que rebotan continuamente en suave no se añadirán a la cuarentena hasta que se haya intentado el número máximo de reintentos (lo que de nuevo varía según la configuración). Algunas de las causas comunes de las devoluciones en blanco son las siguientes:

* Buzón de correo lleno
* Recibiendo el servidor de correo electrónico inactivo
* Problemas de reputación del remitente

![tipos de devolución](assets/bounce-types.png)

>[!NOTE]
>
>Las devoluciones son un indicador clave de un problema de reputación porque pueden resaltar una fuente de datos incorrecta (devolución forzada) o un problema de reputación con un ISP (devolución suave).
Las devoluciones en blanco suelen aparecer como parte del envío de correo electrónico y se les debe permitir resolverse durante el procesamiento de reintentos antes de caracterizarse como un problema de entrega real. Si la tasa de devoluciones suave es buena en más del 30 por ciento para un único ISP y no se resuelve en un plazo de 24 horas, es recomendable plantear una inquietud con el consultor de entregas de Adobe Campaign.

## Reclamaciones

Las quejas se registran cuando un usuario indica que un mensaje de correo electrónico no es deseado o es inesperado. Esta acción del suscriptor generalmente se registra a través del cliente de correo electrónico del suscriptor cuando pulsa el botón de spam o a través de un sistema de sistema de informes de correo no deseado de terceros.

### Denuncia de ISP

La mayoría de los ISP de nivel 1 y algunos de nivel 2 proporcionan un método de sistema de informes de spam a sus usuarios, ya que los procesos de exclusión y cancelación de suscripción se han utilizado de forma maliciosa en el pasado para validar una dirección de correo electrónico. Adobe Campaign recibe estas quejas a través de ISP FBLs. Esto se establece durante el proceso de configuración para cualquier ISP que proporcione FBLs y permite a Adobe Campaign agregar automáticamente direcciones de correo electrónico que se quejen a la tabla de cuarentenas para su supresión. Los picos en las quejas de los ISP pueden ser un indicador de la mala calidad de la lista, de los métodos de recopilación de listas menos que óptimos o de las políticas de participación débiles. También se señalan con frecuencia cuando el contenido no es relevante.

### Denuncias de terceros

Existen varios grupos anti-spam que permiten el sistema de informes de spam a un nivel más amplio. Las métricas de quejas utilizadas por estos terceros se utilizan para etiquetar el contenido del correo electrónico e identificar el correo no deseado. Este proceso también se conoce como huellas dactilares. Los usuarios de estos métodos de queja de terceros generalmente son más conocedores del correo electrónico, por lo que pueden tener un bueno impacto que otras quejas si no se les responde.

>[!NOTE]
>
>Los ISP recopilan quejas y las utilizan para determinar la reputación general de un remitente. Todas las denuncias deben suprimirse y ya no deben ponerse en contacto con la mayor rapidez posible y de conformidad con las leyes y reglamentos locales.

## Trampas de correo no deseado

Una trampa de spam es una dirección que se utiliza para identificar un correo electrónico no solicitado o no autorizado. Existen trampas no deseadas que ayudan a identificar el correo de remitentes fraudulentos o de personas que no siguen las optimizaciones del correo electrónico. La dirección de correo electrónico de la trampa de spam generalmente no se publica públicamente y es casi imposible de identificar. El envío de mensajes de correo electrónico a trampas no deseadas puede afectar su reputación con diferentes grados de gravedad según el tipo de trampa y el ISP. Obtenga más información sobre los distintos tipos de trampas de spam en las siguientes secciones.

### Reciclado

Las trampas recicladas de spam son direcciones que antes eran válidas pero que ya no se utilizan. Una manera clave de mantener las listas lo más limpias posible es enviar correos electrónicos con regularidad a toda la lista y suprimir correctamente los correos electrónicos devueltos. Esto ayuda a que las direcciones de correo electrónico abandonadas se pongan en cuarentena y a que no se utilicen más.

En algunos casos, una dirección puede reciclarse en un plazo de 30 días. El envío regular es un aspecto vital de la buena higiene de la lista, junto con la supresión regular de los usuarios inactivos. Las campañas de reparticipación suelen formar parte de sofisticados programas de marketing por correo electrónico. Este estilo de campaña permite al remitente intentar recuperar usuarios que de otra manera ya no se enviarían por correo.

### Typo

Una trampa de spam tipográfica es una dirección que contiene errores ortográficos o malformaciones. Esto suele ocurrir con errores de ortografía conocidos de dominios importantes como [!DNL Gmail] (por ejemplo: [!DNL gmail] es un error tipográfico frecuente). Los ISP y otros operadores de lista de bloques registrarán los dominios malos conocidos que se utilizarán como trampa de spam para identificar a los remitentes de spam y medir el estado del remitente. La mejor manera de evitar las trampas de spam de errores tipográficos es utilizar un proceso de selección de dobles para la recopilación de listas.

### Pristina

Una trampa de spam prístina es una dirección que no tiene usuario final y que nunca ha tenido un usuario final. Es una dirección que se creó únicamente para identificar el correo no deseado. Este es el tipo de trampa de spam más impactante, ya que es prácticamente imposible identificarlo y requeriría un esfuerzo considerable para limpiarlo de su lista. La mayoría de las listas negras utilizan trampas de spam prístinas para lista a remitentes que no son fiables. La única manera de evitar que las trampas de spam prístinas infecten su lista de correo electrónico de mercadotecnia más amplia es utilizar un proceso de selección de dobles para la recopilación de listas.

## Bulking

Bulking es el envío del correo en la carpeta de correo no deseado o no deseado de un ISP. Es identificable cuando una tasa de apertura baja más de lo normal (y a veces una tasa de clics) se combina con una tasa de entrega alta. Las causas por las que se abrogan los correos electrónicos varían según el ISP. En general, sin embargo, si los mensajes se colocan en la carpeta masiva, un indicador que influye en el envío de reputación (higiene de la lista, por ejemplo) requiere una reevaluación. Es una señal de que la reputación está disminuyendo, lo que es un problema que debe corregirse inmediatamente antes de que afecte a campañas adicionales. Póngase en contacto con su asesor de capacidad de entrega de Adobe Campaign para solucionar cualquier problema relacionado con el llenado de combustible en función de su situación.

## Bloqueo

Se produce un bloqueo cuando los indicadores de spam alcanzan umbrales ISP propietarios y el ISP comienza a bloquear el correo (visible a través de intentos de envío devueltos) de un remitente. Hay varios tipos de bloques. Generalmente, los bloques se producen de forma específica a una dirección IP, pero también pueden producirse a nivel de dominio o entidad de envío. La resolución de un bloque requiere experiencia específica, por lo que póngase en contacto con el consultor de entregas de Adobe Campaign para obtener ayuda.

## Lista negra

Una lista negra se produce cuando un administrador de listas negras de terceros registra un comportamiento de tipo spammer asociado con un remitente. La causa de una lista negra a veces la publica el partido que la pone en la lista negra. Un listado se basa generalmente en la dirección IP, pero en casos más graves puede ser por intervalo de IP o incluso por dominio de envío. La resolución de una lista negra debe incluir la asistencia de su consultor de entregas de Adobe Campaign para resolver y evitar la posible aparición de nuevos anuncios. Algunas listas son extremadamente severas y pueden causar problemas de reputación duraderos que son difíciles de resolver. El resultado de una lista negra varía según la lista negra pero tiene el potencial de afectar el envío de todo el correo electrónico.

## Recursos adicionales

* [Tipos y motivos de errores de entrega](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/monitoring-messages/understanding-delivery-failures.html#delivery-failure-types-and-reasons)
