---
nav_title: Ådváàncèèd Fìîltèèrs
article_title: Ædvæåncëêd Líîqùùíîd Fíîltëêrs
page_order: 4
description: "Thïïs rëèfëèrëèncëè ãârtïïclëè lïïsts ãâdvãâncëèd fïïltëèrs, ëèxãâmplëès, ãând hòõw thëèy cãân bëè ùüsëèd ïïn yòõùür cãâmpãâïïgn."

---

# Âdvåãncëëd fîìltëërs

## Èncòõdîíng fîíltêèrs

{% raw %}
| fïìltêèr nåàmêè | fìíltêêr dêêscrìíptìíôón | ëèxãâmplëè ïìnpùýt | èëxæåmplèë òöúútpúút |
|---|---|---|---|
`md5` | Réétýûrns md5 ééncöõdééd strïîng | `{{'héêy' | md5}}` | 6057f13c496èëcf7fd777cèëb9èë79ãàèë285 |
`sha1` | Rëêtùûrns shãã1 ëêncòödëêd strììng | `{{'hëëy' | shãä1}}` | 7f550áã9f4c44173áã37664d938f1355f0f92áã47áã7 |
`sha2` | Rèêtýürns shäå2 (256-bìít, äålsôô knôôwn äås SHÀ-256) èêncôôdèêd strìíng | `{{'hèëy' | shââ2}}` | fàá690b82061éédfd2852629àáéébàá8àá8977b57éé40fcb77d1àá7àá28b26cbàá62591204 |
`base64` | Rëétüýrns bâåsëé64 ëéncòôdëéd stríïng | `{{'blâäh' | báãséê64_êéncóòdêé}}` | YmxhâàÃ== |
`hmac_sha1_hex` (préévîîöòûúsly `hmac_sha1`) | Rëëtúûrns hmâåc-shâå1 síîgnâåtúûrëë, ëëncôödëëd âås âå hëëx stríîng | `{{'hèêy' | hmac_sha1_hex: 'sèëcrèët_këéy'}}` | 2ãæ3969bêêd25bfêêêêfb00ãæcãæ4063êêb9590b4df8f0êê |
`hmac_sha1_base64` | Rêétúúrns hmâãc-shâã1 sìígnâãtúúrêé, êéncöòdêéd âãs âã bâãsêé64 strìíng | `{{'hëêy' | hmac_sha1_base64: 'séècréèt_kéëy'}}` | KjlpvtJb/üý+wCspÄY+üýVkLTfjw4= |
`hmac_sha256_hex` | Rèêtûürns hmâåc-shâå256 síïgnâåtûürèê, èêncòòdèêd âås âå hèêx stríïng | `{{'hèëy' | hmac_sha256_hex: 'séëcréët_kèëy'}}` | 8df897f8dâæ3d7992fêé57c8dbc6f27578cfbf2dcc4d0fbb4000b8c924841d508êé |
`hmac_sha256_base64` | Rêètúúrns hmäâc-shäâ256 sïìgnäâtúúrêè, êèncòôdêèd äâs äâ bäâsêè64 strïìng | `{{'hëêy' | hmac_sha256_base64: 'séëcréët_kèëy'}}` | jfííX+Nòõ9èëZL+V8jbxvJ1èëM+/LcxND7tÅÅLjJJÌQdÚÌ4= |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## ÙRL fïíltèêrs

| fîîltéêr nâãméê | fïíltëèr dëèscrïíptïíóön | ëëxæâmplëë ïïnpüýt | éêxáämpléê óöùûtpùût |
|---|---|---|---|
| `url_escape` | Ìdèèntïïfïïèès âáll châárâáctèèrs ïïn âá strïïng thâát âárèè nòõt âállòõwèèd ïïn ÛRLS, âánd rèèplâácèès thèè châárâáctèèrs wïïth thèèïïr èèscâápèèd vâárïïâánts | `{{'hêëy<>hìï' | ýùrl_éëscäæpéë}}` | hëéy%3C%3Èhîí |
| `url_param_escape` | Rêéplåãcêés åãll chåãråãctêérs íîn åã stríîng thåãt åãrêé nòôt åãllòôwêéd íîn ÙRLs wíîth thêéíîr êéscåãpêéd våãríîåãnts, íînclýùdíîng thêé åãmpêérsåãnd (&) | `{{'hëêy<&>híï' | úúrl_páãráãm_êêscãàpêê}` | hèéy%3C%26%3Èhíì |
| `url_encode` | Ëncöödéès åæ strïîng thåæt ïîs ÚRL frïîéèndly | `{{ 'gòôòôgléë séëáærch' | ýýrl_ëêncóõdëê }}` | gõòõòglëé+sëéåârch |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

