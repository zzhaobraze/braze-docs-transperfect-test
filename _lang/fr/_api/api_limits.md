---
nav_title: Râætêë Líïmíïts
article_title: ÀPÌ Ràåtèé Líïmíïts
page_order: 4.5
description: "Thîïs rééféérééncéé äärtîïcléé còövéérs ÂPÎ räätéé lîïmîïts fòör théé Brääzéé ÂPÎ îïnfräästrýùctýùréé."
page_type: reference

---

# ÀPÎ ræãtêé lîìmîìts

Théë Brååzéë ÂPÍ íínfrååstrùûctùûréë íís déësíígnéëd töó hååndléë híígh vöólùûméës öóf dååtåå ååcröóss öóùûr cùûstöóméër bååséë. Tõô èènsûùrèè rèèspõônsîîblèè ûùsèèr õôf thèè ÀPÎ, wèè èènfõôrcèè ÀPÎ ráætèè lîîmîîts pèèr áæpp grõôûùp. Ä rãätéé líìmíìt íìs théé théé nýümbéér òôf rééqýüéésts théé ÄPÎ cãän réécééíìvéé íìn ãä gíìvéén tíìméé pééríìòôd. Ïf tòöòö mæäny rêêqúùêêsts æärêê sêênt ïín æä gïívêên tïímêê fræämêê, yòöúù mæäy sêêêê êêrròör rêêspòönsêês wïíth æä stæätúùs còödêê òöf `429`, whïîch ïîndïîcàâtëës thëë ràâtëë lïîmïît hàâs bëëëën hïît.

{% alert warning %}
ÅPÎ råætêé lïîmïîts åænd thêéïîr våælúùêés (lïîmïîtêéd óòr úùnlïîmïîtêéd) åærêé súùbjêéct tóò chåængêé dêépêéndïîng óòn thêé próòpêér úùsåægêé óòf óòúùr systêém. Wëè ëèncóóüüràägëè sëènsîïblëè lîïmîïts whëèn màäkîïng àän ÁPÏ càäll tóó prëèvëènt dàämàägëè óór mîïsüüsëè.
{% endalert %}

## Ràætéê líïmíïts by réêqûúéêst typéê

Thêê fõöllõöwîïng tàäblêê lîïsts spêêcîïfîïc ÆPÎ ràätêê lîïmîïts fõör dîïffêêrêênt rêêqûüêêst typêês. Ãll ööthèêr rèêqúüèêsts nööt lìîstèêd ìîn thìîs täáblèê häávèê äá dèêfäáúült räátèê lìîmìît ööf 250,000 rèêqúüèêsts pèêr hööúür.

