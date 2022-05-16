---
nav_title: Ôvëërvíïëëw
article_title: ÂPÌ Óvëêrvíïëêw
page_order: 0
description: "Thïïs rèéfèérèéncèé àårtïïclèé cõövèérs thèé ÄPÎ bàåsïïcs ïïnclùýdïïng whàåt àå RÈST ÄPÎ ïïs, thèé tèérmïïnõölõögy, àå brïïèéf õövèérvïïèéw õöf ÄPÎ kèéys, àånd ÄPÎ lïïmïïts."
page_type: reference

---
# ÀPÌ òôvëérvííëéw

> Bräåzéë próövïïdéës äå hïïgh-péërfóörmäåncéë RÉST ÀPÌ tóö äållóöw yóöûú tóö träåck ûúséërs, séënd méëssäågéës, éëxpóört däåtäå, äånd móöréë. Thïîs rêêfêêrêêncêê áärtïîclêê cóòvêêrs wháät áä RÉST ÅPÍ ïîs, thêê têêrmïînóòlóògy, áä brïîêêf óòvêêrvïîêêw óòf ÅPÍ kêêys, áänd ÅPÍ lïîmïîts.

## Whäæt ììs äæ RÉST ÀPÏ?

Å RÉST ÅPÎ îìs äà wäày tôõ prôõgräàmmäàtîìcäàlly träànsféêr îìnfôõrmäàtîìôõn ôõvéêr théê wéêb ùýsîìng äà préêdéêfîìnéêd schéêmäà. Bráázëé háás crëéáátëéd máány dîìffëérëént ëéndpõõîìnts whîìch pëérfõõrm váárîìõõûýs ááctîìõõns áánd/õõr rëétûýrn váárîìõõûýs dáátáá.

{% alert note %}
Cúýstõómêèrs úýsîïng Bráåzêè's ÊÙ dáåtáåbáåsêè shõóúýld úýsêè thêè `https://rest.fra-01.braze.eu/` ëèndpöõíînt. Thîïs éëndpòöîïnt wîïll béë üûséëd whéën còönfîïgüûrîïng théë Brææzéë [îìÔS]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/initial_sdk_setup/completing_integration/#compile-time-endpoint-configuration-recommended), [Ãndrõöîíd]({{site.baseurl}}/developer_guide/platform_integration_guides/android/initial_sdk_setup/android_sdk_integration/#step-2-configure-the-braze-sdk-in-brazexml), äänd [Wëèb]({{site.baseurl}}/developer_guide/platform_integration_guides/web/initial_sdk_setup/#step-2-initialize-braze) SDKs.
{% endalert %}

## ÄPÎ dèèfìínìítìíòöns

Thêê fóôllóôwîíng lîísts àá brîíêêf óôvêêrvîíêêw óôf têêrms yóôüý màáy sêêêê îín thêê Bràázêê RÈST ÁPÏ dóôcüýmêêntàátîíóôn.

### Ëndpõõïìnts

Bræäzèè mæänæägèès æä nüýmbèèr òõf díïffèèrèènt íïnstæäncèès fòõr òõüýr dæäshbòõæärd æänd RÈST Èndpòõíïnts. Whëèn yôõýúr ãåccôõýúnt ììs prôõvììsììôõnëèd yôõýú wììll lôõg ììn tôõ ôõnëè ôõf thëè fôõllôõwììng ÚRLs. Ûsèè thèè còòrrèèct RÊST èèndpòòìínt båæsèèd òòn whìích ìínståæncèè yòòúû åærèè pròòvìísìíòònèèd tòò. Îf yöòýý äårëê ýýnsýýrëê, öòpëên äå [sýûppóõrt tììckêêt][support] óôr úüsêë thêë fóôllóôwîïng tàâblêë tóô màâtch thêë ÚRL óôf thêë dàâshbóôàârd yóôúü úüsêë tóô thêë cóôrrêëct RÊST Êndpóôîïnt.

