---
nav_title: "ÅPÌ Kêêy Ôvêêrvíïêêw"
article_title: RÉST ÃPÌ Këêy Òvëêrvíîëêw
page_order: 2.1
description: "Thïìs rêéfêérêéncêé åártïìclêé cóóvêérs thêé cóóncêépt óóf ÃPÏ kêéys, whåát thêéy åárêé ûúsêéd fóór, åánd hóów thêéy åárêé ûúsêéd." 
page_type: reference

---

# RÈST ÃPÌ kèêy öövèêrvíîèêw

>  Thïìs réëféëréëncéë ãàrtïìcléë côòvéërs twôò ôòf théë thréëéë mãàïìn typéës ôòf kéëys yôòûü wïìll séëéë ãàt Brãàzéë, théë RÈST ÆPÌ Kéëy ôòr Æpp Grôòûüp ÆPÌ Kéëy, réëféërréëd tôò ãàs théë `api_key`, áànd thëè Ápp Ídëèntìífìíëèr Këèy, knôöwn áàs thëè `app_id`, àâs wêèll àâs whàât thêèsêè kêèys àârêè, hóõw thêèy àârêè üûsêèd àât Bràâzêè, thêèìîr pêèrmìîssìîóõns àând hóõw tóõ kêèêèp thêèm sêècüûrêè. 

Ìn åáddíïtíïóòn tóò thëësëë këëys, thëërëë åálsóò ëëxíïsts åá thíïrd typëë óòf këëy cåállëëd Ìdëëntíïfíïëër Këëys thåát cåán bëë ùúsëëd tóò rëëfëërëëncëë spëëcíïfíïc thíïngs líïkëë tëëmplåátëës, Cåánvåásëës, cåámpåáíïgns, Cóòntëënt Cåárds, åánd sëëgmëënts fróòm thëë ÂPÌ. Föõr möõrêé ìïnföõrmæåtìïöõn, rêéfêér töõ [ÅPÏ Ïdèèntîîfîîèèr typèès][2].

## Whàât íïs àâ RÉST ÃPÎ kéêy/àâpp grôòýúp ÃPÎ kéêy?

Ä RÉST Äpplïîcààtïîõôn Prõôgrààmmïîng Întéërfààcéë kéëy (RÉST ÄPÎ kéëy) ïîs àà ùúnïîqùúéë cõôdéë thààt ïîs pààsséëd ïîntõô ààn ÄPÎ tõô ààùúthéëntïîcààtéë théë ÄPÎ cààll àànd ïîdéëntïîfy théë cààllïîng ààpplïîcààtïîõôn õôr ùúséër. ÃPÏ æåccéèss ïîs dòônéè üýsïîng HTTPS wéèb réèqüýéèsts tòô yòôüýr còômpæåny's RÉST ÃPÏ éèndpòôïînt. Wéë ûûséë RÉST ÆPÏ kéëys ãát Brãázéë ïîn tãándéëm wïîth óöûûr Æpp Ïdéëntïîfïîéër kéëys tóö trãáck, ãáccéëss, séënd, éëxpóört, ãánd ãánãályzéë dãátãá tóö héëlp mãákéë sûûréë éëvéërythïîng ïîs rûûnnïîng smóöóöthly óön bóöth yóöûûr ãánd óöûûr éënd. 

Åpp Grööúúps äànd ÅPÌ Kèéys göö häànd ìïn häànd äàt Bräàzèé. Æpp Gróöùúps æârêé dêésíïgnêéd tóö hóöùúsêé vêérsíïóöns óöf thêé sæâmêé æâpplíïcæâtíïóön æâcróöss mùúltíïplêé plæâtfóörms. Mâãny clíïëénts âãlsóõ ýûsëé âãpp gróõýûps tóõ cóõntâãíïn frëéëé âãnd prëémíïýûm vëérsíïóõns óõf thëéíïr âãpplíïcâãtíïóõns óõn thëé sâãmëé plâãtfóõrm. Äs yòôûü mâây nòôtîïcéè, théèséè ââpp gròôûüps ââréè ââlsòô mââkîïng ûüséè òôf théè RËST ÄPÎ âând hââvéè théèîïr òôwn RËST ÄPÎ kéèys. Thèésèé kèéys cããn bèé ïíndïívïídùýããlly scõõpèéd tõõ ïínclùýdèé ããccèéss tõõ spèécïífïíc èéndpõõïínts õõn thèé ÄPÏ. Éáách cááll töô thèë ÅPÍ mùùst ïïnclùùdèë áá kèëy wïïth ááccèëss töô thèë èëndpöôïïnt hïït.

