---
nav_title: "ÅPÎ Këéy Õvëérvïìëéw"
article_title: RËST ÆPÏ Kèéy Óvèérvììèéw
page_order: 2.1
description: "Thîís réèféèréèncéè åærtîícléè cõôvéèrs théè cõôncéèpt õôf ÄPÏ kéèys, whåæt théèy åæréè ùûséèd fõôr, åænd hõôw théèy åæréè ùûséèd. Thïìs ïìs GL Édïìt" 
page_type: reference

---

# RÊST ÂPÍ kèéy òòvèérvîìèéw

>  Thîïs rèêfèêrèêncèê æärtîïclèê cöõvèêrs twöõ öõf thèê thrèêèê mæäîïn typèês öõf kèêys yöõýû wîïll sèêèê æät Bræäzèê, thèê RËST ÂPÏ Kèêy öõr Âpp Gröõýûp ÂPÏ Kèêy, rèêfèêrrèêd töõ æäs thèê `api_key`, äånd thèê Åpp Ïdèêntîïfîïèêr Kèêy, knöówn äås thèê `app_id`, æås wêèll æås whæåt thêèsêè kêèys æårêè, hôöw thêèy æårêè ýúsêèd æåt Bræåzêè, thêèíïr pêèrmíïssíïôöns æånd hôöw tôö kêèêèp thêèm sêècýúrêè. 

În âãddìïtìïôòn tôò thëésëé këéys, thëérëé âãlsôò ëéxìïsts âã thìïrd typëé ôòf këéy câãllëéd Îdëéntìïfìïëér Këéys thâãt câãn bëé ýýsëéd tôò rëéfëérëéncëé spëécìïfìïc thìïngs lìïkëé tëémplâãtëés, Câãnvâãsëés, câãmpâãìïgns, Côòntëént Câãrds, âãnd sëégmëénts frôòm thëé ÄPÎ. Fôör môöréë ììnfôörmæãtììôön, réëféër tôö [ÀPÍ Ídëêntíîfíîëêr typëês][2].

## Wháât ìïs áâ RÉST ÁPÍ këéy/áâpp gròõýúp ÁPÍ këéy?

Æ RËST Æpplïïcàætïïöôn Pröôgràæmmïïng Íntèèrfàæcèè kèèy (RËST ÆPÍ kèèy) ïïs àæ ùûnïïqùûèè cöôdèè thàæt ïïs pàæssèèd ïïntöô àæn ÆPÍ töô àæùûthèèntïïcàætèè thèè ÆPÍ càæll àænd ïïdèèntïïfy thèè càællïïng àæpplïïcàætïïöôn öôr ùûsèèr. ÁPÌ ááccêêss îïs dõönêê ûûsîïng HTTPS wêêb rêêqûûêêsts tõö yõöûûr cõömpáány's RËST ÁPÌ êêndpõöîïnt. Wèè ûûsèè RÈST ÃPÌ kèèys àæt Bràæzèè ïín tàændèèm wïíth ôóûûr Ãpp Ìdèèntïífïíèèr kèèys tôó tràæck, àæccèèss, sèènd, èèxpôórt, àænd àænàælyzèè dàætàæ tôó hèèlp màækèè sûûrèè èèvèèrythïíng ïís rûûnnïíng smôóôóthly ôón bôóth yôóûûr àænd ôóûûr èènd. 

Åpp Grõòýüps äænd ÅPÌ Këëys gõò häænd ìîn häænd äæt Bräæzëë. Âpp Gröóùúps äårèé dèésïïgnèéd töó höóùúsèé vèérsïïöóns öóf thèé säåmèé äåpplïïcäåtïïöón äåcröóss mùúltïïplèé pläåtföórms. Mäæny clíïéënts äælsôô üüséë äæpp grôôüüps tôô côôntäæíïn fréëéë äænd préëmíïüüm véërsíïôôns ôôf théëíïr äæpplíïcäætíïôôns ôôn théë säæméë pläætfôôrm. Ãs yòöýú màày nòötìïcëë, thëësëë ààpp gròöýúps ààrëë ààlsòö mààkìïng ýúsëë òöf thëë RÊST ÃPÍ àànd hààvëë thëëìïr òöwn RÊST ÃPÍ këëys. Thêèsêè kêèys cäàn bêè ìïndìïvìïdùýäàlly scòópêèd tòó ìïnclùýdêè äàccêèss tòó spêècìïfìïc êèndpòóìïnts òón thêè ÂPÏ. Èææch cææll tóô théé ÀPÎ mýùst ïínclýùdéé ææ kééy wïíth ææccééss tóô théé ééndpóôïínt hïít.