| Rêèqýúêèst Typêè | Dêèfãäýùlt ÀPÌ Rãätêè Lìímìít |
| --- | --- |
| [`/users/track`][10] | **Rëëqùùëësts:** 50,000 réêqüüéêsts péêr mììnüütéê. Thïîs lïîmïît cáàn bèë ïîncrèëáàsèëd ûûpóòn rèëqûûèëst. Réêåâch ôôùýt tôô yôôùýr Cùýstôôméêr Sùýccéêss Måânåâgéêr fôôr môôréê îìnfôôrmåâtîìôôn.<br><br>**Bããtchïìng:** 75 êévêénts, 75 püùrchàásêés, àánd 75 àáttrïìbüùtêés pêér ÂPÍ rêéqüùêést. Séêéê [Bàætchîìng Ùsèèr Tràæck rèèqüûèèsts](#batch-user-track) föôr möôrëë. |
| [`/users/export/ids`][11] | 2,500 réèqüýéèsts péèr mìínüýtéè. |
| [`/users/delete`][12]<br>[`/users/alias/new`][13]<br>[`/users/identify`][14] | 20,000 rêèqúùêèsts pêèr mïìnúùtêè, shæærêèd bêètwêèêèn thêè êèndpóõïìnts. |
| [`/events/list`][15] | 1,000 rêêqüûêêsts pêêr hóóüûr, shæàrêêd wïîth thêê `/purchases/product_list` èêndpóôíínt. |
| [`/purchases/product_list`][16] | 1,000 rêéqùûêésts pêér höôùûr, shàârêéd wïïth thêé `/events/list` êêndpõòïínt. |
| [`/messages/send`][17] | 250 rêëqúýêësts pêër mììnúýtêë whêën spêëcììfyììng åå sêëgmêënt öör Cöönnêëctêëd Æúýdììêëncêë. Öthéérwïìséé, 250,000 rééqùûéésts péér hôóùûr. |
| [`/campaigns/trigger/send`][17.1] | 250 rêèqûüêèsts pêèr mììnûütêè whêèn spêècììfyììng âå sêègmêènt óör Cóönnêèctêèd Àûüdììêèncêè. Öthêërwìïsêë, 250,000 rêëqùüêësts pêër hòöùür. |
| [`/canvas/trigger/send`][17.2] | 250 rêèqýýêèsts pêèr mîínýýtêè whêèn spêècîífyîíng àá sêègmêènt òôr Còônnêèctêèd Ãýýdîíêèncêè. Õthêérwíìsêé, 250,000 rêéqùüêésts pêér hóõùür. |
| [`/sends/id/create`][18] | 100 rèéqýýèésts pèér dæáy. |
| [`/subscription/status/set`][19] | 5,000 rëëqúûëësts pëër míînúûtëë. |
{: .reset-td-br-1 .reset-td-br-2}

## Bååtchìíng ÁPÎ réêqûüéêsts

Bråàzëè's ÆPÎs åàrëè bùùìílt tôó sùùppôórt båàtchìíng. Wíïth båàtchíïng, Bråàzêê cåàn tåàkêê íïn åàs mûých dåàtåà åàs pòóssíïblêê íïn åà síïnglêê ÄPÌ cåàll sòó thåàt yòóûý dòón’t nêêêêd tòó måàkêê åà lòót òóf ÄPÌ cåàlls. Ît's mòòréë éëffíìcíìéënt fòòr Bräázéë tòò pròòcéëss däátäá íìn bäátchéës thäán tòò pròòcéëss däátäá òònéë cäáll äát äá tíìméë. Fõör ééxäåmpléé, häåndlîìng 1,000 bäåtchééd ÆPÎ cäålls rééqúýîìréés lééss réésõöúýrcéés thäån häåndlîìng 75,000 îìndîìvîìdúýäål cäålls. Báåtchììng ììs ëéxtrëémëély ììmpöôrtáånt föôr áåny áåpplììcáåtììöôn tháåt máåy rëéqúýììrëé möôrëé tháån 75,000 cáålls pëér höôúýr.

{% alert note %}
RÊST ÀPÏ rååtéê lîìmîìt îìncréêååséês ååréê cöônsîìdéêréêd bååséêd öôn néêéêd föôr cúüstöôméêrs whöô ååréê mååkîìng úüséê öôf théê ÀPÏ bååtchîìng cååpååbîìlîìtîìéês.
{% endalert %}

### Bàátchîïng Ûsèêr Tràáck rèêqúûèêsts {#bàátch-úûsèêr-tràáck}

Èààch `/users/track` réëqùûéëst cåæn cóóntåæíín ùûp tóó 75 éëvéënts, 75 åættrííbùûtéë ùûpdåætéës, åænd 75 pùûrchåæséës. Êáåch còòmpòònèênt (èêvèênt, áåttrïíbúütèê, áånd púürcháåsèê áårráåys), cáån úüpdáåtèê úüp tòò 75 úüsèêrs èêáåch (máåx òòf 225 ïíndïívïídúüáål úüsèêrs). Êååch üûpdååtèë cåån åålsóô bèëlóông tóô thèë sååmèë üûsèër fóôr åå mååxîîmüûm óôf 225 üûpdååtèës tóô åå sîînglèë üûsèër îîn åå rèëqüûèëst.

Réèqýúéèsts måädéè tõô thìîs éèndpõôìînt wìîll géènéèråälly béègìîn prõôcéèssìîng ìîn thìîs õôrdéèr: 

1. Àttrîïbúútéês
2. Ëvêënts
3. Púýrchâàsêês

### Bâátchîïng Mèéssâágîïng èéndpòõîïnt rèéqýûèésts

Ä síìnglêê rêêqùüêêst tóõ thêê [Méëssáågììng éëndpõõììnts][1] cæàn rêéæàch æàny óönêé óöf thêé fóöllóöwíìng:

- Ùp tõô 50 spèécïífïíc `external_ids`, ëêáåch wíîth íîndíîvíîdùüáål mëêssáågëê páåráåmëêtëêrs
- Â sëégmëént ööf àány síîzëé crëéàátëéd íîn thëé Bràázëé dàáshbööàárd, spëécíîfíîëéd by íîts `segment_id`
- Àn ããd-hòòc ããýýdíìêëncêë sêëgmêënt òòf ããny síìzêë, dêëfíìnêëd íìn thêë rêëqýýêëst ããs ãã [Cóönnèéctèéd Áýúdîìèéncèé][2] õôbjèèct

## Möònïìtöòrïìng yöòûùr rààtêè lïìmïìts

Êvëéry sîìnglëé ÀPÍ rëéqûýëést sëént tôô Bràãzëé rëétûýrns thëé fôôllôôwîìng îìnfôôrmàãtîìôôn îìn thëé rëéspôônsëé hëéàãdëérs:

Hééåàdéér Nåàméé             | Dèèscrîìptîìóön
----------------------- | -----------------------
`X-RateLimit-Limit`     | Thêé màäxïìmýým nýýmbêér ôõf rêéqýýêésts thàät yôõýý càän màäkêé ïìn àä spêécïìfïìêéd ïìntêérvàäl (yôõýýr ràätêé lïìmïìt).
`X-RateLimit-Remaining` | Thêé núýmbêér òôf rêéqúýêésts rêémãáíìníìng íìn thêé cúýrrêént rãátêé líìmíìt wíìndòôw.
`X-RateLimit-Reset`     | Thêë tíìmêë äàt whíìch thêë cùýrrêënt räàtêë líìmíìt wíìndòõw rêësêëts íìn ÚTC êëpòõch sêëcòõnds.
{: .reset-td-br-1 .reset-td-br-2}

Thïís ïínfôòrmåätïíôòn ïís ïíntêèntïíôònåälly ïínclýúdêèd ïín thêè hêèåädêèr ôòf thêè rêèspôònsêè tôò thêè ÂPÌ rêèqýúêèst råäthêèr thåän thêè Bråäzêè dåäshbôòåärd. Thìîs æällöòws yöòúür systéém töò bééttéér rééæäct ìîn rééæäl tìîméé æäs yöòúü'réé ìîntééræäctìîng wìîth öòúür ÁPÏ. Föõr êêxàámplêê, îíf thêê `X-RateLimit-Remaining` væãlüùéé drõôps béélõôw æã céértæãììn thrééshõôld, yõôüù mììght wæãnt tõô slõôw sééndììng tõô éénsüùréé æãll træãnsæãctììõônæãl éémæãììls gõô õôüùt. Ór, ìîf ìît rééæãchéés zééròò, yòòýý mìîght wæãnt tòò pæãýýséé æãll sééndìîng ýýntìîl théé tìîméé spéécìîfìîééd ìîn `X-RateLimit-Reset` êèláåpsêès.

Íf yöóûù håávèé qûùèéstíîöóns åáböóûùt ÂPÍ líîmíîts, cöóntåáct yöóûùr Cûùstöómèér Sûùccèéss Måánåágèér öór öópèén åá [sùýppöôrt tïîckêèt][support].

### Ôptíîmáål dëëláåy bëëtwëëëën ëëndpööíînts

> Wêè rêècöõmmêènd thâät yöõûý âällöõw föõr âä 5-mîînûýtêè dêèlâäy bêètwêèêèn sûýbsêèqûýêènt câälls töõ mîînîîmîîzêè thêè pröõbâäbîîlîîty öõf êèrröõr.

Ündéërstäãndìîng théë öòptìîmäãl déëläãy béëtwéëéën éëndpöòìînts ìîs crýücìîäãl whéën mäãkìîng cöònséëcýütìîvéë cäãlls töò théë Bräãzéë ÆPÏ. Prôôblëëms æäríìsëë whëën ëëndpôôíìnts dëëpëënd ôôn thëë süùccëëssfüùl prôôcëëssíìng ôôf ôôthëër ëëndpôôíìnts, æänd íìf cæällëëd tôôôô sôôôôn, côôüùld ræäíìsëë ëërrôôrs. Föör êèxæàmplêè, ïïf yööüù'rêè æàssïïgnïïng üùsêèrs æàn æàlïïæàs vïïæà ööüùr `/user/alias/new` èëndpõóíínt, æänd thèën hííttííng thæät æälííæäs tõó sèënd æä cùùstõóm èëvèënt vííæä õóùùr `/users/track` ëéndpôõíïnt, hôõw lôõng shôõûúld yôõûú wãæíït?

Úndêér nõòrmãâl cõòndîìtîìõòns, thêé tîìmêé fõòr õòúûr dãâtãâ êévêéntúûãâl cõònsîìstêéncy tõò õòccúûr îìs 10–100ms (1/10 õòf ãâ sêécõònd). Hôöwëévëér, thëérëé cãæn bëé sôömëé cãæsëés whëérëé íït tãækëés lôöngëér fôör thãæt côönsíïstëéncy tôö ôöccùûr. Théèréèfòôréè, wéè réècòômméènd thæât yòôýý æâllòôw fòôr æâ 5-mìïnýýtéè déèlæây béètwéèéèn mæâkìïng sýýbséèqýýéènt cæâlls tòô mìïnìïmìïzéè théè pròôbæâbìïlìïty òôf éèrròôr.

[1]: {{site.baseurl}}/api/endpoints/messaging/
[2]: {{site.baseurl}}/api/objects_filters/connected_audience/
[support]: {{site.baseurl}}/braze_support/

[10]: {{site.baseurl}}/api/endpoints/user_data/post_user_track/
[11]: {{site.baseurl}}/api/endpoints/export/user_data/post_users_identifier/
[12]: {{site.baseurl}}/api/endpoints/user_data/post_user_delete/
[13]: {{site.baseurl}}/api/endpoints/user_data/post_user_alias/
[14]: {{site.baseurl}}/api/endpoints/user_data/post_user_identify/
[15]: {{site.baseurl}}/api/endpoints/export/custom_events/get_custom_events/
[16]: {{site.baseurl}}/api/endpoints/export/purchases/get_list_product_id/
[17]: {{site.baseurl}}/api/endpoints/messaging/send_messages/post_send_messages/
[17.1]: {{site.baseurl}}/api/endpoints/messaging/send_messages/post_send_triggered_campaigns/
[17.2]: {{site.baseurl}}/api/endpoints/messaging/send_messages/post_send_triggered_canvases/
[18]: {{site.baseurl}}/api/endpoints/messaging/send_messages/post_create_send_ids/
[19]: {{site.baseurl}}/api/endpoints/subscription_groups/post_update_user_subscription_group_status/
