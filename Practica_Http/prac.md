#  Análisis de Peticiones y Respuestas HTTP con HTTP Header Live
---

## Parte 1 : Instalación y configuración

![alt text](1.png)
---

## Parte 2 : Captura de petición HTTP a 3 URL distintas

**https://librebits.info**
![alt text](2.png)

* **Host:** `librebits.info`. Identifica el dominio del servidor de destino.
* **User-Agent:** `Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:146.0) Gecko/20100101 Firefox/146.0`. Informa sobre el navegador y SO del cliente.
* **Accept:** `text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8`. Define los formatos de archivo que el navegador prefiere recibir.


**https://librebits.info/404** 
![alt text](3.png)

**Host:** `librebits.info`. El destino se mantiene igual.
* **User-Agent:** Se mantiene la identificación del navegador Firefox 146.
* **Accept:** El navegador sigue solicitando preferentemente formatos de texto o HTML para mostrar el error.

**https://librebits.info/social.org**

![alt text](4.png)

## Parte 3 : Captura de respuesta HTTP y fotografía de las característa DNS del sitio Web:

![alt text](5.png)

* **Date:** Indica el momento exacto en que se generó la respuesta en el servidor.
* **Server:** `nginx/1.22.1`. Revela el software de servidor web utilizado.
* **Content-Type:** `text/css` (en el caso del recurso CSS) o `text/html`. Define cómo debe interpretar el navegador el cuerpo del mensaje.
* **Content-Length:** `3296`. Indica el tamaño del contenido en bytes.

## Parte 4 : Comparación con otros recursos

![alt text](6.png)
| Recurso | Content-Type | Significado |
| :--- | :--- | :--- |
| **Imagen (.png)** | `image/png` | El navegador lo trata como un archivo gráfico binario. |
| **Estilos (.css)** | `text/css` | El navegador lo interpreta como instrucciones de diseño para el HTML. |

**Diferencia clave:** La cabecera `Content-Type` es vital para que el navegador no confunda código ejecutable con una imagen o un archivo de texto plano.

