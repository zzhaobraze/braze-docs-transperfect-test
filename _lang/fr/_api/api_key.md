---
nav_title: "ÆPÎ Kèéy Övèérvïíèéw"
article_title: RÉST ÁPÏ Kêëy Óvêërvîíêëw
page_order: 2.1
description: "Thììs rèèfèèrèèncèè áærtììclèè côóvèèrs thèè côóncèèpt ôóf ÁPÏ kèèys, wháæt thèèy áærèè ûùsèèd fôór, áænd hôów thèèy áærèè ûùsèèd." 
page_type: reference

---

# RËST ÆPÌ këèy õövëèrvïìëèw

>  Thîïs rëëfëërëëncëë åärtîïclëë cóóvëërs twóó óóf thëë thrëëëë måäîïn typëës óóf këëys yóóýý wîïll sëëëë åät Bråäzëë, thëë RÊST ÀPÌ Këëy óór Àpp Gróóýýp ÀPÌ Këëy, rëëfëërrëëd tóó åäs thëë `api_key`, àànd théë Åpp Îdéëntìîfìîéër Kéëy, knôõwn ààs théë `app_id`, âás wèêll âás whâát thèêsèê kèêys âárèê, hôów thèêy âárèê úúsèêd âát Brâázèê, thèêïír pèêrmïíssïíôóns âánd hôów tôó kèêèêp thèêm sèêcúúrèê. 

Ín âäddïïtïïóön tóö thëësëë këëys, thëërëë âälsóö ëëxïïsts âä thïïrd typëë óöf këëy câällëëd Ídëëntïïfïïëër Këëys thâät câän bëë ùúsëëd tóö rëëfëërëëncëë spëëcïïfïïc thïïngs lïïkëë tëëmplâätëës, Câänvâäsëës, câämpâäïïgns, Cóöntëënt Câärds, âänd sëëgmëënts fróöm thëë ÂPÍ. Föõr möõrèè ìïnföõrmæátìïöõn, rèèfèèr töõ [ÅPÎ Îdèêntíífííèêr typèês][2].

## Whäàt ïís äà RËST ÆPÎ kêéy/äàpp gróõúýp ÆPÎ kêéy?

Ä RËST Äpplïïcáætïïôôn Prôôgráæmmïïng Ìntëêrfáæcëê këêy (RËST ÄPÌ këêy) ïïs áæ úûnïïqúûëê côôdëê tháæt ïïs páæssëêd ïïntôô áæn ÄPÌ tôô áæúûthëêntïïcáætëê thëê ÄPÌ cáæll áænd ïïdëêntïïfy thëê cáællïïng áæpplïïcáætïïôôn ôôr úûsëêr. ÂPÍ ääccééss îìs döònéé ûùsîìng HTTPS wééb rééqûùéésts töò yöòûùr cöòmpääny's RÈST ÂPÍ ééndpöòîìnt. Wêë üüsêë RËST ÁPÌ kêëys ãæt Brãæzêë îín tãændêëm wîíth óöüür Ápp Ìdêëntîífîíêër kêëys tóö trãæck, ãæccêëss, sêënd, êëxpóört, ãænd ãænãælyzêë dãætãæ tóö hêëlp mãækêë süürêë êëvêërythîíng îís rüünnîíng smóöóöthly óön bóöth yóöüür ãænd óöüür êënd. 

Àpp Gröõûüps àànd ÀPÏ Kêëys göõ hàànd íîn hàànd ààt Brààzêë. Åpp Gröõûüps æærëé dëésïïgnëéd töõ höõûüsëé vëérsïïöõns öõf thëé sææmëé ææpplïïcæætïïöõn ææcröõss mûültïïplëé plæætföõrms. Mäæny clîïéènts äælsöö ýüséè äæpp grööýüps töö cööntäæîïn fréèéè äænd préèmîïýüm véèrsîïööns ööf théèîïr äæpplîïcäætîïööns öön théè säæméè pläætföörm. Ás yóóúû mâày nóótïîcëê, thëêsëê âàpp gróóúûps âàrëê âàlsóó mâàkïîng úûsëê óóf thëê RËST ÁPÏ âànd hâàvëê thëêïîr óówn RËST ÁPÏ këêys. Thèësèë kèëys cäãn bèë ìïndìïvìïdüýäãlly scôôpèëd tôô ìïnclüýdèë äãccèëss tôô spèëcìïfìïc èëndpôôìïnts ôôn thèë ÆPÍ. Èâãch câãll tòô thëê ÂPÍ müüst ïînclüüdëê âã këêy wïîth âãccëêss tòô thëê ëêndpòôïînt hïît.

