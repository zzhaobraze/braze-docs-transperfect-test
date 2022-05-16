---
nav_title: "ÅPÌ Kèèy Óvèèrvííèèw"
article_title: RËST ÀPÏ Kêèy Övêèrvíîêèw
page_order: 2.1
description: "Thîís rêëfêërêëncêë áârtîíclêë cõõvêërs thêë cõõncêëpt õõf ÅPÎ kêëys, wháât thêëy áârêë ùüsêëd fõõr, áând hõõw thêëy áârêë ùüsêëd. Thìís ìís GL Édìít" 
page_type: reference

---

# RÊST ÂPÏ kèéy õòvèérvîìèéw

>  Thîïs rêêfêêrêêncêê áãrtîïclêê cöòvêêrs twöò öòf thêê thrêêêê máãîïn typêês öòf kêêys yöòýý wîïll sêêêê áãt Bráãzêê, thêê RÊST ÆPÌ Kêêy öòr Æpp Gröòýýp ÆPÌ Kêêy, rêêfêêrrêêd töò áãs thêê `api_key`, ãànd thèé Ápp Ïdèéntíìfíìèér Kèéy, knóõwn ãàs thèé `app_id`, åàs wêéll åàs whåàt thêésêé kêéys åàrêé, hôów thêéy åàrêé ûûsêéd åàt Bråàzêé, thêéïïr pêérmïïssïïôóns åànd hôów tôó kêéêép thêém sêécûûrêé. 

Ìn æáddîítîíõõn tõõ thëèsëè këèys, thëèrëè æálsõõ ëèxîísts æá thîírd typëè õõf këèy cæállëèd Ìdëèntîífîíëèr Këèys thæát cæán bëè üýsëèd tõõ rëèfëèrëèncëè spëècîífîíc thîíngs lîíkëè tëèmplæátëès, Cæánvæásëès, cæámpæáîígns, Cõõntëènt Cæárds, æánd sëègmëènts frõõm thëè ÁPÌ. Fõòr mõòréê îïnfõòrmáåtîïõòn, réêféêr tõò [ÂPÍ Ídèèntììfììèèr typèès][2].

## Whæàt íîs æà RËST ÂPÏ kèêy/æàpp gröòüùp ÂPÏ kèêy?

Ã RÊST Ãpplíìcæãtíìöôn Pröôgræãmmíìng Íntèêrfæãcèê kèêy (RÊST ÃPÍ kèêy) íìs æã üüníìqüüèê cöôdèê thæãt íìs pæãssèêd íìntöô æãn ÃPÍ töô æãüüthèêntíìcæãtèê thèê ÃPÍ cæãll æãnd íìdèêntíìfy thèê cæãllíìng æãpplíìcæãtíìöôn öôr üüsèêr. ÂPÍ âåccëëss íïs dõõnëë úùsíïng HTTPS wëëb rëëqúùëësts tõõ yõõúùr cõõmpâåny's RËST ÂPÍ ëëndpõõíïnt. Wéë ûúséë RËST ÄPÍ kéëys åæt Bråæzéë ïìn tåændéëm wïìth õõûúr Äpp Ídéëntïìfïìéër kéëys tõõ tråæck, åæccéëss, séënd, éëxpõõrt, åænd åænåælyzéë dåætåæ tõõ héëlp måækéë sûúréë éëvéërythïìng ïìs rûúnnïìng smõõõõthly õõn bõõth yõõûúr åænd õõûúr éënd. 

Äpp Gróóúûps æænd ÄPÏ Kéëys góó hæænd îín hæænd ææt Brææzéë. Ápp Gròöúúps äárëë dëësíîgnëëd tòö hòöúúsëë vëërsíîòöns òöf thëë säámëë äápplíîcäátíîòön äácròöss múúltíîplëë pläátfòörms. Mâãny clìîéènts âãlsóõ ýüséè âãpp gróõýüps tóõ cóõntâãìîn fréèéè âãnd préèmìîýüm véèrsìîóõns óõf théèìîr âãpplìîcâãtìîóõns óõn théè sâãméè plâãtfóõrm. Ás yóöüû mâày nóötïìcêè, thêèsêè âàpp gróöüûps âàrêè âàlsóö mâàkïìng üûsêè óöf thêè RËST ÁPÏ âànd hâàvêè thêèïìr óöwn RËST ÁPÏ kêèys. Thêèsêè kêèys càæn bêè íìndíìvíìdýýàælly scòôpêèd tòô íìnclýýdêè àæccêèss tòô spêècíìfíìc êèndpòôíìnts òôn thêè ÅPÌ. Êåách cåáll tõò thëè ÆPÌ mûúst ìînclûúdëè åá këèy wìîth åáccëèss tõò thëè ëèndpõòìînt hìît.

