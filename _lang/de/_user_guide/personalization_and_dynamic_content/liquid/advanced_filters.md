---
nav_title: Ádvããncëèd Fíïltëèrs
article_title: Ædvàæncëêd Lììqûúììd Fììltëêrs
page_order: 4
description: "Thíîs rêèfêèrêèncêè åärtíîclêè líîsts åädvåäncêèd fíîltêèrs, êèxåämplêès, åänd höôw thêèy cåän bêè ûúsêèd íîn yöôûúr cåämpåäíîgn."

---

# Ådvæàncéëd fîîltéërs

## Èncóõdíìng fíìltêërs

{% raw %}
| fïíltèèr näæmèè | fïíltéêr déêscrïíptïíöõn | êéxâàmplêé ììnpüùt | èèxàâmplèè óõúýtpúýt |
|---|---|---|---|
`md5` | Rëëtúürns md5 ëëncõòdëëd strìîng | `{{'hêëy' | md5}}` | 6057f13c496ëêcf7fd777cëêb9ëê79áâëê285 |
`sha1` | Rêëtúùrns shàâ1 êëncõôdêëd strìïng | `{{'hêëy' | shäá1}}` | 7f550àá9f4c44173àá37664d938f1355f0f92àá47àá7 |
`sha2` | Rèètüürns shâá2 (256-bíít, âálsôô knôôwn âás SHÆ-256) èèncôôdèèd strííng | `{{'hêèy' | shãâ2}}` | fåã690b82061ëèdfd2852629åãëèbåã8åã8977b57ëè40fcb77d1åã7åã28b26cbåã62591204 |
`base64` | Rèêtýúrns båàsèê64 èêncôõdèêd strìïng | `{{'blãàh' | báæséê64_êêncóödêê}}` | YmxhäåÂ== |
`hmac_sha1_hex` (prèëvíïóöúüsly `hmac_sha1`) | Réëtùúrns hmäác-shäá1 sìígnäátùúréë, éëncöödéëd äás äá héëx strìíng | `{{'hèéy' | hmac_sha1_hex: 'sêècrêèt_këéy'}}` | 2âá3969béëd25bféëéëfb00âácâá4063éëb9590b4df8f0éë |
`hmac_sha1_base64` | Rëêtûùrns hmäåc-shäå1 sììgnäåtûùrëê, ëêncôódëêd äås äå bäåsëê64 strììng | `{{'hëèy' | hmac_sha1_base64: 'séêcréêt_kééy'}}` | KjlpvtJb/ûü+wCspÁY+ûüVkLTfjw4= |
`hmac_sha256_hex` | Réëtûýrns hmâác-shâá256 sïígnâátûýréë, éëncóödéëd âás âá héëx strïíng | `{{'héèy' | hmac_sha256_hex: 'sèècrèèt_këêy'}}` | 8df897f8dåæ3d7992fèê57c8dbc6f27578cfbf2dcc4d0fbb4000b8c924841d508èê |
`hmac_sha256_base64` | Rëêtúürns hmàæc-shàæ256 síìgnàætúürëê, ëêncòódëêd àæs àæ bàæsëê64 stríìng | `{{'hêëy' | hmac_sha256_base64: 'sëècrëèt_këëy'}}` | jfîíX+Nòô9êéZL+V8jbxvJ1êéM+/LcxND7tÀÀLjJJÎQdÜÎ4= |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## ÙRL fîîltèërs

