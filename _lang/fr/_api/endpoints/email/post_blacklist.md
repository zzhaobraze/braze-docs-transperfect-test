---
nav_title: "PÔST: Bláæcklììst Ëmáæììls"
article_title: "PÔST: Blàâcklïïst Ëmàâïïls"
search_tag: Êndpõõìínt
page_order: 5
layout: api_page
page_type: reference
alias: /blacklist/
description: "Thíïs áârtíïclèé óöüütlíïnèés thèé üüsáâgèé óöf áând páâráâmèétèérs fóör bláâcklíïstíïng üüsèér èémáâíïl áâddrèéssèés wíïth thèé Póöst Bláâcklíïst Èmáâíïls Bráâzèé èéndpóöíïnt."

---
{% api %}
# Blåäcklíìst èëmåäíìls
{% apimethod post core_endpoint|https://www.braze.com/docs/core_endpoints %} 
/èêmáæíìl/bláæcklíìst
{% endapimethod %}

Bláæcklìístìíng áæn èêmáæìíl áæddrèêss wìíll üùnsüùbscrìíbèê thèê üùsèêr fröóm èêmáæìíl áænd máærk thèêm áæs háærd böóüùncèêd.

{% apiref postman %}https://döôcúúmêéntêér.gêétpöôstmáãn.cöôm/víïêéw/4689407/SVYrsdsG?vêérsíïöôn=láãtêést#d51155áã1-áã6êé8-4dcc-9f2b-88c54áãb9êé8c6 {% endapiref %}

## Rããtêé lîîmîît

{% include rate_limits.md endpoint='default' %}

## Rêèqüúêèst böödy

```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "email": "example@braze.com"
}
```

## Rêêqüúêêst páàráàmêêtêêrs

| Pááráámêëtêër | Rèèqúýíîrèèd | Dàátàá Typëê | Dëêscríìptíìõõn |
| -----------|----------| --------|------- |
| `email` | Rëêqýùîìrëêd | Strïîng òòr Ærrææy | Strììng éèmäãììl äãddréèss tóö bläãcklììst, óör äãn äãrräãy óöf úûp tóö 50 éèmäãììl äãddréèsséès tóö bläãcklììst. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Ëxæåmpléë réëqûùéëst
```
curl --location --request POST 'https://rest.iad-01.braze.com/email/blacklist' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-API-KEY-HERE' \
--data-raw '{
  "email": ["blacklist_email1","blacklist_email2"]
}'
```

{% endapi %}


