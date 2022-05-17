---
nav_title: Ôpëéráãtöòrs
article_title: Líìqýüíìd Öpéêråætöörs
page_order: 2
description: "Thîìs rèéfèérèéncèé páâgèé nóótèés thèé óópèéráâtóórs tháât Lîìqüüîìd süüppóórts, áâs wèéll áâs rèélèéváânt èéxáâmplèés."

---

# Ópêërãâtöõrs

Lìíqùýìíd sùýppôórts mæâny [òôpéêråátòôrs][25] thäæt cäæn bêé ýüsêéd ìïn yòóýür còóndìïtìïòónäæl stäætêémêénts.

|   Syntäåx| Ôpééræætõôr Dééscríîptíîõôn|
|---------|-----------|
| ==  | ëêqýûàæls        |
| !=  | dõõëês nõõt ëêqûûåäl|
|  >  | grëéæãtëér thæãn  |
| <   | lêéss tháæn     |
| >=| grèëààtèër thààn òôr èëqûúààl tòô|
| <= | lêèss thãån õör êèqúüãål tõö |
| óór | cõóndíìtíìõón Ã õór cõóndíìtíìõón B|
| ãænd | cöòndíïtíïöòn Â æând cöòndíïtíïöòn B|
| cóôntäåíìns | chêècks tòó sêèêè îíf äâ strîíng òór strîíng äârräây còóntäâîíns äâ strîíng|
{: .reset-td-br-1 .reset-td-br-2}

## Ópèérâátòõr èéxâámplèés

Hééréé ààréé sòõméé ééxààmpléés òõf hòõw thééséé òõpéérààtòõrs còõúüld béé héélpfúül fòõr yòõúür mààrkéétìïng cààmpààìïgns:

### Chõõõõséê méêssåãgéê vïìåã ïìntéêgéêr cýüstõõm åãttrïìbýütéê

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

Ìn thììs ééxæâmpléé, ììf æâ cúûstöóméér’s "Töótæâl Spéénd" cúûstöóm æâttrììbúûtéé ììs grééæâtéér thæân `0`, thèëy wíìll gèët thèë mèëssåãgèë:

```
Thanks for purchasing! Here's another 10% off!
```
Íf åã cúýstöômêêr’s "Töôtåãl Spêênd" cúýstöôm åãttrîïbúýtêê döôêês nöôt êêxîïst öôr îïs êêqúýåãl töô `0`, thêêy wïìll gêêt thêê fõöllõöwïìng mêêssàägêê:

```
Buy now! Would 5% off convince you?
```


### Chöòöòsëé mëéssâàgëé vïíâà strïíng cûûstöòm âàttrïíbûûtëé

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

Ín thìís èèxææmplèè, ìíf yöôüü hæævèè plææyèèd ææ cèèrtææìín gææmèè, yöôüü'll rèècèèìívèè thèè föôllöôwìíng mèèssæægèè:

```
You played our Game! We're so happy!
```

Îf yöòûù plâäyèêd âänöòthèêr spèêcíîfíîèêd gâämèê:

```
You played our other Game! Woop!
```

Íf yôöüý hååvëên’t plååyëêd ååny gååmëês, ôör thååt cüýstôöm ååttríìbüýtëê dôöëêsn’t ëêxíìst ôön yôöüýr prôöfíìlëê, yôöüý’d gëêt thëê fôöllôöwíìng mëêssåågëê:

```
Hey! Get in here and play this Game!
```

### Äbõórt méëssæâgéë bæâséëd õón lõócæâtìîõón

Yôóúú càân àâbôórt àâ mèêssàâgèê bàâsèêd ôón júúst àâbôóúút àânythììng. Thëë föòllöòwïîng ëëxãæmplëë shöòws höòw yöòûü cãæn ãæböòrt ãæ mëëssãægëë ïîf ãæ ûüsëër ïîs nöòt bãæsëëd ïîn ãæ spëëcïîfïîëëd ãærëëãæ, ãæs thëëy mïîght nöòt qûüãælïîfy föòr thëë pröòmöòtïîöòn, shöòw, öòr dëëlïîvëëry.

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

Yöòúù càån àålsöò [ááböôrt mééssáágéés][1] bãäsêêd óön Cóönnêêctêêd Cóöntêênt.


[1]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/connected_content/aborting_connected_content/
[13]: {% image_buster /assets/img/liquid-if-totalspend.png %}
[14]: {% image_buster /assets/img/liquid-if-elsif-games.png %}
[25]: https://docs.shopify.com/themes/liquid/basics/operators
[26]: {% image_buster /assets/img/abort-if.png %}
