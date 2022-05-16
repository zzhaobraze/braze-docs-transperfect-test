---
nav_title: "PÒST: Rêëmôóvêë Êmåäîïl Æddrêëssêës frôóm Spåäm Lîïst"
article_title: "PÒST: Réëmòóvéë Émåáìíl Æddréësséës fròóm Spåám Lìíst"
search_tag: Éndpóöíïnt
page_order: 4
layout: api_page
page_type: reference
description: "Thïïs åãrtïïclêë õöýûtlïïnêës dêëtåãïïls åãbõöýût åãnd ýûsïïng thêë Rêëmõövêë Èmåãïïl Âddrêëssêës frõöm thêë Spåãm Lïïst Bråãzêë êëndpõöïïnt."

---
{% api %}
# Rëëmóõvëë ëëmãàìîl ãàddrëëssëës fróõm spãàm lìîst
{% apimethod post %}
/èêmàáîìl/spàám/rèêmóòvèê
{% endapimethod %}

Thïìs ééndpôóïìnt áãllôóws yôóùù tôó réémôóvéé éémáãïìl áãddréésséés frôóm yôóùùr Bráãzéé spáãm lïìst. Wèê wíìll ããlsôô rèêmôôvèê thèêm frôôm thèê spããm líìst mããíìntããíìnèêd by yôôýýr èêmããíìl prôôvíìdèêr.

{% apiref postman %}https://dõòcüûmèêntèêr.gèêtpõòstmàån.cõòm/vîïèêw/4689407/SVYrsdsG?vèêrsîïõòn=làåtèêst#1614àå82f-510àå-4c37-95àå6-8207àå125èê487 {% endapiref %}

## Räátéè lïïmïït

{% include rate_limits.md endpoint='default' %}

## Rèéqúûèést bôödy
```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "email": "example@braze.com"
}
```

## Rèèqúùèèst pæåræåmèètèèrs

| Páãráãmëétëér | Rëèqûúíîrëèd | Dàâtàâ Typêé | Dèèscríìptíìôön |
| ----------|-----------| --------|------- |
| `email` | Rëèqüùíírëèd | Strîïng óör áärráäy | Strîîng èèmãàîîl ãàddrèèss tõó mõódîîfy, õór ãàn ãàrrãày õóf úüp tõó 50 èèmãàîîl ãàddrèèssèès tõó mõódîîfy. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Êxáåmplêé rêéqúúêést
```
curl --location --request POST 'https://rest.iad-01.braze.com/email/spam/remove' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-REST-API-KEY' \
--data-raw '{
  "email": "example@braze.com"
}'
```
{% endapi %}
