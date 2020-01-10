---
description: Cree y gestione ofertas para utilizarlas en Adobe Campaign.
seo-description: Cree y gestione ofertas para utilizarlas en Adobe Campaign.
seo-title: Administración de ofertas
title: Administración de ofertas
uuid: 83e1d4cd-c5fa-4df0-9603-2914eb4648f8
index: y
translation-type: tm+mt
source-git-commit: 55ac24fe0fb177a5a81765af1f7d602acc0f5d0f

---


# Ofertas

Cree y gestione ofertas para utilizarlas en Adobe Campaign.

Existen dos tipos de ofertas en la administración de [!UICONTROL ofertas]:

| Tipo | Descripción |
|---|---|
| Oferta general | Permite rellenar el modelo de datos de oferta completo (reglas de elegibilidad, fechas de inicio y finalización y contenido). |
| Oferta alternativa | La oferta de último recurso si un cliente no cumple los requisitos para cualquiera de las otras ofertas seleccionadas. No puede asociar ninguna regla de elegibilidad ni fechas de inicio y finalización con ofertas de reserva. |

>[!NOTE]
>
>En una actividad de oferta, siempre se le pedirá que seleccione una oferta de reserva. Por lo tanto, debe tener al menos una oferta de reserva en el inventario de ofertas para poder crear una actividad de oferta.

## Create an offer {#task_6C4AE487377D424FA133ACCA6AF741D4}

Cree una oferta para agregarla al inventario de ofertas.

1. En la ficha [!UICONTROL Inventario] de Administración [!UICONTROL de]ofertas, haga clic en **[!UICONTROL Crear nueva oferta]**y, a continuación, seleccione**[!UICONTROL  Crear oferta]**.

   ![](assets/create-offerx.png)

1. Complete los campos siguientes:

   <table id="table_60A4001CE9F34422ACB59FB62C9CBDCD">
<thead> 
  <tr> 
   <th colname="col1" class="entry"> Campo </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nombre de la oferta </p> </td> 
   <td colname="col2"> <p>El nombre asociado a la oferta. No puede tener dos ofertas en el inventario con nombres duplicados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fecha de inicio </p> </td> 
   <td colname="col2"> <p>Fecha en la que se puede mostrar la oferta. Si se selecciona una fecha de inicio del 15/15/17, la oferta se puede mostrar a partir de las 12:00 a.m. del 15/17/17. </p> <p>La administración de ofertas funciona según el estándar de tiempo UTC. Esto significa que: </p> <p> 
     <ul id="ul_A9D49B4405F34E6DA8FB52A13437F799"> 
      <li id="li_9490D092B235479A981FC2D5DD0B17B4">Las ofertas pasan a ser válidas a las 00:00 UTC el día en que la oferta está configurada para iniciarse. </li> 
      <li id="li_C28BB1FEB9E1495593826403CF5F67A9">Las ofertas caducan a las 00:00 UTC el día siguiente a la fecha de finalización. Por ejemplo, si una oferta está configurada para tener una fecha de finalización del 14/5, la oferta caducará a las 00:00 UTC del 15/5. La oferta se archiva. </li> 
      <li id="li_D3F7DCD1BF75410A8F4F5BC468B667AB">Cuando se preparan correos electrónicos en Adobe Campaign, solo se mostrarán las ofertas que sean válidas en ese momento. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fecha final </p> </td> 
   <td colname="col2"> <p>Fecha en la que finaliza la oferta. Si se selecciona una fecha de finalización del 20/1/17, la oferta ya no se muestra después de las 11:59 del 20/17/11. Cuando una oferta supera su fecha de finalización, se archiva automáticamente. </p><p>La administración de ofertas funciona según el estándar de tiempo UTC. Consulte la fila de arriba para obtener más información. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reglas de elegibilidad </p> </td> 
   <td colname="col2"> <p>Puede crear reglas de elegibilidad de ofertas basadas en los datos disponibles en la base de datos de <span class="keyword"> Campaign</span> . Las reglas de elegibilidad determinan a quién y cuándo se puede mostrar una oferta. </p> <p>Por ejemplo, puede especificar que solo desea que se muestre una 'Oferta de ropa de invierno para mujeres' cuando (Sexo = 'Mujer') y (Región = 'Noreste'). Los atributos utilizados para crear estas reglas provienen del perfil de Campaign Standard. </p> <p>Nota:  Cuando accede por primera vez a la administración de ofertas, no hay atributos disponibles en el creador de reglas. Debe compartir atributos desde la interfaz de usuario de la campaña. Una vez compartidos, esos atributos están disponibles. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tapón máximo </p> </td> 
   <td colname="col2"> <p>Plazos máximos durante los cuales se puede proponer una oferta. </p> <p>Nota:  El número de veces que se propone una oferta se calcula en el momento de la preparación del correo electrónico. Por ejemplo, si prepara un mensaje de correo electrónico con una cantidad de ofertas, esos números se cuentan hasta el límite máximo independientemente de si se envía o no el correo electrónico. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Límite máximo por usuario </p> </td> 
   <td colname="col2"> <p>El máximo de tiempo que se puede proponer una oferta a un usuario determinado. </p> <p>Nota:  El número de veces que se propone una oferta a un usuario determinado se calcula en el momento de la preparación del correo electrónico. Por ejemplo, si prepara un correo electrónico con un número de ofertas, esos números se contabilizan como límite máximo por usuario, independientemente de si se envía o no el correo electrónico.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Etiquetas </p> </td> 
   <td colname="col2"> <p>Agregue etiquetas a una oferta para agruparlas. Puede escribir y pulsar Intro para crear una nueva etiqueta o empezar a escribir y seleccionar una oferta existente en la lista desplegable. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Rellene los detalles de las representaciones.

   | Campo | Descripción |
   |---|---|
   | Canal | Canal en el que se puede entregar esta representación de contenido. Los mensajes de correo electrónico de Campaign Standard son el único canal disponible actualmente. |
   | Ubicación | Seleccione la ubicación en la que se puede entregar esta representación de contenido. Las ubicaciones se rellenan previamente desde la ficha Colocaciones. Debe asociar cada representación de contenido con una colocación desde el menú desplegable. No se pueden crear varias representaciones de contenido con la misma ubicación en la misma oferta. |
   | Tipo de contenido | Seleccione un tipo de contenido de una imagen, una URL de imagen, un texto o un HTML. |
   | Vínculo de redirección | Este campo se muestra si selecciona un tipo de contenido de imagen o de dirección URL de imagen. Este es el vínculo al que se redirigirá el usuario si hace clic en esa oferta en un mensaje de correo electrónico. |

1. Haga clic en **[!UICONTROL Guardar y previsualizar]**para revisar los detalles de la oferta antes del envío.
1. Haga clic en **[!UICONTROL Aprobar]**para aprobar la oferta. Una vez que la oferta está en el estado aprobado, se puede utilizar en una actividad de oferta.

   Si no dispone de los permisos necesarios para aprobar una oferta, en su lugar hará clic en **[!UICONTROL Enviar]**. La oferta se mostrará en la biblioteca de ofertas con un estado pendiente. Una vez que un usuario con derechos de aprobación lo apruebe, estará disponible para su uso en una actividad de oferta.