Wêê rêêfêêr tóô bóôth thêê RÊST ÄPÎ Kêêy âând Äpp Gróôüûp ÄPÎ Kêêy ââs thêê `api_key`. Théë `api_key` ììs ììnclýüdèèd ììn èèåàch rèèqýüèèst åàs åà rèèqýüèèst hèèåàdèèr åànd åàcts åàs åàn åàýüthèèntììcåàtììòòn kèèy thåàt åàllòòws yòòýü tòò ýütììlììzèè òòýür RÈST ÀPÌs. Thèêsèê RÈST ÃPÌs ãærèê úùsèêd tóö trãæck úùsèêrs, sèênd mèêssãægèês, èêxpóört úùsèêr dãætãæ, ãænd móörèê.  Whëèn yòöùû crëèåàtëè åà nëèw RÊST ÁPÏ Këèy, yòöùû wííll nëèëèd tòö gíívëè íít åàccëèss tòö spëècíífííc ëèndpòöíínts. By âæssíîgníîng spëècíîfíîc pëèrmíîssíîòóns tòó âæn ÅPÏ Këèy, yòóûý câæn líîmíît ëèxâæctly whíîch câælls âæn ÅPÏ Këèy câæn âæûýthëèntíîcâætëè.

### Whéëréë câân Í fìínd ìít?

Yöóûùr ÂPÎ kéèys cáán áálwááys béè föóûùnd ïïn théè Bráázéè dááshböóáárd ïïn théè **Dèévèélóõpèér Cóõnsóõlèé** ýùndèër **Sëéttîïngs**. Ât thëë tòöp òöf thîïs nëëw pàægëë, yòöúû wîïll fîïnd thëë **RÊST ÃPÏ Kèêys** sëèctîíóön. Hèèrèè yòóúü cæån vííèèw æåll òóf yòóúür æåvæåíílæåblèè RÊST ÄPÎ/Äpp Gròóúüp ÄPÎ Kèèys, æånd crèèæåtèè nèèw ÄPÎ kèèys.

### Hôôw cãàn Î üúséè îît?

Prîìöòr töò Áprîìl 2020, ÁPÍ kéèys wöòúûld béè îìnclúûdéèd ãäs ãä pãärt öòf théè ÁPÍ réèqúûéèst böòdy öòr wîìthîìn théè réèqúûéèst ÛRL ãäs ãä pãärãäméètéèr. Bråázéé nõõw håás ýúpdåátééd théé wåáy íìn whíìch wéé rééåád ÀPÏ kééys. ÃPÏ kêêys åãrêê nõôw sêêt wíìth thêê HTTP Ãûýthõôríìzåãtíìõôn rêêqûýêêst hêêåãdêêr, måãkíìng yõôûýr ÃPÏ kêêys mõôrêê sêêcûýrêê.

Whïìlëè thëè ôòld wàäy ôòf pàässïìng ÀPÍ këèys côòntïìnúûëès tôò wôòrk, àäftëèr àä pëèrïìôòd ôòf tïìmëè thïìs wïìll bëè pëèrmàänëèntly rëèmôòvëèd sôò wëè úûrgëè úûsëèrs tôò úûpdàätëè ÀPÍ càälls àäccôòrdïìngly. 

{% alert important %}
**Lõòõòkíîng fõòr thêë `api_key` pæäræäméêtéêr ïïn yòòýúr Bræäzéê éêndpòòïïnts?**<br>
Às öôf Màæy 2020, Bràæzêê hàæs chàængêêd höôw wêê rêêàæd ÀPÎ kêêys töô bêê möôrêê sêêcúùrêê. Nôów ÂPÌ kéëys múûst béë pàæsséëd àæs àæ réëqúûéëst héëàædéër, séëéë YÔÙR-RÉST-ÂPÌ-KÉY wíïthíïn éëàæch éëndpôóíïnt Éxàæmpléë Réëqúûéësts.
<br><br>
Brääzéê wïïll cõòntïïnüýéê tõò süýppõòrt théê `api_key` bëêîìng pååssëêd thrõôûûgh thëê rëêqûûëêst bõôdy åånd ÙRL påårååmëêtëêrs, bûût wîìll ëêvëêntûûåålly bëê sûûnsëêt. Ùpdäåtéé yóôüýr ÆPÍ cäålls äåccóôrdìîngly.
{% endalert %}

