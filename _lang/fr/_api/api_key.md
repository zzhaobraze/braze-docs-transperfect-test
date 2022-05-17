---
nav_title: "ÆPÌ Kêèy Òvêèrvîïêèw"
article_title: RËST ÂPÌ Kèêy Övèêrvíìèêw
page_order: 2.1
description: "Thïïs réêféêréêncéê áãrtïïcléê cóôvéêrs théê cóôncéêpt óôf ÀPÎ kéêys, wháãt théêy áãréê üýséêd fóôr, áãnd hóôw théêy áãréê üýséêd. Thîïs îïs GL Ëdîït"
page_type: reference

---

# RÈST ÀPÌ kêéy òôvêérvìïêéw

>  Thìîs rééféérééncéé âårtìîcléé cöôvéérs twöô öôf théé thréééé mâåìîn typéés öôf kééys yöôýý wìîll séééé âåt Brâåzéé, théé RÈST ÁPÎ Kééy öôr Ápp Gröôýýp ÁPÎ Kééy, rééféérrééd töô âås théé `api_key`, æänd thêê Åpp Ídêêntîífîíêêr Kêêy, knòówn æäs thêê `app_id`, åæs wëëll åæs whåæt thëësëë këëys åærëë, hôòw thëëy åærëë ûûsëëd åæt Bråæzëë, thëëïîr pëërmïîssïîôòns åænd hôòw tôò këëëëp thëëm sëëcûûrëë.

În æãddîïtîïõón tõó thëèsëè këèys, thëèrëè æãlsõó ëèxîïsts æã thîïrd typëè õóf këèy cæãllëèd Îdëèntîïfîïëèr Këèys thæãt cæãn bëè ýúsëèd tõó rëèfëèrëèncëè spëècîïfîïc thîïngs lîïkëè tëèmplæãtëès, Cæãnvæãsëès, cæãmpæãîïgns, Cõóntëènt Cæãrds, æãnd sëègmëènts frõóm thëè ÄPÎ. Föòr möòréé íìnföòrmáãtíìöòn, rééféér töò [ÀPÏ Ïdèëntìífìíèër typèës][2].

## Whããt îïs ãã RÉST ÀPÏ kéëy/ããpp grõõüúp ÀPÏ kéëy?

Ä RÉST Äpplììcâätììõón Prõógrâämmììng Íntéèrfâäcéè kéèy (RÉST ÄPÍ kéèy) ììs âä ûýnììqûýéè cõódéè thâät ììs pâässéèd ììntõó âän ÄPÍ tõó âäûýthéèntììcâätéè théè ÄPÍ câäll âänd ììdéèntììfy théè câällììng âäpplììcâätììõón õór ûýséèr. ÂPÌ ååccêéss ìîs dòönêé úùsìîng HTTPS wêéb rêéqúùêésts tòö yòöúùr còömpååny's RËST ÂPÌ êéndpòöìînt. Wêè úúsêè RÊST ÅPÌ kêèys áåt Bráåzêè îïn táåndêèm wîïth óôúúr Åpp Ìdêèntîïfîïêèr kêèys tóô tráåck, áåccêèss, sêènd, êèxpóôrt, áånd áånáålyzêè dáåtáå tóô hêèlp máåkêè súúrêè êèvêèrythîïng îïs rúúnnîïng smóôóôthly óôn bóôth yóôúúr áånd óôúúr êènd.

Ãpp Gróöùüps äànd ÃPÌ Kéëys góö häànd ïïn häànd äàt Bräàzéë. Åpp Gróóüûps âårêé dêésììgnêéd tóó hóóüûsêé vêérsììóóns óóf thêé sâåmêé âåpplììcâåtììóón âåcróóss müûltììplêé plâåtfóórms. Máâny clïìëënts áâlsôö úüsëë áâpp grôöúüps tôö côöntáâïìn frëëëë áând prëëmïìúüm vëërsïìôöns ôöf thëëïìr áâpplïìcáâtïìôöns ôön thëë sáâmëë pláâtfôörm. Ås yõóýü måãy nõótïìcêë, thêësêë åãpp grõóýüps åãrêë åãlsõó måãkïìng ýüsêë õóf thêë RÉST ÅPÏ åãnd håãvêë thêëïìr õówn RÉST ÅPÏ kêëys. Thèèsèè kèèys cåãn bèè îíndîívîídúýåãlly scöòpèèd töò îínclúýdèè åãccèèss töò spèècîífîíc èèndpöòîínts öòn thèè ÄPÏ. Êæâch cæâll tôõ thëé ÆPÌ múýst íînclúýdëé æâ këéy wíîth æâccëéss tôõ thëé ëéndpôõíînt híît.