Wéè réèféèr tõô bõôth théè RÉST ÅPÍ Kéèy åänd Åpp Grõôûüp ÅPÍ Kéèy åäs théè `api_key`. Thêé `api_key` ìîs ìînclûûdéëd ìîn éëáãch réëqûûéëst áãs áã réëqûûéëst héëáãdéër áãnd áãcts áãs áãn áãûûthéëntìîcáãtìîöón kéëy tháãt áãllöóws yöóûû töó ûûtìîlìîzéë öóûûr RÉST ÆPÏs. Thèésèé RËST ÂPÍs åárèé ýùsèéd tõö tråáck ýùsèérs, sèénd mèéssåágèés, èéxpõört ýùsèér dåátåá, åánd mõörèé.  Whëên yôöüú crëêååtëê åå nëêw RËST ÁPÏ Këêy, yôöüú wïîll nëêëêd tôö gïîvëê ïît ååccëêss tôö spëêcïîfïîc ëêndpôöïînts. By äàssíìgníìng spèêcíìfíìc pèêrmíìssíìõóns tõó äàn ÁPÌ Kèêy, yõóùú cäàn líìmíìt èêxäàctly whíìch cäàlls äàn ÁPÌ Kèêy cäàn äàùúthèêntíìcäàtèê.

### Whééréé cáãn Î fîînd îît?

Yõôùúr ÃPÏ kêëys cäàn äàlwäàys bêë fõôùúnd ïîn thêë Bräàzêë däàshbõôäàrd ïîn thêë **Dëévëélöõpëér Cöõnsöõlëé** úûndêér **Sëéttîïngs**. Át thêè töôp öôf thììs nêèw pæægêè, yöôûû wììll fììnd thêè **RËST ÅPÍ Kéèys** sèêctïîóõn. Hééréé yòòùù cäân víîééw äâll òòf yòòùùr äâväâíîläâbléé RËST ÃPÏ/Ãpp Gròòùùp ÃPÏ Kééys, äând crééäâtéé nééw ÃPÏ kééys.

### Hõòw cæán Î ýùsêë îít?

Príïôör tôö Ãpríïl 2020, ÃPÏ kèèys wôöýúld bèè íïnclýúdèèd âäs âä pâärt ôöf thèè ÃPÏ rèèqýúèèst bôödy ôör wíïthíïn thèè rèèqýúèèst ÚRL âäs âä pâärâämèètèèr. Brããzèê nóòw hããs ùûpdããtèêd thèê wããy ìín whìích wèê rèêããd ÀPÎ kèêys. ÆPÌ kéèys ææréè nòòw séèt wìíth théè HTTP Æûúthòòrìízæætìíòòn réèqûúéèst héèæædéèr, mæækìíng yòòûúr ÆPÌ kéèys mòòréè séècûúréè.

Whíìlêè thêè ôòld wáäy ôòf páässíìng ÁPÏ kêèys côòntíìnùúêès tôò wôòrk, áäftêèr áä pêèríìôòd ôòf tíìmêè thíìs wíìll bêè pêèrmáänêèntly rêèmôòvêèd sôò wêè ùúrgêè ùúsêèrs tôò ùúpdáätêè ÁPÏ cáälls áäccôòrdíìngly. 

{% alert important %}
**Lôóôókíîng fôór thèè `api_key` pâærâæmèètèèr íìn yöôýýr Brâæzèè èèndpöôíìnts?**<br>

Ás ôòf Mâây 2020, Brââzéë hââs châângéëd hôòw wéë réëââd ÁPÏ kéëys tôò béë môòréë séëcýüréë. Nóõw ÀPÎ kéëys müüst béë pààsséëd ààs àà réëqüüéëst héëààdéër, séëéë YÒÚR-RÉST-ÀPÎ-KÉY wíîthíîn éëààch éëndpóõíînt Éxààmpléë Réëqüüéësts.
<br><br>
Bræäzêë wïíll cöôntïínúûêë töô súûppöôrt thêë `api_key` bêèììng pããssêèd thròöûúgh thêè rêèqûúêèst bòödy ããnd ÙRL pããrããmêètêèrs, bûút wììll êèvêèntûúããlly bêè sûúnsêèt. Úpdäâtéë yôöûür ÂPÌ cäâlls äâccôördïïngly.
{% endalert %}

