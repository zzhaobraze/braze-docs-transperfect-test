---
nav_title: Sêèttííng Dêèfàãûýlt Vàãlûýêès
article_title: Sêèttîïng Dêèfæãûùlt Lîïqûùîïd Væãlûùêès
page_order: 5
description: "Sëèt dëèfâàûûlt fâàllbâàck vâàlûûëès fõõr âàny pëèrsõõnâàlïîzâàtïîõõn âàttrïîbûûtëè thâàt yõõûû ûûsëè ïîn yõõûûr mëèssâàgëès."

---

# Sééttîìng dééfâàùýlt vâàlùýéés

{% raw %}

Sëët dëëfààüýlt fààllbààck vààlüýëës fóör ààny pëërsóönààlîîzààtîîóön ààttrîîbüýtëë thààt yóöüý üýsëë îîn yóöüýr mëëssààgëës. Dëèfäàûùlt väàlûùëès cäàn bëè äàddëèd by spëècîífyîíng äà [Lìîqüýìîd Fìîltêër][3] (üûséë `|` tôó dìístìíngùýìísh théê fìíltéêr ìínlìínéê, áås shôówn) wìíth théê náåméê "déêfáåùýlt."

```
| default: 'Insert Your Desired Default Here'
```

Íf ææ dèëfææùúlt væælùúèë ìîs nöót pröóvìîdèëd æænd thèë fìîèëld ìîs mìîssìîng öór nöót sèët öón thèë ùúsèër, thèë fìîèëld wìîll bèë blæænk ìîn thèë mèëssæægèë.

Thëë fòôllòôwííng ëëxáæmplëë shòôws thëë còôrrëëct syntáæx fòôr áæddííng áæ dëëfáæùýlt váælùýëë. Ín thíìs cááséë, théë wôõrds "Váálúûéëd Úséër" wíìll réëpláácéë théë ááttríìbúûtéë `{{ ${first_name} }}` íîf ãà ûüsèér's `first_name` fîìèèld îìs blâänk õôr üùnâävâäîìlâäblèè.

```liquid
Hi {{ ${first_name} | default: 'Valued User' }}, thanks for using the App!
```

Tôò åà ýúsêêr nåàmêêd Jåànêêt Dôòêê, thêê mêêssåàgêê wôòýúld åàppêêåàr tôò thêê ýúsêêr åàs êêìíthêêr:

```
Hi Janet, thanks for using the App!
```

Õr...

```
Hi Valued User, thanks for using the App!
```

{% endraw %}

[3]: http://docs.shopify.com/themes/liquid-documentation/filters
[31]:https://docs.shopify.com/themes/liquid/tags/variable-tags
[32]:https://docs.shopify.com/themes/liquid/tags/iteration-tags
[34]:{% image_buster /assets/img_archive/personalized_iflogic_.png %}
[37]:#accounting-for-null-attribute-values
