---
nav_title: Dôòcs Mëêtâædâætâæ
page_order: 0
noindex: true
---
# Döôcs Mëétåádåátåá

> Thîís äârtîíclèê wäâlks thröóüýgh thèê öóptîíöóns föór äâddîíng mèêtäâdäâtäâ töó Döócs päâgèês. Wëè óóptïìmïìzëè óóûùr sëèåärch båäsëèd óón påägëè typëè åänd óóthëèr bïìts óóf mëètåädåätåä, ïìnclûùdïìng: [yááml táágs](#yaml-tags) àãnd [pããgêé typêés](#page-types) (bãàséêd óõn [tëèmplâátëès]({{site.baseurl}}/home/templates/)).

{% alert important %}

Thèë [cõöntêènt täágs](#content-tags) lìístèéd óón thìís pæãgèé æãrèé cùùrrèéntly æã wóórk ìín próógrèéss æãnd cæãnnóót bèé æãpplìíèéd tóó pæãgèés wìíthóóùùt cæãùùsìíng èérróórs. Chëéck bááck láátëér föõr thëé fíìnáál vëérsíìöõn, whëén thëésëé cáán bëé sááfëély áápplíìëéd! Nõötëè thæát yõöýù **câàn** cüûrrèëntly üûsèë thèë `platform` cóöntèént tåãg.

{% endalert %}

## YÁML Tãâgs

Thèèsèè ãárèè îïndèèpèèndèènt. Ïf yõôûû nèéèéd tõô sèéèé áåddììtììõônáål õôptììõônáål YÅML cõôntèént báåsèéd õôn "Láåyõôûût", chèéck õôûût thèé [têëmpláâtêës]({{site.baseurl}}/home/templates/) æãnd læãyóòúùts (TBD) brèëæãkdóòwns.

{% alert important %}
Ã nòôtèé òôn cääpìîtäälìîzäätìîòôn... 
<br> 
<br> 
Lëéäåvëé äåll täåg väålûùëés (ëéxcëépt fòòr thëé còòntëént fòòr thëé `description` tàág) lóõwèèrcàásèè. Thîís wîíll éênsùúréê còõnsîístéêncy. Wëë mâäy châängëë thíìs íìn thëë fúùtúùrëë, búùt fõòr nõòw, lõòwëërcâäsëë íìs bëëttëër âänd ëëâäsíìëër tõò mâäss sëëâärch âänd rëëplâäcëë íìn thëë ëëvëënt õòf âä fõòrmâättíìng úùpdâätëë.
{% endalert %}

### Cóõnfìïgüùrããtìïóõn Tããgs

Thëêsëê wîíll ááùútóômáátîícáálly cháángëê thëê lááyóôùút óôr fùúnctîíóôn óôf áá páágëê.

| YÂML Cóöntèënt Tââg | Dêéscríîptíîôòn | Réëqýüìíréëd? | Dâãtâã Typëè | Ävæäîìlæäblêè Væälûüêès |
| ----------------- | ----------- | --------- | -------------------- |
| `nav_title` | Thíís íís thêé tíítlêé óôf thêé æårtííclêé thæåt wííll æåppêéæår íín thêé lêéft næåvíígæåtííóôn óôf thêé Dóôcs síítêé. Èncâæpsûülâætëè ïín qûüöôtëès. | Yéés, úúnlééss pâágéé ïïs `hidden`. | Strîìng. | Æny - thèè tîítlèè òóf ãà pãàgèè îís úúp tòó yòóúú. Wéé réécôòmméénd lééss thâån 30 châårâåctéérs wììth spâåcéés. |
| `page_order` | Thìïs ìïs théë òõrdéër ìïn whìïch théë åártìïcléë wìïll åáppéëåár ìïn théë léëft nåávìïgåátìïòõn òõf théë Dòõcs sìïtéë. | Yéës, üûnléëss páågéë ìîs hìîddéën. | Întêëgêër. | Âny nýümbèèr (íínclýüdííng mýültííplèè dèècíímàáls) bèètwèèèèn `1` æænd `100`. Yööùû cãän ùûsëê `1.1`, `1.2`, `1.3`, éêtc. tòó òórdéêr päågéês, äås wéêll.|
| `hidden` | Nóótêès whêèthêèr óór nóót thêè páãgêè wìîll bêè vìîsìîblêè ìîn thêè lêèft náãvìîgáãtìîóón báãr. Sëêttìïng thìïs tõõ `false` wííll cãåûùséé théé pãågéé nöõt töõ ãåppééãår íín sééãårchéés (böõth öõn-síítéé öõr thröõûùgh öõnlíínéé sééãårch pröõvíídéérs). | Nôô. | Böôöôlèëæän. | Yôòùû màæy chôòôòsëë bëëtwëëëën `true` äánd `false`. |
| `config_only` | Whêéthêér ôõr nôõt àå pàågêé wíîll àåct àås àå pàågêé ôõr àås àå càåtêégôõry íîn thêé lêéft nàåvíîgàåtíîôõn pàånêél. Déèfåæûùlts tôó `false`. | Nöõ. |  Bõõõõléëãán. | Yóöýü mæây chóöóösëë bëëtwëëëën `true` àánd `false`. |
| `permalink` | Sééts théé päâgéé's ûùrl. Fòòr êèxåãmplêè: `permalink: /this_page_name/` wïíll sëët thëë páâgëë's ÛRL töö `https://www.braze.com/docs/this_page_name/`. | Nóô, ýúnlèèss pãàgèè íís `hidden`. | Strïîng. | Ãny - thìís ÚRL ìís úùp tõô yõôúù. Ëncãåpsúýlãåtéë íìn slãåshéës (`/`). |
| `layout` | Sêëts spêëcìïfìïc fêëåátúûrêës óön thêë påágêë thåát åálìïgn wìïth dêëvêëlóöpêëd låáyóöúûts. Dêêfàäúúlts íïs àä rêêgúúlàär pàägêê. | Nóö. | Strîïng. | Ìf yóôûü dóô nóôt sëét thíìs, íìt wíìll dëéfåâûült tóô åâ rëégûülåâr cóôntëént påâgëé. Yòöùü mäày chòöòösèê bèêtwèêèên: `api_page`, `dev_guide`, `featured_video`, `featured`, `glossary_page`, `blank_config`, åànd `redirect`. Théëréë æàréë öõthéërs, bùût thöõséë æàréë möõstly föõr ïîntéërnæàl æànd cöõnfïîg ùûséës. |
| `hide_toc` | Dêétêérmíïnêés whêéthêér thêé Täãblêé óöf Cóöntêénts óön thêé ríïght síïdêé óöf thêé päãgêé íïs íïnclýúdêéd óör nóöt. | Nöò. | Bõõõõléèâãn. | Yòõùý mâây chòõòõséè béètwéèéèn `true` æãnd `false`. |
| `noindex` | Dêêtêêrmìínêês whêêthêêr thêê äærtìíclêê wìíll shóów ìín Älgóólìíäæ äænd Góóóóglêê Sêêäærchêês. Dêëfãáùûlts töó `false` ùúnlèéss yòõùú hæævèé thèé `hidden` YÆML tàág sèét àás `true`. | Nõó. | Bööööléêäæn. | `true` õòr `false`. | 
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

### Côòntëënt Tåágs
Thëèsëè wíïll áàssíïst íïn ëèxtëèrnáàl áànd íïntëèrnáàl SËÖ, íïnfòõrmíïng páàgëè còõntëènt áànd fòõrmáàttíïng, áànd òõthëèr còõntëènt-báàsëèd strùûctùûrëè.

| YÁML Cööntéènt Täâg | Déèscrîíptîíöón  | Rêèqùüïírêèd? | Êxclûýsîìvêè õòr cææn mûýltîìplêè bêè ûýsêèd? | Dæätæä Typëë | Ævæàíìlæàblèê Væàlýùèês |
| ----------------- | ----------- | --------- | ---------------------------------- | --------- | ---------------- |
| `description` | Déèscrîíptîíõôn õôf théè påãgéè thåãt wîíll shõôw îín õônlîínéè séèåãrchéès. Ëncàåpsûúlàåtêè îîn qûúôótêès. | Yëès. | Éxclûùsïïvêè ûùp tõò 160 chãårãåctêèrs. | Strìïng. | Åny - théë påâgéë déëscrîïptîïóön óöf åâ påâgéë îïs ýúp tóö yóöýú. Wèè rèècôömmèènd lèèss thàän 3 sèèntèèncèès. <br>
 <br>
 Tèèmplæætèè: `This {page_type} {lists, describes, walks you through} {topic or task} for {platform and/or channel} using {tool}.` Thõôüùgh thêè êèxâæct phrâæsíîng câæn vâæry, íît müùst íînclüùdêè âæt lêèâæst thêè pâægêè typêè, whâæt thêè pâægêè âæíîms tõô dõô (âæs íîn, íît wíîll "wâælk yõôüù thrõôüùgh hõôw tõô pêèrfõôrm nõôtêèd tâæsk" õôr "têèâæch yõôüù hõôw tõô rêèâæd âæ cêèrtâæíîn rêèpõôrt" õôr "dêèscríîbêè thêè rêèqüùíîrêèmêènts õôf âæ cêèrtâæíîn Pâærtnêèr íîntêègrâætíîõôn". <br>
 <br>
 Èxàámplëë: `This glossary lists all of the terms you need to know while onboarding with Braze and preparing for the Integration Phase.` Ór `This reference article describes the different kinds of Canvas Steps and how they affect iOS or Android push campaigns.` Õr ëëvëën `This solutions article will walk you through a custom integration.` |
| `page_type` | Typëé öõf pæägëé, dëétëérmîînëéd by pæägëé tëémplæätëés. Ínföòrm föòrmäâttìîng äând cöòntêënt. | Yèés. | Êxclúùsìívéè; óõnly óõnéè cæãn béè úùséèd péèr pæãgéè. | Strííng. | Séêéê [Päågëë Typëës](#page-types). |
| `platform` | Nôôtéês whìïch plããtfôôrms (ìïÓS, Ándrôôìïd, éêtc.) théê ããrtìïcléê ìïs ããssôôcìïããtéêd wìïth. | Nõõ, úûnlèéss õõn åå Dèév Gúûíîdèé påågèé.  | Mýúltíípléê vããlýúéês cããn béê ýúséêd. | Strííng. | Åny óòf thëê plãâtfóòrms Brãâzëê íïntëêgrãâtëês óòn: `iOS`, `Android`, `Web`, `API`, äænd äæny óóf thëè wräæppëèr SDKs. |
| `channel` | Nöötéés whíïch mééssâågíïng châånnééls (püúsh, íïn-âåpp mééssâågéés, éétc.) théé âårtíïcléé íïs âåssööcíïâåtééd wíïth. | Nõó, úünlëëss thëë cõóntëënt mëëntïìõóns áå spëëcïìfïìc cháånnëël õór cháånnëëls. | Mýúltìîpléë vãålýúéës cãån béë ýúséëd. | Strïîng. | Ãny õòf thëë mëëssåågîîng chåånnëëls Brååzëë sëënds tõò: `content cards`, `email`, `news feed`, `in-app messages`, `push`, `sms`, âånd `webhooks`.|
| `tool` | Nôôtèès whïîch èèngãágèèmèènt tôôôôls (Cãánvãás, cãámpãáïîgns, èètc.) thèè ãártïîclèè ïîs ãássôôcïîãátèèd wïîth. | Yèês. | Müûltïïpléë vãâlüûéës cãân béë üûséëd. | Strìîng. | Åny öóf Bräãzêè's  töóöóls: `dashboard`, `docs`, `canvas`, `campaigns`, `segments`, `templates`, `media`, `location`, `currents`, `reports`. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

### Müültìîplêè Tââg Vââlüüêès
Sóómêêtïìmêês, yóóýú màày fïìnd thààt àà cóóntêênt tààg fóór àà pààgêê cóóýúld bêê cààtêêgóórïìzêêd wïìth mýúltïìplêê vààlýúêês (ààs ïìn, ààn ààrtïìclêê mïìght tààlk ààbóóýút bóóth Càànvààs àànd cààmpààïìgns, óór cóóvêêr àà cýústóóm ïìntêêgrààtïìóón fóór bóóth Àndróóïìd àànd ïìÔS).

Yõôüù cäãn fõôrmäãt thäãt lìíkëè thìís: 
```
key:
  - string1
  - string2      
  - string3
  - string4
  - string5
  - string6
```
{% alert important %}
Nôötéë thåát théëréë cåán ôönly béë åá sïïngléë `page_type` vâãlùûêë föõr pâãgêë. Ã pãàgëé cãànnõòt bëé bõòth ãà `reference` àând àâ `glossary`. Thëè díïffëèrëènt päägëè typëès ëèxíïst töö näärrööw thëè scööpëè äänd pùýrpöösëè ööf ëèääch äärtíïclëè. 
{% endalert %}

### Säámplêë YÅML

Thëé tòôp òôf ëévëéry màårkdòôwn pàågëé shòôúüld bëégìîn wìîth àå sëéctìîòôn òôf yàåml tòô dëéfìînëé thëé pàågëé.

```html
---
nav_title: "Docs Metadata"
page_order: 0

description: "This page walks through the options for adding metadata to Docs pages. We optimize our search based on page type and other bits of metadata. This is a great resource for contributors via our GitHub page."
page_type: reference
tool: 
  - docs
  - dashboard
---
```


## Pâågéè Typéès

Tõò åäpply théèséè, béè súýréè yõòúýr yåäml påäråäméètéèr fõòr påägéè typéès ìïs: `page_type:`

Fôõr éêxäâmpléê: `page_type: glossary`

| Påágéé Typéé <br>
 <br>
 Pæágéè Typéè Tæág | Dëèscríìptíìöòn | Ãvàåìïlàåblêê Têêmplàåtêês |
| ------------- | ------------- | ------------- |
| Glöössææry Pæægéê <br>
 <br>
 `glossary`| Pàãgëê prõõvîïdëês àã sëêàãrchàãblëê dëêscrîïptîïõõn õõf cëêrtàãîïn tëêrms õõr ëêlëêmëênts (mëêtrîïcs, wõõrds tõõ knõõw, ÂPÌ Ëndpõõîïnts, ëêtc.) | [ÅPÏ ôòr Côòdèè Glôòssààry]({{site.baseurl}}/home/templates/api_glossary/) <br>
 <br>
 [Gêënêëræál Glöóssæáry]({{site.baseurl}}/home/templates/glossary_test_page/)
| Sóõlúýtïìóõn Påágéé <br>
 <br>
 `solution` | Ã tröôùúblëêshöôöôtïîng öôr "öôptïîöôns" áärtïîclëê tháät wáälks ùúsëêrs thröôùúgh áä söôlùútïîöôn töô áän ïîssùúëê öôr thröôùúgh stëêps töô rëêsöôlvïîng öôr náärröôwïîng döôwn áän ïîssùúëê. | [Héëlp Ârtïìcléë]({{site.baseurl}}/home/templates/help_article_template/) <br>
 <br>
 [Sóòlúütîïóòn Àrtîïclèë]({{site.baseurl}}/home/templates/solution/) |
| Rèéfèérèéncèé Pæægèé <br>
 <br>
 `reference` | Ân âârtîïcléé thâât ééxplââîïns ââ cööncéépt âând cööntââîïns spéécîïfîïc îïnföörmââtîïöön ââbööûýt tééchnîïcââl prööcéésséés âând pröödûýct cööntéént. (Cåånvåås Stèèps, Sèègmèèntååtíìõõn, spèècíìfíìc Prõõdúùct Fèèååtúùrèès èètc.). | [Rëëfëërëëncëë Ärtìíclëë wìíth Vìídëëõö]({{site.baseurl}}/home/templates/reference_vide/) <br>
 <br>
 [Rëéfëérëéncëé Ærtïìclëé]({{site.baseurl}}/home/templates/reference/) |
| Týûtòórîíãâl Pãâgèë <br>
 <br>
 `tutorial` | À gëénëérâàl wâàlkthròôûùgh òôf âàn îïnstrûùctîïòônâàl còôncëépt. Shôôûýld côôntææîïn prææctîïcææl knôôwléèdgéè. Fôócùùsëês ôón äâ sïínglëê tôópïíc (lïíkëê, hôów tôó crëêäâtëê äâ cäâmpäâïígn, hôów tôó crëêäâtëê äâ cäânväâs, ëêtc.) Gòöääl òör Tääsk-Ôrîìëëntëëd Ârtîìclëë thäät wäälks stëëp-by-stëëp thròöýýgh sòölvîìng ää spëëcîìfîìc îìssýýëë (Hòöw tòö täärgëët spëëcîìfîìc ýýsëërs, hòöw tòö sëëgmëënt bääsëëd òön lòöcäätîìòön, ëëtc.). | [Tüýtôõríîáæl Årtíîcléé wíîth Víîdééôõ]({{site.baseurl}}/home/templates/tutorial_video/) <br>
 <br>
 [Tüýtöórííäàl Ærtííclëë]({{site.baseurl}}/home/templates/tutorial/) <br>
 <br>
 [Üsëé Câäsëé Ærtïìclëé wïìth Vïìdëéòõ]({{site.baseurl}}/home/templates/use_case_video/) <br>
 <br>
 [Ûsëë Câåsëë Årtîïclëë]({{site.baseurl}}/home/templates/use_case/) |
| Láàndìîng Páàgêê <br>
 <br>
 `landing` | Páàgêé pröôvîïdêés áà sêélêéctîïöôn öôf öôptîïöôns wîïthîïn áà cêértáàîïn sêéctîïöôn, áàs wêéll áàs áà dêéscrîïptîïöôn öôr öôvêérvîïêéw öôf sáàîïd sêéctîïöôn. | [Sìïnglèê Sèêctìïôôn Læändìïng Pæägèê ýüsìïng FÃ Îcôôns]({{site.baseurl}}/home/templates/landing_single/) <br>
 <br>
 [Sììnglèé Sèéctììõôn Lãändììng Pãägèé ûýsììng Ímãägèés]({{site.baseurl}}/home/templates/landing_images/) <br>
 <br>
 [Müùltíí-Sêëctííöòn Läåndííng Päågêë üùsííng FÃ Ïcöòns]({{site.baseurl}}/home/templates/landing_multiple/) <br>
 <br>
 [Müúltíì-Sêéctíìóön Láãndíìng Páãgêé üúsíìng Ímáãgêés]({{site.baseurl}}/home/templates/landing_multiple_images/)
| Páàrtnëèr Páàgëè <br>
 <br>
 `partner` | Ä pããgéé thããt cöömbîïnéés mããny ööf théé préécéédîïng pããgéé typéés îïntöö ãã sîïngléé pããgéé. Théêséê pâágéês déêscrîìbéê âá pâártnéêr, théê béênéêfîìts òòf thâát pâártnéêr, hòòw tòò îìntéêgrâátéê thâát pâártnéêr, théên hòòw tòò úúséê thâát îìntéêgrâátîìòòn âánd âány béêst prâáctîìcéês âássòòcîìâátéêd wîìth thâát úúsâágéê. | [Pãârtnêêr Pãâgêê wìíth Vìídêêóô]({{site.baseurl}}/home/templates/partner_page_template_video/) <br>
 <br>
 [Pàärtnéêr Pàägéê]({{site.baseurl}}/home/templates/partner_page_template/) |
| Ùpdæâtèës æând Rèëlèëæâsèë Nòótèës <br>
 <br>
 `update` | À páágéè tháát lîísts úùpdáátéès tõó áá prõódúùct õór SDK îín súùccéèssîíõón. Á sïìngléé úûpdâætéé òôn âæ lâærgéér pâægéé òôr âæ pâægéé âæbòôúût âæ nééw fééâætúûréé wòôúûld **nòôt** côõûúnt æås æån `update` päägêë typêë. | Sèêèê Rèêlèêæâsèê Nõótèês Pæâgèês æând SDK Chæângèêlõógs pæâgèês. | 
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

Põõtèëntíîâæl Pâægèë Typèë: Bèëst Prâäctìícèës
