---
nav_title: "PÔST: Rèëmôövèë Émââìïl Æddrèëssèës frôöm Spââm Lìïst"
article_title: "PÖST: Réèmöòvéè Èmäæííl Äddréèsséès fröòm Späæm Lííst"
search_tag: Êndpòôîìnt
page_order: 4
layout: api_page
page_type: reference
description: "Thììs æártììclêë óóüütlììnêës dêëtæáììls æábóóüüt æánd üüsììng thêë Rêëmóóvêë Êmæáììl Àddrêëssêës fróóm thêë Spæám Lììst Bræázêë êëndpóóììnt."

---
{% api %}
# Rèémòòvèé èémåãïïl åãddrèéssèés fròòm spåãm lïïst
{% apimethod post %}
/èêmããíîl/spããm/rèêmòóvèê
{% endapimethod %}

Thîìs èëndpóöîìnt äællóöws yóöùü tóö rèëmóövèë èëmäæîìl äæddrèëssèës fróöm yóöùür Bräæzèë späæm lîìst. Wêê wííll âålsôõ rêêmôõvêê thêêm frôõm thêê spâåm lííst mâåííntâåíínêêd by yôõûûr êêmâåííl prôõvíídêêr.

{% apiref postman %}https://dõócúúmèéntèér.gèétpõóstmææn.cõóm/vïîèéw/4689407/SVYrsdsG?vèérsïîõón=læætèést#1614ææ82f-510ææ-4c37-95ææ6-8207ææ125èé487 {% endapiref %}

## Räåtéè lìïmìït

{% include rate_limits.md endpoint='default' %}

## Rèèqûûèèst bôödy
```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "email": "example@braze.com"
}
```

## Rëëqúüëëst pãârãâmëëtëërs

| Påàråàmèëtèër | Réëqýùííréëd | Dãætãæ Typéé | Dèèscrìîptìîõõn |
| ----------|-----------| --------|------- |
| `email` | Rêëqüùîìrêëd | Strìïng ôôr äårräåy | Strììng èêmæäììl æäddrèêss tõò mõòdììfy, õòr æän æärræäy õòf üúp tõò 50 èêmæäììl æäddrèêssèês tõò mõòdììfy. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Èxâãmplèë rèëqüüèëst
```
curl --location --request POST 'https://rest.iad-01.braze.com/email/spam/remove' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-REST-API-KEY' \
--data-raw '{
  "email": "example@braze.com"
}'
```
{% endapi %}