Wèè rèèfèèr töô böôth thèè RÈST ÁPÏ Kèèy àånd Ápp Gröôúýp ÁPÏ Kèèy àås thèè `api_key`. Thëé `api_key` ìïs ìïnclúüdêéd ìïn êéæäch rêéqúüêést æäs æä rêéqúüêést hêéæädêér æänd æäcts æäs æän æäúüthêéntìïcæätìïòõn kêéy thæät æällòõws yòõúü tòõ úütìïlìïzêé òõúür RÉST ÄPÌs. Thëèsëè RÈST ÅPÍs âårëè ùùsëèd tòô trâåck ùùsëèrs, sëènd mëèssâågëès, ëèxpòôrt ùùsëèr dâåtâå, âånd mòôrëè.  Whèën yöõûú crèëæàtèë æà nèëw RÊST ÄPÏ Kèëy, yöõûú wììll nèëèëd töõ gììvèë ììt æàccèëss töõ spèëcììfììc èëndpöõììnts. By äæssîîgnîîng spéêcîîfîîc péêrmîîssîîôõns tôõ äæn ÂPÎ Kéêy, yôõùý cäæn lîîmîît éêxäæctly whîîch cäælls äæn ÂPÎ Kéêy cäæn äæùýthéêntîîcäætéê.

### Whêèrêè cåàn Ï fíìnd íìt?

Yòöüùr ÀPÌ kééys câán âálwâáys béé fòöüùnd îîn théé Brâázéé dâáshbòöâárd îîn théé **Dèévèélôòpèér Côònsôòlèé** ùùndëér **Séëttîíngs**. Åt théë tòòp òòf thîìs néëw pâägéë, yòòûû wîìll fîìnd théë **RËST ÃPÍ Kêëys** sééctìîôön. Hééréé yöóýý cäæn vìíééw äæll öóf yöóýýr äæväæìíläæbléé RÉST ÃPÎ/Ãpp Gröóýýp ÃPÎ Kééys, äænd crééäætéé nééw ÃPÎ kééys.

### Hòów cäån Í ýûséê îît?

Prìîòör tòö Æprìîl 2020, ÆPÌ kèèys wòöûüld bèè ìînclûüdèèd äãs äã päãrt òöf thèè ÆPÌ rèèqûüèèst bòödy òör wìîthìîn thèè rèèqûüèèst ÚRL äãs äã päãräãmèètèèr. Bræåzêé nöõw hæås üûpdæåtêéd thêé wæåy ïìn whïìch wêé rêéæåd ÅPÌ kêéys. ÁPÏ këëys âárëë nõôw sëët wìíth thëë HTTP Áüûthõôrìízâátìíõôn rëëqüûëëst hëëâádëër, mâákìíng yõôüûr ÁPÏ këëys mõôrëë sëëcüûrëë.

Whììlêë thêë õòld wæày õòf pæàssììng ÁPÍ kêëys cõòntììnýýêës tõò wõòrk, æàftêër æà pêërììõòd õòf tììmêë thììs wììll bêë pêërmæànêëntly rêëmõòvêëd sõò wêë ýýrgêë ýýsêërs tõò ýýpdæàtêë ÁPÍ cæàlls æàccõòrdììngly. 

{% alert important %}
**Löóöókìîng föór thêé `api_key` pâârââmêétêér íìn yôòûùr Brââzêé êéndpôòíìnts?**<br>

Ás ööf Mâáy 2020, Brâázéé hâás châángééd hööw wéé rééâád ÁPÎ kééys töö béé mööréé séécûüréé. Nõöw ÆPÏ kêêys múùst bêê pææssêêd ææs ææ rêêqúùêêst hêêæædêêr, sêêêê YÕÜR-RÈST-ÆPÏ-KÈY wìîthìîn êêææch êêndpõöìînt Èxææmplêê Rêêqúùêêsts.
<br><br>
Bræãzêé wíîll cöõntíînýùêé töõ sýùppöõrt thêé `api_key` bêéïíng pæâssêéd thròòýûgh thêé rêéqýûêést bòòdy æând ÛRL pæâræâmêétêérs, býût wïíll êévêéntýûæâlly bêé sýûnsêét. Ûpdàâtêë yòöùýr ÁPÏ càâlls àâccòördîïngly.
{% endalert %}

