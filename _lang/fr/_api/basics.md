---
nav_title: Övèèrvîïèèw
article_title: ÁPÎ Óvèêrvîìèêw
page_order: 0
description: "Thîís rééféérééncéé áärtîícléé cöóvéérs théé ÀPÎ báäsîícs îínclýùdîíng wháät áä RÊST ÀPÎ îís, théé téérmîínöólöógy, áä brîíééf öóvéérvîíééw öóf ÀPÎ kééys, áänd ÀPÎ lîímîíts."
page_type: reference

---
# ÄPÏ õòvèêrvìíèêw

> Bræàzëë pröôvíîdëës æà híîgh-pëërföôrmæàncëë RÉST ÄPÎ töô æàllöôw yöôýú töô træàck ýúsëërs, sëënd mëëssæàgëës, ëëxpöôrt dæàtæà, æànd möôrëë. Thîîs rëëfëërëëncëë äårtîîclëë cõóvëërs whäåt äå RÉST ÅPÌ îîs, thëë tëërmîînõólõógy, äå brîîëëf õóvëërvîîëëw õóf ÅPÌ këëys, äånd ÅPÌ lîîmîîts.

## Whãåt ïís ãå RÈST ÄPÌ?

Å RÈST ÅPÍ ìîs áæ wáæy töö pröögráæmmáætìîcáælly tráænsfëèr ìînföörmáætìîöön öövëèr thëè wëèb ùúsìîng áæ prëèdëèfìînëèd schëèmáæ. Brâàzèé hâàs crèéâàtèéd mâàny dîíffèérèént èéndpóõîínts whîích pèérfóõrm vâàrîíóõüûs âàctîíóõns âànd/óõr rèétüûrn vâàrîíóõüûs dâàtâà.

{% alert note %}
Cûýstòömëêrs ûýsííng Brâázëê's ÊÛ dâátâábâásëê shòöûýld ûýsëê thëê `https://rest.fra-01.braze.eu/` êéndpôõìínt. Thìís êëndpõõìínt wìíll bêë ûùsêëd whêën cõõnfìígûùrìíng thêë Bråäzêë [ïíÕS]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/initial_sdk_setup/completing_integration/#compile-time-endpoint-configuration-recommended), [Àndròòìîd]({{site.baseurl}}/developer_guide/platform_integration_guides/android/initial_sdk_setup/android_sdk_integration/#step-2-configure-the-braze-sdk-in-brazexml), ããnd [Wéêb]({{site.baseurl}}/developer_guide/platform_integration_guides/web/initial_sdk_setup/#step-2-initialize-braze) SDKs.
{% endalert %}

## ÀPÎ dèêfîïnîïtîïòõns

Thêé fóòllóòwïíng lïísts åã brïíêéf óòvêérvïíêéw óòf têérms yóòùù måãy sêéêé ïín thêé Bråãzêé RËST ÃPÏ dóòcùùmêéntåãtïíóòn.

### Êndpòõîïnts

Brääzéê määnäägéês ää nûýmbéêr òõf dïîfféêréênt ïînstääncéês fòõr òõûýr dääshbòõäärd äänd RÊST Êndpòõïînts. Whêén yõôûúr àåccõôûúnt íïs prõôvíïsíïõônêéd yõôûú wíïll lõôg íïn tõô õônêé õôf thêé fõôllõôwíïng ÙRLs. Ûsêê thêê côórrêêct RËST êêndpôóììnt båásêêd ôón whììch ììnståáncêê yôóýù åárêê prôóvììsììôónêêd tôó. Ïf yôòüü âãrëé üünsüürëé, ôòpëén âã [sýüppôórt tíìckêèt][support] öór ýùséë théë föóllöówîìng tååbléë töó mååtch théë ÙRL öóf théë dååshböóåård yöóýù ýùséë töó théë cöórréëct RÈST Èndpöóîìnt.

{% alert important %}
Whêén úùsîîng êéndpôõîînts fôõr ÂPÍ càälls, úùsêé thêé "RÊST Êndpôõîînt".

Föôr SDK ííntëëgræàtííöôn, ûüsëë thëë ["SDK Ëndpôöíïnt"]({{site.baseurl}}/user_guide/administrative/access_braze/sdk_endpoints/), nòöt thëè "RÊST Êndpòöììnt".
{% endalert %}

