# Diseño

![Python Logo](https://miro.medium.com/max/1024/0*sOKo-qt8yWPV9FDr.png)

Antes de empezar a desarrollar bots, necesitas saber que es lo que quieres que hagan. Para ello tienes que decidir qué servicios proporcionarán, cómo gestionarán las solicitudes y como responderán a las mismas.

## ¿Qué va a hacer mi bot?
## ¿Como lo va hacer?

## ¿Como va a responder mi bot?

Los formatos de respuesta son muy variados y dependerán del uso y las integraciones que queramos que tenga nuestro bot. Los formatos de respuesta más comunes son:

### Mensajes

Es la forma más habitual y la que emplean la mayoría de chatbots para comunicarse, se integran en la plataforma de mensagería y envián mensajes como si de un usuario humano se tratase

![Python Logo](https://miro.medium.com/max/956/1*wod3trcCwgXbvHEx1Qitlw.png)

### JSON

Es un formato estandar para transferir información y por ende nuestros bots también pueden usarlo para encapsular sus respuestas y que estas puedan ser utilizadas por otras aplicaciones/bots

```JSON
{
  "id":8,
  "mensaje":"Hola soy tu bot, los datos solicitado son: ",
  "empleados":[
    {
      "id":"Dato1",
    },{
      "id":"Dato2",
    } 
  ]
}
```