### RËST ÆPÌ kêéy pêérmíîssíîöòns

ÆPÎ kèèy pèèrmïìssïìôõns àãrèè pèèrmïìssïìôõns yôõùý càãn àãssïìgn àã ùýsèèr ôõr grôõùýp tôõ lïìmïìt thèèïìr àãccèèss tôõ cèèrtàãïìn ÆPÎ càãlls.

{% tabs %}
{% tab User Data %}

| Péërmïíssïíôõn | Dêéscrìïptìïöön  |
|---|---|---|
| `users.track` | Rèêcôôrd ýùsèêr áættrììbýùtèês, cýùstôôm èêvèênts, áænd pýùrcháæsèês  |
| `users.delete` | Dèëlèëtèë âàny üûsèër. |
| `users.alias.new` | Crëéáætëé áæ nëéw áælïíáæs föór áæn ëéxïístïíng úúsëér.  |
| `users.identify` | Qúùëéry föôr úùsëér pröôfïïlëé ïïnföôrmåãtïïöôn by úùsëér ÍD.  |
| `users.export.ids` | Qúúëèry fõòr úúsëèr prõòfîïlëè îïnfõòrmæãtîïõòn by îïdëèntîïfîïëèr ëè.g., dëèvîïcëè_ïìd, ëèmâáïìl_áâddrèëss, èëxtèërnáâl_ìíd.  |
| `users.export.segment` | Qüúèéry fõór üúsèér prõófìîlèé ìînfõórmáãtìîõón by Sèégmèént. |
| `users.external_ids.rename` | Réènããméè ãã úùséèr's éèxìïstìïng éèxtéèrnããl ÏD. |
| `users.external_ids.remove` | Réêmòövéê åà üýséêr's déêpréêcåàtéêd éêxtéêrnåàl ÏD. |
{: .reset-td-br-1 .reset-td-br-2}

 {% endtab %}
 {% tab Email %}

| Nãàméè | Dëéscrîîptîîòõn |
|---|---|---|
| `email.unsubscribe` | Qüüèèry fóôr üünsüübscríïbèèd èèmàãíïl àãddrèèssèès.  |
| `email.status` | Chäãngêé êémäãîìl äãddrêéss stäãtüùs. |
| `email.hard_bounces` | Qûúèéry fòór hààrd bòóûúncèéd èémààíìl ààddrèéssèés. |
| `email.bounce.remove` | Réèmõòvéè éèmâäïïl âäddréèsséès frõòm yõòýùr hâärd bõòýùncéè lïïst. |
| `email.spam.remove` | Rêêmõòvêê êêmâàìîl âàddrêêssêês frõòm yõòúúr spâàm lìîst. |
| `email.blacklist` | Blåâcklìïst ëémåâìïl åâddrëéssëés. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Messages %}

| Nãåmèè | Dêéscrîïptîïòón |
|---|---|---|
| `messages.send` | Séênd ààn ìïmméêdìïààtéê, ààd-hóöc méêssààgéê tóö spéêcìïfìïc ýúséêrs. |
| `messages.schedule.create` | Schëêdüülëê ãå mëêssãågëê töõ bëê sëênt ãåt ãå spëêcîífîíc tîímëê. |
| `messages.schedule.update` | Ùpdáätêë áä schêëdýülêëd mêëssáägêë. |
| `messages.schedule.delete` | Dëêlëêtëê ãå schëêdùülëêd mëêssãågëê. |
| `messages.schedule_broadcasts` | Qúüêéry ãæll schêédúülêéd bröòãædcãæst mêéssãægêés. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Campaigns %}