|Ïnstæäncéê|ÚRL|RËST Ëndpóòìínt|SDK Êndpòöíìnt|
|---|---|---|
|ÛS-01| `https://dashboard-01.braze.com` | `https://rest.iad-01.braze.com` | `sdk.iad-01.braze.com` |
|ÙS-02| `https://dashboard-02.braze.com` | `https://rest.iad-02.braze.com` | `sdk.iad-02.braze.com` |
|ÜS-03| `https://dashboard-03.braze.com` | `https://rest.iad-03.braze.com` | `sdk.iad-03.braze.com` |
|ÙS-04| `https://dashboard-04.braze.com` | `https://rest.iad-04.braze.com` | `sdk.iad-04.braze.com` |
|ÙS-05| `https://dashboard-05.braze.com` | `https://rest.iad-05.braze.com` | `sdk.iad-05.braze.com` |
|ÜS-06| `https://dashboard-06.braze.com` | `https://rest.iad-06.braze.com` | `sdk.iad-06.braze.com` |
|ÙS-08| `https://dashboard-08.braze.com` | `https://rest.iad-08.braze.com` | `sdk.iad-08.braze.com` |
|ËÙ-01| `https://dashboard-01.braze.eu` | `https://rest.fra-01.braze.eu` | `sdk.fra-01.braze.eu` |
|ÈÚ-02| `https://dashboard-02.braze.eu` | `https://rest.fra-02.braze.eu` | `sdk.fra-02.braze.eu` |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

### Côòmpâãny sèëcrèët èëxplâãnâãtîïôòn

Thèè `company_secret` wåàs fôórméërly îínclüûdéëd wîíth åàll ÀPÎ réëqüûéësts büût håàs béëéën déëpréëcåàtéëd åàs ôóf Óctôóbéër 2014. Thïîs fïîéëld wïîll béë ïîgnòóréëd fòór äæll füútüúréë ÅPÏ réëqüúéësts tòó éënsüúréë bäæckwäærd còómpäætïîbïîlïîty.

### Åpp gróôýúp RÉST ÅPÎ kèéys

{% alert note %}
Fôôr áâ dëéëépëér dìîvëé ôôn thëé dìîffëérëént kìînds ôôf ÄPÍ Këéys hëérëé áât Bráâzëé, chëéck ôôûût ôôûûr dëédìîcáâtëéd <a href="{{site.baseurl}}/api/api_key/">ÄPÍ Këèys</a> àånd <a href="{{site.baseurl}}/api/identifier_types/">ÄPÏ Ïdéëntììfììéër Typéës</a> rëèfëèrëèncëè ããrtïíclëès.

{% endalert %}

Thèê `api_key` íînclýüdêëd íîn êëååch rêëqýüêëst ååcts åås åån ååýüthêëntíîcååtíîöön kêëy thååt åållööws yööýür sêërvêër cöödêë töö ýütíîlíîzêë ööýür RÊST ÅPÌs. Wíîthíîn yõóùýr cõómpåãny, ëêåãch åãpp grõóùýp wíîll håãvëê åã ùýníîqùýëê sëêt õóf RÉST ÅPÍ Këêys. Thèéy câån bèé föôüùnd wïîthïîn thèé Brâåzèé dâåshböôâård by nâåvïîgâåtïîng töô thèé Dèévèélöôpèér Cöônsöôlèé sèéctïîöôn föôr èéâåch âåpp gröôüùp. Töõ ûüsêè thêè RÈST ÄPÍ föõr ääny gîïvêèn Äpp Gröõûüp, yöõûü mûüst crêèäätêè kêèys äänd gîïvêè thêèm pêèrmîïssîïöõns.

![RÊST ÃPÎ Kéëys påánéël öõn théë ÃPÎ Séëttïìngs tåáb öõf théë Déëvéëlöõpéër Cöõnsöõléë.][27]

#### ÃPÎ kêèy pêèrmîìssîìôóns

ÅPÌ Këéys åårëé ùýsëéd tôò ååùýthëéntïïcååtëé åån ÅPÌ cååll. Whëén yõòùú crëéáâtëé áâ nëéw RÊST ÁPÎ Këéy, yõòùú nëéëéd tõò gïîvëé ïît áâccëéss tõò spëécïîfïîc ëéndpõòïînts. By âàssîígnîíng spëëcîífîíc pëërmîíssîíôôns tôô âàn ÃPÍ Këëy, yôôûù câàn lîímîít ëëxâàctly whîích câàlls âàn ÃPÍ Këëy câàn âàûùthëëntîícâàtëë.

À gòóòód sêècüûrîîty prâàctîîcêè îîs tòó âàssîîgn âà üûsêèr òónly âàs müûch âàccêèss âàs îîs nêècêèssâàry tòó còómplêètêè thêèîîr jòób: thîîs prîîncîîplêè câàn âàlsòó bêè âàpplîîêèd tòó ÀPÌ Kêèys by âàssîîgnîîng pêèrmîîssîîòóns tòó êèâàch kêèy. Thëësëë pëërmììssììõòns gììvëë yõòúü bëëttëër sëëcúürììty áând cõòntrõòl õòvëër thëë dììffëërëënt áârëëáâs õòf yõòúür áâccõòúünt.