### RÉST ÄPÎ kêêy pêêrmîïssîïõòns

ÅPÍ kêëy pêërmïíssïíöóns àärêë pêërmïíssïíöóns yöóûû càän àässïígn àä ûûsêër öór gröóûûp töó lïímïít thêëïír àäccêëss töó cêërtàäïín ÅPÍ càälls.

{% tabs %}
{% tab User Data %}

| Péérmîîssîîõõn | Dëèscríïptíïòón  |
|---|---|---|
| `users.track` | Rêêcõörd ûûsêêr ãåttrìíbûûtêês, cûûstõöm êêvêênts, ãånd pûûrchãåsêês  |
| `users.delete` | Dêélêétêé ààny úúsêér. |
| `users.alias.new` | Crèëâätèë âä nèëw âälîîâäs fõór âän èëxîîstîîng úúsèër.  |
| `users.identify` | Qüùêêry föör üùsêêr prööfïílêê ïínföörmâàtïíöön by üùsêêr ÍD.  |
| `users.export.ids` | Qúýëéry fõór úýsëér prõófìîlëé ìînfõórmáåtìîõón by ìîdëéntìîfìîëér ëé.g., dëévìîcëé_îïd, êèmåáîïl_ãáddréêss, éêxtéêrnãál_íîd.  |
| `users.export.segment` | Qûýéêry fòór ûýséêr pròófíìléê íìnfòórmæátíìòón by Séêgméênt. |
| `users.external_ids.rename` | Rèênæåmèê æå ýùsèêr's èêxïìstïìng èêxtèêrnæål ÍD. |
| `users.external_ids.remove` | Rëêmôòvëê åâ ùûsëêr's dëêprëêcåâtëêd ëêxtëêrnåâl ÌD. |
{: .reset-td-br-1 .reset-td-br-2}

 {% endtab %}
 {% tab Email %}

| Nàáméë | Dëêscríîptíîöôn |
|---|---|---|
| `email.unsubscribe` | Qüýêéry fòór üýnsüýbscrîìbêéd êémàâîìl àâddrêéssêés.  |
| `email.status` | Chäãngêè êèmäãíïl äãddrêèss stäãtýùs. |
| `email.hard_bounces` | Qýùêêry fôör häãrd bôöýùncêêd êêmäãìîl äãddrêêssêês. |
| `email.bounce.remove` | Réémóòvéé éémãáìîl ãáddréésséés fróòm yóòüûr hãárd bóòüûncéé lìîst. |
| `email.spam.remove` | Rëémöövëé ëémæåìíl æåddrëéssëés frööm yööýúr spæåm lìíst. |
| `email.blacklist` | Blàácklíìst èémàáíìl àáddrèéssèés. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Messages %}

| Näämèé | Dèéscrìïptìïôôn |
|---|---|---|
| `messages.send` | Séènd ããn ïïmméèdïïããtéè, ããd-hòõc méèssããgéè tòõ spéècïïfïïc ûüséèrs. |
| `messages.schedule.create` | Schëêdûülëê âå mëêssâågëê tóò bëê sëênt âåt âå spëêcïîfïîc tïîmëê. |
| `messages.schedule.update` | Ùpdãátëè ãá schëèdýúlëèd mëèssãágëè. |
| `messages.schedule.delete` | Dêëlêëtêë âä schêëdýülêëd mêëssâägêë. |
| `messages.schedule_broadcasts` | Qúúëëry ãáll schëëdúúlëëd bròöãádcãást mëëssãágëës. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Campaigns %}

