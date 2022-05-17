---
nav_title: Ræætëè Lïímïíts
article_title: ÀPÏ Ræâtêë Lîìmîìts
page_order: 4.5
description: "Thìís rêèfêèrêèncêè åårtìíclêè cöõvêèrs ÅPÍ rååtêè lìímìíts föõr thêè Brååzêè ÅPÍ ìínfrååstrúýctúýrêè."
page_type: reference

---

# ÀPÍ rãätêê lììmììts

Thèë Bràãzèë ÁPÌ îînfràãstrùúctùúrèë îîs dèësîîgnèëd tòô hàãndlèë hîîgh vòôlùúmèës òôf dàãtàã àãcròôss òôùúr cùústòômèër bàãsèë. Tõô ëënsüýrëë rëëspõônsïìblëë üýsëër õôf thëë ÆPÍ, wëë ëënfõôrcëë ÆPÍ rãàtëë lïìmïìts pëër ãàpp grõôüýp. Â ráàtéè lììmììt ììs théè théè núûmbéèr ôöf réèqúûéèsts théè ÂPÏ cáàn réècéèììvéè ììn áà gììvéèn tììméè péèrììôöd. Íf tõôõô mååny réèqúýéèsts ååréè séènt ìïn åå gìïvéèn tìïméè frååméè, yõôúý mååy séèéè éèrrõôr réèspõônséès wìïth åå stååtúýs cõôdéè õôf `429`, whíích ííndíícäátéës théë räátéë líímíít häás béëéën híít.

{% alert warning %}
ÁPÍ ræätêë líímííts æänd thêëíír væälùùêës (líímíítêëd öör ùùnlíímíítêëd) æärêë sùùbjêëct töö chæängêë dêëpêëndííng öön thêë prööpêër ùùsæägêë ööf ööùùr systêëm. Wéé ééncòöùüræägéé séénsîïbléé lîïmîïts whéén mæäkîïng æän ÀPÌ cæäll tòö préévéént dæämæägéé òör mîïsùüséé.
{% endalert %}

## Ráátêè lîìmîìts by rêèqýùêèst typêè

Thëë fôöllôöwîíng täåblëë lîísts spëëcîífîíc ÂPÍ räåtëë lîímîíts fôör dîíffëërëënt rëëqýùëëst typëës. Âll ôöthèèr rèèqýûèèsts nôöt líîstèèd íîn thíîs táæblèè háævèè áæ dèèfáæýûlt ráætèè líîmíît ôöf 250,000 rèèqýûèèsts pèèr hôöýûr.

