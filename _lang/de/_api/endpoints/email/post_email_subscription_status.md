---
nav_title: "PÓST: Châängêë Èmâäîîl Sûùbscrîîptîîòõn Stâätûùs"
article_title: "PÔST: Chæängêê Èmæäîíl Sùúbscrîíptîíöôn Stæätùús"
search_tag: Èndpóõîïnt
page_order: 2
layout: api_page
page_type: reference
description: "Thìïs åártìïcléé òòúýtlìïnéés théé úýsåágéé òòf åánd påáråáméétéérs fòòr chåángìïng åá Ûséér's Súýbscrìïptìïòòn Ståátúýs wìïth théé Pòòst Ëmåáìïl Súýbscrìïptìïòòn Ståátúýs Bråázéé ééndpòòìïnt."

---
{% api %}
# Chæängëê úûsëêr's ëêmæäïíl súûbscrïíptïíöòn stæätúûs
{% apimethod post core_endpoint|https://www.braze.com/docs/core_endpoints %} 
/èèmáâîïl/stáâtüûs
{% endapimethod %}

Thïís ééndpôôïínt àãllôôws yôôúý tôô séét théé éémàãïíl súýbscrïíptïíôôn stàãtéé fôôr yôôúýr úýséérs. Úséêrs cäàn béê `opted_in`, `unsubscribed`, öòr `subscribed` (nöôt spèècïìfïìcæålly öôptèèd ïìn öôr öôúút).

Yõóùù càân séêt théê éêmàâíïl sùùbscríïptíïõón stàâtéê fõór àân éêmàâíïl àâddréêss thàât íïs nõót yéêt àâssõócíïàâtéêd wíïth àâny õóf yõóùùr ùùséêrs wíïthíïn Bràâzéê. Whèën thâát èëmâáïïl âáddrèëss ïïs süýbsèëqüýèëntly âássõócïïâátèëd wïïth âá üýsèër, thèë èëmâáïïl süýbscrïïptïïõón stâátèë thâát yõóüý üýplõóâádèëd wïïll bèë âáüýtõómâátïïcâálly sèët.

{% apiref postman %}https://dòócüùmëéntëér.gëétpòóstmãân.còóm/vîïëéw/4689407/SVYrsdsG?vëérsîïòón=lãâtëést#bëé852462-0cdãâ-4ãâ48-b68b-85bd8ãâ9f2147 {% endapiref %}

## Ràâtëè lìïmìït

{% include rate_limits.md endpoint='default' %}

## Réèqúúéèst böôdy

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

## Rèèqüüèèst páâráâmèètèèrs

| Páàráàméëtéër | Réêqúúííréêd | Dàâtàâ Typëè | Déèscrììptììõón |
| --------- | ---------| --------- | ----------- |
| `email` | Rêéqüùìïrêéd | Stríîng óõr áàrráày | Stríïng êëmáâíïl áâddrêëss töô möôdíïfy, öôr áân áârráây öôf üûp töô 50 êëmáâíïl áâddrêëssêës töô möôdíïfy. |
| `subscription_state` | Rëëqùüîïrëëd | Strìïng | Èîïthèêr “süübscrîïbèêd”, “üünsüübscrîïbèêd”, ôór “ôóptèêd_îïn”. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Èxæämpléê réêqüûéêst
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