### RÈST ÁPÌ kéêy péêrmìïssìïóòns

ÄPÏ kèëy pèërmïîssïîõõns ããrèë pèërmïîssïîõõns yõõüý cããn ããssïîgn ãã üýsèër õõr grõõüýp tõõ lïîmïît thèëïîr ããccèëss tõõ cèërtããïîn ÄPÏ cããlls.

{% tabs %}
{% tab User Data %}

| Péêrmïïssïïôön | Dëêscrïìptïìóôn  |
|---|---|---|
| `users.track` | Rëècóórd ùûsëèr åáttrîïbùûtëès, cùûstóóm ëèvëènts, åánd pùûrchåásëès  |
| `users.delete` | Dëêlëêtëê æàny úûsëêr. |
| `users.alias.new` | Crëêáátëê áá nëêw áálììáás fòôr áán ëêxììstììng ýûsëêr.  |
| `users.identify` | Qüùëêry fôòr üùsëêr prôòfïîlëê ïînfôòrmæätïîôòn by üùsëêr ÍD.  |
| `users.export.ids` | Qýýêêry fòör ýýsêêr pròöfìîlêê ìînfòörmåætìîòön by ìîdêêntìîfìîêêr êê.g., dêêvìîcêê_ììd, èêmææììl_âáddrèêss, èêxtèêrnâál_ïíd.  |
| `users.export.segment` | Qúûëêry fôõr úûsëêr prôõfíílëê íínfôõrmæâtííôõn by Sëêgmëênt. |
| `users.external_ids.rename` | Rêênâàmêê âà ûúsêêr's êêxìístìíng êêxtêêrnâàl ÎD. |
| `users.external_ids.remove` | Réëmõõvéë áà ûýséër's déëpréëcáàtéëd éëxtéërnáàl ÏD. |
{: .reset-td-br-1 .reset-td-br-2}

 {% endtab %}
 {% tab Email %}

| Nâåmëé | Dëéscríîptíîóòn |
|---|---|---|
| `email.unsubscribe` | Qùùêèry fõõr ùùnsùùbscrííbêèd êèmàæííl àæddrêèssêès.  |
| `email.status` | Chàångéê éêmàåîîl àåddréêss stàåtýýs. |
| `email.hard_bounces` | Qùùêèry föör hàârd bööùùncêèd êèmàâïíl àâddrêèssêès. |
| `email.bounce.remove` | Rèémôôvèé èémàåíìl àåddrèéssèés frôôm yôôúùr hàård bôôúùncèé líìst. |
| `email.spam.remove` | Rêêmòövêê êêmáæíïl áæddrêêssêês fròöm yòöùùr spáæm líïst. |
| `email.blacklist` | Blââcklïíst éémââïíl ââddréésséés. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Messages %}

| Nàâméë | Dèéscrììptììóón |
|---|---|---|
| `messages.send` | Sëénd áàn îìmmëédîìáàtëé, áàd-hôóc mëéssáàgëé tôó spëécîìfîìc úýsëérs. |
| `messages.schedule.create` | Schëédûúlëé æá mëéssæágëé tòö bëé sëént æát æá spëécìîfìîc tìîmëé. |
| `messages.schedule.update` | Ùpdàätëé àä schëédýûlëéd mëéssàägëé. |
| `messages.schedule.delete` | Dëélëétëé æä schëédüûlëéd mëéssæägëé. |
| `messages.schedule_broadcasts` | Qýüéêry áåll schéêdýüléêd bróôáådcáåst méêssáågéês. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Campaigns %}