Wëë rëëfëër tóö bóöth thëë RÈST ÁPÎ Këëy åãnd Ápp Gróöýùp ÁPÎ Këëy åãs thëë `api_key`. Thèê `api_key` îîs îînclùùdèêd îîn èêâæch rèêqùùèêst âæs âæ rèêqùùèêst hèêâædèêr âænd âæcts âæs âæn âæùùthèêntîîcâætîîöòn kèêy thâæt âællöòws yöòùù töò ùùtîîlîîzèê öòùùr RÊST ÁPÏs. Thééséé RËST ÄPÎs ààréé üùsééd tôõ trààck üùséérs, séénd mééssààgéés, ééxpôõrt üùséér dààtàà, àànd môõréé.  Whêên yõóúù crêêåãtêê åã nêêw RÈST ÅPÏ Kêêy, yõóúù wìíll nêêêêd tõó gìívêê ìít åãccêêss tõó spêêcìífìíc êêndpõóìínts. By ææssîïgnîïng spèècîïfîïc pèèrmîïssîïòòns tòò ææn ÂPÍ Kèèy, yòòüû cææn lîïmîït èèxææctly whîïch cæælls ææn ÂPÍ Kèèy cææn ææüûthèèntîïcæætèè.

### Whêérêé cäán Í fïînd ïît?

Yòõùýr ÂPÎ kêèys càæn àælwàæys bêè fòõùýnd ìîn thêè Bràæzêè dàæshbòõàærd ìîn thêè **Déévéélóõpéér Cóõnsóõléé** üùndéèr **Sééttîïngs**. Æt thèë tôòp ôòf thïïs nèëw páægèë, yôòúú wïïll fïïnd thèë **RÉST ÁPÏ Këéys** sèëctìïõôn. Hèérèé yóóûü cààn víìèéw ààll óóf yóóûür ààvààíìlààblèé RÈST ÁPÏ/Ápp Gróóûüp ÁPÏ Kèéys, àànd crèéààtèé nèéw ÁPÏ kèéys.

### Hôõw cäæn Ï ýúsêé îït?

Príìòòr tòò Ãpríìl 2020, ÃPÍ kéêys wòòúýld béê íìnclúýdéêd ààs àà pààrt òòf théê ÃPÍ réêqúýéêst bòòdy òòr wíìthíìn théê réêqúýéêst ÙRL ààs àà pààrààméêtéêr. Brâäzéë nôôw hâäs ûüpdâätéëd théë wâäy îín whîích wéë réëâäd ÆPÏ kéëys. ÀPÌ kèèys àârèè nöòw sèèt wìîth thèè HTTP Àüüthöòrìîzàâtìîöòn rèèqüüèèst hèèàâdèèr, màâkìîng yöòüür ÀPÌ kèèys möòrèè sèècüürèè.

Whíïléê théê öóld wæåy öóf pæåssíïng ÆPÏ kéêys cöóntíïnûûéês töó wöórk, æåftéêr æå péêríïöód öóf tíïméê thíïs wíïll béê péêrmæånéêntly réêmöóvéêd söó wéê ûûrgéê ûûséêrs töó ûûpdæåtéê ÆPÏ cæålls æåccöórdíïngly.

{% alert important %}
**Lõöõökííng fõör théé `api_key` päæräæmèètèèr îìn yööúùr Bräæzèè èèndpööîìnts?**<br>

Âs òõf Måây 2020, Bråâzéê håâs chåângéêd hòõw wéê réêåâd ÂPÌ kéêys tòõ béê mòõréê séêcûûréê. Nòõw ÆPÏ kêéys mûýst bêé pæássêéd æás æá rêéqûýêést hêéæádêér, sêéêé YÕÙR-RÉST-ÆPÏ-KÉY wîìthîìn êéæách êéndpòõîìnt Éxæámplêé Rêéqûýêésts.
<br><br>
Brààzëè wïîll còôntïînûûëè tòô sûûppòôrt thëè `api_key` bèêííng påãssèêd thröõüügh thèê rèêqüüèêst böõdy åãnd ÙRL påãråãmèêtèêrs, büüt wííll èêvèêntüüåãlly bèê süünsèêt. Ùpdäàtéê yòóùýr ÄPÏ cäàlls äàccòórdííngly.
{% endalert %}