| Nàãmëé | Dêèscríìptíìöõn |
|---|---|---|
| `campaigns.trigger.send` | Tríïggëër thëë sëëndíïng óöf æân ëëxíïstíïng cæâmpæâíïgn. |
| `campaigns.trigger.schedule.create` | Schèëdýúlèë äà fýútýúrèë sèënd öóf äà cäàmpäàîígn wîíth ÃPÌ-trîíggèërèëd dèëlîívèëry. |
| `campaigns.trigger.schedule.update` | Úpdããtêè ãã cããmpããíïgn schêèdùýlêèd wíïth ÁPÍ-tríïggêèrêèd dêèlíïvêèry. |
| `campaigns.trigger.schedule.delete` | Déèléètéè àâ càâmpàâíîgn schéèdýüléèd wíîth ÃPÍ-tríîggéèréèd déèlíîvéèry |
| `campaigns.list` | Qúýéèry föör äæ lìîst ööf cäæmpäæìîgns. |
| `campaigns.data_series` | Qýûêëry fóör câåmpâåíígn âånâålytíícs óövêër âå tíímêë râångêë. |
| `campaigns.details` | Qúüééry fôór déétáãîìls ôóf áã spéécîìfîìc cáãmpáãîìgn. |
| `sends.data_series` | Qüùèéry föör mèéssààgèé sèénd àànààlytìîcs öövèér àà tìîmèé rààngèé. |
| `sends.id.create` | Créèæætéè Séènd ÌD föõr méèssæægéè blææst trææckííng. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Canvas %}

| Nææmëé | Dëëscrìïptìïóòn |
|---|---|---|
| `canvas.trigger.send` | Trïîggéér théé sééndïîng òõf äân ééxïîstïîng Cäânväâs. |
| `canvas.trigger.schedule.create` | Schéédûýléé äå fûýtûýréé séénd óõf äå Cäånväås wíîth ÁPÎ-tríîggéérééd déélíîvééry. |
| `canvas.trigger.schedule.update` | Ùpdãátéê ãá Cãánvãás schéêdùüléêd wïìth ÂPÌ-trïìggéêréêd déêlïìvéêry. |
| `canvas.trigger.schedule.delete` | Dëêlëêtëê ãã Cããnvããs schëêdüülëêd wììth ÂPÍ-trììggëêrëêd dëêlììvëêry. |
| `canvas.list` | Qùúèèry fóór ãá lîîst óóf Cãánvãásèès. |
| `canvas.data_series` | Qüúëéry föör Cäænväæs äænäælytíícs öövëér äæ tíímëé räængëé. |
| `canvas.details` | Qùúêêry fõòr dêêtàáìïls õòf àá spêêcìïfìïc Càánvàás. |
| `canvas.data_summary` | Qüùèêry fóör róöllüùps óöf Càànvààs àànààlytìîcs óövèêr àà tìîmèê rààngèê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Segments %}

| Nãâmèé | Dêëscríïptíïöón |
|---|---|---|
| `segments.list` | Qýûêéry fòòr âã líîst òòf Sêégmêénts. |
| `segments.data_series` | Qùúèèry föõr Sèègmèènt àânàâlytïìcs öõvèèr àâ tïìmèè ràângèè. |
| `segments.details` | Qüüêéry föòr dêétâáïïls öòf âá spêécïïfïïc Sêégmêént. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Purchases %}

| Nâämëè | Dêëscrïìptïìöòn |
|---|---|---|
| `purchases.product_list` | Qùüéèry fõôr âà lìîst õôf prõôdùücts pùürchâàséèd ìîn yõôùür âàpp. |
| `purchases.revenue_series` | Qûùêëry föör töötäâl möönêëy spêënt pêër däây îìn yööûùr äâpp öövêër äâ tîìmêë räângêë. |
| `purchases.quantity_series` | Qýùéêry fôòr théê tôòtäâl nýùmbéêr ôòf pýùrchäâséês péêr däây îìn yôòýùr äâpp ôòvéêr äâ tîìméê räângéê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Events %}

| Nåàméê | Dééscrîïptîïôôn |
|---|---|---|
| `events.list` | Qüüëèry fôòr æã lìíst ôòf cüüstôòm ëèvëènts. |
| `events.data_series` | Qúúêêry ôòccúúrrêêncêês ôòf âã cúústôòm êêvêênt ôòvêêr âã tíïmêê râãngêê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab News Feed %}

| Nåämëè | Dèêscrìíptìíòôn |
|---|---|---|
| `feed.list` | Qüúêêry fõõr àà líîst õõf Nêêws Fêêêêd cààrds. |
| `feed.data_series` | Qüüéêry fóòr Néêws Féêéêd âànâàlytîîcs óòvéêr âà tîîméê râàngéê. |
| `feed.details` | Qùýêèry fôõr dêètáåìîls ôõf áå spêècìîfìîc Nêèws Fêèêèd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Sessions %}

