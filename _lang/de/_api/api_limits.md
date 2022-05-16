---
nav_title: Råætèê Lîìmîìts
article_title: ÂPÏ Rãátèè Líìmíìts
page_order: 4.5
description: "Thíìs rèêfèêrèêncèê åærtíìclèê còövèêrs ÅPÌ råætèê líìmíìts fòör thèê Bråæzèê ÅPÌ íìnfråæstrüüctüürèê."
page_type: reference

---

# ÀPÌ räätèè lîîmîîts

Thêê Bråäzêê ÄPÌ îînfråästrúýctúýrêê îîs dêêsîîgnêêd töô håändlêê hîîgh vöôlúýmêês öôf dåätåä åäcröôss öôúýr cúýstöômêêr båäsêê. Tòô êënsûúrêë rêëspòônsïìblêë ûúsêër òôf thêë ÄPÎ, wêë êënfòôrcêë ÄPÎ rãåtêë lïìmïìts pêër ãåpp gròôûúp. À räâtêë lìïmìït ìïs thêë thêë nûûmbêër óóf rêëqûûêësts thêë ÀPÌ cäân rêëcêëìïvêë ìïn äâ gìïvêën tìïmêë pêërìïóód. Íf tóöóö måàny rëêqùùëêsts åàrëê sëênt ïín åà gïívëên tïímëê fråàmëê, yóöùù måày sëêëê ëêrróör rëêspóönsëês wïíth åà ståàtùùs cóödëê óöf `429`, whììch ììndììcæåtèès thèè ræåtèè lììmììt hæås bèèèèn hììt.

{% alert warning %}
ÅPÌ râätèê lìïmìïts âänd thèêìïr vâälúýèês (lìïmìïtèêd öór úýnlìïmìïtèêd) âärèê súýbjèêct töó châängèê dèêpèêndìïng öón thèê pröópèêr úýsâägèê öóf öóúýr systèêm. Wéë éëncóöýûrãágéë séënsíîbléë líîmíîts whéën mãákíîng ãán ÁPÌ cãáll tóö préëvéënt dãámãágéë óör míîsýûséë.
{% endalert %}

## Râãtêë lïìmïìts by rêëqüúêëst typêë

Thêè fôòllôòwîìng tåâblêè lîìsts spêècîìfîìc ÆPÌ råâtêè lîìmîìts fôòr dîìffêèrêènt rêèqüüêèst typêès. Ãll ööthèër rèëqûüèësts nööt lîîstèëd îîn thîîs tââblèë hââvèë ââ dèëfââûült rââtèë lîîmîît ööf 250,000 rèëqûüèësts pèër hööûür.

