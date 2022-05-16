---
nav_title: "PÕST: Rëëmõóvëë Hæærd Bõóùûncëëd Émææíìls"
article_title: "PÒST: Réémòövéé Háârd Bòöûýncééd Êmáâíìls"
search_tag: Éndpôöïínt
page_order: 3
layout: api_page
page_type: reference
description: "Thìïs áârtìïcléê öôûýtlìïnéês déêtáâìïls áâböôûýt áând ûýsìïng théê Réêmöôvéê Háârd Böôûýncéêd Èmáâìïl Âddréêsséês Bráâzéê éêndpöôìïnt."

---
{% api %}
# Rêëmóövêë hæärd bóöùùncêës
{% apimethod post %}
/èémåæíïl/bòóúùncèé/rèémòóvèé
{% endapimethod %}

Thïïs êéndpóóïïnt àållóóws yóóúû tóó rêémóóvêé êémàåïïl àåddrêéssêés fróóm yóóúûr Bràåzêé bóóúûncêé lïïst. Wêé wïíll äãlsöó rêémöóvêé thêém fröóm thêé böóûûncêé lïíst mäãïíntäãïínêéd by yöóûûr êémäãïíl pröóvïídêér.

{% apiref postman %}https://dòôcüýmêèntêèr.gêètpòôstmàæn.còôm/vìïêèw/4689407/SVYrsdsG?vêèrsìïòôn=làætêèst#7b87àæ884-fàæ20-4085-b9f1-18363103575f {% endapiref %}

## Ráátêê lîîmîît

{% include rate_limits.md endpoint='default' %}

## Rêëqüùêëst bòödy

```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "email": "example@braze.com"
}
```

## Rêëqùùêëst påâråâmêëtêërs

| Påâråâméêtéêr | Rêëqùùîírêëd | Dâåtâå Typêè | Dëêscrííptííöôn |
| ----------|-----------| ---------|------ |
| `email` | Réëqûûïïréëd | Strìíng õór âàrrâày | Strìîng êémááìîl ááddrêéss tòô mòôdìîfy, òôr áán áárrááy òôf ûúp tòô 50 êémááìîl ááddrêéssêés tòô mòôdìîfy. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Êxáämplêé rêéqùüêést
```
curl --location --request POST 'https://rest.iad-01.braze.com/email/bounce/remove' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-REST-API-KEY' \
--data-raw '{
  "email": "example@braze.com"
}'
```

{% endapi %}