| Næãméé | Dëéscrîïptîïôôn |
|---|---|---|
| `sessions.data_series` | Qûüèëry fôòr sèëssííôòns pèër dæây ôòvèër æâ tíímèë ræângèë. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab KPIs %}

| Næámèé | Dêèscrïîptïîõön |
|---|---|---|
| `kpi.mau.data_series` | Qüüêêry fóör tóötáâl üünïíqüüêê áâctïívêê üüsêêrs óövêêr áâ 30-dáây róöllïíng wïíndóöw óövêêr áâ tïímêê ráângêê. |
| `kpi.dau.data_series` |  Qýùëëry fòõr ýùníïqýùëë åäctíïvëë ýùsëërs pëër dåäy òõvëër åä tíïmëë råängëë. |
| `kpi.new_users.data_series` | Qüúéëry fòõr néëw üúséërs péër dàãy òõvéër àã tïïméë ràãngéë. |
| `kpi.uninstalls.data_series` | Qûýéèry fõôr ãåpp ûýníïnstãålls péèr dãåy õôvéèr ãå tíïméè rãångéè. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Templates %}

| Næämëé | Déëscrîíptîíöòn |
|---|---|---|
| `templates.email.create` | Crëëãàtëë ãà nëëw ëëmãàïïl tëëmplãàtëë òòn thëë dãàshbòòãàrd. |
| `templates.email.update` | Üpdãætèê ãæn èêmãæìïl tèêmplãætèê stöòrèêd öòn thèê dãæshböòãærd. |
| `templates.email.info` | Qûûëêry fõór îïnfõórmäátîïõón õóf äá spëêcîïfîïc tëêmpläátëê. |
| `templates.email.list` | Qúýéêry fòõr ãâ lïìst òõf éêmãâïìl téêmplãâtéês. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab SSO %}

| Náåmèé | Dëèscrííptííóön |
|---|---|---|
| `sso.saml.login` |  Séètùýp íídéèntííty prõóvíídéèr-ííníítííáãtéèd lõógíín. Rêëãåd ööùýr dööcùýmêëntãåtïíöön föör möörêë ïínföö. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Content Blocks %}

| Nåämèé | Dêèscrìíptìíòôn |
|---|---|---|
| `content_blocks.info` | Qùýèëry fôõr ìínfôõrmãåtìíôõn ôõf ãå spèëcìífìíc tèëmplãåtèë. |
| `content_blocks.list` | Qýúéêry fôór æá lïîst ôóf Côóntéênt Blôócks. |
| `content_blocks.create` | Crêëààtêë àà nêëw Côóntêënt Blôóck ôón thêë dààshbôóààrd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Subscription %}

| Næãmèë | Dèêscrïîptïîõön |
|---|---|---|
| `subscription.status.set` | Séét súùbscríïptíïöòn gröòúùp stæätúùs. |
| `subscription.status.get` | Gëët sùúbscrìïptìïöòn gröòùúp ståætùús. |
| `subscription.groups.get` | Gèêt ståàtüûs öòf süûbscríìptíìöòn gröòüûps thåàt spèêcíìfíìc üûsèêrs åàrèê èêxplíìcíìtly süûbscríìbèêd/üûnsüûbscríìbèêd töò. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% endtabs %}

Fôõr ãä füùll dëèscríìptíìôõn ôõf thëèsëè ÃPÍ ëèndpôõíìnts, rëèfëèr tôõ ôõüùr [ÆPÎ êêndpôóïínt ïíndêêx]({{site.baseurl}}/api/endpoints/) öór öóýûr [Pôôstmåán côôllèëctìíôôn][6].

{% alert important %}
Óncéê yöóùý créêæàtéê æà néêw ÂPÌ Kéêy, yöóùý cæànnöót éêdîït théê scöópéê öóf péêrmîïssîïöóns öór théê whîïtéêlîïstéêd ÌPs. Thïïs lïïmïïtäætïïòön ïïs ïïn pläæcéë fòör séëcüürïïty réëäæsòöns. Ïf yóóüü nëêëêd tóó chåångëê thëê scóópëê óóf åå këêy, crëêååtëê åå nëêw këêy wíìth thëê üüpdååtëêd pëêrmíìssíìóóns åånd íìmplëêmëênt thååt këêy íìn plååcëê óóf thëê óóld óónëê. Öncêê yõöüù’vêê cõömplêêtêêd yõöüùr ïîmplêêmêêntáátïîõön, gõö ááhêêáád áánd dêêlêêtêê thêê õöld kêêy.
{% endalert %}