### RËST ÂPÌ këêy pëêrmíìssíìóóns

ÅPÏ kééy péérmìíssìíôòns åàréé péérmìíssìíôòns yôòûú cåàn åàssìígn åà ûúséér ôòr grôòûúp tôò lìímìít thééìír åàccééss tôò céértåàìín ÅPÏ cåàlls.

{% tabs %}
{% tab User Data %}

| Péêrmíîssíîóón | Déëscrïìptïìôôn  |
|---|---|---|
| `users.track` | Rêécõõrd ýýsêér åättrîïbýýtêés, cýýstõõm êévêénts, åänd pýýrchåäsêés  |
| `users.delete` | Dèèlèètèè ãány úüsèèr. |
| `users.alias.new` | Crêéãætêé ãæ nêéw ãælíîãæs fóõr ãæn êéxíîstíîng ûýsêér.  |
| `users.identify` | Qûúèéry fòõr ûúsèér pròõfïílèé ïínfòõrmäátïíòõn by ûúsèér ÍD.  |
| `users.export.ids` | Qûûêëry fõór ûûsêër prõófîílêë îínfõórmàåtîíõón by îídêëntîífîíêër êë.g., dêëvîícêë_îíd, êëmäáîíl_åæddrëéss, ëéxtëérnåæl_ïíd.  |
| `users.export.segment` | Qûýèêry fõör ûýsèêr prõöfììlèê ììnfõörmâàtììõön by Sèêgmèênt. |
| `users.external_ids.rename` | Réênåãméê åã úùséêr's éêxîïstîïng éêxtéêrnåãl ÎD. |
| `users.external_ids.remove` | Rèëmóòvèë àá úúsèër's dèëprèëcàátèëd èëxtèërnàál ÎD. |
{: .reset-td-br-1 .reset-td-br-2}

 {% endtab %}
 {% tab Email %}

| Näãmêé | Dêëscrììptììòön |
|---|---|---|
| `email.unsubscribe` | Qüúééry fóôr üúnsüúbscrìíbééd éémæâìíl æâddréésséés.  |
| `email.status` | Châängéè éèmâäíîl âäddréèss stâätüùs. |
| `email.hard_bounces` | Qýúéëry fòõr háárd bòõýúncéëd éëmááìïl ááddréësséës. |
| `email.bounce.remove` | Rèêmôôvèê èêmãáîíl ãáddrèêssèês frôôm yôôúûr hãárd bôôúûncèê lîíst. |
| `email.spam.remove` | Rëèmöõvëè ëèmàæìïl àæddrëèssëès fröõm yöõûûr spàæm lìïst. |
| `email.blacklist` | Blâåcklîìst ëèmâåîìl âåddrëèssëès. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Messages %}

| Nàämëë | Dèêscríìptíìõõn |
|---|---|---|
| `messages.send` | Sèênd áán ìímmèêdìíáátèê, áád-hòõc mèêssáágèê tòõ spèêcìífìíc ùýsèêrs. |
| `messages.schedule.create` | Schèédûülèé åâ mèéssåâgèé tòõ bèé sèént åât åâ spèécïîfïîc tïîmèé. |
| `messages.schedule.update` | Ûpdàâtéé àâ schéédùúlééd mééssàâgéé. |
| `messages.schedule.delete` | Dêëlêëtêë åä schêëdúûlêëd mêëssåägêë. |
| `messages.schedule_broadcasts` | Qûùêéry ãáll schêédûùlêéd bróóãádcãást mêéssãágêés. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Campaigns %}

