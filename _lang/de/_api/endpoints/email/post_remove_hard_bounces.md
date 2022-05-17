---
nav_title: "PÔST: Rëèmóòvëè Håård Bóòûüncëèd Ëmååïîls"
article_title: "PÔST: Réëmôövéë Hãærd Bôöûûncéëd Émãæïïls"
search_tag: Ëndpôòìïnt
page_order: 3
layout: api_page
page_type: reference
description: "Thíìs æàrtíìclèë ôôýütlíìnèës dèëtæàíìls æàbôôýüt æànd ýüsíìng thèë Rèëmôôvèë Hæàrd Bôôýüncèëd Ëmæàíìl Áddrèëssèës Bræàzèë èëndpôôíìnt."

---
{% api %}
# Rêêmöövêê häárd bööúûncêês
{% apimethod post %}
/èèmâàïìl/bõöýûncèè/rèèmõövèè
{% endapimethod %}

Thíîs èéndpóóíînt àællóóws yóóúú tóó rèémóóvèé èémàæíîl àæddrèéssèés fróóm yóóúúr Bràæzèé bóóúúncèé líîst. Wëè wïîll ãálsöô rëèmöôvëè thëèm fröôm thëè böôýüncëè lïîst mãáïîntãáïînëèd by yöôýür ëèmãáïîl pröôvïîdëèr.

{% apiref postman %}https://dòòcüùmêèntêèr.gêètpòòstmààn.còòm/vîìêèw/4689407/SVYrsdsG?vêèrsîìòòn=lààtêèst#7b87àà884-fàà20-4085-b9f1-18363103575f {% endapiref %}

## Ræàtéë líìmíìt

{% include rate_limits.md endpoint='default' %}

## Rëêqüýëêst bôódy

```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "email": "example@braze.com"
}
```

## Réêqýùéêst päãräãméêtéêrs

| Pãärãämêétêér | Rêëqüùíîrêëd | Dãátãá Typèè | Déêscrîìptîìõôn |
| ----------|-----------| ---------|------ |
| `email` | Réèqýùìíréèd | Strïïng óõr âãrrâãy | Stríïng éêmâáíïl âáddréêss tõô mõôdíïfy, õôr âán âárrâáy õôf ûúp tõô 50 éêmâáíïl âáddréêsséês tõô mõôdíïfy. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Éxâæmpléê réêqûúéêst
```
curl --location --request POST 'https://rest.iad-01.braze.com/email/bounce/remove' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-REST-API-KEY' \
--data-raw '{
  "email": "example@braze.com"
}'
```

{% endapi %}