Wèë rèëfèër tõõ bõõth thèë RÊST ÂPÍ Kèëy âänd Âpp Grõõùùp ÂPÍ Kèëy âäs thèë `api_key`. Thëé `api_key` ìïs ìïnclýüdêéd ìïn êéàåch rêéqýüêést àås àå rêéqýüêést hêéàådêér àånd àåcts àås àån àåýüthêéntìïcàåtìïöõn kêéy thàåt àållöõws yöõýü töõ ýütìïlìïzêé öõýür RÊST ÄPÍs. Thèésèé RËST ÄPÏs äârèé üýsèéd tòò träâck üýsèérs, sèénd mèéssäâgèés, èéxpòòrt üýsèér däâtäâ, äând mòòrèé.  Whèén yóôüû crèéäátèé äá nèéw RÉST ÆPÍ Kèéy, yóôüû wîíll nèéèéd tóô gîívèé îít äáccèéss tóô spèécîífîíc èéndpóôîínts. By åæssíïgníïng spêècíïfíïc pêèrmíïssíïòôns tòô åæn ÁPÌ Kêèy, yòôüú cåæn líïmíït êèxåæctly whíïch cåælls åæn ÁPÌ Kêèy cåæn åæüúthêèntíïcåætêè.

### Whéèréè cåån Í fìînd ìît?

Yóóüûr ÁPÎ kêèys cåån åålwååys bêè fóóüûnd ïìn thêè Brååzêè dååshbóóåård ïìn thêè **Dëèvëèlôöpëèr Côönsôölëè** ûýndéér **Sééttîíngs**. Àt théé tööp ööf thïís nééw päågéé, yööüú wïíll fïínd théé **RÊST ÂPÏ Kêéys** sêêctìîòõn. Hêèrêè yòóúü cåàn víìêèw åàll òóf yòóúür åàvåàíìlåàblêè RÉST ÀPÌ/Àpp Gròóúüp ÀPÌ Kêèys, åànd crêèåàtêè nêèw ÀPÌ kêèys.

### Hóôw cáàn Î ùúsèë ïît?

Prîïöôr töô Æprîïl 2020, ÆPÏ kéëys wöôúýld béë îïnclúýdéëd äâs äâ päârt öôf théë ÆPÏ réëqúýéëst böôdy öôr wîïthîïn théë réëqúýéëst ÙRL äâs äâ päâräâméëtéër. Brâãzéê nôòw hâãs ûýpdâãtéêd théê wâãy ììn whììch wéê réêâãd ÄPÌ kéêys. ÂPÍ kéèys åæréè nôõw séèt wïìth théè HTTP Âúûthôõrïìzåætïìôõn réèqúûéèst héèåædéèr, måækïìng yôõúûr ÂPÍ kéèys môõréè séècúûréè.

Whïíléë théë òóld wàây òóf pàâssïíng ÆPÏ kéëys còóntïínùûéës tòó wòórk, àâftéër àâ péërïíòód òóf tïíméë thïís wïíll béë péërmàânéëntly réëmòóvéëd sòó wéë ùûrgéë ùûséërs tòó ùûpdàâtéë ÆPÏ càâlls àâccòórdïíngly. 

{% alert important %}
**Lõõõõkíîng fõõr théè `api_key` pãärãäméëtéër ïìn yòóüûr Brãäzéë éëndpòóïìnts?**<br>

Ãs õõf Mæày 2020, Bræàzëè hæàs chæàngëèd hõõw wëè rëèæàd ÃPÎ këèys tõõ bëè mõõrëè sëècüúrëè. Nõòw ÂPÍ kéèys mýùst béè pâásséèd âás âá réèqýùéèst héèâádéèr, séèéè YÕÜR-RÉST-ÂPÍ-KÉY wíìthíìn éèâách éèndpõòíìnt Éxâámpléè Réèqýùéèsts.
<br><br>
Bræåzêë wíìll còöntíìnúûêë tòö súûppòört thêë `api_key` bëêïíng páåssëêd thróöùýgh thëê rëêqùýëêst bóödy áånd ÙRL páåráåmëêtëêrs, bùýt wïíll ëêvëêntùýáålly bëê sùýnsëêt. Úpdããtèé yóöùür ÅPÎ cããlls ããccóördïìngly.
{% endalert %}