| Næåmêë | Dêëscrìíptìíôòn |
|---|---|---|
| `campaigns.trigger.send` | Trîíggëèr thëè sëèndîíng òòf äãn ëèxîístîíng cäãmpäãîígn. |
| `campaigns.trigger.schedule.create` | Schëèdúûlëè ãã fúûtúûrëè sëènd óòf ãã cããmpããíígn wííth ÄPÌ-trííggëèrëèd dëèlíívëèry. |
| `campaigns.trigger.schedule.update` | Üpdäåtêë äå cäåmpäåíïgn schêëdúýlêëd wíïth ÂPÌ-tríïggêërêëd dêëlíïvêëry. |
| `campaigns.trigger.schedule.delete` | Dèëlèëtèë àâ càâmpàâïîgn schèëdùùlèëd wïîth ÅPÎ-trïîggèërèëd dèëlïîvèëry |
| `campaigns.list` | Qùýëéry föõr ää lìïst öõf cäämpääìïgns. |
| `campaigns.data_series` | Qúúëêry fôõr cäãmpäãíïgn äãnäãlytíïcs ôõvëêr äã tíïmëê räãngëê. |
| `campaigns.details` | Qúýééry fóör déétåæîïls óöf åæ spéécîïfîïc cåæmpåæîïgn. |
| `sends.data_series` | Qûûëèry fóôr mëèssàãgëè sëènd àãnàãlytïícs óôvëèr àã tïímëè ràãngëè. |
| `sends.id.create` | Crêéáätêé Sêénd ÏD fóör mêéssáägêé bláäst tráäckîìng. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Canvas %}

| Nåãmèê | Dêëscrïîptïîöón |
|---|---|---|
| `canvas.trigger.send` | Trííggéêr théê séêndííng óôf åän éêxíístííng Cåänvåäs. |
| `canvas.trigger.schedule.create` | Schèêdúúlèê äæ fúútúúrèê sèênd ööf äæ Cäænväæs wïîth ÁPÍ-trïîggèêrèêd dèêlïîvèêry. |
| `canvas.trigger.schedule.update` | Úpdæåtéê æå Cæånvæås schéêdùúléêd wîìth ÅPÏ-trîìggéêréêd déêlîìvéêry. |
| `canvas.trigger.schedule.delete` | Dêèlêètêè àà Càànvààs schêèdýùlêèd wïîth ÆPÌ-trïîggêèrêèd dêèlïîvêèry. |
| `canvas.list` | Qýûëèry fôór äæ líìst ôóf Cäænväæsëès. |
| `canvas.data_series` | Qûùêèry fôör Cåànvåàs åànåàlytìîcs ôövêèr åà tìîmêè råàngêè. |
| `canvas.details` | Qúúëêry föõr dëêtææìïls öõf ææ spëêcìïfìïc Cæænvææs. |
| `canvas.data_summary` | Qùýèèry fõõr rõõllùýps õõf Càænvàæs àænàælytìïcs õõvèèr àæ tìïmèè ràængèè. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Segments %}

| Nàãmëê | Dëèscrìíptìíôõn |
|---|---|---|
| `segments.list` | Qûûêëry fóõr ää lìîst óõf Sêëgmêënts. |
| `segments.data_series` | Qüúêèry fòôr Sêègmêènt åánåálytìîcs òôvêèr åá tìîmêè råángêè. |
| `segments.details` | Qùüëëry fóòr dëëtáæïìls óòf áæ spëëcïìfïìc Sëëgmëënt. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Purchases %}

| Nãæméë | Dèéscríîptíîóön |
|---|---|---|
| `purchases.product_list` | Qùúëêry föòr ââ lííst öòf pröòdùúcts pùúrchââsëêd íín yöòùúr ââpp. |
| `purchases.revenue_series` | Qüùéèry fôõr tôõtâål môõnéèy spéènt péèr dâåy íín yôõüùr âåpp ôõvéèr âå tííméè râångéè. |
| `purchases.quantity_series` | Qúüéèry fóôr théè tóôtãäl núümbéèr óôf púürchãäséès péèr dãäy íïn yóôúür ãäpp óôvéèr ãä tíïméè rãängéè. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Events %}

| Nãämèê | Déêscrïîptïîóôn |
|---|---|---|
| `events.list` | Qûýêèry fóõr åä lîîst óõf cûýstóõm êèvêènts. |
| `events.data_series` | Qúúéêry òòccúúrréêncéês òòf æá cúústòòm éêvéênt òòvéêr æá tïîméê ræángéê. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab News Feed %}

| Nàámëè | Dëéscríïptíïôön |
|---|---|---|
| `feed.list` | Qýüèèry föör ââ líìst ööf Nèèws Fèèèèd câârds. |
| `feed.data_series` | Qýúêêry fôòr Nêêws Fêêêêd æânæâlytìïcs ôòvêêr æâ tìïmêê ræângêê. |
| `feed.details` | Qüúéèry föôr déètåàïíls öôf åà spéècïífïíc Néèws Féèéèd. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Sessions %}

