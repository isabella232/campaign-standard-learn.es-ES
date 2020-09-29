---
title: 'Proceso de transición: cambio de las plataformas de correo electrónico'
description: 'Al mover proveedores de servicio de correo electrónico (ESP), tampoco es posible realizar transiciones en las direcciones IP existentes. Es importante que siga las prácticas recomendadas para desarrollar una reputación positiva a partir de ahora. Debido a que las nuevas direcciones IP que va a usar todavía no tienen reputación, los ISP no pueden confiar plenamente en el correo que les viene y deben ser cautelosos en lo que permiten que se entreguen a sus clientes. '
feature: null
topics: Deliverability
kt: null
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f4dbccc1fea3db4dbddec0d4329b359993b62d20
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---


# Proceso de transición: cambio de las plataformas de correo electrónico

Al mover proveedores de servicio de correo electrónico (ESP), tampoco es posible realizar transiciones en las direcciones IP existentes. Es importante que siga las prácticas recomendadas para desarrollar una reputación positiva a partir de ahora. Debido a que las nuevas direcciones IP que va a usar todavía no tienen reputación, los ISP no pueden confiar plenamente en el correo que les viene y deben ser cautelosos en lo que permiten que se entreguen a sus clientes.

Piensen en lo que hacen cuando conocen a alguien nuevo. Generalmente, necesita generar confianza en lugar de confiar en ellos de inmediato. No pienses que tu marca va a ayudar automáticamente con esa confianza, porque los remitentes de spam usarán tu nombre para hacer cosas malas. Los ISP necesitan revaluar sus prácticas de envío, ya que la acción es más reveladora en la entrega de correo electrónico.

Establecer una reputación positiva es un proceso. Pero una vez que se haya establecido, los indicadores negativos pequeños tendrán menos impacto en usted y en su envío de correo.

![El proceso de transición](assets/transition-process.png)

La cantidad de tiempo para calentar sus direcciones IP y dominios puede variar, pero hasta un punto de referencia de ocho semanas es común para los remitentes típicos para establecer una reputación en la mayoría de los ISPs de Nivel 1 ([!DNL Gmail], [!DNL Microsoft], [!DNL Verizon]/[!DNL Yahoo]/[!DNL AOL], etc.).
En las siguientes secciones, investigaremos algunas áreas clave en las que centrarnos correctamente.

## Infraestructura

El éxito de la entrega depende de una base sólida. La infraestructura de correo electrónico es un elemento central. Una infraestructura de correo electrónico correctamente construida incluye varios componentes: a saber, dominio(s) y dirección(es) IP. Estos componentes son como la maquinaria que hay detrás de los correos electrónicos que se envían y suelen ser el ancla del envío de reputación. Los consultores de capacidad de entrega garantizan que estos elementos se configuran correctamente durante la implementación, pero debido al elemento de reputación, es importante que tenga esta comprensión básica.

### Configuración y estrategia del dominio

Los tiempos han cambiado, y algunos ISP (como [!DNL Gmail] y [!DNL Yahoo]) ahora incorporan la reputación de dominio como un punto adicional cuando se trata de adjuntar la reputación de correo electrónico a un remitente. Su reputación de dominio se basa en su dominio de envío en lugar de en su dirección IP. Esto significa que su marca tiene prioridad cuando se trata de decisiones de filtrado de ISP.

Parte del proceso de integración de nuevos remitentes en Adobe Campaign incluye la configuración de los dominios de envío y la garantía de que la infraestructura se ha establecido correctamente. Debe trabajar con un experto en los dominios que planea utilizar a largo plazo. A continuación se ofrecen algunas sugerencias que dan forma a una buena estrategia de dominio:

* Sea lo más claro y reflexivo posible de la marca con el dominio que elija para que los usuarios no identifiquen incorrectamente el correo como correo no deseado. Algunos ejemplos son [!DNL newsletter.foo.com], [!DNL receipts.foo.com]etc.
* No debe usar el dominio principal o corporativo, ya que podría afectar el envío de correo de su organización a los ISP.
* Considere utilizar un subdominio del dominio principal para legitimar el dominio de envío.
* Separe los subdominios para las categorías de mensajes de marketing y transaccionales. Esto ayudará al flujo de tráfico de correo electrónico de forma más fiable, ya que los ISP buscan este método de envío, que es una práctica recomendada conocida y muy recomendable.