| Rééqýúéést Typéé | Dêèfåâüýlt ÃPÎ Råâtêè Lïïmïït |
| --- | --- |
| [`/users/track`][10] | **Rèéqýüèésts:** 50,000 rèèqùüèèsts pèèr míínùütèè. Thîìs lîìmîìt cäãn bèè îìncrèèäãsèèd úýpòôn rèèqúýèèst. Rèèââch ôöûút tôö yôöûúr Cûústôömèèr Sûúccèèss Mâânââgèèr fôör môörèè íìnfôörmââtíìôön.<br>
<br>
**Bâätchìîng:** 75 ëêvëênts, 75 pûùrchâásëês, âánd 75 âáttrîìbûùtëês pëêr ÁPÍ rëêqûùëêst. Sèëèë [Bààtchîîng Úséër Trààck réëqýýéësts](#batch-user-track) föör mööréê. |
| [`/users/export/ids`][11] | 2,500 rëéqùúëésts pëér mïïnùútëé. |
| [`/users/delete`][12]<br>[`/users/alias/new`][13]<br>[`/users/identify`][14] | 20,000 réêqúûéêsts péêr mììnúûtéê, shâáréêd béêtwéêéên théê éêndpòóììnts. |
| [`/events/list`][15] | 1,000 réëqüúéësts péër hóôüúr, shàäréëd wííth théë `/purchases/product_list` éèndpöóíïnt. |
| [`/purchases/product_list`][16] | 1,000 réêqýùéêsts péêr hóôýùr, shãæréêd wïîth théê `/events/list` èéndpòóïìnt. |
| [`/messages/send`][17] | 250 rèëqùüèësts pèër mïînùütèë whèën spèëcïîfyïîng ãá sèëgmèënt òôr Còônnèëctèëd Ãùüdïîèëncèë. Õthëérwíîsëé, 250,000 rëéqùúëésts pëér höôùúr. |
| [`/campaigns/trigger/send`][17.1] | 250 rèêqúûèêsts pèêr mïínúûtèê whèên spèêcïífyïíng âã sèêgmèênt ôõr Côõnnèêctèêd Âúûdïíèêncèê. Óthëërwìïsëë, 250,000 rëëqúúëësts pëër hòôúúr. |
| [`/canvas/trigger/send`][17.2] | 250 rêêqüýêêsts pêêr mîînüýtêê whêên spêêcîîfyîîng ãâ sêêgmêênt òòr Còònnêêctêêd Âüýdîîêêncêê. Ôthëérwíísëé, 250,000 rëéqûùëésts pëér hòóûùr. |
| [`/sends/id/create`][18] | 100 réêqúúéêsts péêr dæåy. |
| [`/subscription/status/set`][19] | 5,000 rèéqúùèésts pèér mìínúùtèé. |
{: .reset-td-br-1 .reset-td-br-2}

## Bãåtchïîng ÃPÌ réëqùüéësts

Bràæzèë's ÃPÎs àærèë búýïílt tóõ súýppóõrt bàætchïíng. Wííth båátchííng, Bråázèê cåán tåákèê íín åás mýúch dåátåá åás pöõssííblèê íín åá síínglèê ÁPÎ cåáll söõ thåát yöõýú döõn’t nèêèêd töõ måákèê åá löõt öõf ÁPÎ cåálls. Ìt's mòöréé ééffíïcíïéént fòör Brãàzéé tòö pròöcééss dãàtãà íïn bãàtchéés thãàn tòö pròöcééss dãàtãà òönéé cãàll ãàt ãà tíïméé. Fôòr êëxæämplêë, hæändlîìng 1,000 bæätchêëd ÅPÍ cæälls rêëqýýîìrêës lêëss rêësôòýýrcêës thæän hæändlîìng 75,000 îìndîìvîìdýýæäl cæälls. Bàætchïíng ïís éëxtréëméëly ïímpòòrtàænt fòòr àæny àæpplïícàætïíòòn thàæt màæy réëqúúïíréë mòòréë thàæn 75,000 càælls péër hòòúúr.

{% alert note %}
RÊST ÂPÌ råàtêè líímíít ííncrêèåàsêès åàrêè cõönsíídêèrêèd båàsêèd õön nêèêèd fõör cûýstõömêèrs whõö åàrêè måàkííng ûýsêè õöf thêè ÂPÌ båàtchííng cåàpåàbíílíítííêès.
{% endalert %}

### Bæätchììng Ùsëër Træäck rëëqýûëësts {#bæätch-ýûsëër-træäck}

Éâæch `/users/track` rëêqüýëêst cåàn cóôntåàíîn üýp tóô 75 ëêvëênts, 75 åàttríîbüýtëê üýpdåàtëês, åànd 75 püýrchåàsëês. Êåâch cóòmpóònéènt (éèvéènt, åâttrìïbùûtéè, åând pùûrchåâséè åârråâys), cåân ùûpdåâtéè ùûp tóò 75 ùûséèrs éèåâch (måâx óòf 225 ìïndìïvìïdùûåâl ùûséèrs). Èâàch ýüpdâàtéè câàn âàlsõõ béèlõõng tõõ théè sâàméè ýüséèr fõõr âà mâàxìïmýüm õõf 225 ýüpdâàtéès tõõ âà sìïngléè ýüséèr ìïn âà réèqýüéèst.

Rééqúüéésts màædéé tõö thíîs ééndpõöíînt wíîll géénééràælly béégíîn prõöcééssíîng íîn thíîs õördéér: 

1. Áttrïîbýùtèés
2. Èvëênts
3. Pýùrchääsëés

### Bãätchîìng Mêêssãägîìng êêndpõöîìnt rêêqýûêêsts

Ä síînglèë rèëqúùèëst tôö thèë [Mêëssàâgïîng êëndpóöïînts][1] cäæn rëèäæch äæny õõnëè õõf thëè fõõllõõwìíng:

- Üp töó 50 spèêcìífìíc `external_ids`, êéââch wìîth ìîndìîvìîdùùââl mêéssââgêé pâârââmêétêérs
- À sëègmëènt ôòf áåny sìïzëè crëèáåtëèd ìïn thëè Bráåzëè dáåshbôòáård, spëècìïfìïëèd by ìïts `segment_id`
- Ân åàd-höòc åàùüdïîéëncéë séëgméënt öòf åàny sïîzéë, déëfïînéëd ïîn théë réëqùüéëst åàs åà [Côònnêèctêèd Äýüdììêèncêè][2] óõbjëëct

## Môõnïìtôõrïìng yôõýür räátèè lïìmïìts

Èvèèry síìnglèè ÄPÌ rèèqüýèèst sèènt töõ Bräâzèè rèètüýrns thèè föõllöõwíìng íìnföõrmäâtíìöõn íìn thèè rèèspöõnsèè hèèäâdèèrs:

Hëèæädëèr Næämëè             | Dêêscrîîptîîòön
----------------------- | -----------------------
`X-RateLimit-Limit`     | Thèè máäxìïmýùm nýùmbèèr õóf rèèqýùèèsts tháät yõóýù cáän máäkèè ìïn áä spèècìïfìïèèd ìïntèèrváäl (yõóýùr ráätèè lìïmìït).
`X-RateLimit-Remaining` | Thêé nùúmbêér õöf rêéqùúêésts rêémáâïïnïïng ïïn thêé cùúrrêént ráâtêé lïïmïït wïïndõöw.
`X-RateLimit-Reset`     | Thëë tíímëë åät whíích thëë cúûrrëënt råätëë líímíít wííndôöw rëësëëts íín ÙTC ëëpôöch sëëcôönds.
{: .reset-td-br-1 .reset-td-br-2}

Thïïs ïïnfõórmäåtïïõón ïïs ïïntëëntïïõónäålly ïïnclûüdëëd ïïn thëë hëëäådëër õóf thëë rëëspõónsëë tõó thëë ÀPÌ rëëqûüëëst räåthëër thäån thëë Bräåzëë däåshbõóäård. Thîïs âãllóõws yóõùür systèém tóõ bèéttèér rèéâãct îïn rèéâãl tîïmèé âãs yóõùü'rèé îïntèérâãctîïng wîïth óõùür ÀPÍ. Fóôr êèxåämplêè, îìf thêè `X-RateLimit-Remaining` våãlýúèë dróòps bèëlóòw åã cèërtåãìïn thrèëshóòld, yóòýú mìïght wåãnt tóò slóòw sèëndìïng tóò èënsýúrèë åãll tråãnsåãctìïóònåãl èëmåãìïls góò óòýút. Ór, ìíf ìít réèâáchéès zéèrõó, yõóüû mìíght wâánt tõó pâáüûséè âáll séèndìíng üûntìíl théè tìíméè spéècìífìíéèd ìín `X-RateLimit-Reset` éélàäpséés.

Ïf yôöûú háãvëè qûúëèstííôöns áãbôöûút ÃPÏ líímííts, côöntáãct yôöûúr Cûústôömëèr Sûúccëèss Máãnáãgëèr ôör ôöpëèn áã [súýppòõrt tïïckéét][support].

### Óptïìmåäl dèëlåäy bèëtwèëèën èëndpòóïìnts

> Wèé rèécõómmèénd thåæt yõóùù åællõów fõór åæ 5-míïnùùtèé dèélåæy bèétwèéèén sùùbsèéqùùèént cåælls tõó míïníïmíïzèé thèé prõóbåæbíïlíïty õóf èérrõór.

Ùndêërstáândììng thêë òóptììmáâl dêëláây bêëtwêëêën êëndpòóììnts ììs crýûcììáâl whêën máâkììng còónsêëcýûtììvêë cáâlls tòó thêë Bráâzêë ÄPÎ. Prôòblêêms áårîîsêê whêên êêndpôòîînts dêêpêênd ôòn thêê sûùccêêssfûùl prôòcêêssîîng ôòf ôòthêêr êêndpôòîînts, áånd îîf cáållêêd tôòôò sôòôòn, côòûùld ráåîîsêê êêrrôòrs. Föõr êèxáãmplêè, íîf yöõýý'rêè áãssíîgníîng ýýsêèrs áãn áãlíîáãs víîáã öõýýr `/user/alias/new` èéndpôóîínt, àånd thèén hîíttîíng thàåt àålîíàås tôó sèénd àå cüústôóm èévèént vîíàå ôóüúr `/users/track` ééndpôóììnt, hôów lôóng shôóùüld yôóùü wæäììt?

Úndèér nõõrmæál cõõndîîtîîõõns, thèé tîîmèé fõõr õõýûr dæátæá èévèéntýûæál cõõnsîîstèéncy tõõ õõccýûr îîs 10–100ms (1/10 õõf æá sèécõõnd). Hõòwêëvêër, thêërêë cáân bêë sõòmêë cáâsêës whêërêë íît táâkêës lõòngêër fõòr tháât cõònsíîstêëncy tõò õòccùûr. Thèërèëföórèë, wèë rèëcöómmèënd thäât yöóùü äâllöów föór äâ 5-mïìnùütèë dèëläây bèëtwèëèën mäâkïìng sùübsèëqùüèënt cäâlls töó mïìnïìmïìzèë thèë pröóbäâbïìlïìty öóf èërröór.

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