| Nåæméé | Dêéscrììptììóón |
|---|---|---|
| `campaigns.trigger.send` | Trììggèêr thèê sèêndììng öòf äân èêxììstììng cäâmpäâììgn. |
| `campaigns.trigger.schedule.create` | Schêèdüûlêè ãã füûtüûrêè sêènd òõf ãã cããmpããîïgn wîïth ÄPÎ-trîïggêèrêèd dêèlîïvêèry. |
| `campaigns.trigger.schedule.update` | Ûpdáãtëë áã cáãmpáãíìgn schëëdýúlëëd wíìth ÁPÌ-tríìggëërëëd dëëlíìvëëry. |
| `campaigns.trigger.schedule.delete` | Dëëlëëtëë äæ cäæmpäæìîgn schëëdüûlëëd wìîth ÁPÎ-trìîggëërëëd dëëlìîvëëry |
| `campaigns.list` | Qûýèèry fóõr æá líîst óõf cæámpæáíîgns. |
| `campaigns.data_series` | Qùùëéry fõör càãmpàãîîgn àãnàãlytîîcs õövëér àã tîîmëé ràãngëé. |
| `campaigns.details` | Qúúééry fôõr déétåäìíls ôõf åä spéécìífìíc cåämpåäìígn. |
| `sends.data_series` | Qùýèèry föôr mèèssåàgèè sèènd åànåàlytïïcs öôvèèr åà tïïmèè råàngèè. |
| `sends.id.create` | Crêêããtêê Sêênd ÏD fòõr mêêssããgêê blããst trããckîíng. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Canvas %}

| Nààmèë | Dêêscríìptíìõôn |
|---|---|---|
| `canvas.trigger.send` | Trìïggêér thêé sêéndìïng óòf æân êéxìïstìïng Cæânvæâs. |
| `canvas.trigger.schedule.create` | Schêêdýùlêê äæ fýùtýùrêê sêênd óóf äæ Cäænväæs wîíth ÁPÍ-trîíggêêrêêd dêêlîívêêry. |
| `canvas.trigger.schedule.update` | Ùpdæátèê æá Cæánvæás schèêdûýlèêd wîìth ÂPÏ-trîìggèêrèêd dèêlîìvèêry. |
| `canvas.trigger.schedule.delete` | Dèëlèëtèë åæ Cåænvåæs schèëdúùlèëd wìïth ÃPÏ-trìïggèërèëd dèëlìïvèëry. |
| `canvas.list` | Qüùëëry fóör áå líîst óöf Cáånváåsëës. |
| `canvas.data_series` | Qúüèëry fôòr Càånvàås àånàålytîícs ôòvèër àå tîímèë ràångèë. |
| `canvas.details` | Qúýëéry fòör dëétàâìïls òöf àâ spëécìïfìïc Càânvàâs. |
| `canvas.data_summary` | Qùúééry fóór róóllùúps óóf Cåänvåäs åänåälytïìcs óóvéér åä tïìméé råängéé. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Segments %}

| Nâãmêè | Dééscrîîptîîôõn |
|---|---|---|
| `segments.list` | Qùýêêry fõôr äå lïïst õôf Sêêgmêênts. |
| `segments.data_series` | Qúýéêry fôör Séêgméênt äånäålytîïcs ôövéêr äå tîïméê räångéê. |
| `segments.details` | Qýýéëry fòõr déëtáãïíls òõf áã spéëcïífïíc Séëgméënt. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Purchases %}

| Nææméé | Déëscrïîptïîõôn |
|---|---|---|
| `purchases.product_list` | Qùùêèry fôôr àã líîst ôôf prôôdùùcts pùùrchàãsêèd íîn yôôùùr àãpp. |
| `purchases.revenue_series` | Qùüèéry fòór tòótåäl mòónèéy spèént pèér dåäy ïïn yòóùür åäpp òóvèér åä tïïmèé råängèé. |
| `purchases.quantity_series` | Qýüëèry fõòr thëè tõòtããl nýümbëèr õòf pýürchããsëès pëèr dããy ïín yõòýür ããpp õòvëèr ãã tïímëè rããngëè. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Events %}

| Nååmêê | Dèéscrìíptìíõön |
|---|---|---|
| `events.list` | Qúüêêry fòôr àâ lííst òôf cúüstòôm êêvêênts. |
| `events.data_series` | Qùûèëry ôóccùûrrèëncèës ôóf àâ cùûstôóm èëvèënt ôóvèër àâ tïîmèë ràângèë. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab News Feed %}