{% alert important %}
Whëên üýsìíng ëêndpõòìínts fõòr ÃPÍ càâlls, üýsëê thëê "RËST Ëndpõòìínt".

Fòör SDK ïïntèêgràåtïïòön, ýüsèê thèê ["SDK Éndpòõíînt"]({{site.baseurl}}/user_guide/administrative/access_braze/sdk_endpoints/), nöõt thêê "RÈST Èndpöõììnt".
{% endalert %}

|Ìnståäncëë|ÚRL|RÈST Èndpôòíînt|SDK Èndpöòîînt|
|---|---|---|
|ÚS-01| `https://dashboard-01.braze.com` | `https://rest.iad-01.braze.com` | `sdk.iad-01.braze.com` |
|ÛS-02| `https://dashboard-02.braze.com` | `https://rest.iad-02.braze.com` | `sdk.iad-02.braze.com` |
|ÚS-03| `https://dashboard-03.braze.com` | `https://rest.iad-03.braze.com` | `sdk.iad-03.braze.com` |
|ÛS-04| `https://dashboard-04.braze.com` | `https://rest.iad-04.braze.com` | `sdk.iad-04.braze.com` |
|ÜS-05| `https://dashboard-05.braze.com` | `https://rest.iad-05.braze.com` | `sdk.iad-05.braze.com` |
|ÚS-06| `https://dashboard-06.braze.com` | `https://rest.iad-06.braze.com` | `sdk.iad-06.braze.com` |
|ÚS-08| `https://dashboard-08.braze.com` | `https://rest.iad-08.braze.com` | `sdk.iad-08.braze.com` |
|ÊÜ-01| `https://dashboard-01.braze.eu` | `https://rest.fra-01.braze.eu` | `sdk.fra-01.braze.eu` |
|ÊÜ-02| `https://dashboard-02.braze.eu` | `https://rest.fra-02.braze.eu` | `sdk.fra-02.braze.eu` |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

### Cóömpæány sèëcrèët èëxplæánæátîìóön

Thèè `company_secret` wáäs fôôrmêèrly ïïnclüùdêèd wïïth áäll ÃPÎ rêèqüùêèsts büùt háäs bêèêèn dêèprêècáätêèd áäs ôôf Öctôôbêèr 2014. Thíîs fíîêêld wíîll bêê íîgnóórêêd fóór áæll fûütûürêê ÆPÌ rêêqûüêêsts tóó êênsûürêê báæckwáærd cóómpáætíîbíîlíîty.

### Ãpp grõôüùp RËST ÃPÍ kèêys

{% alert note %}
Fòôr âã dëëëëpëër dîîvëë òôn thëë dîîffëërëënt kîînds òôf ÆPÎ Këëys hëërëë âãt Brâãzëë, chëëck òôüût òôüûr dëëdîîcâãtëëd <âã hrëëf="{{site.baseurl}}/ãàpìí/ãàpìí_kèéy/">ÂPÍ Kèéys</a> âænd <âæ hrêëf="{{site.baseurl}}/ãåpíì/íìdêéntíìfíìêér_typëés/">ÀPÌ Ìdëéntíïfíïëér Typëés</a> rêéfêérêéncêé äårtìîclêés.

{% endalert %}

Théé `api_key` îínclûýdéèd îín éèàãch réèqûýéèst àãcts àãs àãn àãûýthéèntîícàãtîíòön kéèy thàãt àãllòöws yòöûýr séèrvéèr còödéè tòö ûýtîílîízéè òöûýr RÊST ÄPÏs. Wìïthìïn yöóüùr cöómpææny, éèææch ææpp gröóüùp wìïll hæævéè ææ üùnìïqüùéè séèt öóf RËST ÅPÎ Kéèys. Thèëy càân bèë fòòùýnd wîîthîîn thèë Bràâzèë dàâshbòòàârd by nàâvîîgàâtîîng tòò thèë Dèëvèëlòòpèër Còònsòòlèë sèëctîîòòn fòòr èëàâch àâpp gròòùýp. Tôô ýüsëë thëë RËST ÅPÏ fôôr ãäny gïïvëën Åpp Grôôýüp, yôôýü mýüst crëëãätëë këëys ãänd gïïvëë thëëm pëërmïïssïïôôns.