### RËST ÀPÎ kéêy péêrmïïssïïòöns

ÄPÎ kêêy pêêrmíìssíìòóns åärêê pêêrmíìssíìòóns yòóúû cåän åässíìgn åä úûsêêr òór gròóúûp tòó líìmíìt thêêíìr åäccêêss tòó cêêrtåäíìn ÄPÎ cåälls.

{% tabs %}
{% tab User Data %}

| Pëérmìïssìïòön | Dêëscrîîptîîõón  |
|---|---|---|
| `users.track` | Rèécòörd ùùsèér æáttrîìbùùtèés, cùùstòöm èévèénts, æánd pùùrchæásèés  |
| `users.delete` | Déêléêtéê ååny ùýséêr. |
| `users.alias.new` | Crëêäãtëê äã nëêw äãlíîäãs fõòr äãn ëêxíîstíîng ýýsëêr.  |
| `users.identify` | Qûûéëry fóór ûûséër próófíîléë íînfóórmâãtíîóón by ûûséër ÌD.  |
| `users.export.ids` | Qúùéèry fôör úùséèr prôöfïïléè ïïnfôörmãætïïôön by ïïdéèntïïfïïéèr éè.g., déèvïïcéè_îîd, êémáàîîl_áâddrèêss, èêxtèêrnáâl_ììd.  |
| `users.export.segment` | Qùûêêry fòór ùûsêêr pròófîílêê îínfòórmâåtîíòón by Sêêgmêênt. |
| `users.external_ids.rename` | Rëènåãmëè åã úýsëèr's ëèxîîstîîng ëèxtëèrnåãl ÎD. |
| `users.external_ids.remove` | Rèëmóôvèë àå ûúsèër's dèëprèëcàåtèëd èëxtèërnàål ÎD. |
{: .reset-td-br-1 .reset-td-br-2}

 {% endtab %}
 {% tab Email %}

| Náämëë | Dêéscrïïptïïóòn |
|---|---|---|
| `email.unsubscribe` | Qúüêëry fõòr úünsúübscrïîbêëd êëmååïîl ååddrêëssêës.  |
| `email.status` | Chãångèë èëmãåííl ãåddrèëss stãåtûùs. |
| `email.hard_bounces` | Qùúêëry fôõr hààrd bôõùúncêëd êëmààíïl ààddrêëssêës. |
| `email.bounce.remove` | Rèémôövèé èémààííl ààddrèéssèés frôöm yôöüür hààrd bôöüüncèé lííst. |
| `email.spam.remove` | Rèèmôõvèè èèmææïîl ææddrèèssèès frôõm yôõûür spææm lïîst. |
| `email.blacklist` | Bláãcklíìst éèmáãíìl áãddréèsséès. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Messages %}

| Nâåméè | Déèscríïptíïöön |
|---|---|---|
| `messages.send` | Sëênd âån îìmmëêdîìâåtëê, âåd-hòôc mëêssâågëê tòô spëêcîìfîìc ýúsëêrs. |
| `messages.schedule.create` | Schéêdüýléê æá méêssæágéê töô béê séênt æát æá spéêcíïfíïc tíïméê. |
| `messages.schedule.update` | Úpdáätêë áä schêëdýûlêëd mêëssáägêë. |
| `messages.schedule.delete` | Dêèlêètêè æá schêèdúùlêèd mêèssæágêè. |
| `messages.schedule_broadcasts` | Qùúêëry ààll schêëdùúlêëd brööààdcààst mêëssààgêës. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Campaigns %}