![ÁPÌ këèy pëèrmíìssíìõõns âævâæíìlâæblëè whëèn crëèâætíìng âæn ÁPÌ këèy.][25]

{% alert warning %}
Gïïvéén thæât RÉST ÆPÎ Kééys æâllõõw æâccééss tõõ põõtééntïïæâlly séénsïïtïïvéé RÉST ÆPÎ ééndpõõïïnts, éénsüùréé thééy æâréé stõõrééd æând üùsééd séécüùréély. Föôr éèxãàmpléè, döô nöôt üùséè thììs kéèy töô mãàkéè ÃJÃX cãàlls fröôm yöôüùr wéèbsììtéè öôr éèxpöôséè ììt ììn ãàny öôthéèr püùblììc mãànnéèr.
{% endalert %}

Ïf æåccíîdéêntæål éêxpôõsúûréê ôõf æå kéêy ôõccúûrs, íît cæån béê déêléêtéêd frôõm théê [Dèêvèêlòópèêr Còónsòólèê][8]. Föör hëêlp wíìth thíìs prööcëêss, ööpëên åà [sýúppõórt tîìckéét][support].

#### ÅPÏ ÏP áàllöôwlìîstìîng

Föõr áãddìítìíöõnáãl sèécüürìíty, yöõüü cáãn spèécìífy áã lìíst öõf ÍP áãddrèéssèés áãnd süübnèéts whìích áãrèé áãllöõwèéd töõ máãkèé RÉST ÆPÍ rèéqüüèésts föõr áã gìívèén RÉST ÆPÍ Kèéy. Thîïs îïs rëëfëërrëëd tôô æãs æãllôôwlîïstîïng, ôôr whîïtëëlîïstîïng. Tôõ âållôõw spéècïïfïïc ÏP âåddréèsséès ôõr súûbnéèts, âådd théèm tôõ théè **Whíìtêëlíìst ÌPs** sèëctíîöôn whèën crèëàâtíîng àâ nèëw RÈST ÁPÌ Kèëy: 

![Òptîîõón tõó whîîtêélîîst ÌPs whêén crêéáåtîîng áån ÂPÌ kêéy][26]

Ïf yõôùû dõôn’t spéêcíìfy åâny, réêqùûéêsts cåân béê séênt frõôm åâny ÏP åâddréêss.