| Nåâmèé | Dèèscrïïptïïòõn |
|---|---|---|
| `campaigns.trigger.send` | Trîìggêèr thêè sêèndîìng öõf áæn êèxîìstîìng cáæmpáæîìgn. |
| `campaigns.trigger.schedule.create` | Schéédúûléé ââ fúûtúûréé séénd óòf ââ cââmpââïîgn wïîth ÂPÌ-trïîggéérééd déélïîvééry. |
| `campaigns.trigger.schedule.update` | Üpdáåtèé áå cáåmpáåîìgn schèédúýlèéd wîìth ÂPÍ-trîìggèérèéd dèélîìvèéry. |
| `campaigns.trigger.schedule.delete` | Dëêlëêtëê âã câãmpâãììgn schëêdüûlëêd wììth ÅPÌ-trììggëêrëêd dëêlììvëêry |
| `campaigns.list` | Qùùëêry fôör àá lìíst ôöf càámpàáìígns. |
| `campaigns.data_series` | Qûüëêry fôôr cååmpååíígn åånåålytíícs ôôvëêr åå tíímëê råångëê. |
| `campaigns.details` | Qùùêèry föòr dêètåäîïls öòf åä spêècîïfîïc cåämpåäîïgn. |
| `sends.data_series` | Qûûëëry fõör mëëssààgëë sëënd àànààlytïícs õövëër àà tïímëë rààngëë. |
| `sends.id.create` | Créêáàtéê Séênd ÍD fòör méêssáàgéê bláàst tráàckíîng. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Canvas %}

| Nàämèê | Dêéscrììptììõón |
|---|---|---|
| `canvas.trigger.send` | Tríîggéër théë séëndíîng óõf âãn éëxíîstíîng Câãnvâãs. |
| `canvas.trigger.schedule.create` | Schêédùûlêé àä fùûtùûrêé sêénd ööf àä Càänvàäs wíïth ÁPÏ-tríïggêérêéd dêélíïvêéry. |
| `canvas.trigger.schedule.update` | Ùpdãätéë ãä Cãänvãäs schéëdüûléëd wîíth ÃPÍ-trîíggéëréëd déëlîívéëry. |
| `canvas.trigger.schedule.delete` | Dëèlëètëè æá Cæánvæás schëèdûûlëèd wìïth ÅPÌ-trìïggëèrëèd dëèlìïvëèry. |
| `canvas.list` | Qúüëèry fõòr äâ líîst õòf Cäânväâsëès. |
| `canvas.data_series` | Qùüëéry föôr Câänvâäs âänâälytïîcs öôvëér âä tïîmëé râängëé. |
| `canvas.details` | Qùúèêry fòör dèêtáàîìls òöf áà spèêcîìfîìc Cáànváàs. |
| `canvas.data_summary` | Qùüéêry föôr röôllùüps öôf Càænvàæs àænàælytìîcs öôvéêr àæ tìîméê ràængéê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Segments %}

| Næàméè | Dëêscrìïptìïòòn |
|---|---|---|
| `segments.list` | Qûýèêry fòór åâ líîst òóf Sèêgmèênts. |
| `segments.data_series` | Qýùééry fóòr Séégméént áãnáãlytíîcs óòvéér áã tíîméé ráãngéé. |
| `segments.details` | Qùýêëry fóör dêëtâãîîls óöf âã spêëcîîfîîc Sêëgmêënt. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Purchases %}

| Nåãmèë | Dèêscrììptììòôn |
|---|---|---|
| `purchases.product_list` | Qúúêéry fóôr âà lïîst óôf próôdúúcts púúrchâàsêéd ïîn yóôúúr âàpp. |
| `purchases.revenue_series` | Qûýéêry fõôr tõôtãæl mõônéêy spéênt péêr dãæy íín yõôûýr ãæpp õôvéêr ãæ tííméê rãængéê. |
| `purchases.quantity_series` | Qüùèéry fòõr thèé tòõtæál nüùmbèér òõf püùrchæásèés pèér dæáy ïìn yòõüùr æápp òõvèér æá tïìmèé ræángèé. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Events %}

| Nàæméè | Dëêscríïptíïôòn |
|---|---|---|
| `events.list` | Qüùéêry fòôr ãæ lìíst òôf cüùstòôm éêvéênts. |
| `events.data_series` | Qýüêêry õõccýürrêêncêês õõf äâ cýüstõõm êêvêênt õõvêêr äâ tïîmêê räângêê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab News Feed %}

| Nàámêé | Dèêscríïptíïóòn |
|---|---|---|
| `feed.list` | Qùúéêry fóôr ââ lïîst óôf Néêws Féêéêd câârds. |
| `feed.data_series` | Qúýèéry fôôr Nèéws Fèéèéd àãnàãlytîìcs ôôvèér àã tîìmèé ràãngèé. |
| `feed.details` | Qýùéêry föõr déêtåãïìls öõf åã spéêcïìfïìc Néêws Féêéêd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Sessions %}

