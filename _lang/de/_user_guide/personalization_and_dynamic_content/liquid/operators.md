---
nav_title: Õpéérãätôôrs
article_title: Lïíqùúïíd Ôpéèrååtóörs
page_order: 2
description: "Thîîs réëféëréëncéë pàágéë nóótéës théë óópéëràátóórs thàát Lîîqüüîîd süüppóórts, àás wéëll àás réëléëvàánt éëxàámpléës."

---

# Öpéëræãtòôrs

Líîqùùíîd sùùppóörts máæny [ôôpêèrãàtôôrs][25] thæåt cæån béê úûséêd ìîn yóóúûr cóóndìîtìîóónæål stæåtéêméênts.

|   Syntåàx| Òpèérãátõör Dèéscrìïptìïõön|
|---------|-----------|
| ==  | éëqúúåãls        |
| !=  | dõòêës nõòt êëqúúãäl|
|  >  | grëëáätëër tháän  |
| <   | lêèss thàán     |
| >=| grêëæátêër thæán òôr êëqýúæál tòô|
| <= | lëëss thâân öòr ëëqùýââl töò |
| óõr | côòndìîtìîôòn Â ôòr côòndìîtìîôòn B|
| àànd | cõóndïîtïîõón Ã ãånd cõóndïîtïîõón B|
| cóõntàåìïns | chêécks tòò sêéêé ïîf ãá strïîng òòr strïîng ãárrãáy còòntãáïîns ãá strïîng|
{: .reset-td-br-1 .reset-td-br-2}

## Öpêèrâãtóõr êèxâãmplêès

Hèërèë äàrèë sõòmèë èëxäàmplèës õòf hõòw thèësèë õòpèëräàtõòrs cõòûûld bèë hèëlpfûûl fõòr yõòûûr mäàrkèëtîíng cäàmpäàîígns:

### Chôóôósëè mëèssäægëè vïïäæ ïïntëègëèr cûýstôóm äættrïïbûýtëè

{% raw %}
```liquid
{% if {{custom_attribute.${total_spend}}} >0 %}
Thanks for purchasing! Here's another 10% off!
{% else %}
Buy now! Would 5% off convince you?
{% endif %}
```
{% endraw %}

![][13]{: width="100%"}

În thììs éêxààmpléê, ììf àà cúüstöóméêr’s "Töótààl Spéênd" cúüstöóm ààttrììbúütéê ììs gréêààtéêr thààn `0`, théèy wíìll géèt théè méèssâågéè:

```
Thanks for purchasing! Here's another 10% off!
```
Íf áá cýústôómëèr’s "Tôótáál Spëènd" cýústôóm ááttrîìbýútëè dôóëès nôót ëèxîìst ôór îìs ëèqýúáál tôó `0`, théèy wîîll géèt théè fòòllòòwîîng méèssäågéè:

```
Buy now! Would 5% off convince you?
```


### Chöööösèê mèêssäâgèê vîîäâ strîîng cûûstööm äâttrîîbûûtèê

{% raw %}

```liquid
{% if {{custom_attribute.${Game}}} == Game1 %}
You played our Game! We're so happy!
{% elsif{{custom_attribute.${Game}}} == Game2 %}
You played our other Game! Woop!
{% else %}
Hey! Get in here and play this Game!
{% endif %}
```
{% endraw %}

![][14]

Ín thîís ëêxæämplëê, îíf yöõûù hæävëê plæäyëêd æä cëêrtæäîín gæämëê, yöõûù'll rëêcëêîívëê thëê föõllöõwîíng mëêssæägëê:

```
You played our Game! We're so happy!
```

Íf yöòúý plâæyèëd âænöòthèër spèëcîîfîîèëd gâæmèë:

```
You played our other Game! Woop!
```

Íf yôôúù hàävéën’t plàäyéëd àäny gàäméës, ôôr thàät cúùstôôm àättríìbúùtéë dôôéësn’t éëxíìst ôôn yôôúùr prôôfíìléë, yôôúù’d géët théë fôôllôôwíìng méëssàägéë:

```
Hey! Get in here and play this Game!
```

### Âbôört mèéssæægèé bææsèéd ôön lôöcæætïíôön

Yóöüý cáãn áãbóört áã méêssáãgéê báãséêd óön jüýst áãbóöüýt áãnythììng. Thëé fôöllôöwìîng ëéxæàmplëé shôöws hôöw yôöýý cæàn æàbôört æà mëéssæàgëé ìîf æà ýýsëér ìîs nôöt bæàsëéd ìîn æà spëécìîfìîëéd æàrëéæà, æàs thëéy mìîght nôöt qýýæàlìîfy fôör thëé prôömôötìîôön, shôöw, ôör dëélìîvëéry.

{% raw %}
```liquid
{% if {{${time_zone.$}}} =='America/Los_Angeles' %}
Stream now!
{% else %}
{% abort_message () %}
{% endif %}
```
{% endraw %}

![][26]

Yóõûý cäân äâlsóõ [äábòôrt mëèssäágëès][1] bâásêêd óôn Cóônnêêctêêd Cóôntêênt.


[1]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/connected_content/aborting_connected_content/
[13]: {% image_buster /assets/img/liquid-if-totalspend.png %}
[14]: {% image_buster /assets/img/liquid-if-elsif-games.png %}
[25]: https://docs.shopify.com/themes/liquid/basics/operators
[26]: {% image_buster /assets/img/abort-if.png %}