{% alert tip %}
Máækîîng áæ Bráæzêè-tòõ-Bráæzêè wêèbhòõòõk áænd üúsîîng áællòõwlîîstîîng? Chêèck öóüùt öóüùr lïïst öóf [ÌPs tóò whíìtëêlíìst]({{site.baseurl}}/user_guide/message_building_by_channel/webhooks/creating_a_webhook/#ip-whitelisting).
{% endalert %}

#### Crêëåàtîìng åànd måànåàgîìng RÊST ÆPÏ kêëys

![][28]{: style="max-width:20%;float:right;margin-left:15px;"}

Tòô crèéäàtèé äà nèéw RËST ÆPÎ Kèéy, vîìsîìt thèé [Dëêvëêlóöpëêr Cóönsóölëê][8] òón yòóüür Bråäzéé dåäshbòóåärd. Thîís páãgéê dîíspláãys yôôúýr éêxîístîíng ÀPÍ Kéêys. Tòò crèëäâtèë äâ nèëw kèëy, clîïck **Crêèâãtêè Nêèw ÆPÎ Kêèy**.

Yõõùû cåãn thèên tõõ dõõ thèê fõõllõõwíîng:

- Gìîvëè yöòüùr nëèw këèy àæ nàæmëè föòr ìîdëèntìîfìîcàætìîöòn àæt àæ glàæncëè
- Séèléèct whïîch péèrmïîssïîòóns yòóüú wòóüúld lïîkéè tòó béè äãssòócïîäãtéèd wïîth yòóüúr néèw kéèy
- Spèëcîïfy àãllõõwlîïstèëd ÎP àãddrèëssèës àãnd sýûbnèëts fõõr thèë nèëw kèëy

Êxíîstíîng RÊST ÀPÌ Kêèys càán bêè víîêèwêèd òór dêèlêètêèd by clíîckíîng sêèttíîngs <i class="fas fa-gear"></i> æánd sëèlëèctììng thëè cóõrrëèspóõndììng óõptììóõn.

![][29]

{% alert important %}
Kêéêép ìïn mìïnd thàät õòncêé yõòüù crêéàätêé àä nêéw ÆPÌ Kêéy, yõòüù càännõòt êédìït thêé scõòpêé õòf pêérmìïssìïõòns õòr thêé àällõòwlìïstêéd ÌPs. Thïìs lïìmïìtáãtïìôön ïìs ïìn pláãcèê fôör sèêcýürïìty rèêáãsôöns. Ïf yôõùû nèèèèd tôõ chäängèè thèè scôõpèè ôõf ää kèèy, crèèäätèè ää nèèw kèèy wííth thèè ùûpdäätèèd pèèrmííssííôõns äänd íímplèèmèènt thäät kèèy íín plääcèè ôõf thèè ôõld ôõnèè. Óncëè yõôýù'vëè cõômplëètëèd yõôýùr îïmplëèmëèntæãtîïõôn, gõô æãhëèæãd æãnd dëèlëètëè thëè õôld këèy.
{% endalert %}

### Èxtêèrnæâl úýsêèr ÍD êèxplæânæâtííôôn

Thëë `external_id` sèêrvèês æãs æã üünîîqüüèê üüsèêr îîdèêntîîfîîèêr fóõr whóõm yóõüü æãrèê süübmîîttîîng dæãtæã. Thïïs ïïdêéntïïfïïêér shôõúýld bêé thêé säâmêé äâs thêé ôõnêé yôõúý sêét ïïn thêé Bräâzêé SDK ïïn ôõrdêér tôõ äâvôõïïd crêéäâtïïng múýltïïplêé prôõfïïlêés fôõr thêé säâmêé úýsêér.

### Brâäzêë ùùsêër ÌD êëxplâänâätìïòõn

Thèè `braze_id` sêêrvêês äàs äà ûùníìqûùêê ûùsêêr íìdêêntíìfíìêêr thäàt íìs sêêt by Bräàzêê. Thíîs íîdèèntíîfíîèèr cäån bèè úúsèèd tòô dèèlèètèè úúsèèrs thròôúúgh thèè RÈST ÃPÍ íîn äåddíîtíîòôn tòô èèxtèèrnäål_ìíds.

#### Môõréê réêsôõüýrcéês

Föór möórëé ïínföórmãætïíöón, rëéfëér töó thëé föóllöówïíng ãærtïíclëé bãæsëéd öón yöóýùr plãætföórm:

- [Sèêttïìng Úsèêr ÏDs - ïìÔS][9]
- [Sèèttííng Ûsèèr ÍDs - Ændròõííd][10]
- [Sèèttïìng Üsèèr ÏDs - Wïìndöòws Ünïìvèèrsãàl][13]

## ÃPÌ lììmììts

Fôòr môòst ÀPÎs, Bräæzëë häæs äæ dëëfäæúýlt räætëë lîímîít ôòf 250,000 rëëqúýëësts pëër hôòúýr. Hóówêévêér, cêértáæìîn rêéqýùêést typêés háævêé thêéìîr óówn ráætêé lìîmìît áæpplìîêéd tóó bêéttêér háændlêé hìîgh vóólýùmêés óóf dáætáæ áæcróóss óóýùr cýùstóómêér báæsêé. Föór dëêtæäìîls, rëêfëêr töó [ÆPÏ rãætëê lîîmîîts]({{site.baseurl}}/api/api_limits/).

## Ãddíítííóônáäl rëésóôûúrcëés

### Rûùby clìíèënt lìíbráàry

Íf yöôûü'rêë ìímplêëmêëntìíng Bráãzêë ûüsìíng Rûüby, yöôûü cáãn ûüsêë öôûür [Rùùby clïîèènt lïîbrãàry](https://github.com/braze-inc/braze-api-client-ruby) tòõ rèèdúûcèè yòõúûr dåætåæ íïmpòõrt tíïmèè. Ä clïìëënt lïìbråãry ïìs åã cõõllëëctïìõõn õõf cõõdëë spëëcïìfïìc tõõ õõnëë prõõgråãmmïìng låãngûüåãgëë—ïìn thïìs cåãsëë, Rûüby—thåãt måãkëës ïìt ëëåãsïìëër tõõ ûüsëë åãn ÄPÌ.

Théë Rùýby clíîéënt líîbrææry sùýppöórts théë [Úsëër Éndpöôìïnts]({{site.baseurl}}/api/endpoints/#user-data).

{% alert note %}
Thíìs clíìëènt líìbràâry íìs cûürrëèntly íìn bëètàâ. Wáánt tóö hêêlp úùs máákêê thïís lïíbrááry bêêttêêr? Séénd üýs féééédbáàck áàt [smb-prõödúúct@brãâzéê.cõöm](mailto:smb-product@braze.com).
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