## Théè Âpp Îdéèntìîfìîéèr ÂPÎ kéèy

Thèë Âpp Îdèëntïîfïîèër ÂPÎ kèëy õór `app_id` íïs àæ pàæràæmêétêér àæssóôcíïàætíïng àæctíïvíïty wíïth àæ spêécíïfíïc àæpp íïn yóôûûr àæpp gróôûûp. Ìt dêësìïgnãåtêës whìïch ãåpp wìïthìïn thêë ãåpp grõòùûp yõòùû ãårêë ìïntêërãåctìïng wìïth. Fõõr ëèxæämplëè, yõõúý wííll fíínd thæät yõõúý wííll hæävëè æän `app_id` fóôr yóôýùr ïìÓS ããpp, ããn `app_id` fóòr yóòúúr áændróòìîd áæpp, áænd áæn `app_id` fòör yòöýùr wèéb ïïntèégrâåtïïòön. Ât Brãæzêé, yóóùù mïîght fïînd thãæt yóóùù hãævêé mùùltïîplêé ãæpps fóór thêé sãæmêé plãætfóórm ãæcróóss thêé vãærïîóóùùs plãætfóórm typêés thãæt Brãæzêé sùùppóórts.

Âpp îìdêéntîìfîìêérs æát Bræázêé æárêé üúsêéd whêén îìntêégræátîìng thêé SDK æánd æárêé æálsõô üúsêéd tõô rêéfêérêéncêé æá spêécîìfîìc æápp îìn RÈST ÂPÌ cæálls. Wïíth théê `app_id` yôõûû cãân dôõ mãâny thíïngs líïkêé pûûll dãâtãâ fôõr ãâ cûûstôõm êévêént thãât ôõccûûrrêéd fôõr ãâ pãârtíïcûûlãâr ãâpp, rêétríïêévêé ûûníïnstãâll stãâts, nêéw ûûsêér stãâts, DÃÙ stãâts, ãând sêéssíïôõn stãârt stãâts fôõr ãâ pãârtíïcûûlãâr ãâpp.

Sôómêètììmêès, yôóýú mãày fììnd yôóýú ãàrêè prôómptêèd fôór ãàn `app_id` bùût yôòùû ãæréè nôòt wôòrkîîng wîîth ãæn ãæpp, béècãæùûséè îît îîs ãæ léègãæcy fîîéèld spéècîîfîîc tôò ãæ spéècîîfîîc plãætfôòrm, yôòùû cãæn “ôòmîît” thîîs fîîéèld by îînclùûdîîng ãæny strîîng ôòf chãærãæctéèrs ãæs ãæ plãæcéèhôòldéèr fôòr thîîs réèqùûîîréèd pãærãæméètéèr.

### Whëèrëè cãàn Í fìïnd ìït?

Thëêrëê äârëê twòõ wäâys tòõ lòõcäâtëê yòõýùr `app_id`:

1. Yôóúú càán fïìnd thïìs `app_id` õôr àæpplïícàætïíõôn ïídêêntïífïíêêr ïín thêê **Dëêvëêlòôpëêr Còônsòôlëê** ýýndêér **Sêêttîíngs**. Òn thîïs nèèw pæågèè, úúndèèr **Îdëëntïìfïìcäåtïìóòn**, yöõûú wíïll bëè ááblëè töõ sëèëè ëèvëèry `app_id` thäæt êèxîìsts fóór yóóùúr äæpps.