### Estrategia IP

Es importante formar una estrategia de IP bien estructurada para ayudar a establecer una reputación positiva. La cantidad de IPs y la configuración varía según el modelo de negocio y los objetivos de mercadotecnia. Trabajar con un experto para desarrollar una estrategia clara para el inicio correcto. Tenga en cuenta lo siguiente:

* Demasiadas direcciones IP pueden provocar problemas de reputación ya que es una táctica común de los remitentes de spam para las raquetas de nieve, una táctica utilizada por los remitentes de spam, donde el tráfico se propaga en muchas direcciones IP para maximizar el envío del correo no deseado. Aunque no sea un remitente de spam, es posible que tenga el mismo aspecto si utiliza demasiadas direcciones IP, especialmente si estas no han tenido ningún tráfico anterior.
* Muy pocas IP pueden causar problemas de rendimiento y desencadenar problemas de reputación. El rendimiento varía según el ISP. La cantidad y la rapidez con que un ISP está dispuesto a aceptar se basan generalmente en su infraestructura y en el envío de umbrales de reputación.
* Es fundamental separar el tráfico de los tipos de mensajes. Es importante separar, como mínimo, el correo transaccional y de mercadotecnia en grupos de IP independientes.
* Según la estrategia de correo, también puede ser aconsejable separar diferentes productos o flujos de mercadotecnia en diferentes grupos de IP si su reputación es drásticamente diferente. Algunos especialistas en marketing también segmentan por región. La separación de la IP para el tráfico con una reputación menor no solucionará el problema de reputación, pero evitará problemas con sus envíos de correo electrónico de &quot;buena&quot; reputación. Después de todo, no quieres sacrificar tu buena audiencia por una más riesgosa.

### Bucles de comentarios

Entre bastidores, Adobe Campaign está procesando datos sobre devoluciones, quejas, cancelaciones de suscripción y más. La configuración de estos bucles de comentarios es un aspecto importante de la capacidad de entrega. Las quejas pueden dañar la reputación, por lo que debe eliminar las direcciones de correo electrónico que registran las quejas de la audiencia de destinatario. Es importante tener en cuenta que [!DNL Gmail] no devuelve estos datos. Los encabezados de cancelación de suscripción de listas y el filtrado de participación son especialmente importantes para [!DNL Gmail] los suscriptores, que ahora comprenden la mayoría de las bases de datos de suscriptores.

### Autenticación

La autenticación es el proceso que utilizan los ISP para validar la identidad de un remitente. Los dos protocolos de autenticación más comunes son [!DNL Sender Policy Framework (SPF)] y [!DNL DomainKeys Identified Mail] (DKIM). Estos no son visibles para el usuario final, pero sí ayudan a los ISP a filtrar el correo electrónico de remitentes verificados. [!DNL Domain-based Message Authentication Reporting and Conformance] (DMARC) está ganando popularidad, aunque sus políticas todavía no están incorporadas por todos los ISP en sus sistemas de reputación.

#### **SPF**

[!DNL Sender Policy Framework (SPF)] es un método de autenticación que permite al propietario de un dominio especificar qué servidores de correo utilizan para enviar correo desde ese dominio.

#### **DKIM**

[!DNL Domain Keys Identified Mail (DKIM)] es un método de autenticación que se utiliza para detectar direcciones de remitente falsificadas (comúnmente llamadas [!DNL spoofing]). Si DKIM está habilitado, permite al receptor confirmar si el remitente está autorizado para enviar correo desde ese dominio.

#### **DMARC**

[!DNL Domain-based Message Authentication, Reporting and Conformance (DMARC)] es un método de autenticación que permite a los propietarios de dominios proteger su dominio de usos no autorizados. DMARC utiliza SPF o DKIM o ambos para permitir que el propietario de un dominio controle lo que sucede con el correo que falla la autenticación: entregado, puesto en cuarentena o rechazado.

## Criterios de objetivo

Al enviar nuevo tráfico, solo destinatario a los usuarios más comprometidos durante las primeras fases del calentamiento de la IP. Esto ayuda a establecer una reputación positiva desde el principio para generar confianza de manera efectiva antes de avanzar en sus audiencias menos comprometidas. Esta es una fórmula básica para la participación:

![Fórmula de compromiso](assets/formula-for-enagement.png)

Normalmente, una tasa de participación se basa en un período de tiempo específico. Esta métrica puede variar drásticamente dependiendo de si la fórmula se aplica en un nivel general o para tipos o campañas de correo específicos. Los criterios de objetivo específicos deben proporcionarse trabajando con el consultor de entregas de Adobe Campaign, ya que cada remitente y ISP varía y generalmente requiere un plan personalizado.

## Consideraciones específicas de los ISP durante el calentamiento de la propiedad intelectual

Los ISP tienen diferentes reglas y diferentes maneras de ver su tráfico. Por ejemplo, [!DNL Gmail] es uno de los ISP más sofisticados porque ven la participación muy estrictamente (aperturas y clics) además de todas las demás medidas de reputación. Esto requiere un plan personalizado que solo destinatario a los usuarios más comprometidos al principio. Otros ISP pueden requerir lo mismo. Trabaje con el consultor de entregas de Adobe Campaign para un plan específico.

## Volumen

El volumen de correo que envía es fundamental para establecer una reputación positiva. Pónganse en un ISP - si inicio ver un montón de tráfico de alguien que no conoce, sería alarmante. Enviar un gran volumen de correo inmediatamente es arriesgado y sin duda causará problemas de reputación que a menudo son difíciles de resolver. Puede ser frustrante, llevar mucho tiempo y costoso sacarse de una mala reputación y resolver problemas de bloqueo que resultan de enviar demasiado pronto.

Los umbrales de volumen varían según el ISP y también pueden variar según las métricas de participación promedio. Algunos remitentes requieren una rampa de volumen muy baja y lenta, mientras que otros pueden permitir una rampa de volumen más pronunciada. Recomendamos trabajar con un experto, como un consultor de entregas de Adobe Campaign, para desarrollar un plan de volumen personalizado.

Esta es una lista de sugerencias y sugerencias para la transición sin problemas:

* **El permiso** es la base de cualquier programa de correo electrónico exitoso.
* **Inicio** bajo y lento con volúmenes de envío bajos y luego aumentar a medida que se establece la reputación del remitente.
* Una estrategia **de correo** en tándem le permite aumentar el volumen en la Campaña mientras se desplaza con el ESP actual, sin interrumpir el calendario de correo electrónico.
* **La participación importa** : inicio con los suscriptores que abren y hagan clic en sus correos electrónicos con regularidad.
* **Siga el plan** — nuestras recomendaciones han ayudado a cientos de clientes de Campaña a aumentar con éxito sus programas de correo electrónico.
* **Monitoree su cuenta** de correo electrónico de respuesta. Es una mala experiencia que el cliente use [!DNL nore-ply@xyz.com] o no responda.
* Las direcciones inactivas pueden tener un impacto negativo en la entrega. **Reactive y vuelva a autorizar** en su plataforma actual, no en sus nuevas IP.
* **Dominios** : utilice un dominio emisor que sea un subdominio del dominio real de la compañía. Por ejemplo, si el dominio de compañía es [!DNL xyz.com], [!DNL email.xyz.com] proporciona más credibilidad a los ISP que [!DNL xyzemail.com]
* **Transparencia** : los detalles de registro de su dominio de correo electrónico deberían estar disponibles públicamente y no deberían ser privados.

En muchas circunstancias, el correo transaccional no sigue el enfoque tradicional de calentamiento promocional. Obviamente, es difícil controlar el volumen en el correo transaccional debido a su naturaleza, ya que generalmente requiere una interacción del usuario para activar el contacto por correo electrónico. En algunos casos, el correo transaccional puede simplemente ser transitado sin un plan formal. En otros casos, puede ser mejor transición de cada tipo de mensaje con el paso del tiempo para aumentar el volumen lentamente. Por ejemplo, puede que desee realizar la transición de la siguiente manera:

1. Confirmaciones de compra: alta participación en general
2. Abandono del carro de compras: compromiso alto medio en general
3. Correos electrónicos de bienvenida: alta participación pero pueden contener direcciones incorrectas según los métodos de recopilación de listas
4. Correos electrónicos de respaldo: participación más baja en general

## Recursos adicionales

* [Inicio de una nueva plataforma](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/managing-deliverability/starting-new-platform.html)