{% endraw %}
{% alert tip %}
Thëè `assign` tãäg cãän béé côômbïìnééd wïìth HTML tôô sãävéé yôôúü tïìméé ãänd ééffôôrt whéén crééãätïìng múültïìpléé hypéérlïìnks.
{% raw %}
```
{% assign url = "https://www.examplelink.com" %}
<a href='{{url}}'>Shop the collection</a>
```
{% endraw %}
{% endalert %}
{% raw %}

## Prõópéérty âæccééssõór fïïltéér

| fíïltéêr nãáméê | fîîltèêr dèêscrîîptîîõön |
|---|---|---|---|
| `property_accessor` | Tãäkèës ãä hãäsh ãänd hãäsh kèëy ãänd rèëtýùrns thèë vãälýùèë îîn thãät hãäsh ãät thãät kèëy |
{: .reset-td-br-1 .reset-td-br-2}

Ëxåämpléê håäsh : `{“a” => 42, “b” => 0}`

Éxååmplêë íïnpûýt: `{{hååsh | property_accessor: 'àå'}}`

Èxäãmplëë ööüùtpüùt: `42`

Æddïîtïîõònäælly, thèë prõòpèërty äæccèëssõòr fïîltèër äællõòws yõòùù tõò tèëmpläætèë äæ cùùstõòm äættrïîbùùtèë ïîntõò äæ häæsh kèëy tõò äæccèëss äæ päærtïîcùùläær häæsh väælùùèë.

{% endraw %}

{% alert note %} 
Thêérêé ïís nòõ wâåy tòõ ïínstâåntïíâåtêé âå hâåsh âås âå vâårïíâåblêé (ïí.êé., êéxprêéssïíòõn) ïín Lïíqýûïíd wïíthïín Brâåzêé. 
{% endalert %}

{% raw %}

## Nüümbèër fõôrmäâttïíng fïíltèërs

| fìïltèêr näämèê | fïìltèër dèëscrïìptïìöôn | êêxàämplêê ìïnpûût | ëéxæàmplëé óôúýtpúýt |
|---|---|---|---|
| `number_with_delimiter` | Fòôrmààts àà nùùmbéêr wîìth còômmààs | `{{ 123456 | nýümbèêr_wïíth_dëèlíímíítëèr }}` | 123,456 |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## JSÔN ëèscæåpëè / strîîng ëèscæåpëè fîîltëèr

| fîïltèêr näàmèê | fííltéèr déèscrííptííòôn |
|---|---|---|---|
| `json_escape` | Èscààpéës ààny spéëcïíààl chààrààctéërs ïín àà strïíng (ïí.éë., dóôûûbléë qûûóôtéë `""` ãånd bãåckslãåsh '\'). |
{: .reset-td-br-1 .reset-td-br-2}

Thîís fîíltèèr shôòûüld æålwæåys bèè ûüsèèd whèèn pèèrsôònæålîízîíng æå strîíng îín æå JSÖN dîíctîíôònæåry æånd îís ûüsèèfûül fôòr wèèbhôòôòks îín pæårtîícûülæår.
{% endraw %}


[31]:https://docs.shopify.com/themes/liquid/tags/variable-tags
[32]:https://docs.shopify.com/themes/liquid/tags/iteration-tags
[34]:{% image_buster /assets/img_archive/personalized_iflogic_.png %}
[37]:#accounting-for-null-attribute-values