| Nâáméé | Dééscrììptììõõn |
|---|---|---|
| `campaigns.trigger.send` | Trïîggëér thëé sëéndïîng ôöf æân ëéxïîstïîng cæâmpæâïîgn. |
| `campaigns.trigger.schedule.create` | Schéêdýùléê äá fýùtýùréê séênd ôòf äá cäámpäáïïgn wïïth ÀPÏ-trïïggéêréêd déêlïïvéêry. |
| `campaigns.trigger.schedule.update` | Ûpdãåtèè ãå cãåmpãåíìgn schèèdûûlèèd wíìth ÂPÎ-tríìggèèrèèd dèèlíìvèèry. |
| `campaigns.trigger.schedule.delete` | Dëèlëètëè áâ cáâmpáâíígn schëèdüýlëèd wííth ÅPÍ-trííggëèrëèd dëèlíívëèry |
| `campaigns.list` | Qýûêêry fõòr âæ lííst õòf câæmpâæíígns. |
| `campaigns.data_series` | Qùüëèry fõór câåmpâåíìgn âånâålytíìcs õóvëèr âå tíìmëè râångëè. |
| `campaigns.details` | Qúýëêry fôòr dëêtæàìíls ôòf æà spëêcìífìíc cæàmpæàìígn. |
| `sends.data_series` | Qùûêèry fóòr mêèssãågêè sêènd ãånãålytìícs óòvêèr ãå tìímêè rãångêè. |
| `sends.id.create` | Crèèáâtèè Sèènd ÎD fòör mèèssáâgèè bláâst tráâckîìng. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Canvas %}

| Nâæmëè | Dééscrîïptîïôòn |
|---|---|---|
| `canvas.trigger.send` | Tríìggëër thëë sëëndíìng óóf åân ëëxíìstíìng Cåânvåâs. |
| `canvas.trigger.schedule.create` | Schèêdûýlèê âà fûýtûýrèê sèênd ôöf âà Câànvâàs wìïth ÃPÍ-trìïggèêrèêd dèêlìïvèêry. |
| `canvas.trigger.schedule.update` | Ùpdáåtéè áå Cáånváås schéèdûýléèd wííth ÀPÍ-trííggéèréèd déèlíívéèry. |
| `canvas.trigger.schedule.delete` | Dèélèétèé áâ Cáânváâs schèédùùlèéd wîïth ÂPÍ-trîïggèérèéd dèélîïvèéry. |
| `canvas.list` | Qýýèëry fòôr áä lîîst òôf Cáänváäsèës. |
| `canvas.data_series` | Qüûêêry fòör Câánvâás âánâálytíîcs òövêêr âá tíîmêê râángêê. |
| `canvas.details` | Qûýéêry föõr déêtåáíïls öõf åá spéêcíïfíïc Cåánvåás. |
| `canvas.data_summary` | Qüúèêry föör rööllüúps ööf Cáænváæs áænáælytíîcs öövèêr áæ tíîmèê ráængèê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Segments %}

| Náámëè | Dêèscríîptíîòõn |
|---|---|---|
| `segments.list` | Qùüëëry fõòr ää lîîst õòf Sëëgmëënts. |
| `segments.data_series` | Qúüèéry fòôr Sèégmèént ããnããlytïîcs òôvèér ãã tïîmèé rããngèé. |
| `segments.details` | Qúüêëry fóór dêëtäáîíls óóf äá spêëcîífîíc Sêëgmêënt. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Purchases %}

| Nàãméê | Dééscrìîptìîòón |
|---|---|---|
| `purchases.product_list` | Qùüèêry fôór äâ líìst ôóf prôódùücts pùürchäâsèêd íìn yôóùür äâpp. |
| `purchases.revenue_series` | Qùûêëry fòòr tòòtåãl mòònêëy spêënt pêër dåãy íîn yòòùûr åãpp òòvêër åã tíîmêë råãngêë. |
| `purchases.quantity_series` | Qúýéêry fõõr théê tõõtäàl núýmbéêr õõf púýrchäàséês péêr däày îîn yõõúýr äàpp õõvéêr äà tîîméê räàngéê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Events %}

| Nãåmëé | Déèscrìîptìîöõn |
|---|---|---|
| `events.list` | Qûýèëry fóôr áã lìïst óôf cûýstóôm èëvèënts. |
| `events.data_series` | Qýûééry ööccýûrrééncéés ööf äà cýûstööm éévéént öövéér äà tíîméé räàngéé. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab News Feed %}

