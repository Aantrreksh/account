---

copyright:

  years: 2016, 2018

lastupdated: "2018-03-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Cómo cambiar a IBMid y enlazar cuentas
{: #unifyingaccounts}

Ahora la autenticación en SoftLayer utiliza el IBMid para proporcionar un inicio de sesión único para todo {{site.data.keyword.Bluemix}}. Un IBMid es un ID único que utiliza para iniciar sesión en la cuenta de {{site.data.keyword.Bluemix_notm}} para acceder a las características de infraestructura, servicios y aplicaciones, y adquirirlas. Todas las nuevas cuentas automáticamente recibirán un IBMid y las cuentas existentes de SoftLayer, excepto las cuentas federadas SAML, estarán habilitadas para conmutar a la autenticación de IBMid.
{:shortdesc}

## Cambio a IBMid
{: #switchtoIBMid}

Cuando empiece el proceso de cambiar a un IBMid, siempre podrá cancelar el proceso de cambio antes de finalizarlo. Sin embargo, cada vez que inicie una sesión, se mostrará el indicador para cambiar a un IBMid. Cada cuenta de SoftLayer que piense enlazar a la cuenta de {{site.data.keyword.Bluemix_notm}} debe ser propiedad de un IBMid exclusivo con una dirección de correo electrónico exclusiva.

Para cambiar desde su cuenta de SoftLayer existente a un IBMid, cree un IBMid y utilice el código de registro para confirmarlo.

### Solicitud de un IBMid y un código de registro
{: #reqIBMidandregcode}

1. Inicie una sesión en su cuenta de SoftLayer y pulse **Aceptar** cuando se visualice una solicitud para cambiar a un IBMid.

   Si es un usuario maestro y no ve un indicador para cambiar a un IBMid en el portal de cliente de infraestructura de {{site.data.keyword.BluSoftlayer_full}} póngase en contacto con el equipo de soporte de IBM para obtener ayuda. Consulte [Soporte de IBM](/docs/get-support/howtogetsupport.html#getting-customer-support) para obtener información de contacto.

   Si con anterioridad inició una sesión y pulso **Más tarde** en la solicitud, y desea cambiar a la autenticación de IBMid en la sesión actual, vaya a la página Editar perfil de usuario y pulse **Cambiar a IBMid**.

2. Siga las indicaciones del asistente para crear el IBMid.

   Especifique una dirección de correo electrónico que no utilice actualmente ningún otro IBMid. Esta dirección de correo electrónico sirve como el nombre de usuario para el nuevo IBMid, y es adónde se envía su código de registro después de que se cree su IBMid. Más tarde podrá actualizar la dirección de correo electrónico asociada al IBMid, pero no podrá cambiar el nombre de usuario.

### Confirmación del IBMid con el código de registro
{: #confIBMiduseregcode}

1. Cuando reciba el código de registro, pulse en el enlace en el correo electrónico o copie el URL en un navegador y especifique su código de registro.

   El código de registro es válido durante 7 días y solo se puede utilizar una vez.

2. Después de enviar su código de registro, utilice el IBMid para iniciar una sesión en el portal de cliente.

   En el indicador de inicio de sesión de la cuenta, vaya a la sección **Inicio de sesión de cuenta de IBMid** y pulse **Iniciar sesión con IBMid**. No utilice los campos el **Nombre de usuario** y **Contraseña** que ha utilizado previamente con su ID de SoftLayer.

Si es un nuevo cliente, se le solicitará su IBMid existente o que cree un nuevo IBMid al crear su pedido.
  * Para utilizar un IBMid existente, escriba el nombre de usuario o la dirección de correo electrónico del IBMid si es exclusivo (es decir, no compartido con varios IBMid).
  * Para crear un nuevo IBMid, escriba una dirección de correo electrónico que no utilice actualmente ningún otro IBMid. Esta dirección de correo electrónico es el nombre de usuario para el IBMid, y es adónde se enviará su código de registro después de que se cree su IBMid. Más tarde podrá actualizar la dirección de correo electrónico asociada al IBMid, pero no podrá cambiar el nombre de usuario.

Para resolver cualquier problema de inicio de sesión con su IBMid, consulte [Resolución de problemas para acceder a {{site.data.keyword.Bluemix_notm}}](/docs/troubleshoot/ts_accessing.html#accessing).

## Cómo enlazar cuentas de usuario de IBMid
{: #link_user_accounts}

Después de que sus cuentas de usuario se hayan cambiado a la autenticación de IBMid, los concesionarios y distribuidores pueden enlazar cuentas de SoftLayer y cuentas de {{site.data.keyword.Bluemix_notm}} para un uso combinado de los recursos de la infraestructura como un servicio (IaaS) y de la plataforma como un servicio (PaaS). Puede acceder a recursos de IaaS desde el portal de cliente de infraestructura de {{site.data.keyword.BluSoftlayer_full}} y a los recursos de PaaS desde la consola de {{site.data.keyword.Bluemix_notm}}, todo ello a partir de un único inicio de sesión. Enlazar sus cuentas también supondrá una única factura para todos los recursos IaaS y PaaS que utilice.

Para enlazar cuentas, debe ser un usuario maestro de SoftLayer. El IBMid que es el usuario maestro de la cuenta debe ser el propietario de la cuenta de la plataforma {{site.data.keyword.Bluemix_notm}} a la que se va a enlazar. Asegúrese de revisar las siguientes notas importantes para enlazar cuentas:

  * El usuario maestro de la cuenta de SoftLayer a la que se está enlazando debe tener un IBMid.
  * Cada cuenta de usuario que enlace con una cuenta de {{site.data.keyword.Bluemix_notm}} debe ser propiedad de un IBMid exclusivo con una dirección de correo electrónico exclusiva. A pesar de que un único IBMid puede poseer varias cuentas de SoftLayer, debe cambiar el usuario maestro para que sea un IBMid exclusivo para cada cuenta. Póngase en contacto con el equipo de soporte para cambiar el usuario maestro de una cuenta de SoftLayer. Consulte [Obtención de soporte para la infraestructura de {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal/cpsupport.html) para obtener más información.
  * Cuando añada nuevos usuarios a una cuenta enlazada, debe añadirlos tanto a la cuenta de SoftLayer como a la cuenta de {{site.data.keyword.Bluemix_notm}} de forma que puedan acceder a todas las funcionalidades de la consola unificada.
  * Si tiene una cuenta derivada, utilice BAP (Brand Agent Portal). Necesitará soporte al enlazar su cuenta, póngase en contacto con el equipo de Revenue Services enviando un correo electrónico a softlayer_revenue_services_team@wwpdl.vnet.ibm.com.
  * Todas las cuentas vinculadas en {{site.data.keyword.Bluemix_notm}} deben ser cuentas de Pago según uso. Puede crear una nueva cuenta de Pago según uso, enlazar a una cuenta de Pago según uso existente o enlazar con una cuenta de prueba existente, que se actualizará a una cuenta de Pago según uso. No puede enlazar a cuentas de suscripción de {{site.data.keyword.Bluemix_notm}}.

Siga estos pasos para enlazar cada cuenta de SoftLayer con una cuenta de plataforma de {{site.data.keyword.Bluemix_notm}} existente o para crear una nueva:

   1. Inicie sesión en el portal de cliente de infraestructura de {{site.data.keyword.BluSoftlayer_full}} con su IBMid de cuenta de usuario maestro.
   2. Desde el portal de cliente de infraestructura de {{site.data.keyword.Bluemix_notm}}, pulse **Enlazar a una cuenta de Bluemix**.
   3. Lea y acepte las condiciones para enlazar cuentas de SoftLayer y {{site.data.keyword.Bluemix_notm}}.
   4. Siga las indicaciones del asistente, incluida la adición de los usuarios de la cuenta de SoftLayer a la cuenta de {{site.data.keyword.Bluemix_notm}}.
   5. Cuando se le solicite, realice una de las siguientes acciones:
     * Si ya tiene una cuenta de {{site.data.keyword.Bluemix_notm}}, proporcione la dirección de correo electrónico asociada a la cuenta para enlazar las cuentas.
     * Si no tiene una cuenta de {{site.data.keyword.Bluemix_notm}}, especifique la dirección de correo electrónico que desea utilizar y siga las instrucciones para ser invitado a {{site.data.keyword.Bluemix_notm}} y cree una cuenta.
   6. Después de que haya enlazado la cuenta, informe al usuario final de cada cuenta para que migre a un IBMid siguiendo el procedimiento que se ha descrito en la sección anterior de [Cambio a IBMid](/docs/account/softlayerlink.html#switchtoIBMid).

Migre únicamente cuentas de usuario final a IBMid. No migre cuentas derivadas, que son cuentas padre de cuentas de usuario final y no contienen recursos. Los usuarios de cuentas derivadas que migren a un IBMid pierden la posibilidad de iniciar una sesión en el Brand Agent Portal (BAP).
{: tip}

Las cuentas enlazadas inician una sesión en la consola de [{{site.data.keyword.Bluemix}} ![Icono de enlace externo](../icons/launch-glyph.svg)](https://console.bluemix.net){: new_window}.

Además, tenga en cuenta los siguientes cambios después de que se hayan enlazado sus cuentas:
  * Debe utilizar las credenciales de ID de IBM para acceder a sus cuentas tanto de SoftLayer como de {{site.data.keyword.Bluemix_notm}}.
  * Cualquier descuento existente de SoftLayer se aplicará en cargos de {{site.data.keyword.Bluemix_notm}}.
  * Recibirá una factura en dólares de Estados Unidos (USD). Si tiene una cuenta de {{site.data.keyword.Bluemix_notm}}, la facturación a través de {{site.data.keyword.Bluemix_notm}} para los recursos de infraestructura será efectiva para el nuevo ciclo de facturación que empieza una vez que se hayan enlazado las cuentas.
  * Puede supervisar el uso de los recursos de infraestructura en la consola de {{site.data.keyword.Bluemix_notm}}.

Después de enlazar sus cuentas, no podrá desenlazarlas.
{: tip}

## Uso de la autenticación de multifactores en cuentas enlazadas
{: #2fa}

Si tiene una cuenta enlazada, puede utilizar la página **Valores** de Identidad y Acceso para habilitar la autenticación de multifactores para su cuenta. Se trata de la autenticación de dos factores (2FA) donde se añade una capa de seguridad para acceder a su cuenta más allá del IBMid y de la contraseña necesarios estándares. La autenticación de multifactores para su cuenta se aplica a todos los recursos de la cuenta de {{site.data.keyword.Bluemix_notm}} enlazada. Cuando se habilita para su cuenta, también se aplicará a todos los usuarios que se hayan añadido a su cuenta.

La autenticación de multifactores no es por IBMid. Sigue siendo por cuenta. Cuando un IBMid está asociado con varias cuentas, y cambia entre ellas, debe confirmar su identidad cada vez que cambie a una cuenta distinta que requiera la autenticación de dos factores. Esto es cierto incluso si la cuenta anterior y la cuenta nueva están configuradas con el mismo mecanismo de autenticación de dos factores.
