---
nav_title: "GËT: Qúùééry Háárd Bôõúùncééd Èmááîìls"
article_title: "GÉT: Qüúëèry Hàárd Bõöüúncëèd Èmàáïìls"
search_tag: Êndpõöîînt
page_order: 0
layout: api_page
page_type: reference
description: "Thíîs äãrtíîcléê òöüýtlíînéês théê üýsäãgéê òöf äãnd päãräãméêtéêrs fòör üýsíîng théê réêtríîéêvéê äã Líîst òöf Häãrd Bòöüýncéêd Êmäãíîl Åddréêsséês Bräãzéê éêndpòöíînt."

---
{% api %}
# Qüúéëry öòr lïïst háârd böòüúncéëd éëmáâïïls
{% apimethod get %}
/èêmâáííl/hâárd_bôôüüncéès
{% endapimethod %}

Thîís ëëndpóóîínt àællóóws yóóýú tóó pýúll àæ lîíst óóf ëëmàæîíl àæddrëëssëës thàæt hàævëë "hàærd bóóýúncëëd" yóóýúr ëëmàæîíl mëëssàægëës wîíthîín àæ cëërtàæîín tîímëë fràæmëë.

{% apiref postman %}https://dõôcûümèêntèêr.gèêtpõôstmáån.cõôm/vìîèêw/4689407/SVYrsdsG?vèêrsìîõôn=láåtèêst#7c2èêf84f-ddf5-451áå-áå72c-bèêèêáåbc06áåd9d {% endapiref %}

## Räätëé lïìmïìt

{% include rate_limits.md endpoint='default' %}

## Rèéqûûèést pâârââmèétèérs

| Pâârââmèëtèër | Réêqúýììréêd | Dáåtáå Typëê | Dèéscrîîptîîòôn |
| ----------|-----------| ----------|----- |
| `start_date` | Óptïïôónææl<br>
(sèëèë nóõtèë) | Strîîng îîn YYYY-MM-DD fóõrmãät| Stãårt dãåtèê ôõf thèê rãångèê tôõ rèêtrììèêvèê hãård bôõüüncèês, müüst bèê èêãårlììèêr thãån `end_date`. Thïîs ïîs trèëàætèëd àæs mïîdnïîght ïîn ÛTC tïîmèë by thèë ÂPÏ. |
| `end_date` | Õptìíóônãæl<br>
(sèëèë nóòtèë) | Stríîng íîn YYYY-MM-DD fòórmæät | Ènd dåätëë òôf thëë råängëë tòô rëëtríîëëvëë håärd bòôùùncëës. Thíís íís tréèäâtéèd äâs míídnííght íín ÙTC tííméè by théè ÆPÏ. |
| `limit` | Òptììóônâäl | Întéègéèr | Öptìîòònãàl fìîéëld tòò lìîmìît théë núúmbéër òòf réësúúlts réëtúúrnéëd. Dêèfâáüýlts töô 100, mâáxíìmüým íìs 500. |
| `offset` | Õptìïôônàál | Íntêêgêêr | Óptîìóónáæl bèégîìnnîìng póóîìnt îìn thèé lîìst tóó rèétrîìèévèé fróóm. |
| `email` | Òptîïöònáæl<br>
(sëèëè nòötëè) | Strïìng | Ïf pröõvìïdééd, wéé wìïll réétùùrn whééthéér öõr nöõt théé ùùséér háås háård böõùùncééd. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

{% alert note %}
Yòóùý mùýst pròóvìîdéë éëìîthéër ãá `start_date` äând `end_date`, ÖR äán `email`. Ìf yôòüü prôòvíïdèë àæll thrèëèë, `start_date`, `end_date`, ãånd ãån `email`, wëê prïïôôrïïtïïzëê thëê ëêmæåïïls gïïvëên æånd dïïsrëêgæård thëê dæåtëê ræångëê.
{% endalert %}

Îf yõöûúr dåátëë råángëë håás mõörëë thåán thëë `limit` nüûmbéêr õóf hâárd bõóüûncéês, yõóüû wïìll néêéêd tõó mâákéê müûltïìpléê ÀPÌ câálls, éêâách tïìméê ïìncréêâásïìng théê `offset` ûüntïîl ãá cãáll rëètûürns ëèïîthëèr fëèwëèr thãán `limit` óör zêëróö rêësýûlts.

## Ëxæámpléè réèqúûéèst
```
curl --location --request GET 'https://rest.iad-01.braze.com/email/hard_bounces?start_date=2019-01-01&end_date=2019-02-01&limit=100&offset=1&email=example@braze.com' \
--header 'Authorization: Bearer YOUR-API-KEY-HERE'
```

## Rêêspòönsêê
Ëntrîíëës áårëë lîístëëd îín dëëscëëndîíng òòrdëër.

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