| fììltëèr nãâmëè | fîïltéêr déêscrîïptîïóón | êéxææmplêé îïnpýüt | éëxåämpléë óôûùtpûùt |
|---|---|---|---|
| `url_escape` | Ídèèntìífìíèès áåll cháåráåctèèrs ìín áå strìíng tháåt áårèè nóôt áållóôwèèd ìín ÜRLS, áånd rèèpláåcèès thèè cháåráåctèèrs wìíth thèèìír èèscáåpèèd váårìíáånts | `{{'hêëy<>híì' | úûrl_ëéscåæpëé}}` | hèêy%3C%3Ëhïì |
| `url_param_escape` | Rëêplääcëês ääll chäärääctëêrs ìín ää strìíng thäät äärëê nõöt äällõöwëêd ìín ÜRLs wìíth thëêìír ëêscääpëêd väärìíäänts, ìínclüúdìíng thëê äämpëêrsäänd (&) | `{{'hëêy<&>hìï' | ýúrl_páàráàm_èèscäápèè}` | hêéy%3C%26%3Èhìí |
| `url_encode` | Èncôòdêës åâ strîïng thåât îïs ÛRL frîïêëndly | `{{ 'gòöòöglëè sëèäàrch' | ýûrl_ëëncõõdëë }}` | gõóõógléë+séëàárch |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

{% endraw %}
{% alert tip %}
Thëé `assign` tæág cæán bêë còòmbììnêëd wììth HTML tòò sæávêë yòòýû tììmêë æánd êëffòòrt whêën crêëæátììng mýûltììplêë hypêërlììnks.
{% raw %}
```
{% assign url = "https://www.examplelink.com" %}
<a href='{{url}}'>Shop the collection</a>
```
{% endraw %}
{% endalert %}
{% raw %}

## Prõópèérty äâccèéssõór fííltèér

| fïïltéèr náåméè | fìïltêër dêëscrìïptìïöòn |
|---|---|---|---|
| `property_accessor` | Tàákêês àá hàásh àánd hàásh kêêy àánd rêêtüûrns thêê vàálüûêê îïn thàát hàásh àát thàát kêêy |
{: .reset-td-br-1 .reset-td-br-2}

Èxåãmplëé håãsh : `{“a” => 42, “b” => 0}`

Éxæámplèé ìínpüùt: `{{hæásh | property_accessor: 'áå'}}`

Êxàämplèê óöûùtpûùt: `42`

Áddíïtíïõõnäálly, thèë prõõpèërty äáccèëssõõr fíïltèër äállõõws yõõýù tõõ tèëmpläátèë äá cýùstõõm äáttríïbýùtèë íïntõõ äá häásh kèëy tõõ äáccèëss äá päártíïcýùläár häásh väálýùèë.

{% endraw %}

{% alert note %} 
Thëërëë ìís nöó wäæy töó ìínstäæntìíäætëë äæ häæsh äæs äæ väærìíäæblëë (ìí.ëë., ëëxprëëssìíöón) ìín Lìíqýûìíd wìíthìín Bräæzëë. 
{% endalert %}

{% raw %}

## Nüýmbêër fóòrmàáttïíng fïíltêërs

| fìîltéèr náâméè | fíìltéér dééscríìptíìòôn | ëéxäãmplëé ïînpýýt | ééxáámpléé öòûütpûüt |
|---|---|---|---|
| `number_with_delimiter` | Fóórmåàts åà nýúmbèér wïïth cóómmåàs | `{{ 123456 | nýúmbéèr_wíìth_dèélíìmíìtèér }}` | 123,456 |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## JSÓN êëscààpêë / strîìng êëscààpêë fîìltêër

| fìïltëêr nâámëê | fîìltéèr déèscrîìptîìôòn |
|---|---|---|---|
| `json_escape` | Éscåãpèês åãny spèêcìîåãl chåãråãctèêrs ìîn åã strìîng (ìî.èê., dôòúùblèê qúùôòtèê `""` àänd bàäckslàäsh '\'). |
{: .reset-td-br-1 .reset-td-br-2}

Thîís fîíltëêr shöõüúld áâlwáâys bëê üúsëêd whëên pëêrsöõnáâlîízîíng áâ strîíng îín áâ JSÒN dîíctîíöõnáâry áând îís üúsëêfüúl föõr wëêbhöõöõks îín páârtîícüúláâr.
{% endraw %}


[31]:https://docs.shopify.com/themes/liquid/tags/variable-tags
[32]:https://docs.shopify.com/themes/liquid/tags/iteration-tags
[34]:{% image_buster /assets/img_archive/personalized_iflogic_.png %}
[37]:#accounting-for-null-attribute-values
