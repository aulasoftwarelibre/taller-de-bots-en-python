# Despliegue

Una vez que hemos acabado de diseñar y programar nuestro bot, nos surge la gran pregunta y es donde alojarlo, pues bién, tenemos varias opciones: 

## ¿Dónde se va a alojar mi bot?

Existen diversas opciones las principales son:

### Localhost
<div align="center">
    <img width="100%" src="http://www.userlogos.org/files/logos/Brentc/localhost_logo.png" alt="FOTO">
</div>

Es la solución más sencilla y barata ya que no nos costará nada, simplemente debemos dejar nuesta máquina encendida y nuestro bot seguirá ejecutándose como un programa más.

```Bash
python3 nombre_de_nuestro_bot.py
```

### RaspberryPi
<div align="center">
    <img width="100%" src="https://piscinadeentropia.es/wp-content/uploads/2021/06/raspberrypi_logo_icon_168030.png" alt="FOTO">
</div>

Si no queremos dejar un programa siempre ejecutándose en segundo plano en nuestro equipo, disponemos de pocos recursos o no queremos dejarlo todo el día encendido, podemos obtar por dejarlo ejecutándose en una RasberryPi, al final, estos mini ordenadores consumen muy poco y pueden ejecutar casi cualquier aplicación que se ejecute en un equipo de escritorio.

Para hacerlo, simplemente, llevamos a ella el código de nuestro bot y lo ejecutamos en una terminal como hacíamos en nuestro equipo:

```Bash
python3 nombre_de_nuestro_bot.py
```

### Cloud

<div align="center">
    <img width="100%" src="https://static.wixstatic.com/media/7a8852_60c510392e594da5b959f00d50e473e1~mv2.png/v1/fill/w_640,h_170,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/7a8852_60c510392e594da5b959f00d50e473e1~mv2.png" alt="FOTO">
</div>

Si nos decantamos por una opción más profesional, y decidimos desplegar nuestro bot en la nube contamos con diferentes alternativas gratuitas o con un precio reducido que pueden alojar nuestro programa:

- [Heroku](https://heroku.com/)
- [Pythonanywhere](https://www.pythonanywhere.com/)
- [AWS](https://aws.amazon.com/es/free/?trk=2d5aad89-991b-4184-98b5-1f562e3102c8&sc_channel=ps&s_kwcid=AL!4422!3!561218200770!e!!g!!aws&ef_id=Cj0KCQiAmaibBhCAARIsAKUlaKTfApkMLdq5gR0AyZJosqnol3z8cAUAkmcHX1fUzxY-XJUG2w-LojYaAtCtEALw_wcB:G:s&s_kwcid=AL!4422!3!561218200770!e!!g!!aws&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)
- [GoogleCloud](https://cloud.google.com/gcp/?hl=es&utm_source=google&utm_medium=cpc&utm_campaign=emea-es-all-es-bkws-all-all-trial-e-gcp-1011340&utm_content=text-ad-none-any-DEV_c-CRE_593880918212-ADGP_Hybrid+%7C+BKWS+-+EXA+%7C+Txt+~+GCP+~+General%23v3-KWID_43700060384861663-aud-606988878454:kwd-6458750523-userloc_1005411&utm_term=KW_google%20cloud-NET_g-PLAC_&gclid=Cj0KCQiAmaibBhCAARIsAKUlaKTtbS9dp5PI3D-6cH-augTIoMPNU4LyG1N6aQfbLBcV2PnQN5nsPT0aAj3NEALw_wcB&gclsrc=aw.ds)
- [Azure](https://azure.microsoft.com/es-es/free/search/?&ef_id=Cj0KCQiAmaibBhCAARIsAKUlaKTekLsbJHts976CL8eao22-PuMxFSQmKVTWuksk1B5a7cUzXElTuDkaAqheEALw_wcB:G:s&OCID=AIDcmm68ejnsa0_SEM_Cj0KCQiAmaibBhCAARIsAKUlaKTekLsbJHts976CL8eao22-PuMxFSQmKVTWuksk1B5a7cUzXElTuDkaAqheEALw_wcB:G:s&gclid=Cj0KCQiAmaibBhCAARIsAKUlaKTekLsbJHts976CL8eao22-PuMxFSQmKVTWuksk1B5a7cUzXElTuDkaAqheEALw_wcB)