| Náæmëë | Déêscrììptììöòn |
|---|---|---|
| `feed.list` | Qýûèèry fòõr áâ lìíst òõf Nèèws Fèèèèd cáârds. |
| `feed.data_series` | Qüüèêry fòõr Nèêws Fèêèêd àänàälytîîcs òõvèêr àä tîîmèê ràängèê. |
| `feed.details` | Qùýêèry fôór dêètææíïls ôóf ææ spêècíïfíïc Nêèws Fêèêèd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Sessions %}

| Näãmèê | Dêêscrìíptìíòön |
|---|---|---|
| `sessions.data_series` | Qüýèëry föör sèëssíïööns pèër dâáy öövèër âá tíïmèë râángèë. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab KPIs %}

| Nàãmèê | Déêscrîìptîìöõn |
|---|---|---|
| `kpi.mau.data_series` | Qùýèëry fõör tõötæäl ùýnììqùýèë æäctììvèë ùýsèërs õövèër æä 30-dæäy rõöllììng wììndõöw õövèër æä tììmèë ræängèë. |
| `kpi.dau.data_series` |  Qüûèêry fôõr üûnííqüûèê åãctíívèê üûsèêrs pèêr dåãy ôõvèêr åã tíímèê råãngèê. |
| `kpi.new_users.data_series` | Qûûêëry fôór nêëw ûûsêërs pêër däây ôóvêër äâ tîïmêë räângêë. |
| `kpi.uninstalls.data_series` | Qýùéëry fôõr äâpp ýùnïînstäâlls péër däây ôõvéër äâ tïîméë räângéë. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Templates %}

| Náámèê | Dêéscrìîptìîöôn |
|---|---|---|
| `templates.email.create` | Créèåátéè åá néèw éèmåáïîl téèmplåátéè õòn théè dåáshbõòåárd. |
| `templates.email.update` | Üpdãâtèé ãân èémãâîïl tèémplãâtèé stóôrèéd óôn thèé dãâshbóôãârd. |
| `templates.email.info` | Qùùêèry fòór îínfòórmàätîíòón òóf àä spêècîífîíc têèmplàätêè. |
| `templates.email.list` | Qúýèéry fõõr ää lïïst õõf èémääïïl tèémpläätèés. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab SSO %}

| Näámëè | Déèscrìîptìîôôn |
|---|---|---|
| `sso.saml.login` |  Sëêtúüp íïdëêntíïty prôövíïdëêr-íïníïtíïäàtëêd lôögíïn. Rééæád öôùýr döôcùýmééntæátïîöôn föôr möôréé ïînföô. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Content Blocks %}

| Næàméé | Dëèscrìíptìíôôn |
|---|---|---|
| `content_blocks.info` | Qüüëéry fôör îïnfôörmäätîïôön ôöf ää spëécîïfîïc tëémpläätëé. |
| `content_blocks.list` | Qüûéëry fòör àæ lïîst òöf Còöntéënt Blòöcks. |
| `content_blocks.create` | Créëæætéë ææ néëw Cööntéënt Blööck öön théë dææshbööæærd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Subscription %}

| Nãámëè | Dëêscrïîptïîõõn |
|---|---|---|
| `subscription.status.set` | Sèét súýbscrìîptìîóòn gróòúýp stâåtúýs. |
| `subscription.status.get` | Géèt sûýbscrííptííòón gròóûýp stââtûýs. |
| `subscription.groups.get` | Gêët stæåtùùs õóf sùùbscrïìptïìõón grõóùùps thæåt spêëcïìfïìc ùùsêërs æårêë êëxplïìcïìtly sùùbscrïìbêëd/ùùnsùùbscrïìbêëd tõó. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% endtabs %}

Fòõr áä füùll dëêscrííptííòõn òõf thëêsëê ÄPÌ ëêndpòõíínts, rëêfëêr tòõ òõüùr [ÄPÏ éèndpòöíînt íîndéèx]({{site.baseurl}}/api/endpoints/) öór öóúùr [Póôstmáân cóôllêéctïìóôn][6].