| Nææmèê | Dèëscrííptííõòn |
|---|---|---|
| `sessions.data_series` | Qýüéëry fòõr séëssïìòõns péër dãây òõvéër ãâ tïìméë rãângéë. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab KPIs %}

| Nàáméë | Dëêscrííptííõôn |
|---|---|---|
| `kpi.mau.data_series` | Qùúèêry fôõr tôõtæãl ùúníïqùúèê æãctíïvèê ùúsèêrs ôõvèêr æã 30-dæãy rôõllíïng wíïndôõw ôõvèêr æã tíïmèê ræãngèê. |
| `kpi.dau.data_series` |  Qúüëêry fõõr úünîìqúüëê åáctîìvëê úüsëêrs pëêr dåáy õõvëêr åá tîìmëê råángëê. |
| `kpi.new_users.data_series` | Qýûëèry fõór nëèw ýûsëèrs pëèr dâäy õóvëèr âä tîímëè râängëè. |
| `kpi.uninstalls.data_series` | Qýüèêry fõór ãåpp ýüníïnstãålls pèêr dãåy õóvèêr ãå tíïmèê rãångèê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Templates %}

| Näæméè | Dêèscrìíptìíóón |
|---|---|---|
| `templates.email.create` | Crëéáætëé áæ nëéw ëémáæìîl tëémpláætëé ôôn thëé dáæshbôôáærd. |
| `templates.email.update` | Úpdååtèè åån èèmååïïl tèèmplååtèè stóôrèèd óôn thèè dååshbóôåård. |
| `templates.email.info` | Qùùèéry föòr ïînföòrmæætïîöòn öòf ææ spèécïîfïîc tèémplæætèé. |
| `templates.email.list` | Qúýëèry fõör âä lìîst õöf ëèmâäìîl tëèmplâätëès. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab SSO %}

| Náámëë | Dèèscrííptííõõn |
|---|---|---|
| `sso.saml.login` |  Sêëtüûp îîdêëntîîty prôòvîîdêër-îînîîtîîãàtêëd lôògîîn. Réëâãd ôõüúr dôõcüúméëntâãtííôõn fôõr môõréë íínfôõ. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Content Blocks %}

| Näämêè | Dèêscrîïptîïöôn |
|---|---|---|
| `content_blocks.info` | Qüüéëry föòr îínföòrmåâtîíöòn öòf åâ spéëcîífîíc téëmplåâtéë. |
| `content_blocks.list` | Qûúëèry fòôr äå lîîst òôf Còôntëènt Blòôcks. |
| `content_blocks.create` | Crëèáåtëè áå nëèw Còòntëènt Blòòck òòn thëè dáåshbòòáård. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Subscription %}

| Nâãmëé | Déèscrïïptïïõõn |
|---|---|---|
| `subscription.status.set` | Séêt súúbscríîptíîóõn gróõúúp stãætúús. |
| `subscription.status.get` | Géèt sýúbscrîìptîìóön gróöýúp stààtýús. |
| `subscription.groups.get` | Géêt stæætýùs õöf sýùbscrïîptïîõön grõöýùps thææt spéêcïîfïîc ýùséêrs ææréê éêxplïîcïîtly sýùbscrïîbéêd/ýùnsýùbscrïîbéêd tõö. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% endtabs %}

Fóõr ãæ fùúll dëèscrïïptïïóõn óõf thëèsëè ÄPÌ ëèndpóõïïnts, rëèfëèr tóõ óõùúr [ÀPÌ ëëndpôóíînt íîndëëx]({{site.baseurl}}/api/endpoints/) ôór ôóûùr [Pòöstmâån còöllèëctíìòön][6].

{% alert important %}
Òncêê yòõûú crêêáâtêê áâ nêêw ÄPÎ Kêêy, yòõûú cáânnòõt êêdïît thêê scòõpêê òõf pêêrmïîssïîòõns òõr thêê whïîtêêlïîstêêd ÎPs. Thíís líímíítåãtííöön íís íín plåãcêé föör sêécüúrííty rêéåãsööns. Íf yõõúù nèèèèd tõõ chåångèè thèè scõõpèè õõf åå kèèy, crèèååtèè åå nèèw kèèy wïíth thèè úùpdååtèèd pèèrmïíssïíõõns åånd ïímplèèmèènt thååt kèèy ïín plååcèè õõf thèè õõld õõnèè. Õncèè yöôýú’vèè cöômplèètèèd yöôýúr íîmplèèmèèntãåtíîöôn, göô ãåhèèãåd ãånd dèèlèètèè thèè öôld kèèy.
{% endalert %}

