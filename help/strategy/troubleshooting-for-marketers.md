---
title: Solución de problemas para los especialistas en marketing
description: Conocer los errores más comunes puede ayudarle a solucionar problemas más rápidamente y aumentar su productividad. Estas sugerencias para la solución de problemas le ayudarán a resolver de forma eficaz errores similares a medida que se producen.
version: Standard
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
source-git-commit: bc9e83e1864b02208f9cd7fe591c77bf6d049a37
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 1%

---


# Solución de problemas para los especialistas en marketing: 5 Errores comunes de flujo de trabajo y envío

Por: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Consultor Superior, Meijer

Como ingeniero sénior y experto en clientes en productos de Adobe Experience Cloud durante los últimos cinco años, habilito a los usuarios empresariales en [Meijer](https://www.meijer.com/){target="_blank"}, una cadena de supercentros norteamericana fundada en 1934, para ejecutar campañas complejas y de marketing y transaccionales con ACS. Algunos proyectos en los que he trabajado incluyen campañas personalizadas para almacenar ofertas y detalles de pedidos para su personalización, integradas con Adobe Audience Manager, y perspectiva del cliente para la incorporación de segmentos.


En mi tiempo usando ACS, he encontrado errores que pueden consumir mucho tiempo y ser frustrantes de resolver. Conocer los errores más comunes puede ayudarle a solucionar problemas más rápidamente y aumentar su productividad. A continuación encontrará mis sugerencias para la resolución de problemas a fin de ayudarle a resolver de forma eficaz errores similares a medida que se producen.

## Error de no coincidencia de tipo de datos

**Código de error:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**Causa:**
Estos tipos de errores aparecen en un flujo de trabajo cuando intenta conciliar utilizando campos de diferentes tipos de datos. Por ejemplo, cuando se carga un archivo utilizando un archivo de carga que tiene un campo de cadena, y se intenta reconciliar el campo de cadena con un campo de perfil que tiene un tipo de datos de int.

![data-type-mismatch-error](/help/assets/kt-13256/data-type-mismatch.png)

**Solución:**
Cambie el tipo de datos del campo en la actividad &quot;Cargar archivo&quot; por el que coincida. Abra la actividad &quot;Cargar archivo&quot;. Vaya a la pestaña &quot;DEFINICIÓN DE COLUMNA&quot; y cambie el tipo de datos del campo deseado.


![data-type-dismatch-solution](/help/assets/kt-13256/data-type-mismatch-solution.png)

## Error de personalización de entregas

**Código de error:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Causa:**
Este error aparece cuando envía un correo electrónico a una dirección, pero el correo electrónico o cualquier otro identificador no se concilia con un perfil. Para enviar una comunicación por correo electrónico, el correo electrónico o el identificador siempre deben estar vinculados a un perfil.

Utilice la actividad de reconciliación como se muestra a continuación:

![flujo de trabajo con actividad de reconciliación](/help/assets/kt-13256/del-persn-error-wf.png)

**Solución:**
Debe existir un ID común del archivo cargado con la tabla de destinatarios. Esta clave común une el archivo de carga a la tabla de destinatarios dentro de la actividad de reconciliación. Es posible que no se envíen correos electrónicos a registros que no existen en la tabla de destinatarios y que requieran este paso de reconciliación dentro del flujo de trabajo. Al hacerlo, reconciliaría la actividad del archivo de carga entrante con un identificador como el ID de correo electrónico del perfil. La variable `nms:recipient` schema hace referencia a la tabla de perfiles y reconciliar los registros entrantes con el perfil lo hace disponible durante la preparación del correo electrónico.

Consulte la captura de pantalla para la actividad de reconciliación como se muestra a continuación.

![flujo de trabajo con detalle de reconciliación](/help/assets/kt-13256/del-persn-error-wf-solution.png)

Más información sobre [reconciliación](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## Error de conjunto de datos de campo común

**Código de error:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**Causa:**
Este problema se produce al usar la variable **actividad de exclusión** en flujos de trabajo ACS. El error se produce, al realizar y excluir en función del ID, cuando el conjunto principal y el conjunto excluido no tienen los mismos nombres de campo.


![Error de conjunto de datos de campo común](/help/assets/kt-13256/dataset-error.png)

**Solución:**

Existen dos maneras de resolver este error:

1. Utilice el mismo nombre de campo tanto en el campo principal como en el excluido y utilice ese campo como ID

   O

1. Utilice el método de exclusión JOINS para seleccionar el campo en función del cual desea excluir los registros.

![Error de conjunto de datos de campo común: solución ](/help/assets/kt-13256/dataset-error-solution.png)

## Error perdido de nombre de campo

**Código de error:**
`XTK-170036 Unable to parse expression 'i__name'`

**Causa:**

Los puntos de error pueden aparecer en una **actividad de enriquecimiento**. A continuación se muestra uno de los más comunes.

![Error perdido de nombre de campo](/help/assets/kt-13256/field-name-dropped-error.png)

Esto sucede cuando edita manualmente un nombre de expresión en la actividad. La imagen muestra que la expresión se modificó de `name `a `i__name`.

**Solución:**

Puede resolver este error de tres maneras:

1. Vuelva a cambiar el nombre a la expresión que estaba presente originalmente.

2. Si desea utilizar un nombre nuevo, cambie los valores en las actividades de la variable **actividad de enriquecimiento**.

3. Si no recuerda lo que ha cambiado, lo mejor sería volver a crear la actividad.

## Error de pérdida de tabla temporal 

**Código de error:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Causa:**
Este es un error común en flujos de trabajo complicados que implican enriquecimiento u otra actividad. Probablemente significa que algunos de los flujos de trabajo de actividad no se guardan correctamente durante varios cambios en el flujo de trabajo.

![Error de pérdida de tabla temporal ](/help/assets/kt-13256/temp-table-dropped-error.png)

**Solución:**
Hay muchas maneras de que este error pueda ocurrir, por lo que no hay una solución simple. Si es un flujo de trabajo simple, entonces sería mejor reconfigurar la actividad. En un flujo de trabajo complicado, es mejor copiar las actividades de flujo de trabajo en un nuevo flujo de trabajo, guardarlas y volver a ejecutarlas.