![RËST ÂPÏ Kêéys påãnêél óön thêé ÂPÏ Sêéttìîngs tåãb óöf thêé Dêévêélóöpêér Cóönsóölêé.][27]

#### ÆPÌ kêéy pêérmïïssïïòôns

ÃPÍ Kéêys åáréê ûýséêd tôô åáûýthéêntîìcåátéê åán ÃPÍ cåáll. Whéën yóöúü créëãâtéë ãâ néëw RÊST ÂPÍ Kéëy, yóöúü néëéëd tóö gíìvéë íìt ãâccéëss tóö spéëcíìfíìc éëndpóöíìnts. By æàssïígnïíng spëêcïífïíc pëêrmïíssïíõóns tõó æàn ÃPÍ Këêy, yõóûú cæàn lïímïít ëêxæàctly whïích cæàlls æàn ÃPÍ Këêy cæàn æàûúthëêntïícæàtëê.

Á gõóõód sëècüüríîty prââctíîcëè íîs tõó ââssíîgn ââ üüsëèr õónly ââs müüch ââccëèss ââs íîs nëècëèssââry tõó cõómplëètëè thëèíîr jõób: thíîs príîncíîplëè câân ââlsõó bëè ââpplíîëèd tõó ÁPÎ Këèys by ââssíîgníîng pëèrmíîssíîõóns tõó ëèââch këèy. Thêésêé pêérmïìssïìôôns gïìvêé yôôúü bêéttêér sêécúürïìty æànd côôntrôôl ôôvêér thêé dïìffêérêént æàrêéæàs ôôf yôôúür æàccôôúünt.

![ÅPÍ kéèy péèrmííssííõöns äæväæííläæbléè whéèn créèäætííng äæn ÅPÍ kéèy.][25]

{% alert warning %}
Gîìvëën thæàt RËST ÀPÍ Këëys æàllôów æàccëëss tôó pôótëëntîìæàlly sëënsîìtîìvëë RËST ÀPÍ ëëndpôóîìnts, ëënsûürëë thëëy æàrëë stôórëëd æànd ûüsëëd sëëcûürëëly. Fóôr ééxææmpléé, dóô nóôt ûúséé thíìs kééy tóô mæækéé ÃJÃX cæælls fróôm yóôûúr wéébsíìtéé óôr ééxpóôséé íìt íìn ææny óôthéér pûúblíìc mæænnéér.
{% endalert %}

Íf àáccìîdèêntàál èêxpõòsýùrèê õòf àá kèêy õòccýùrs, ìît càán bèê dèêlèêtèêd frõòm thèê [Dëévëélöópëér Cöónsöólëé][8]. Fóòr hèêlp wììth thììs próòcèêss, óòpèên äã [sýûppôört tïïckéêt][support].

#### ÃPÌ ÌP áàllöòwlïîstïîng

Fôõr æãddìîtìîôõnæãl sèêcùûrìîty, yôõùû cæãn spèêcìîfy æã lìîst ôõf ÌP æãddrèêssèês æãnd sùûbnèêts whìîch æãrèê æãllôõwèêd tôõ mæãkèê RÉST ÆPÌ rèêqùûèêsts fôõr æã gìîvèên RÉST ÆPÌ Kèêy. Thîìs îìs rêëfêërrêëd tòõ äãs äãllòõwlîìstîìng, òõr whîìtêëlîìstîìng. Tõó àãllõów spèécïìfïìc ÍP àãddrèéssèés õór süùbnèéts, àãdd thèém tõó thèé **Whïìtèèlïìst ÌPs** sèêctííóòn whèên crèêååtííng åå nèêw RÈST ÅPÎ Kèêy: 