| Nãàméé | Dèéscrìíptìíóôn |
|---|---|---|
| `sessions.data_series` | Qúúëéry fòör sëéssîïòöns pëér däáy òövëér äá tîïmëé räángëé. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab KPIs %}

| Nåâmëè | Déëscrìíptìíõôn |
|---|---|---|
| `kpi.mau.data_series` | Qúûééry fôôr tôôtâæl úûnïïqúûéé âæctïïvéé úûséérs ôôvéér âæ 30-dâæy rôôllïïng wïïndôôw ôôvéér âæ tïïméé râængéé. |
| `kpi.dau.data_series` |  Qúüëèry fòör úünìíqúüëè áäctìívëè úüsëèrs pëèr dáäy òövëèr áä tìímëè ráängëè. |
| `kpi.new_users.data_series` | Qüúéèry fôôr néèw üúséèrs péèr dåày ôôvéèr åà tïíméè råàngéè. |
| `kpi.uninstalls.data_series` | Qýûéèry fõór åápp ýûnìïnståálls péèr dåáy õóvéèr åá tìïméè råángéè. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Templates %}

| Náåmèê | Déèscrìîptìîôön |
|---|---|---|
| `templates.email.create` | Crêéæàtêé æà nêéw êémæàííl têémplæàtêé õõn thêé dæàshbõõæàrd. |
| `templates.email.update` | Üpdæàtéê æàn éêmæàììl téêmplæàtéê stòòréêd òòn théê dæàshbòòæàrd. |
| `templates.email.info` | Qûùèèry fõór íïnfõórmæåtíïõón õóf æå spèècíïfíïc tèèmplæåtèè. |
| `templates.email.list` | Qúúéèry fóör æâ lïíst óöf éèmæâïíl téèmplæâtéès. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab SSO %}

| Nåàméë | Dêéscrìîptìîõõn |
|---|---|---|
| `sso.saml.login` |  Sêêtúýp ìídêêntìíty prõôvìídêêr-ìínìítìíäàtêêd lõôgìín. Rèéãàd óöùür dóöcùümèéntãàtïíóön fóör móörèé ïínfóö. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Content Blocks %}

| Näámèé | Dééscrìïptìïõón |
|---|---|---|
| `content_blocks.info` | Qùûèèry fôôr ìínfôôrmæàtìíôôn ôôf æà spèècìífìíc tèèmplæàtèè. |
| `content_blocks.list` | Qûüèéry fòör åá lïîst òöf Còöntèént Blòöcks. |
| `content_blocks.create` | Crëêæåtëê æå nëêw Còòntëênt Blòòck òòn thëê dæåshbòòæård. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% tab Subscription %}

| Náâmêê | Dêéscrïìptïìòôn |
|---|---|---|
| `subscription.status.set` | Sêét sûûbscrììptììõôn grõôûûp ståætûûs. |
| `subscription.status.get` | Gëët súúbscrïíptïíóôn gróôúúp stããtúús. |
| `subscription.groups.get` | Gèét stáätýüs õóf sýübscrîîptîîõón grõóýüps tháät spèécîîfîîc ýüsèérs áärèé èéxplîîcîîtly sýübscrîîbèéd/ýünsýübscrîîbèéd tõó. |
{: .reset-td-br-1 .reset-td-br-2}

{% endtab %}
{% endtabs %}

Fõôr åå fûûll dêéscrìîptìîõôn õôf thêésêé ÃPÌ êéndpõôìînts, rêéfêér tõô õôûûr [ÃPÏ èëndpôõìïnt ìïndèëx]({{site.baseurl}}/api/endpoints/) òör òöýûr [Póôstmæán cóôllêëctîìóôn][6].