{% alert important %}
Óncêè yóóùü crêèáâtêè áâ nêèw ÁPÌ Kêèy, yóóùü cáânnóót êèdíït thêè scóópêè óóf pêèrmíïssíïóóns óór thêè whíïtêèlíïstêèd ÌPs. Thíîs líîmíîtåàtíîõôn íîs íîn plåàcéé fõôr séécýûríîty rééåàsõôns. Ïf yòôùú néèéèd tòô chãàngéè théè scòôpéè òôf ãà kéèy, créèãàtéè ãà néèw kéèy wïìth théè ùúpdãàtéèd péèrmïìssïìòôns ãànd ïìmpléèméènt thãàt kéèy ïìn plãàcéè òôf théè òôld òônéè. Ôncêë yòôúý’vêë còômplêëtêëd yòôúýr íìmplêëmêëntååtíìòôn, gòô ååhêëååd åånd dêëlêëtêë thêë òôld kêëy.
{% endalert %}

## Thëê Àpp Ìdëêntïífïíëêr ÀPÌ këêy

Thèë Âpp Ïdèëntîìfîìèër ÂPÏ kèëy õör `app_id` ììs ãä pãärãäméêtéêr ãässôõcììãätììng ãäctììvììty wììth ãä spéêcììfììc ãäpp ììn yôõùür ãäpp grôõùüp. Ît dèésïîgnãåtèés whïîch ãåpp wïîthïîn thèé ãåpp grôóûýp yôóûý ãårèé ïîntèérãåctïîng wïîth. Fõór èéxåãmplèé, yõóùù wìîll fìînd thåãt yõóùù wìîll håãvèé åãn `app_id` fôõr yôõüùr îìÖS ãäpp, ãän `app_id` fòör yòöüür àåndròöìíd àåpp, àånd àån `app_id` fóõr yóõûür wèèb íîntèègrãätíîóõn. Ãt Brâàzéê, yôóúý míìght fíìnd thâàt yôóúý hâàvéê múýltíìpléê âàpps fôór théê sâàméê plâàtfôórm âàcrôóss théê vâàríìôóúýs plâàtfôórm typéês thâàt Brâàzéê súýppôórts.

Âpp îîdëèntîîfîîëèrs äåt Bräåzëè äårëè ýúsëèd whëèn îîntëègräåtîîng thëè SDK äånd äårëè äålsóó ýúsëèd tóó rëèfëèrëèncëè äå spëècîîfîîc äåpp îîn RÊST ÂPÏ cäålls. Wíïth thëë `app_id` yòöüú cáãn dòö máãny thíìngs líìkêé püúll dáãtáã fòör áã cüústòöm êévêént tháãt òöccüúrrêéd fòör áã páãrtíìcüúláãr áãpp, rêétríìêévêé üúníìnstáãll stáãts, nêéw üúsêér stáãts, DÂÙ stáãts, áãnd sêéssíìòön stáãrt stáãts fòör áã páãrtíìcüúláãr áãpp.

Sôómêétíïmêés, yôóúû mäåy fíïnd yôóúû äårêé prôómptêéd fôór äån `app_id` bùùt yôõùù æàrêé nôõt wôõrkîìng wîìth æàn æàpp, bêécæàùùsêé îìt îìs æà lêégæàcy fîìêéld spêécîìfîìc tôõ æà spêécîìfîìc plæàtfôõrm, yôõùù cæàn “ôõmîìt” thîìs fîìêéld by îìnclùùdîìng æàny strîìng ôõf chæàræàctêérs æàs æà plæàcêéhôõldêér fôõr thîìs rêéqùùîìrêéd pæàræàmêétêér.

### Whéêréê cäån Î fïínd ïít?

Thèêrèê áãrèê twõö wáãys tõö lõöcáãtèê yõöúýr `app_id`:

1. Yôóùü cææn fìînd thìîs `app_id` ôòr æãpplìícæãtìíôòn ìídèéntìífìíèér ìín thèé **Dêëvêëlõöpêër Cõönsõölêë** ýýndèër **Sèêttîïngs**. Ön thïìs nêéw päågêé, üúndêér **Îdëëntïîfïîcãætïîôón**, yöóùû wìïll bêê æãblêê töó sêêêê êêvêêry `app_id` thàât êëxïïsts föòr yöòýür àâpps.

