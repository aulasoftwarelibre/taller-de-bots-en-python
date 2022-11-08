# MailBot

## Gmail

```Python
import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText

me = "riveragavilanmarcos@gmail.com"
you = "i92rigam@uco.es"

# Create message container - the correct MIME type is multipart/alternative.
msg = MIMEMultipart('alternative')
msg['Subject'] = "Recibo Fotos Orla Derecho y ADE"
msg['From'] = me
msg['To'] = you

font = "{font-family: 'Roboto', sans-serif;}"

# Create the body of the message (a plain-text and an HTML version).
html = f"""\
<html lang="es">
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
    <style>
    body {font}
  </style>
  </head>
  <body>
    <div style="display: flex; align-items: center; justify-content: center">
      <a href="https://imgur.com/l8qu2f7"
        ><img src="https://i.imgur.com/l8qu2f7.png" title="source: imgur.com"
      /></a>
    </div>
    <div style="display: flex; align-items: center; justify-content: center;">
      <h2>RESUMEN Del Partido</h2>
    </div>
  </body>
</html>
    """

# Record the MIME types of both parts - text/plain and text/html.
part2 = MIMEText(html, 'html')
 # Attach parts into message container.
 # According to RFC 2046, the last part of a multipart message, in this case
 # the HTML message, is best and preferred.
msg.attach(part2)
try:
   # Send the message via local SMTP server.
    mail = smtplib.SMTP('smtp.gmail.com', 587)
    mail.ehlo()
    mail.starttls()
    mail.login('moyanofotografia@gmail.com', 'biqlfxmxkbiicbmp')
    mail.sendmail(me, you, msg.as_string())
    mail.sendmail(me, "moyanofotografia@gmail.com", msg.as_string())
    mail.quit()
    print("Mail sent")
except:
    print("Error unable to send mail")
```

## UCO

```Python
import smtplib,ssl
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
def sendEmail(email):
    sender_address = ""
    receiver_address = email
    sender_pass = ""

    # Create message container - the correct MIME type is multipart/alternative.
    msg = MIMEMultipart('alternative')
    msg['Subject'] = "Prueba"
    msg['From'] =sender_address
    msg['To'] = receiver_address

    font = "{font-family: 'Roboto', sans-serif;}"

    # Create the body of the message (a plain-text and an HTML version).
    html = f"""\
<html lang="es">
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
    <style>
    body {font}
  </style>
  </head>
  <body>
    <div>Hola, prueba 1</div>
  </body>
</html>
    """

    # Record the MIME types of both parts - text/plain and text/html.
    part2 = MIMEText(html, 'html')

    # Attach parts into message container.
    # According to RFC 2046, the last part of a multipart message, in this case
    # the HTML message, is best and preferred.
    msg.attach(part2)

    try:
        session = smtplib.SMTP('mandarcorreo.uco.es', 587) #use gmail with port
        context = ssl.SSLContext(ssl.PROTOCOL_TLSv1_2) 
        session.starttls(context=context) #enable security
        session.login("i92xxxx", sender_pass) #login with mail_id and password
        text = msg.as_string()
        session.sendmail(sender_address, receiver_address, text)
        session.quit()
        # Send the message via local SMTP server.
        print("Mail sent to: " + receiver_address)

    except:
        print("Error unable to send mail")

recipientsFile = open('recipients.txt', 'r')
lines = recipientsFile.readlines()
  
for line in lines:
    sendEmail(line.strip())
```