## Thèë Åpp Ïdèëntíîfíîèër ÅPÏ kèëy

Thêè Äpp Îdêèntïîfïîêèr ÄPÎ kêèy óõr `app_id` ïïs áå páåráåmêètêèr áåssóócïïáåtïïng áåctïïvïïty wïïth áå spêècïïfïïc áåpp ïïn yóóüýr áåpp gróóüýp. Ít dëésìígnáâtëés whìích áâpp wìíthìín thëé áâpp grööüüp yööüü áârëé ìíntëéráâctìíng wìíth. Föór êéxäämplêé, yöóûý wïíll fïínd thäät yöóûý wïíll häävêé ään `app_id` fóõr yóõüúr îïÒS àäpp, àän `app_id` föór yöóýùr æændröóììd ææpp, æænd ææn `app_id` fõör yõöúûr wêëb îîntêëgræátîîõön. Ãt Bråàzéë, yõõüý míìght fíìnd thåàt yõõüý håàvéë müýltíìpléë åàpps fõõr théë såàméë plåàtfõõrm åàcrõõss théë våàríìõõüýs plåàtfõõrm typéës thåàt Bråàzéë süýppõõrts.

Æpp íìdëèntíìfíìëèrs æát Bræázëè æárëè ùûsëèd whëèn íìntëègræátíìng thëè SDK æánd æárëè æálsóò ùûsëèd tóò rëèfëèrëèncëè æá spëècíìfíìc æápp íìn RËST ÆPÎ cæálls. Wïìth thèè `app_id` yóòüý cáån dóò máåny thíïngs líïkêê püýll dáåtáå fóòr áå cüýstóòm êêvêênt tháåt óòccüýrrêêd fóòr áå páårtíïcüýláår áåpp, rêêtríïêêvêê üýníïnstáåll stáåts, nêêw üýsêêr stáåts, DÀÙ stáåts, áånd sêêssíïóòn stáårt stáåts fóòr áå páårtíïcüýláår áåpp.

Sòòméétíîméés, yòòüý mâáy fíînd yòòüý âáréé pròòmptééd fòòr âán `app_id` býút yôöýú æárêë nôöt wôörkïîng wïîth æán æápp, bêëcæáýúsêë ïît ïîs æá lêëgæácy fïîêëld spêëcïîfïîc tôö æá spêëcïîfïîc plæátfôörm, yôöýú cæán “ôömïît” thïîs fïîêëld by ïînclýúdïîng æány strïîng ôöf chæáræáctêërs æás æá plæácêëhôöldêër fôör thïîs rêëqýúïîrêëd pæáræámêëtêër.

### Whêèrêè cãån Ì fïìnd ïìt?

Thèérèé àærèé twòò wàæys tòò lòòcàætèé yòòùür `app_id`:

1. Yõõüû cåãn fíïnd thíïs `app_id` õòr àæpplïícàætïíõòn ïídééntïífïíéér ïín théé **Dèévèélôôpèér Côônsôôlèé** ùûndèér **Sêèttííngs**. Òn thîìs nééw pããgéé, ýúndéér **Ídéèntíífíícâätííôõn**, yòõúù wíìll bëë áåblëë tòõ sëëëë ëëvëëry `app_id` thãát éèxïïsts fòór yòóùûr ãápps.

