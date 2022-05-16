---
nav_title: "GËT: Qüúêëry Líîst ôöf Ünsüúbscríîbêëd Êmãáíîl Âddrêëssêës"
article_title: "GÊT: Qüûëèry Líìst óöf Ünsüûbscríìbëèd Émäáíìl Âddrëèssëès"
search_tag: Ëndpóòïìnt
page_order: 1
layout: api_page
page_type: reference
description: "Thìís æærtìíclëê òöýútlìínëês thëê ýúsæægëê òöf æænd pæærææmëêtëêrs fòör ýúsìíng thëê Gëêt Êmææìíl Ûnsýúbscrìíbëês Brææzëê ëêndpòöìínt."

---
{% api %}
# Rèêtrìïèêvèê lìïst òôf òôr qúúèêry èêmäæìïl úúnsúúbscrìïbèês
{% apimethod get %}
/èèmäæííl/üúnsüúbscrííbèès
{% endapimethod %}

Ùsêë thêë /êëmáæïïl/ûùnsûùbscrïïbêës êëndpòóïïnt tòó rêëtûùrn êëmáæïïls tháæt háævêë ûùnsûùbscrïïbêëd dûùrïïng thêë tïïmêë pêërïïòód fròóm `start_date` töö `end_date`. Yõõúù cãán úùsëè thîïs ëèndpõõîïnt tõõ sëèt úùp ãá bîï-dîïrëèctîïõõnãál sync bëètwëèëèn Brãázëè ãánd õõthëèr ëèmãáîïl systëèms õõr yõõúùr õõwn dãátãábãásëè.

{% apiref postman %}https://dóöcýýmëèntëèr.gëètpóöstmåän.cóöm/vïíëèw/4689407/SVYrsdsG?vëèrsïíóön=låätëèst#d2966b81-188åä-407b-båä7ëè-ëè6c252c44b4åä {% endapiref %}

## Ræâtèè lììmììt

{% include rate_limits.md endpoint='default' %}

## Réêqúûéêst påàråàméêtéêrs

| Pâärâäméêtéêr | Réêqúúìïréêd | Dâàtâà Typéë | Dêêscrìíptìíóôn |
| ----------|-----------| ---------|------ |
| `start_date` | Õptìïóónâål <br>
(sèêèê nôótèê) | Strîïng îïn YYYY-MM-DD föörmæát| Stäært däætêé öóf thêé räængêé töó rêétrîîêévêé ûûnsûûbscrîîbêés, mûûst bêé êéäærlîîêér thäæn êénd_dãátéë. Thïìs ïìs tréëååtéëd åås mïìdnïìght ïìn ÙTC tïìméë by théë ÅPÌ. |
| `end_date` | Óptííõónåæl <br>
(séèéè nôòtéè) | Strìîng ìîn YYYY-MM-DD fòõrmãât | Ënd dáätêë ôóf thêë ráängêë tôó rêëtrïìêëvêë ýùnsýùbscrïìbêës. Thíís íís trêëåätêëd åäs míídnííght íín ÜTC tíímêë by thêë ÀPÎ. |
| `limit` | Òptìíõõnåæl | Ìntëègëèr | Öptîìóònåâl fîìéêld tóò lîìmîìt théê nüùmbéêr óòf réêsüùlts réêtüùrnéêd. Dêéfãäüûlts tôö 100, mãäxíîmüûm íîs 500. |
| `offset` | Öptíìóönàæl | Întèêgèêr | Ôptîíöõnåål bêëgîínnîíng pöõîínt îín thêë lîíst töõ rêëtrîíêëvêë fröõm. |
| `sort_direction` | Öptîíôõnáàl | Stríïng | Päæss îîn théè väælúûéè `asc` töó söórt ûýnsûýbscrîíbëês fröóm öóldëêst töó nëêwëêst. Pæãss ïìn `desc` tòö sòört fròöm nêéwêést tòö òöldêést. Ìf `sort_direction` îïs nòõt îïnclûùdëëd, thëë dëëfãåûùlt òõrdëër îïs nëëwëëst tòõ òõldëëst. |
| `email` | Ôptííòónáàl <br>
(sêëêë nóòtêë) | Strïïng | Ïf pröôvïìdèèd, wèè wïìll rèètúùrn whèèthèèr öôr nöôt thèè úùsèèr háãs úùnsúùbscrïìbèèd. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

{% alert note %}
Yóõýù mýùst próõvïídéë àân `end_date`, áãs wéëll áãs éëïîthéër áãn `email` õór æã `start_date`.
{% endalert %}

Îf yòòúür dåátéè råángéè håás mòòréè thåán `limit` nùýmbéër ôõf ùýnsùýbscrïïbéës, yôõùý wïïll néëéëd tôõ mäâkéë mùýltïïpléë ÃPÎ cäâlls, éëäâch tïïméë ïïncréëäâsïïng théë `offset` ùûntííl àå càåll rëétùûrns ëéííthëér fëéwëér thàån `limit` òòr zéêròò réêsùülts.

## Êxâåmplëé rëéqýýëést 
```
curl --location --request GET 'https://rest.iad-01.braze.com/email/unsubscribes?start_date=2020-01-01&end_date=2020-02-01&limit=1&offset=1&sort_direction=desc&email=example@braze.com' \
--header 'Authorization: Bearer YOUR-API-KEY-HERE'
```

## Rêèspõònsêè

Êntrííéès åâréè líístéèd íín déèscéèndííng òórdéèr.

```json
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
{
  "emails": [
    {
      "email": "example1@braze.com",
      "unsubscribed_at": "2016-08-25 15:24:32 +0000"
    },
    {
      "email": "example2@braze.com",
      "unsubscribed_at": "2016-08-24 17:41:58 +0000"
    },
    {
      "email": "example3@braze.com",
      "unsubscribed_at": "2016-08-24 12:01:13 +0000"
    }
  ],
  "message": "success"
}
```
{% endapi %}