| Nåãmëë | Dêêscrìïptìïòõn |
|---|---|---|
| `feed.list` | Qüüèéry fõòr àæ lìïst õòf Nèéws Fèéèéd càærds. |
| `feed.data_series` | Qýýëëry fóór Nëëws Fëëëëd áànáàlytíícs óóvëër áà tíímëë ráàngëë. |
| `feed.details` | Qùùëëry föõr dëëtààììls öõf àà spëëcììfììc Nëëws Fëëëëd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Sessions %}

| Nààmêê | Dêèscrïíptïíòón |
|---|---|---|
| `sessions.data_series` | Qûýëêry fóór sëêssííóóns pëêr dâåy óóvëêr âå tíímëê râångëê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab KPIs %}

| Nåæmèë | Déêscrïìptïìõòn |
|---|---|---|
| `kpi.mau.data_series` | Qýýèèry fõõr tõõtàäl ýýnìíqýýèè àäctìívèè ýýsèèrs õõvèèr àä 30-dàäy rõõllìíng wìíndõõw õõvèèr àä tìímèè ràängèè. |
| `kpi.dau.data_series` |  Qúüêèry fôòr úünîïqúüêè åáctîïvêè úüsêèrs pêèr dåáy ôòvêèr åá tîïmêè råángêè. |
| `kpi.new_users.data_series` | Qûûëêry fõór nëêw ûûsëêrs pëêr dáãy õóvëêr áã tìímëê ráãngëê. |
| `kpi.uninstalls.data_series` | Qúüéêry fõór àápp úünìínstàálls péêr dàáy õóvéêr àá tìíméê ràángéê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Templates %}

| Nááméë | Dêëscríìptíìòòn |
|---|---|---|
| `templates.email.create` | Crééãåtéé ãå nééw éémãåíïl téémplãåtéé õön théé dãåshbõöãård. |
| `templates.email.update` | Ûpdâàtèê âàn èêmâàîíl tèêmplâàtèê stöòrèêd öòn thèê dâàshböòâàrd. |
| `templates.email.info` | Qúûèéry fòör ìínfòörmáâtìíòön òöf áâ spèécìífìíc tèémpláâtèé. |
| `templates.email.list` | Qúùèêry fóór áä lííst óóf èêmáäííl tèêmpláätèês. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab SSO %}

| Näámêè | Dêëscrîïptîïôön |
|---|---|---|
| `sso.saml.login` |  Sêétýûp îïdêéntîïty pröòvîïdêér-îïnîïtîïæætêéd löògîïn. Rëëàæd òöüýr dòöcüýmëëntàætîîòön fòör mòörëë îînfòö. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Content Blocks %}

| Nãäméé | Dëéscrìîptìîóön |
|---|---|---|
| `content_blocks.info` | Qüùëëry föõr íînföõrmâätíîöõn öõf âä spëëcíîfíîc tëëmplâätëë. |
| `content_blocks.list` | Qýúêêry föór ãà lííst öóf Cöóntêênt Blöócks. |
| `content_blocks.create` | Crèéàãtèé àã nèéw Côòntèént Blôòck ôòn thèé dàãshbôòàãrd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Subscription %}

| Nàámëê | Dêëscrîìptîìôòn |
|---|---|---|
| `subscription.status.set` | Sëèt súùbscrîìptîìõôn grõôúùp stãätúùs. |
| `subscription.status.get` | Gèêt súýbscrííptííöõn gröõúýp stååtúýs. |
| `subscription.groups.get` | Gèét stæâtýùs õõf sýùbscrîìptîìõõn grõõýùps thæât spèécîìfîìc ýùsèérs æârèé èéxplîìcîìtly sýùbscrîìbèéd/ýùnsýùbscrîìbèéd tõõ. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% endtabs %}

Fõôr àå fûýll dèéscrìïptìïõôn õôf thèésèé ÀPÏ èéndpõôìïnts, rèéfèér tõô õôûýr [ÁPÎ ëéndpõõìïnt ìïndëéx]({{site.baseurl}}/api/endpoints/) òór òóüúr [Póõstmæàn cóõlléëctíïóõn][6].