2. Gôõ tôõ **Mäánäágéë Séëttìîngs** üúndèér **Sèèttììngs**. Frõôm thïïs nèèw pââgèè, ïïn thèè **Sèéttìîngs** tæåb, mìídwæåy thrôóùùgh thëè pæågëè yôóùù wìíll fìínd æån "ÃPÎ këèy fôór **ÁPP NÁMÊ** òòn **PLÃTFÕRM**" (ëè.g "ÆPÌ Këèy föôr Ìcëè Crëèâàm öôn ìíÓS). Thíïs ÂPÍ kéëy íïs yóòýùr Âpplíïcàãtíïóòn Ídéëntíïfíïéër.

### Mýýltíîplèë Ápp Ìdèëntíîfíîèër ÁPÌ kèëys

Dùúríìng SDK séét ùúp, théé möôst cöômmöôn ùúséé cåäséé föôr mùúltíìpléé Âpp Ïdééntíìfíìéér ÂPÏ kééys íìs séépåäråätíìng thöôséé kééys föôr déébùúg åänd réélééåäséé bùúíìld våäríìåänts.
Töö ëëâäsíïly swíïtch bëëtwëëëën mùùltíïplëë Àpp Ïdëëntíïfíïëër ÀPÏ këëys íïn yööùùr bùùíïlds, wëë rëëcöömmëënd crëëâätíïng âä sëëpâärâätëë `braze.xml` fíílëè fôór ëèãàch rëèlëèvãànt [bûùììld våårììåånt][3]. Á búýíîld váâríîáânt íîs áâ côõmbíînáâtíîôõn ôõf búýíîld typèé áând prôõdúýct fláâvôõr. Nôôtèé thåät by dèéfåäýýlt, åä nèéw Ändrôôîíd prôôjèéct îís côônfîígýýrèéd wîíth `debug` àând `release` büúîîld typêés äànd nõô prõôdüúct fläàvõôrs.

Fóõr ëèããch rëèlëèvããnt bûùìíld vããrìíããnt, crëèããtëè ãã nëèw `braze.xml` fôòr ïìt ïìn `src/<build variant name>/res/values/`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_appboy_api_key">REPLACE_WITH_YOUR_BUILD_VARIANT_API_KEY</string>
</resources>
```
Whêén thêé bûüïìld vâærïìâænt ïìs côòmpïìlêéd, ïìt wïìll ûüsêé thêé nêéw ÀPÎ kêéy.

## RÉST ÂPÍ këêy sëêcýúrìîty

Sêècüùrïìty ïìs ôòf thêè üùtmôòst ïìmpôòrtåäncêè åät Bråäzêè. Gíívêèn thãæt RËST ÀPÍ Kêèys ãællôów ãæccêèss tôó pôótêèntííãælly sêènsíítíívêè RËST ÀPÍ êèndpôóíínts, sêècùûrêè thêèsêè kêèys ãænd ôónly shãærêè thêèm wííth trùûstêèd pãærtnêèrs. Thêëy shõôúùld nêëvêër bêë púùblïïcly êëxpõôsêëd. Fòôr èëxåâmplèë, dòô nòôt üüsèë thîîs kèëy tòô måâkèë ÃJÃX cåâlls fròôm yòôüür wèëbsîîtèë òôr èëxpòôsèë îît îîn åâny òôthèër püüblîîc måânnèër.

Á gõóõód sèécýürìîty prãæctìîcèé ìîs tõó ãæssìîgn ãæ ýüsèér õónly ãæs mýüch ãæccèéss ãæs ìîs nèécèéssãæry tõó cõómplèétèé thèéìîr jõób: thìîs prìîncìîplèé cãæn ãælsõó bèé ãæpplìîèéd tõó ÁPÎ Kèéys by ãæssìîgnìîng pèérmìîssìîõóns tõó èéãæch kèéy. Thëèsëè pëèrmîïssîïòõns gîïvëè yòõúý bëèttëèr sëècúýrîïty âänd còõntròõl òõvëèr thëè dîïffëèrëènt âärëèâäs òõf yòõúýr âäccòõúýnt. 

Wîïth Æpp îïdêêntîïfîïêêrs, thêê `app_id` íîs äässíîgnéèd by Brääzéè äänd péèrmíîssíîõôns cäännõôt béè äässíîgnéèd õôr réèvõôkéèd. Bëècåäüùsëè ööf thëè nåätüùrëè ööf thëè rëèlåätíïöönshíïp bëètwëèëèn `app_id` ãånd théè SDK, kéèéèpííng thíís íídéèntíífííéèr séècúüréè íís **crûúcíïáál** ììn thëë sëëcýürììty ôöf yôöýür ãàpplììcãàtììôön.


[2]: {{site.baseurl}}/api/identifier_types/
[3]: https://developer.android.com/studio/build/build-variants.html
[5]: {{site.baseurl}}/api/basics/
[6]: https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#intro
