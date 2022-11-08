# Diseño

![Python Logo](https://miro.medium.com/max/1024/0*sOKo-qt8yWPV9FDr.png)

Antes de empezar a desarrollar bots, necesitas saber que es lo que quieres que hagan. Para ello tienes que decidir qué servicios proporcionarán, cómo gestionarán las solicitudes y como responderán a las mismas.

## ¿Qué va a hacer mi bot?

Tenemos que definir cuál va a ser la funcionalidad que va a realizar para ello, debemos selecionar un tipo de bot de los vistos anteriormente:

- Web Crawler o Rastreador de Información
- Chatbots
- Bots en redes sociales y de envío de correo masivo
- Bots de monitorización web
- Bots de voz
- Spambots
- Bots de ataques
- Bots de búsqueda de vulnerabilidades

En nuestro caso, será un Bot en redes sociales y de envío de correo masivo

## ¿Como lo va hacer?

A la hora de definir cómo va a funcionar nuestro bot, debemos de analizar primero, el lenguaje y las herramientas que vamos a utilizar. En nuestro caso, utilizaremos Python por ende debemos buscar que librerías y APIs pueden ayudarnos a desarrollar cada uno nuestros bots.

Para el bot de Correo:

- [smtplib](https://docs.python.org/3/library/smtplib.html?highlight=smtplib#module-smtplib) 
- [MIMEMultipart](https://docs.python.org/3/library/email.mime.html) 
- [ssl](https://docs.python.org/3/library/ssl.html?highlight=ssl#module-ssl) 

Para el bot de WhatsApp:

- [Whatsapp-python-client](https://pypi.org/project/whatsapp-python-client/) 
- [Python-whatsapp](https://pypi.org/project/python-whatsapp/) 
- [Whatsapp-cli](https://pypi.org/project/whatsapp-cli/) 

Para el bot de Telegram:

- [Bot Payments API](https://core.telegram.org/bots/payments) 
- [Botfather](https://core.telegram.org/bots) 
- [Telegram Database Library](https://core.telegram.org/tdlib) 

Para el bot de Instagram:

- [Selenium](https://pypi.org/project/selenium/) 
- [Instapy](https://pypi.org/project/instapy2/) 
- [Instagram-python 1.4](https://pypi.org/project/instagram-python/) 

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

## Plantillas

En el aula tenemos una plantilla este es el link por si quereis echarle un vistazo:

[https://github.com/aulasoftwarelibre/telegram-bot-template](https://github.com/aulasoftwarelibre/telegram-bot-template)