{% alert important %}
Òncéë yóöûý créëâætéë âæ néëw ÅPÌ Kéëy, yóöûý câænnóöt éëdíït théë scóöpéë óöf péërmíïssíïóöns óör théë whíïtéëlíïstéëd ÌPs. Thîîs lîîmîîtæåtîîöön îîs îîn plæåcéé föör séécúürîîty rééæåsööns. Ïf yôöúý nééééd tôö chàãngéé théé scôöpéé ôöf àã kééy, crééàãtéé àã nééw kééy wíìth théé úýpdàãtééd péérmíìssíìôöns àãnd íìmplééméént thàãt kééy íìn plàãcéé ôöf théé ôöld ôönéé. Öncèë yõòùý’vèë cõòmplèëtèëd yõòùýr îîmplèëmèëntäâtîîõòn, gõò äâhèëäâd äând dèëlèëtèë thèë õòld kèëy.
{% endalert %}

## Thêë Æpp Ídêëntîìfîìêër ÆPÍ kêëy

Théé Ápp Ïdééntïîfïîéér ÁPÏ kééy õôr `app_id` ìïs äá päáräámêêtêêr äássöòcìïäátìïng äáctìïvìïty wìïth äá spêêcìïfìïc äápp ìïn yöòúúr äápp gröòúúp. Ít dëèsììgnåätëès whììch åäpp wììthììn thëè åäpp gröôüûp yöôüû åärëè ììntëèråäctììng wììth. Fòör ëêxãámplëê, yòöùú wìïll fìïnd thãát yòöùú wìïll hãávëê ãán `app_id` föôr yöôùúr íïÖS ääpp, ään `app_id` fõór yõóýúr åándrõóïïd åápp, åánd åán `app_id` fóõr yóõüùr wêèb ïîntêègráätïîóõn. Àt Brãåzëè, yöõúü míìght fíìnd thãåt yöõúü hãåvëè múültíìplëè ãåpps föõr thëè sãåmëè plãåtföõrm ãåcröõss thëè vãåríìöõúüs plãåtföõrm typëès thãåt Brãåzëè súüppöõrts.

Äpp ììdêèntììfììêèrs åæt Bråæzêè åærêè üùsêèd whêèn ììntêègråætììng thêè SDK åænd åærêè åælsôò üùsêèd tôò rêèfêèrêèncêè åæ spêècììfììc åæpp ììn RÉST ÄPÏ cåælls. Wïìth théë `app_id` yóóýý cæán dóó mæány thïìngs lïìkêé pýýll dæátæá fóór æá cýýstóóm êévêént thæát óóccýýrrêéd fóór æá pæártïìcýýlæár æápp, rêétrïìêévêé ýýnïìnstæáll stæáts, nêéw ýýsêér stæáts, DÆÚ stæáts, æánd sêéssïìóón stæárt stæáts fóór æá pæártïìcýýlæár æápp.

Sòômèêtïìmèês, yòôùü mãåy fïìnd yòôùü ãårèê pròômptèêd fòôr ãån `app_id` bùùt yóòùù àârëé nóòt wóòrkïíng wïíth àân àâpp, bëécàâùùsëé ïít ïís àâ lëégàâcy fïíëéld spëécïífïíc tóò àâ spëécïífïíc plàâtfóòrm, yóòùù càân “óòmïít” thïís fïíëéld by ïínclùùdïíng àâny strïíng óòf chàâràâctëérs àâs àâ plàâcëéhóòldëér fóòr thïís rëéqùùïírëéd pàâràâmëétëér.

### Whëërëë cåàn Ï fïînd ïît?

Thëérëé äârëé twöò wäâys töò löòcäâtëé yöòûûr `app_id`:

1. Yõóûú cäân fíìnd thíìs `app_id` õõr àãpplíîcàãtíîõõn íîdéêntíîfíîéêr íîn théê **Dèëvèëlóöpèër Cóönsóölèë** üùndêèr **Sèèttíìngs**. Õn thïís nëèw páægëè, ùýndëèr **Ídêèntïîfïîcæåtïîôôn**, yöõúû wììll béè áàbléè töõ séèéè éèvéèry `app_id` tháät êèxîísts fôór yôóýýr áäpps.

