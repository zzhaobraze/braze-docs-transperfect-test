---
nav_title: Äbòôrtíîng Mëëssãâgëës
article_title: Âböórtîïng Lîïqüûîïd Mëèssäágëès
page_order: 7
description: "Mëëssåægëës måæy nòöw bëë åæbòörtëëd wìïthìïn còöndìïtìïòönåæl ståætëëmëënts. În thîís rèëfèërèëncèë âàrtîíclèë, wèë lîíst sòòmèë èëxâàmplèë ùúsèë câàsèës fòòr thîís fùúnctîíòònâàlîíty."

---

# Äbõòrtîïng Lîïqüüîïd mêëssãágêës

Òptíìöònáâlly, yöòùý cáân áâlsöò áâböòrt mèëssáâgèës wíìthíìn cöòndíìtíìöònáâls. Hèérèé æærèé sõõmèé èéxææmplèés õõf hõõw thíîs fèéæætûýrèé cææn bèé ûýsèéd íîn mæærkèétíîng cææmpææíîgns:

## Âböòrt méëssåågéë îìf "Núýmbéër Gååméës Âttéëndéëd" = 0

Fòõr ëéxäâmplëé, lëét’s säây thäât yòõúú dïíd nòõt wäânt tòõ sëénd äâ mëéssäâgëé tòõ cúústòõmëérs whòõ häâvëé nòõt äâttëéndëéd äâ gäâmëé:

{% raw %}
```liquid
{% if customer_attribute.${Number_Game_Attended} == 1 %}
Loved the game? Get 10% off your second one with code SAVE10.
{% elsif customer_attribute.${Number_Game Attended} > 1 %}
Love the games? Get 10% off your next one with code SAVE10.
{% else %}
{% abort_message() %}
{% endif %}
```
{% endraw %}

Thîís méëssããgéë wîíll õònly séënd tõò cûústõòméërs whõò ããréë knõòwn tõò hããvéë ããttéëndéëd ãã gããméë.

## Méëssæägéë Ènglîîsh spéëæäkîîng cýüstõôméërs õônly

Yöòûú cåán mèêssåágèê Ènglïìsh spèêåákïìng cûústöòmèêrs öònly by crèêåátïìng åán "ïìf" ståátèêmèênt thåát'll måátch whèên åá cûústöòmèêr's låángûúåágèê ïìs Ènglïìsh åánd åán èêlsèê ståátèêmèênt thåát'll åáböòrt thèê mèêssåágèê föòr åányöònèê whöò döòèês nöòt spèêåák Ènglïìsh öòr döòèês nöòt håávèê åá låángûúåágèê öòn thèêïìr pröòfïìlèê.

{% raw %}
```liquid

{% if ${language} == 'en' %}
Send this message in English!
{% else %}
{% abort_message() %}
{% endif %}
```

By dèëfâäúýlt Brâäzèë wîïll lóòg âä gèënèërîïc èërróòr mèëssâägèë tóò yóòúýr Dèëvèëlóòpèër Cóònsóòlèë lóòg:

```text
{% abort_message %} called
```

Yòòúû cæãn æãlsòò hæãvèë thèë æãbòòrt mèëssæãgèë lòòg sòòmèëthïîng tòò yòòúûr Dèëvèëlòòpèër Còònsòòlèë lòòg by ïînclúûdïîng æã strïîng ïînsïîdèë thèë pæãrèënthèësèës:

```liquid
{% abort_message('language was nil') %}
```
{% endraw %}

![Mêêssààgêê êêrróór lóóg ïîn thêê Dêêvêêlóópêêr Cóónsóólêê wïîth ààn ààbóórt mêêssààgêê óóf "lààngúûààgêê wààs nïîl".][26]

[15]: {% image_buster /assets/img_archive/liquid_abort.png %}
[26]: {% image_buster /assets/img_archive/developer_console.png %}
[31]:https://docs.shopify.com/themes/liquid/tags/variable-tags
[32]:https://docs.shopify.com/themes/liquid/tags/iteration-tags
[34]:{% image_buster /assets/img_archive/personalized_iflogic_.png %}
[37]:#accounting-for-null-attribute-values
