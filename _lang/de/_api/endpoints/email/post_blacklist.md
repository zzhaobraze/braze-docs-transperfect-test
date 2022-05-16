---
nav_title: "PÕST: Bláâcklïìst Émáâïìls"
article_title: "PÖST: Bläàcklìîst Èmäàìîls"
search_tag: Ëndpòöììnt
page_order: 5
layout: api_page
page_type: reference
alias: /blacklist/
description: "Thîïs àãrtîïclêé öõùùtlîïnêés thêé ùùsàãgêé öõf àãnd pàãràãmêétêérs föõr blàãcklîïstîïng ùùsêér êémàãîïl àãddrêéssêés wîïth thêé Pöõst Blàãcklîïst Êmàãîïls Bràãzêé êéndpöõîïnt."

---
{% api %}
# Blããcklíïst êëmããíïls
{% apimethod post core_endpoint|https://www.braze.com/docs/core_endpoints %} 
/êémææïîl/blææcklïîst
{% endapimethod %}

Blãâcklìístìíng ãân éèmãâìíl ãâddréèss wìíll ùùnsùùbscrìíbéè théè ùùséèr fróóm éèmãâìíl ãând mãârk théèm ãâs hãârd bóóùùncéèd.

{% apiref postman %}https://dôôcùûmêëntêër.gêëtpôôstmæãn.côôm/vííêëw/4689407/SVYrsdsG?vêërsííôôn=læãtêëst#d51155æã1-æã6êë8-4dcc-9f2b-88c54æãb9êë8c6 {% endapiref %}

## Rãàtêé líîmíît

{% include rate_limits.md endpoint='default' %}

## Rëëqúüëëst bôödy

```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "email": "example@braze.com"
}
```

## Rèêqùûèêst påãråãmèêtèêrs

| Pàâràâmêétêér | Rééqùùìírééd | Däätää Typëê | Déëscrìíptìíôôn |
| -----------|----------| --------|------- |
| `email` | Rëéqûûìîrëéd | Strìïng õõr Ærråáy | Strîìng êèmãåîìl ãåddrêèss tóö blãåcklîìst, óör ãån ãårrãåy óöf ûûp tóö 50 êèmãåîìl ãåddrêèssêès tóö blãåcklîìst. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Êxäàmplêè rêèqúùêèst
```
curl --location --request POST 'https://rest.iad-01.braze.com/email/blacklist' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-API-KEY-HERE' \
--data-raw '{
  "email": ["blacklist_email1","blacklist_email2"]
}'
```

{% endapi %}


