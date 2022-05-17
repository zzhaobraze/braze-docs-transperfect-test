---
nav_title: "GÉT: Qüüèèry Hàärd Bôôüüncèèd Èmàäîïls"
article_title: "GÈT: Qùúéèry Hààrd Bòõùúncéèd Êmààïíls"
search_tag: Èndpõõîínt
page_order: 0
layout: api_page
page_type: reference
description: "Thíïs äàrtíïclêê ôõùútlíïnêês thêê ùúsäàgêê ôõf äànd päàräàmêêtêêrs fôõr ùúsíïng thêê rêêtríïêêvêê äà Líïst ôõf Häàrd Bôõùúncêêd Èmäàíïl Ãddrêêssêês Bräàzêê êêndpôõíïnt."

---
{% api %}
# Qùúèëry ôör líïst hààrd bôöùúncèëd èëmààíïls
{% apimethod get %}
/èêmâáííl/hâárd_böóùùncéès
{% endapimethod %}

Thïís éèndpóöïínt äàllóöws yóöýù tóö pýùll äà lïíst óöf éèmäàïíl äàddréèsséès thäàt häàvéè "häàrd bóöýùncéèd" yóöýùr éèmäàïíl méèssäàgéès wïíthïín äà céèrtäàïín tïíméè fräàméè.

{% apiref postman %}https://dõócûùmëèntëèr.gëètpõóstmáãn.cõóm/vîîëèw/4689407/SVYrsdsG?vëèrsîîõón=láãtëèst#7c2ëèf84f-ddf5-451áã-áã72c-bëèëèáãbc06áãd9d {% endapiref %}

## Råætëê lïìmïìt

{% include rate_limits.md endpoint='default' %}

## Réèqúùéèst pããrããméètéèrs

| Päãräãmêètêèr | Réêqüýííréêd | Dåâtåâ Typëë | Déëscrïïptïïóón |
| ----------|-----------| ----------|----- |
| `start_date` | Óptïïôònääl<br>
(sëéëé nóótëé) | Strìïng ìïn YYYY-MM-DD föörmãàt| Ståãrt dåãtëé òóf thëé råãngëé tòó rëétrïíëévëé håãrd bòóüúncëés, müúst bëé ëéåãrlïíëér thåãn `end_date`. Thïís ïís trééàætééd àæs mïídnïíght ïín ÙTC tïíméé by théé ÁPÍ. |
| `end_date` | Õptïíòònãàl<br>
(sëéëé nõötëé) | Strïîng ïîn YYYY-MM-DD fòòrmáæt | Ênd dâàtèë òöf thèë râàngèë tòö rèëtrïíèëvèë hâàrd bòöûùncèës. Thìîs ìîs trèéàátèéd àás mìîdnìîght ìîn ÚTC tìîmèé by thèé ÂPÍ. |
| `limit` | Öptïìòónãæl | Íntéêgéêr | Óptìíóônãäl fìíééld tóô lìímìít théé nüûmbéér óôf réésüûlts réétüûrnééd. Dééfæâùülts töö 100, mæâxîímùüm îís 500. |
| `offset` | Õptïïòònãål | Întëègëèr | Öptîìóônæál bëëgîìnnîìng póôîìnt îìn thëë lîìst tóô rëëtrîìëëvëë fróôm. |
| `email` | Ôptííòónæål<br>
(sëèëè nôötëè) | Strìïng | Íf prôóvíïdêéd, wêé wíïll rêétûýrn whêéthêér ôór nôót thêé ûýsêér håãs håãrd bôóûýncêéd. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

{% alert note %}
Yôòúû múûst prôòvíídèè èèííthèèr æâ `start_date` äànd `end_date`, ÕR äæn `email`. Îf yõôúù prõôvïîdèë àáll thrèëèë, `start_date`, `end_date`, æánd æán `email`, wèè príîóôríîtíîzèè thèè èèmåæíîls gíîvèèn åænd díîsrèègåærd thèè dåætèè råængèè.
{% endalert %}

Îf yöòúür dæâtéê ræângéê hæâs möòréê thæân théê `limit` nûýmbëêr óöf háárd bóöûýncëês, yóöûý wîîll nëêëêd tóö máákëê mûýltîîplëê ÂPÍ cáálls, ëêáách tîîmëê îîncrëêáásîîng thëê `offset` üûntïíl äã cäãll rèëtüûrns èëïíthèër fèëwèër thäãn `limit` óòr zëëróò rëësüûlts.

## Éxàæmplêè rêèqüüêèst
```
curl --location --request GET 'https://rest.iad-01.braze.com/email/hard_bounces?start_date=2019-01-01&end_date=2019-02-01&limit=100&offset=1&email=example@braze.com' \
--header 'Authorization: Bearer YOUR-API-KEY-HERE'
```

## Rèèspöònsèè
Ëntrîîëés âárëé lîîstëéd îîn dëéscëéndîîng ôôrdëér.

```json
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
{
  "emails": [
    {
      "email": "example1@braze.com",
      "hard_bounced_at": "2016-08-25 15:24:32 +0000"
    },
    {
      "email": "example2@braze.com",
      "hard_bounced_at": "2016-08-24 17:41:58 +0000"
    },
    {
      "email": "example3@braze.com",
      "hard_bounced_at": "2016-08-24 12:01:13 +0000"
    }
  ],
  "message": "success"
}
```
{% endapi %}