![Ôptìîòòn tòò whìîtèëlìîst ÎPs whèën crèëàætìîng àæn ÅPÎ kèëy][26]

Íf yòóùû dòón’t spêëcïífy ààny, rêëqùûêësts cààn bêë sêënt fròóm ààny ÍP ààddrêëss.

{% alert tip %}
Máãkïïng áã Bráãzéê-tôò-Bráãzéê wéêbhôòôòk áãnd úýsïïng áãllôòwlïïstïïng? Chèëck õóýýt õóýýr lïìst õóf [ÌPs töó whîítèêlîíst]({{site.baseurl}}/user_guide/message_building_by_channel/webhooks/creating_a_webhook/#ip-whitelisting).
{% endalert %}

#### Crèêæàtïïng æànd mæànæàgïïng RÈST ÅPÏ kèêys

![][28]{: style="max-width:20%;float:right;margin-left:15px;"}

Töö crêëãätêë ãä nêëw RÈST ÄPÍ Kêëy, víìsíìt thêë [Dêèvêèlóõpêèr Cóõnsóõlêè][8] õòn yõòýùr Bræäzèè dæäshbõòæärd. Thíîs pããgéè díîsplããys yõöüúr éèxíîstíîng ÁPÎ Kéèys. Tõó crèéæätèé æä nèéw kèéy, clïíck **Crèêåátèê Nèêw ÄPÌ Kèêy**.

Yòóúù câân thèén tòó dòó thèé fòóllòówííng:

- Gíìvêè yòõúûr nêèw kêèy åá nåámêè fòõr íìdêèntíìfíìcåátíìòõn åát åá glåáncêè
- Séélééct whìích péérmìíssìíòõns yòõùú wòõùúld lìíkéé tòõ béé ãássòõcìíãátééd wìíth yòõùúr nééw kééy
- Spëècîìfy âællôôwlîìstëèd ÎP âæddrëèssëès âænd sûûbnëèts fôôr thëè nëèw këèy

Êxîìstîìng RÊST ÄPÍ Kéèys cãân béè vîìéèwéèd óòr déèléètéèd by clîìckîìng séèttîìngs <i class="fas fa-gear"></i> àând séëléëctíïng théë cõórréëspõóndíïng õóptíïõón.

![][29]

{% alert important %}
Kèêèêp îìn mîìnd thåàt ôóncèê yôóýý crèêåàtèê åà nèêw ÂPÌ Kèêy, yôóýý cåànnôót èêdîìt thèê scôópèê ôóf pèêrmîìssîìôóns ôór thèê åàllôówlîìstèêd ÌPs. Thîîs lîîmîîtæàtîîôõn îîs îîn plæàcéè fôõr séècüûrîîty réèæàsôõns. Îf yôôüý nèèèèd tôô chåångèè thèè scôôpèè ôôf åå kèèy, crèèååtèè åå nèèw kèèy wïìth thèè üýpdååtèèd pèèrmïìssïìôôns åånd ïìmplèèmèènt thååt kèèy ïìn plååcèè ôôf thèè ôôld ôônèè. Õncëë yöõýý'vëë cöõmplëëtëëd yöõýýr ìímplëëmëëntâàtìíöõn, göõ âàhëëâàd âànd dëëlëëtëë thëë öõld këëy.
{% endalert %}

### Èxtêérnãäl üûsêér ÏD êéxplãänãätìîóón

Théé `external_id` sëérvëés ääs ää ùünïïqùüëé ùüsëér ïïdëéntïïfïïëér fõôr whõôm yõôùü äärëé sùübmïïttïïng däätää. Thíìs íìdèëntíìfíìèër shöòúùld bèë thèë såãmèë åãs thèë öònèë yöòúù sèët íìn thèë Bråãzèë SDK íìn öòrdèër töò åãvöòíìd crèëåãtíìng múùltíìplèë pröòfíìlèës föòr thèë såãmèë úùsèër.

### Bräázéê ýýséêr ÏD éêxpläánäátìïöón

Thêê `braze_id` sèèrvèès ãås ãå ùúníïqùúèè ùúsèèr íïdèèntíïfíïèèr thãåt íïs sèèt by Brãåzèè. Thìís ìídêéntìífìíêér cåãn bêé ûûsêéd tôô dêélêétêé ûûsêérs thrôôûûgh thêé RÉST ÂPÍ ìín åãddìítìíôôn tôô êéxtêérnåãl_îíds.

#### Môòrèë rèësôòýýrcèës

Fòòr mòòrêé ììnfòòrmâàtììòòn, rêéfêér tòò thêé fòòllòòwììng âàrtììclêé bâàsêéd òòn yòòûür plâàtfòòrm:

- [Sëêttíïng Üsëêr ÍDs - íïÔS][9]
- [Sêêttïìng Üsêêr ÍDs - Åndrõõïìd][10]
- [Sèëttîîng Ùsèër ÌDs - Wîîndöóws Ùnîîvèërsääl][13]

## ÃPÎ lîìmîìts

Föór möóst ÀPÎs, Brâäzêè hâäs âä dêèfâäûúlt râätêè líïmíït öóf 250,000 rêèqûúêèsts pêèr höóûúr. Hôöwéévéér, céértãàíín rééqüúéést typéés hãàvéé thééíír ôöwn rãàtéé líímíít ãàpplííééd tôö bééttéér hãàndléé híígh vôölüúméés ôöf dãàtãà ãàcrôöss ôöüúr cüústôöméér bãàséé. Föôr dèétäæïîls, rèéfèér töô [ÁPÍ ráàtëè lììmììts]({{site.baseurl}}/api/api_limits/).

## Ãddîïtîïôönâål réésôöùürcéés

### Rûüby clìíéênt lìíbråáry

Îf yöóùù'rêê íìmplêêmêêntíìng Brãázêê ùùsíìng Rùùby, yöóùù cãán ùùsêê öóùùr [Rùýby clíìèént líìbråàry](https://github.com/braze-inc/braze-api-client-ruby) tôõ rêédýýcêé yôõýýr dàãtàã íímpôõrt tíímêé. Ã clîîéènt lîîbrãáry îîs ãá cõólléèctîîõón õóf cõódéè spéècîîfîîc tõó õónéè prõógrãámmîîng lãángüùãágéè—îîn thîîs cãáséè, Rüùby—thãát mãákéès îît éèãásîîéèr tõó üùséè ãán ÃPÎ.

Thèê Rùýby clììèênt lììbræâry sùýppôörts thèê [Üsèér Éndpóòïînts]({{site.baseurl}}/api/endpoints/#user-data).

{% alert note %}
Thíìs clíìêênt líìbräáry íìs cýùrrêêntly íìn bêêtäá. Wãånt tôõ hèèlp ûüs mãåkèè thîìs lîìbrãåry bèèttèèr? Séènd úüs féèéèdbâäck âät [smb-prõòdûûct@bråãzêè.cõòm](mailto:smb-product@braze.com).
{% endalert %}

[1]: https://en.wikipedia.org/wiki/UTF-8
[7]: {{site.baseurl}}/api/objects_filters/connected_audience/
[8]: https://dashboard-01.braze.com/app_settings/developer_console/ "Developer Console"
[9]: {{site.baseurl}}/developer_guide/platform_integration_guides/ios/analytics/setting_user_ids/
[10]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/analytics/setting_user_ids/
[13]: {{site.baseurl}}/developer_guide/platform_integration_guides/windows_universal/analytics/setting_user_ids/#setting-user-ids
[support]: {{site.baseurl}}/braze_support/
[25]: {% image_buster /assets/img_archive/api-key-permissions.png %}
[26]: {% image_buster /assets/img_archive/api-key-ip-whitelisting.png %}
[27]: {% image_buster /assets/img_archive/rest-api-key.png %}
[28]: {% image_buster /assets/img_archive/create-new-key.png %}
[29]: {% image_buster /assets/img_archive/api-key-options.png %}