| Rêéqüüêést Typêé | Dêêfäåýúlt ÄPÏ Räåtêê Lìïmìït |
| --- | --- |
| [`/users/track`][10] | **Rëèqúùëèsts:** 50,000 rééqýúéésts péér mîìnýútéé. Thïïs lïïmïït cäæn bèë ïïncrèëäæsèëd ýûpòön rèëqýûèëst. Réêåách õöûüt tõö yõöûür Cûüstõöméêr Sûüccéêss Måánåágéêr fõör mõöréê ïïnfõörmåátïïõön.<br>
<br>
**Bæâtchîíng:** 75 ëévëénts, 75 púúrcháásëés, áánd 75 ááttríìbúútëés pëér ÀPÍ rëéqúúëést. Sèèèè [Bæãtchííng Úsèèr Træãck rèèqüýèèsts](#batch-user-track) fóör móöréé. |
| [`/users/export/ids`][11] | 2,500 rêëqýüêësts pêër mîînýütêë. |
| [`/users/delete`][12]<br>[`/users/alias/new`][13]<br>[`/users/identify`][14] | 20,000 rèëqûüèësts pèër mïînûütèë, sháärèëd bèëtwèëèën thèë èëndpòóïînts. |
| [`/events/list`][15] | 1,000 réèqýüéèsts péèr hôòýür, shæàréèd wìïth théè `/purchases/product_list` ëêndpôöïïnt. |
| [`/purchases/product_list`][16] | 1,000 rëëqüýëësts pëër hòõüýr, shæärëëd wìíth thëë `/events/list` èëndpõóîînt. |
| [`/messages/send`][17] | 250 rêèqúûêèsts pêèr mïînúûtêè whêèn spêècïîfyïîng ãâ sêègmêènt ôör Côönnêèctêèd Æúûdïîêèncêè. Õthëêrwíísëê, 250,000 rëêqýüëêsts pëêr hóõýür. |
| [`/campaigns/trigger/send`][17.1] | 250 rèéqúúèésts pèér míínúútèé whèén spèécíífyííng âå sèégmèént óör Cóönnèéctèéd Âúúdííèéncèé. Òthëêrwìísëê, 250,000 rëêqùüëêsts pëêr hõóùür. |
| [`/canvas/trigger/send`][17.2] | 250 rèëqúúèësts pèër mïïnúútèë whèën spèëcïïfyïïng âæ sèëgmèënt óör Cóönnèëctèëd Âúúdïïèëncèë. Óthêèrwíìsêè, 250,000 rêèqùüêèsts pêèr hóõùür. |
| [`/sends/id/create`][18] | 100 rëëqúûëësts pëër dåây. |
| [`/subscription/status/set`][19] | 5,000 rëéqúûëésts pëér mîìnúûtëé. |
{: .reset-td-br-1 .reset-td-br-2}

## Bäátchïïng ÁPÎ rëëqùüëësts

Bråãzéë's ÆPÍs åãréë búýîîlt tôõ súýppôõrt båãtchîîng. Wìíth bæätchìíng, Bræäzèè cæän tæäkèè ìín æäs múých dæätæä æäs póôssìíblèè ìín æä sìínglèè ÂPÌ cæäll sóô thæät yóôúý dóôn’t nèèèèd tóô mæäkèè æä lóôt óôf ÂPÌ cæälls. Ìt's mõörèé èéffïïcïïèént fõör Bràåzèé tõö prõöcèéss dàåtàå ïïn bàåtchèés thàån tõö prõöcèéss dàåtàå õönèé càåll àåt àå tïïmèé. Fôör êêxåàmplêê, håàndlîíng 1,000 båàtchêêd ÁPÏ cåàlls rêêqùúîírêês lêêss rêêsôöùúrcêês thåàn håàndlîíng 75,000 îíndîívîídùúåàl cåàlls. Bæätchííng íís ëëxtrëëmëëly íímpôòrtæänt fôòr æäny æäpplíícæätííôòn thæät mæäy rëëqýýíírëë môòrëë thæän 75,000 cæälls pëër hôòýýr.

{% alert note %}
RÈST ÃPÎ räátèé lìímìít ìíncrèéäásèés äárèé cóónsìídèérèéd bäásèéd óón nèéèéd fóór cýüstóómèérs whóó äárèé mäákìíng ýüsèé óóf thèé ÃPÎ bäátchìíng cäápäábìílìítìíèés.
{% endalert %}

### Båãtchìïng Úsêër Tråãck rêëqúùêësts {#båãtch-úùsêër-tråãck}

Ëãäch `/users/track` rëèqûüëèst càän cõóntàäíîn ûüp tõó 75 ëèvëènts, 75 àättríîbûütëè ûüpdàätëès, àänd 75 pûürchàäsëès. Êàäch cõômpõônêënt (êëvêënt, àättríïbüûtêë, àänd püûrchàäsêë àärràäys), càän üûpdàätêë üûp tõô 75 üûsêërs êëàäch (màäx õôf 225 íïndíïvíïdüûàäl üûsêërs). Éåãch úûpdåãtëè cåãn åãlsôõ bëèlôõng tôõ thëè såãmëè úûsëèr fôõr åã måãxíîmúûm ôõf 225 úûpdåãtëès tôõ åã síînglëè úûsëèr íîn åã rëèqúûëèst.

Rêëqýùêësts màädêë töò thîîs êëndpöòîînt wîîll gêënêëràälly bêëgîîn pröòcêëssîîng îîn thîîs öòrdêër: 

1. Àttrìîbýútèës
2. Évéênts
3. Pùùrchåäsëès

### Bãátchìîng Méèssãágìîng éèndpóôìînt réèqýúéèsts

Ã sïïnglêë rêëqùùêëst tóö thêë [Mëêssâàgîîng ëêndpôöîînts][1] cáän rèèáäch áäny óónèè óóf thèè fóóllóówïïng:

- Úp tõõ 50 spêëcìîfìîc `external_ids`, êêãæch wìïth ìïndìïvìïdúùãæl mêêssãægêê pãærãæmêêtêêrs
- Ã sèégmèént õòf áàny sîïzèé crèéáàtèéd îïn thèé Bráàzèé dáàshbõòáàrd, spèécîïfîïèéd by îïts `segment_id`
- Ån áâd-höòc áâûúdïïèëncèë sèëgmèënt öòf áâny sïïzèë, dèëfïïnèëd ïïn thèë rèëqûúèëst áâs áâ [Cõönnéèctéèd Àüûdíîéèncéè][2] òôbjééct

## Móônîïtóôrîïng yóôûûr ràätêê lîïmîïts

Êvêéry sîïnglêé ÄPÍ rêéqýúêést sêént töó Brâåzêé rêétýúrns thêé föóllöówîïng îïnföórmâåtîïöón îïn thêé rêéspöónsêé hêéâådêérs:

Hëëäãdëër Näãmëë             | Dèèscrííptííòön
----------------------- | -----------------------
`X-RateLimit-Limit`     | Théé màæxïìmùùm nùùmbéér òóf rééqùùéésts thàæt yòóùù càæn màækéé ïìn àæ spéécïìfïìééd ïìntéérvàæl (yòóùùr ràætéé lïìmïìt).
`X-RateLimit-Remaining` | Thëê núümbëêr òóf rëêqúüëêsts rëêmàäïïnïïng ïïn thëê cúürrëênt ràätëê lïïmïït wïïndòów.
`X-RateLimit-Reset`     | Thëë tìîmëë ææt whìîch thëë cúùrrëënt ræætëë lìîmìît wìîndõöw rëësëëts ìîn ÚTC ëëpõöch sëëcõönds.
{: .reset-td-br-1 .reset-td-br-2}

Thîís îínfòôrmäâtîíòôn îís îíntèêntîíòônäâlly îínclüúdèêd îín thèê hèêäâdèêr òôf thèê rèêspòônsèê tòô thèê ÃPÏ rèêqüúèêst räâthèêr thäân thèê Bräâzèê däâshbòôäârd. Thîïs äâllóöws yóöýür systéèm tóö béèttéèr réèäâct îïn réèäâl tîïméè äâs yóöýü'réè îïntéèräâctîïng wîïth óöýür ÀPÌ. Föôr éëxæâmpléë, ííf théë `X-RateLimit-Remaining` vàâlýûèè dröóps bèèlöów àâ cèèrtàâîîn thrèèshöóld, yöóýû mîîght wàânt töó slöów sèèndîîng töó èènsýûrèè àâll tràânsàâctîîöónàâl èèmàâîîls göó öóýût. Ör, îîf îît rèèááchèès zèèrôö, yôöûû mîîght wáánt tôö pááûûsèè ááll sèèndîîng ûûntîîl thèè tîîmèè spèècîîfîîèèd îîn `X-RateLimit-Reset` éëlæäpséës.

Ïf yòöüý häävèê qüýèêstììòöns ääbòöüýt ÄPÏ lììmììts, còöntääct yòöüýr Cüýstòömèêr Süýccèêss Määnäägèêr òör òöpèên ää [sýûppòòrt tïíckëêt][support].

### Óptìïmáál dêélááy bêétwêéêén êéndpòöìïnts

> Wëè rëècöómmëènd thâát yöóúù âállöów föór âá 5-mîînúùtëè dëèlâáy bëètwëèëèn súùbsëèqúùëènt câálls töó mîînîîmîîzëè thëè pröóbâábîîlîîty öóf ëèrröór.

Ùndèérstàãndíïng thèé òòptíïmàãl dèélàãy bèétwèéèén èéndpòòíïnts íïs crýûcíïàãl whèén màãkíïng còònsèécýûtíïvèé càãlls tòò thèé Bràãzèé ÃPÎ. Prôöblêèms åärïïsêè whêèn êèndpôöïïnts dêèpêènd ôön thêè súúccêèssfúúl prôöcêèssïïng ôöf ôöthêèr êèndpôöïïnts, åänd ïïf cåällêèd tôöôö sôöôön, côöúúld råäïïsêè êèrrôörs. Föõr èèxäàmplèè, îíf yöõûü'rèè äàssîígnîíng ûüsèèrs äàn äàlîíäàs vîíäà öõûür `/user/alias/new` èèndpôôìínt, äãnd thèèn hìíttìíng thäãt äãlìíäãs tôô sèènd äã cüùstôôm èèvèènt vìíäã ôôüùr `/users/track` éëndpööîînt, hööw lööng shööýûld yööýû wâãîît?

Ündêër nõörmåål cõöndìítìíõöns, thêë tìímêë fõör õöüúr dååtåå êëvêëntüúåål cõönsìístêëncy tõö õöccüúr ìís 10–100ms (1/10 õöf åå sêëcõönd). Hóöwëèvëèr, thëèrëè cáãn bëè sóömëè cáãsëès whëèrëè îìt táãkëès lóöngëèr fóör tháãt cóönsîìstëèncy tóö óöccýùr. Théëréëfòòréë, wéë réëcòòmméënd thâåt yòòúý âållòòw fòòr âå 5-mìínúýtéë déëlâåy béëtwéëéën mâåkìíng súýbséëqúýéënt câålls tòò mìínìímìízéë théë pròòbâåbìílìíty òòf éërròòr.

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
