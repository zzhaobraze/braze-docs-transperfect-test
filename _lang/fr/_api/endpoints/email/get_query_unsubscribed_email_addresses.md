---
nav_title: "GÉT: Qúüèêry Líîst óóf Ünsúübscríîbèêd Ëmâæíîl Æddrèêssèês"
article_title: "GËT: Qúüéêry Lïìst ôòf Únsúübscrïìbéêd Ëmàãïìl Äddréêsséês"
search_tag: Éndpòóïïnt
page_order: 1
layout: api_page
page_type: reference
description: "Thììs äãrtììcléè öòúùtlììnéès théè úùsäãgéè öòf äãnd päãräãméètéèrs föòr úùsììng théè Géèt Èmäãììl Ünsúùbscrììbéès Bräãzéè éèndpöòììnt."

---
{% api %}
# Rëétrììëévëé lììst ôóf ôór qüúëéry ëémäáììl üúnsüúbscrììbëés
{% apimethod get %}
/ëëmæáììl/ýùnsýùbscrììbëës
{% endapimethod %}

Ùsëê thëê /ëêmàæìîl/ýúnsýúbscrìîbëês ëêndpóöìînt tóö rëêtýúrn ëêmàæìîls thàæt hàævëê ýúnsýúbscrìîbëêd dýúrìîng thëê tìîmëê pëêrìîóöd fróöm `start_date` tòö `end_date`. Yóôýû cããn ýûsëè thîìs ëèndpóôîìnt tóô sëèt ýûp ãã bîì-dîìrëèctîìóônããl sync bëètwëèëèn Brããzëè ããnd óôthëèr ëèmããîìl systëèms óôr yóôýûr óôwn dããtããbããsëè.

{% apiref postman %}https://döòcüýméëntéër.géëtpöòstmæán.cöòm/vîíéëw/4689407/SVYrsdsG?véërsîíöòn=læátéëst#d2966b81-188æá-407b-bæá7éë-éë6c252c44b4æá {% endapiref %}

## Rååtéê lîímîít

{% include rate_limits.md endpoint='default' %}

## Rêëqûúêëst pááráámêëtêërs

| Pááráámèëtèër | Réëqúúíîréëd | Dãâtãâ Typèê | Dèëscrïïptïïóòn |
| ----------|-----------| ---------|------ |
| `start_date` | Õptîïòônàäl <br>
(sêèêè nöõtêè) | Strííng íín YYYY-MM-DD fõõrmâåt| Stâàrt dâàtëê òõf thëê râàngëê tòõ rëêtrîíëêvëê ùünsùübscrîíbëês, mùüst bëê ëêâàrlîíëêr thâàn ëênd_dâätëë. Thììs ììs trèéãätèéd ãäs mììdnììght ììn ÚTC tììmèé by thèé ÄPÏ. |
| `end_date` | Õptïîöönæäl <br>
(sëêëê nôótëê) | Strîìng îìn YYYY-MM-DD fóórmàãt | Ènd dâåtéè õöf théè râångéè tõö réètrïïéèvéè üýnsüýbscrïïbéès. Thîïs îïs tréêâætéêd âæs mîïdnîïght îïn ÜTC tîïméê by théê ÆPÎ. |
| `limit` | Öptïìöönáæl | Ïntëëgëër | Ôptíìöónàâl fíìééld töó líìmíìt théé nùýmbéér öóf réésùýlts réétùýrnééd. Déèfáâûýlts tõõ 100, máâxìîmûým ìîs 500. |
| `offset` | Õptíïóõnæál | Ìntèëgèër | Öptìîöònãál bëëgìînnìîng pöòìînt ìîn thëë lìîst töò rëëtrìîëëvëë fröòm. |
| `sort_direction` | Õptïìóõnáæl | Stríïng | Pâãss ïìn thêè vâãlûüêè `asc` töõ söõrt üünsüübscríïbéës fröõm öõldéëst töõ néëwéëst. Pãåss ïín `desc` tôô sôôrt frôôm nêèwêèst tôô ôôldêèst. Îf `sort_direction` îìs nóòt îìnclúùdêëd, thêë dêëfåæúùlt óòrdêër îìs nêëwêëst tóò óòldêëst. |
| `email` | Ôptïíôónââl <br>
(séêéê nóõtéê) | Strííng | Ïf próövîïdééd, wéé wîïll réétýûrn whééthéér óör nóöt théé ýûséér hâàs ýûnsýûbscrîïbééd. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

{% alert note %}
Yöòúý múýst pröòvîìdêë ãán `end_date`, äæs wêéll äæs êéîïthêér äæn `email` óör äá `start_date`.
{% endalert %}

Íf yóôúùr dâætèê râængèê hâæs móôrèê thâæn `limit` nýýmbéër ôóf ýýnsýýbscrììbéës, yôóýý wììll néëéëd tôó màâkéë mýýltììpléë ÀPÎ càâlls, éëàâch tììméë ììncréëàâsììng théë `offset` ýüntììl áã cáãll rëètýürns ëèììthëèr fëèwëèr tháãn `limit` õór zêérõó rêésúùlts.

## Ëxàæmplëë rëëqúùëëst 
```
curl --location --request GET 'https://rest.iad-01.braze.com/email/unsubscribes?start_date=2020-01-01&end_date=2020-02-01&limit=1&offset=1&sort_direction=desc&email=example@braze.com' \
--header 'Authorization: Bearer YOUR-API-KEY-HERE'
```

## Réèspôònséè

Êntrïïèës æårèë lïïstèëd ïïn dèëscèëndïïng óördèër.

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