2. Göô töô **Máänáägéê Séêttîïngs** úúndéër **Sèèttîìngs**. Frôóm thìïs nêëw pããgêë, ìïn thêë **Sëéttîìngs** táäb, mïïdwáäy thröóüügh thëè páägëè yöóüü wïïll fïïnd áän "ÀPÌ këèy föór **ÁPP NÁMÉ** óòn **PLÃTFÓRM**" (éé.g "ÃPÍ Kééy föór Ícéé Crééâãm öón îíÒS). Thïís ÅPÌ kèêy ïís yòõýúr Åpplïícäätïíòõn Ìdèêntïífïíèêr.

### Mûýltïïpléê Æpp Îdéêntïïfïïéêr ÆPÎ kéêys

Dúýríîng SDK séêt úýp, théê mõôst cõômmõôn úýséê cåàséê fõôr múýltíîpléê Åpp Ïdéêntíîfíîéêr ÅPÏ kéêys íîs séêpåàråàtíîng thõôséê kéêys fõôr déêbúýg åànd réêléêåàséê búýíîld våàríîåànts.
Tõõ ëêååsîíly swîítch bëêtwëêëên mûùltîíplëê Àpp Ídëêntîífîíëêr ÀPÍ këêys îín yõõûùr bûùîílds, wëê rëêcõõmmëênd crëêååtîíng åå sëêpåårååtëê `braze.xml` fíìlèë fóôr èëáâch rèëlèëváânt [búüìïld vâårìïâånt][3]. Ä býüîíld váârîíáânt îís áâ cóòmbîínáâtîíóòn óòf býüîíld typêë áând próòdýüct fláâvóòr. Nõòtèê thâæt by dèêfâæùýlt, âæ nèêw Ándrõòïíd prõòjèêct ïís cõònfïígùýrèêd wïíth `debug` åând `release` büúííld typëës áánd nóò próòdüúct fláávóòrs.

Fòór èèåách rèèlèèvåánt bùùïíld våárïíåánt, crèèåátèè åá nèèw `braze.xml` föôr îît îîn `src/<build variant name>/res/values/`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_appboy_api_key">REPLACE_WITH_YOUR_BUILD_VARIANT_API_KEY</string>
</resources>
```
Whêën thêë büýííld vâãrííâãnt íís côómpíílêëd, íít wííll üýsêë thêë nêëw ÆPÎ kêëy.

## RÈST ÅPÎ kêêy sêêcûüríìty

Sêëcùürîîty îîs öòf thêë ùütmöòst îîmpöòrtáâncêë áât Bráâzêë. Gíîvéén thæàt RÉST ÃPÍ Kééys æàllõöw æàccééss tõö põötééntíîæàlly séénsíîtíîvéé RÉST ÃPÍ ééndpõöíînts, séécýúréé thééséé kééys æànd õönly shæàréé théém wíîth trýústééd pæàrtnéérs. Thèéy shòòýúld nèévèér bèé pýúblíïcly èéxpòòsèéd. Fóör èëxàæmplèë, dóö nóöt üýsèë thîîs kèëy tóö màækèë ÅJÅX càælls fróöm yóöüýr wèëbsîîtèë óör èëxpóösèë îît îîn àæny óöthèër püýblîîc màænnèër.

Å góóóód séécùýrïíty pràâctïícéé ïís tóó àâssïígn àâ ùýséér óónly àâs mùých àâccééss àâs ïís néécééssàâry tóó cóómpléétéé thééïír jóób: thïís prïíncïípléé càân àâlsóó béé àâpplïíééd tóó ÅPÏ Kééys by àâssïígnïíng péérmïíssïíóóns tóó ééàâch kééy. Thèèsèè pèèrmíìssíìôóns gíìvèè yôóýý bèèttèèr sèècýýríìty äánd côóntrôól ôóvèèr thèè díìffèèrèènt äárèèäás ôóf yôóýýr äáccôóýýnt. 

Wííth Ãpp íídëëntíífííëërs, thëë `app_id` ïïs ææssïïgnêëd by Brææzêë æænd pêërmïïssïïôöns cæænnôöt bêë ææssïïgnêëd ôör rêëvôökêëd. Bëécââýüsëé óóf thëé nââtýürëé óóf thëé rëélââtíïóónshíïp bëétwëéëén `app_id` àând thèê SDK, kèêèêpíîng thíîs íîdèêntíîfíîèêr sèêcûýrèê íîs **crûýcîïàål** ïìn théé séécýürïìty òõf yòõýür àäpplïìcàätïìòõn.


[2]: {{site.baseurl}}/api/identifier_types/
[3]: https://developer.android.com/studio/build/build-variants.html
[5]: {{site.baseurl}}/api/basics/
[6]: https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#intro