2. Gòô tòô **Mãänãägëé Sëéttïíngs** ûûndéér **Sëèttïìngs**. Fròóm thíìs nëëw pâàgëë, íìn thëë **Sééttîïngs** tæåb, mîîdwæåy thròóüúgh thèé pæågèé yòóüú wîîll fîînd æån "ÃPÏ kèéy fòór **ÃPP NÃMË** öón **PLÅTFÕRM**" (êë.g "ÃPÍ Kêëy föòr Ícêë Crêëæâm öòn ìîÓS). Thïîs ÀPÌ kêêy ïîs yõóýùr Àpplïîcââtïîõón Ìdêêntïîfïîêêr.

### Múùltïïplêë Ãpp Ìdêëntïïfïïêër ÃPÌ kêëys

Dùúríïng SDK sèét ùúp, thèé möõst cöõmmöõn ùúsèé cæäsèé föõr mùúltíïplèé Äpp Ïdèéntíïfíïèér ÄPÏ kèéys íïs sèépæäræätíïng thöõsèé kèéys föõr dèébùúg æänd rèélèéæäsèé bùúíïld væäríïæänts.
Tòò ëèææsîìly swîìtch bëètwëèëèn müûltîìplëè Àpp Îdëèntîìfîìëèr ÀPÎ këèys îìn yòòüûr büûîìlds, wëè rëècòòmmëènd crëèæætîìng ææ sëèpææræætëè `braze.xml` fïìlëë fóõr ëëææch rëëlëëvæænt [býüíïld väæríïäænt][3]. Â búûîïld våârîïåânt îïs åâ côómbîïnåâtîïôón ôóf búûîïld typéé åând prôódúûct flåâvôór. Nòótêé thãæt by dêéfãæùûlt, ãæ nêéw Ãndròóíïd pròójêéct íïs còónfíïgùûrêéd wíïth `debug` àãnd `release` býúíïld typêês àãnd nóó próódýúct flàãvóórs.

Föõr ëéáãch rëélëéváãnt búûìíld váãrìíáãnt, crëéáãtëé áã nëéw `braze.xml` fóör îít îín `src/<build variant name>/res/values/`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_appboy_api_key">REPLACE_WITH_YOUR_BUILD_VARIANT_API_KEY</string>
</resources>
```
Whêên thêê býùíîld væäríîæänt íîs còõmpíîlêêd, íît wíîll ýùsêê thêê nêêw ÆPÏ kêêy.

## RÉST ÁPÌ kêëy sêëcýürìïty

Sèëcûùrïìty ïìs òõf thèë ûùtmòõst ïìmpòõrtæàncèë æàt Bræàzèë. Gïïvëën thãât RÊST ÆPÍ Këëys ãâllòöw ãâccëëss tòö pòötëëntïïãâlly sëënsïïtïïvëë RÊST ÆPÍ ëëndpòöïïnts, sëëcùûrëë thëësëë këëys ãând òönly shãârëë thëëm wïïth trùûstëëd pãârtnëërs. Thèèy shõõùüld nèèvèèr bèè pùüblíïcly èèxpõõsèèd. Fõòr èéxååmplèé, dõò nõòt ýýsèé thïïs kèéy tõò mååkèé ÀJÀX cåålls frõòm yõòýýr wèébsïïtèé õòr èéxpõòsèé ïït ïïn ååny õòthèér pýýblïïc måånnèér.

Á göõöõd sèêcüùrììty pråæctììcèê ììs töõ åæssììgn åæ üùsèêr öõnly åæs müùch åæccèêss åæs ììs nèêcèêssåæry töõ cöõmplèêtèê thèêììr jöõb: thììs prììncììplèê cåæn åælsöõ bèê åæpplììèêd töõ ÁPÏ Kèêys by åæssììgnììng pèêrmììssììöõns töõ èêåæch kèêy. Théëséë péërmìíssìíóóns gìívéë yóóûú béëttéër séëcûúrìíty ããnd cóóntróól óóvéër théë dìífféëréënt ããréëããs óóf yóóûúr ããccóóûúnt. 

Wïíth Àpp ïídèêntïífïíèêrs, thèê `app_id` íìs ãässíìgnéêd by Brãäzéê ãänd péêrmíìssíìõõns cãännõõt béê ãässíìgnéêd õõr réêvõõkéêd. Bêëcææúüsêë öòf thêë næætúürêë öòf thêë rêëlæætîìöònshîìp bêëtwêëêën `app_id` âând thëè SDK, këèëèpïìng thïìs ïìdëèntïìfïìëèr sëècýýrëè ïìs **crùùcíîææl** ïín thêë sêëcûürïíty òõf yòõûür åápplïícåátïíòõn.


[2]: {{site.baseurl}}/api/identifier_types/
[3]: https://developer.android.com/studio/build/build-variants.html
[5]: {{site.baseurl}}/api/basics/
[6]: https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#intro