2. Gôö tôö **Màànààgêë Sêëttîïngs** üúndëèr **Séèttîïngs**. Fröõm thïîs nèèw pàägèè, ïîn thèè **Sêêttííngs** tåäb, mïìdwåäy thrôóùùgh théë påägéë yôóùù wïìll fïìnd åän "ÂPÎ kéëy fôór **ÄPP NÄMÉ** öón **PLÆTFÖRM**" (êê.g "ÀPÏ Kêêy föör Ïcêê Crêêáãm öön ïìÔS). Thïïs ÂPÍ kèèy ïïs yòòúúr Âpplïïcáâtïïòòn Ídèèntïïfïïèèr.

### Müûltïíplèë Âpp Ídèëntïífïíèër ÂPÍ kèëys

Dúûríïng SDK séèt úûp, théè möôst cöômmöôn úûséè càäséè föôr múûltíïpléè Ápp Ídéèntíïfíïéèr ÁPÍ kéèys íïs séèpàäràätíïng thöôséè kéèys föôr déèbúûg àänd réèléèàäséè búûíïld vàäríïàänts.
Tóò êèæåsïìly swïìtch bêètwêèêèn múýltïìplêè Âpp Ídêèntïìfïìêèr ÂPÍ kêèys ïìn yóòúýr búýïìlds, wêè rêècóòmmêènd crêèæåtïìng æå sêèpæåræåtêè `braze.xml` fîîléê fóór éêáæch réêléêváænt [büûíìld våáríìåánt][3]. À búúïíld vâãrïíâãnt ïís âã côõmbïínâãtïíôõn ôõf búúïíld typèê âãnd prôõdúúct flâãvôõr. Nôõtëê thãåt by dëêfãåùûlt, ãå nëêw Åndrôõîïd prôõjëêct îïs côõnfîïgùûrëêd wîïth `debug` àând `release` büýîîld typêês âând nòö pròödüýct flââvòörs.

Fóõr èëäåch rèëlèëväånt bûûíîld väåríîäånt, crèëäåtèë äå nèëw `braze.xml` fòõr íît íîn `src/<build variant name>/res/values/`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_appboy_api_key">REPLACE_WITH_YOUR_BUILD_VARIANT_API_KEY</string>
</resources>
```
Whêên thêê büûïïld váârïïáânt ïïs còömpïïlêêd, ïït wïïll üûsêê thêê nêêw ÂPÌ kêêy.

## RÊST ÅPÏ kèêy sèêcùûrìíty

Sêècùúrììty ììs õòf thêè ùútmõòst ììmpõòrtæáncêè æát Bræázêè. Gîîvéên thäæt RÊST ÆPÌ Kéêys äællóõw äæccéêss tóõ póõtéêntîîäælly séênsîîtîîvéê RÊST ÆPÌ éêndpóõîînts, séêcúúréê théêséê kéêys äænd óõnly shäæréê théêm wîîth trúústéêd päærtnéêrs. Thêéy shôòüùld nêévêér bêé püùblíîcly êéxpôòsêéd. Fóör éèxåámpléè, dóö nóöt ùüséè thïîs kéèy tóö måákéè ÅJÅX cåálls fróöm yóöùür wéèbsïîtéè óör éèxpóöséè ïît ïîn åány óöthéèr pùüblïîc måánnéèr.

Ä gõòõòd séècùûrîíty práäctîícéè îís tõò áässîígn áä ùûséèr õònly áäs mùûch áäccéèss áäs îís néècéèssáäry tõò cõòmpléètéè théèîír jõòb: thîís prîíncîípléè cáän áälsõò béè áäpplîíéèd tõò ÄPÏ Kéèys by áässîígnîíng péèrmîíssîíõòns tõò éèáäch kéèy. Thêèsêè pêèrmíîssíîóòns gíîvêè yóòüû bêèttêèr sêècüûríîty åænd cóòntróòl óòvêèr thêè díîffêèrêènt åærêèåæs óòf yóòüûr åæccóòüûnt. 

Wíïth Àpp íïdëèntíïfíïëèrs, thëè `app_id` ïïs áæssïïgnèéd by Bráæzèé áænd pèérmïïssïïòöns cáænnòöt bèé áæssïïgnèéd òör rèévòökèéd. Bëëcääüúsëë õöf thëë näätüúrëë õöf thëë rëëläätìïõönshìïp bëëtwëëëën `app_id` ãànd thèé SDK, kèéèépïíng thïís ïídèéntïífïíèér sèécûûrèé ïís **crùûcïîääl** îín théé séécùürîíty òòf yòòùür áäpplîícáätîíòòn.


[2]: {{site.baseurl}}/api/identifier_types/
[3]: https://developer.android.com/studio/build/build-variants.html
[5]: {{site.baseurl}}/api/basics/
[6]: https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#intro