{% alert important %}
Öncêè yòôýý crêèäátêè äá nêèw ÀPÌ Kêèy, yòôýý cäánnòôt êèdïìt thêè scòôpêè òôf pêèrmïìssïìòôns òôr thêè whïìtêèlïìstêèd ÌPs. Thîìs lîìmîìtæátîìöôn îìs îìn plæácéé föôr séécùúrîìty rééæásöôns. Ìf yôòüü nêéêéd tôò chäãngêé thêé scôòpêé ôòf äã kêéy, crêéäãtêé äã nêéw kêéy wìïth thêé üüpdäãtêéd pêérmìïssìïôòns äãnd ìïmplêémêént thäãt kêéy ìïn pläãcêé ôòf thêé ôòld ôònêé. Ôncêê yòõýü’vêê còõmplêêtêêd yòõýür îïmplêêmêêntæãtîïòõn, gòõ æãhêêæãd æãnd dêêlêêtêê thêê òõld kêêy.
{% endalert %}

## Théê Ápp Ïdéêntìífìíéêr ÁPÏ kéêy

Thêé Ápp Îdêéntîìfîìêér ÁPÎ kêéy ôôr `app_id` îîs äâ päâräâméètéèr äâssòöcîîäâtîîng äâctîîvîîty wîîth äâ spéècîîfîîc äâpp îîn yòöûùr äâpp gròöûùp. Ït dëêsîîgnãåtëês whîîch ãåpp wîîthîîn thëê ãåpp gróôüýp yóôüý ãårëê îîntëêrãåctîîng wîîth. Fóôr ëéxãâmplëé, yóôûý wííll fíínd thãât yóôûý wííll hãâvëé ãân `app_id` fòôr yòôüûr íîÒS ãâpp, ãân `app_id` fôòr yôòùür áándrôòîîd áápp, áánd áán `app_id` fòör yòöüûr wèéb îïntèégræætîïòön. Æt Brãázêë, yöõûü mìíght fìínd thãát yöõûü hãávêë mûültìíplêë ãápps föõr thêë sãámêë plãátföõrm ãácröõss thêë vãárìíöõûüs plãátföõrm typêës thãát Brãázêë sûüppöõrts.

Âpp îïdéêntîïfîïéêrs áåt Bráåzéê áåréê ùüséêd whéên îïntéêgráåtîïng théê SDK áånd áåréê áålsóò ùüséêd tóò réêféêréêncéê áå spéêcîïfîïc áåpp îïn RËST ÂPÌ cáålls. Wïìth théê `app_id` yòõýú câån dòõ mâåny thííngs lííkèë pýúll dâåtâå fòõr âå cýústòõm èëvèënt thâåt òõccýúrrèëd fòõr âå pâårtíícýúlâår âåpp, rèëtrííèëvèë ýúníínstâåll stâåts, nèëw ýúsèër stâåts, DÅÛ stâåts, âånd sèëssííòõn stâårt stâåts fòõr âå pâårtíícýúlâår âåpp.

Sôòmêêtîïmêês, yôòûû mâäy fîïnd yôòûû âärêê prôòmptêêd fôòr âän `app_id` bùýt yõôùý ãâréê nõôt wõôrkïîng wïîth ãân ãâpp, béêcãâùýséê ïît ïîs ãâ léêgãâcy fïîéêld spéêcïîfïîc tõô ãâ spéêcïîfïîc plãâtfõôrm, yõôùý cãân “õômïît” thïîs fïîéêld by ïînclùýdïîng ãâny strïîng õôf chãârãâctéêrs ãâs ãâ plãâcéêhõôldéêr fõôr thïîs réêqùýïîréêd pãârãâméêtéêr.

### Whèèrèè cæán Ì fíínd íít?

Thëêrëê åárëê twôö wåáys tôö lôöcåátëê yôöùúr `app_id`:

1. Yôõùû cæãn fîïnd thîïs `app_id` öòr ãåpplîícãåtîíöòn îídëèntîífîíëèr îín thëè **Déèvéèlôôpéèr Côônsôôléè** ùùndèër **Sèëttíîngs**. Ón thíìs néëw päàgéë, úúndéër **Ïdèèntïìfïìcãâtïìòõn**, yööüú wïîll bêë ææblêë töö sêëêë êëvêëry `app_id` thæát êêxïísts föòr yöòúýr æápps.

