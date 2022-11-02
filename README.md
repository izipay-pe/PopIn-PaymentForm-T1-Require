# PopIn-PaymentForm-T1-Require

Ejemplo de formulario pop-in para utilizar la librería Require dentro de tu proyecto, que te permitirá cargar los scripts de forma asíncrona.

<p align="center">
  <img src="/src/formulario_popin.png?raw=true" alt="Formulario"/>
</p> 

<a name="Requisitos_Previos"></a>

## Requisitos Previos

* Extraer credenciales del Back Office Vendedor. [Guía Aquí](https://github.com/izipay-pe/obtener-credenciales-de-conexion)
* Servidor web o servidor local.

## 1.- Crear el proyecto

Descargar el proyecto .zip haciendo click [Aquí](https://github.com/izipay-pe/PopIn-PaymentForm-T1-Require/archive/refs/heads/main.zip) o clonarlo desde Git.  
```sh
git clone https://github.com/izipay-pe/PopIn-PaymentForm-T1-Require.git
``` 

## 2.- Configurar datos de conexión

Editar el archivo `keys.example.php` en la ruta raiz del proyecto `public_html/`.

![Clave](https://github.com/izipay-pe/Embedded-PaymentFormT1-Php/blob/main/images/key.png)

**Nota**: Reemplace **[CHANGE_ME]** con sus credenciales de `API REST` extraídas desde el Back Office Vendedor en el archivo `carpta_raiz/keys.example.php` de la ruta raíz del proyecto, ver [Requisitos Previos](#Requisitos_Previos).   

```sh
// Identificador de su tienda
IzipayController::setDefaultUsername("~ CHANGE_ME_USER_ID ~");

// Clave de Test o Producción
IzipayController::setDefaultPassword("~ CHANGE_ME_PASSWORD ~");

// Clave Pública de Test o Producción
IzipayController::setDefaultPublicKey("~ CHANGE_ME_PUBLIC_KEY ~");

// Clave HMAC-SHA-256 de Test o Producción
IzipayController::setDefaultHmacSha256("~ CHANGE_ME_HMAC_SHA_256 ~");

// URL del servidor de Izipay
IzipayController::setDefaultEndpointApiRest("https://api.micuentaweb.pe");
``` 

## 3.- Transacción de prueba

El formulario de pago está listo, puede intentar realizar una transacción utilizando una tarjeta de prueba con la barra de herramientas de depuración (en la parte inferior de la página).

![tarjetas de prueba](https://github.com/izipay-pe/Embedded-PaymentForm-T1.Net/blob/main/images/tarjetasprueba2.png)

Para obtener más información, eche un vistazo a:

* [Formulario incrustado: prueba rápida](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/javascript/quick_start_js.html)
* [Primeros pasos: pago simple](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/javascript/guide/start.html)
* [Servicios web - referencia de la API REST](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/api/reference.html)

## 4.- Implementar IPN

* Ver manual de implementacion de la IPN [Aquí](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/kb/payment_done.html).

* Ver el ejemplo de la respuesta IPN con PHP [Aquí](https://github.com/izipay-pe/Redirect-PaymentForm-IpnT1-PHP).

* Ver el ejemplo de la respuesta IPN con NODE.JS [Aquí](https://github.com/izipay-pe/Response-PaymentFormT1-Ipn).

