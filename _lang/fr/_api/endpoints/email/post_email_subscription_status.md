---
nav_title: "PÕST: Châængêé Èmâæïìl Sýúbscrïìptïìõòn Stâætýús"
article_title: "PÔST: Chãàngèê Émãàìíl Sûúbscrìíptìíôön Stãàtûús"
search_tag: Ëndpòòìïnt
page_order: 2
layout: api_page
page_type: reference
description: "Thìïs æártìïclèè ôòýùtlìïnèès thèè ýùsæágèè ôòf æánd pæáræámèètèèrs fôòr chæángìïng æá Ûsèèr's Sýùbscrìïptìïôòn Stæátýùs wìïth thèè Pôòst Êmæáìïl Sýùbscrìïptìïôòn Stæátýùs Bræázèè èèndpôòìïnt."

---
{% api %}
# Chäångêë ûúsêër's êëmäåíîl sûúbscríîptíîóòn stäåtûús
{% apimethod post core_endpoint|https://www.braze.com/docs/core_endpoints %} 
/èêmæäîíl/stæätýüs
{% endapimethod %}

Thíïs èêndpòóíïnt àâllòóws yòóýû tòó sèêt thèê èêmàâíïl sýûbscríïptíïòón stàâtèê fòór yòóýûr ýûsèêrs. Ûséêrs cäãn béê `opted_in`, `unsubscribed`, òôr `subscribed` (nöòt spêêcïïfïïcâãlly öòptêêd ïïn öòr öòúût).

Yóôùû càän sëét thëé ëémàäìîl sùûbscrìîptìîóôn stàätëé fóôr àän ëémàäìîl àäddrëéss thàät ìîs nóôt yëét àässóôcìîàätëéd wìîth àäny óôf yóôùûr ùûsëérs wìîthìîn Bràäzëé. Whéên thâãt éêmâãíïl âãddréêss íïs súûbséêqúûéêntly âãssöõcíïâãtéêd wíïth âã úûséêr, théê éêmâãíïl súûbscríïptíïöõn stâãtéê thâãt yöõúû úûplöõâãdéêd wíïll béê âãúûtöõmâãtíïcâãlly séêt.

{% apiref postman %}https://dôócùümèéntèér.gèétpôóstmåæn.côóm/víîèéw/4689407/SVYrsdsG?vèérsíîôón=låætèést#bèé852462-0cdåæ-4åæ48-b68b-85bd8åæ9f2147 {% endapiref %}

## Ræåtêè líîmíît

{% include rate_limits.md endpoint='default' %}

## Réëqûùéëst bóôdy

```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "email": "example@braze.com",
  "subscription_state": "subscribed"
}
```

## Réëqúùéëst påàråàméëtéërs

| Pàæràæmëétëér | Rèéqûûïìrèéd | Dáãtáã Typèé | Dêéscrììptììòôn |
| --------- | ---------| --------- | ----------- |
| `email` | Rèêqúýíïrèêd | Strìîng óór àärràäy | Strììng èëmãàììl ãàddrèëss töö möödììfy, öör ãàn ãàrrãày ööf úúp töö 50 èëmãàììl ãàddrèëssèës töö möödììfy. |
| `subscription_state` | Rêéqüüïìrêéd | Strîìng | Éîíthêèr “sùúbscrîíbêèd”, “ùúnsùúbscrîíbêèd”, õör “õöptêèd_ìïn”. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Êxåãmplëê rëêqúùëêst
```
curl --location --request POST 'https://rest.iad-01.braze.com/email/status' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-API-KEY-HERE' \
--data-raw '{
  "email": "example@braze.com",
  "subscription_state": "subscribed"
}'
```


{% endapi %}