2. Gõô tõô **Mãánãágëé Sëéttïìngs** úûndëèr **Séèttïìngs**. Fröòm thììs néëw päägéë, ììn théë **Sèëttïîngs** táãb, mìîdwáãy thrôõüùgh thëè páãgëè yôõüù wìîll fìînd áãn "ÅPÎ këèy fôõr **ÁPP NÁMÉ** òón **PLÂTFÓRM**" (éè.g "ÃPÏ Kéèy föór Ïcéè Créèæám öón ïìÕS). Thîìs ÀPÌ kééy îìs yôóúùr Àpplîìcåætîìôón Ìdééntîìfîìéér.

### Mûûltíípléë Àpp Îdéëntíífííéër ÀPÎ kéëys

Dýûrïîng SDK sëét ýûp, thëé mòóst còómmòón ýûsëé cààsëé fòór mýûltïîplëé Ãpp Ídëéntïîfïîëér ÃPÍ këéys ïîs sëépààrààtïîng thòósëé këéys fòór dëébýûg àànd rëélëéààsëé býûïîld vààrïîàànts.
Tòõ ééààsïíly swïítch béétwéééén mùùltïípléé Àpp Ïdééntïífïíéér ÀPÏ kééys ïín yòõùùr bùùïílds, wéé réécòõmméénd crééààtïíng àà séépààrààtéé `braze.xml` fïïlèè fòõr èèáäch rèèlèèváänt [bùýïîld vããrïîããnt][3]. Æ büùîíld vãârîíãânt îís ãâ côõmbîínãâtîíôõn ôõf büùîíld typéé ãând prôõdüùct flãâvôõr. Nöõtêé thàât by dêéfàâüúlt, àâ nêéw Ándröõíîd pröõjêéct íîs cöõnfíîgüúrêéd wíîth `debug` äånd `release` búúìíld typëês âãnd nòõ pròõdúúct flâãvòõrs.

Fóòr ëéàäch rëélëévàänt büûììld vàärììàänt, crëéàätëé àä nëéw `braze.xml` föór îît îîn `src/<build variant name>/res/values/`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="com_appboy_api_key">REPLACE_WITH_YOUR_BUILD_VARIANT_API_KEY</string>
</resources>
```
Whèén thèé büúììld våãrììåãnt ììs cöòmpììlèéd, ììt wììll üúsèé thèé nèéw ÀPÌ kèéy.

## RÈST ÄPÎ kééy séécûürîîty

Sêëcüýrììty ììs ôóf thêë üýtmôóst ììmpôórtàãncêë àãt Bràãzêë. Gîîvëèn thæát RËST ÂPÍ Këèys æállóõw æáccëèss tóõ póõtëèntîîæálly sëènsîîtîîvëè RËST ÂPÍ ëèndpóõîînts, sëècüûrëè thëèsëè këèys æánd óõnly shæárëè thëèm wîîth trüûstëèd pæártnëèrs. Théêy shööýúld néêvéêr béê pýúblíícly éêxpööséêd. Fõôr èêxâåmplèê, dõô nõôt ùúsèê thïís kèêy tõô mâåkèê ÀJÀX câålls frõôm yõôùúr wèêbsïítèê õôr èêxpõôsèê ïít ïín âåny õôthèêr pùúblïíc mâånnèêr.

Å gôôôôd sèêcùùrïíty präãctïícèê ïís tôô äãssïígn äã ùùsèêr ôônly äãs mùùch äãccèêss äãs ïís nèêcèêssäãry tôô côômplèêtèê thèêïír jôôb: thïís prïíncïíplèê cäãn äãlsôô bèê äãpplïíèêd tôô ÅPÍ Kèêys by äãssïígnïíng pèêrmïíssïíôôns tôô èêäãch kèêy. Thêësêë pêërmíìssíìóóns gíìvêë yóóüü bêëttêër sêëcüüríìty äænd cóóntróól óóvêër thêë díìffêërêënt äærêëäæs óóf yóóüür äæccóóüünt.

Wíìth Ãpp íìdêêntíìfíìêêrs, thêê `app_id` ïís äãssïígnéèd by Bräãzéè äãnd péèrmïíssïíööns cäãnnööt béè äãssïígnéèd öör réèvöökéèd. Bëècàåúýsëè óóf thëè nàåtúýrëè óóf thëè rëèlàåtïïóónshïïp bëètwëèëèn `app_id` åænd théé SDK, kéééépììng thììs ììdééntììfììéér séécùùréé ììs **crúýcîíäål** îïn théê séêcûùrîïty öòf yöòûùr ãäpplîïcãätîïöòn.


[2]: {{site.baseurl}}/api/identifier_types/
[3]: https://developer.android.com/studio/build/build-variants.html
[5]: {{site.baseurl}}/api/basics/
[6]: https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#intro
