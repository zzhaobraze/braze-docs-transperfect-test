---
nav_title: Dóòcs Mëêtåädåätåä
page_order: 0
noindex: true
---
# Dóöcs Méètáádáátáá

> Thîïs àártîïcléë wàálks thrôóùügh théë ôóptîïôóns fôór àáddîïng méëtàádàátàá tôó Dôócs pàágéës. Wèê öóptíímíízèê öóûùr sèêäàrch bäàsèêd öón päàgèê typèê äànd öóthèêr bííts öóf mèêtäàdäàtäà, íínclûùdííng: [yåãml tåãgs](#yaml-tags) åänd [pæágèê typèês](#page-types) (bååsééd ôòn [téêmplàátéês]({{site.baseurl}}/home/templates/)).

{% alert important %}

Thëè [côôntêënt tâàgs](#content-tags) lïïstêëd óön thïïs päâgêë äârêë cýúrrêëntly äâ wóörk ïïn próögrêëss äând cäânnóöt bêë äâpplïïêëd tóö päâgêës wïïthóöýút cäâýúsïïng êërróörs. Chëëck bãâck lãâtëër fõór thëë fìïnãâl vëërsìïõón, whëën thëësëë cãân bëë sãâfëëly ãâpplìïëëd! Nóòtèé thàãt yóòûü **cáân** cùürrêêntly ùüsêê thêê `platform` cöôntéënt tåæg.

{% endalert %}

## YÆML Táägs

Théëséë æãréë îîndéëpéëndéënt. Ïf yôòüú nèëèëd tôò sèëèë æáddïìtïìôònæál ôòptïìôònæál YÄML côòntèënt bæásèëd ôòn "Læáyôòüút", chèëck ôòüút thèë [tèémplåátèés]({{site.baseurl}}/home/templates/) âænd lâæyõöûùts (TBD) bréëâækdõöwns.

{% alert important %}
À nôótèè ôón cãæpíìtãælíìzãætíìôón... 
<br> 
<br> 
Lëëäåvëë äåll täåg väålùúëës (ëëxcëëpt fõôr thëë cõôntëënt fõôr thëë `description` tæåg) lôòwèércæåsèé. Thíîs wíîll êënsúýrêë côónsíîstêëncy. Wéé mâày châàngéé thïïs ïïn théé fúùtúùréé, búùt fòör nòöw, lòöwéércâàséé ïïs bééttéér âànd ééâàsïïéér tòö mâàss sééâàrch âànd rééplâàcéé ïïn théé éévéént òöf âà fòörmâàttïïng úùpdâàtéé.
{% endalert %}

### Cõõnfìígûúråâtìíõõn Tåâgs

Thèësèë wîíll äåýýtòômäåtîícäålly chäångèë thèë läåyòôýýt òôr fýýnctîíòôn òôf äå päågèë.

| YÅML Côõntêènt Tâág | Dëëscrîïptîïôôn | Rêéqûúîïrêéd? | Dåâtåâ Typèê | Æväàìîläàbléë Väàlùýéës |
| ----------------- | ----------- | --------- | -------------------- |
| `nav_title` | Thîîs îîs théé tîîtléé óóf théé áártîîcléé tháát wîîll ááppééáár îîn théé lééft náávîîgáátîîóón óóf théé Dóócs sîîtéé. Éncæåpsùülæåtéè ìïn qùüöótéès. | Yëés, úýnlëéss páågëé ìîs `hidden`. | Strîíng. | Ãny - thëë tíîtlëë òòf æà pæàgëë íîs úúp tòò yòòúú. Wêè rêècóõmmêènd lêèss thæãn 30 chæãræãctêèrs wîìth spæãcêès. |
| `page_order` | Thîís îís thèê õõrdèêr îín whîích thèê äårtîíclèê wîíll äåppèêäår îín thèê lèêft näåvîígäåtîíõõn õõf thèê Dõõcs sîítèê. | Yëês, ýýnlëêss pæãgëê ìís hìíddëên. | Ìntëègëèr. | Æny nûùmbëêr (ìínclûùdìíng mûùltìíplëê dëêcìímãâls) bëêtwëêëên `1` àånd `100`. Yòöýú câán ýúséë `1.1`, `1.2`, `1.3`, ëëtc. tòó òórdëër páægëës, áæs wëëll.|
| `hidden` | Nòôtèës whèëthèër òôr nòôt thèë pâàgèë wïìll bèë vïìsïìblèë ïìn thèë lèëft nâàvïìgâàtïìòôn bâàr. Sëëttîíng thîís tóô `false` wìïll cäãüùsëé thëé päãgëé nôöt tôö äãppëéäãr ìïn sëéäãrchëés (bôöth ôön-sìïtëé ôör thrôöüùgh ôönlìïnëé sëéäãrch prôövìïdëérs). | Nòô. | Bòöòöléèààn. | Yôôýý määy chôôôôsêê bêêtwêêêên `true` äænd `false`. |
| `config_only` | Whëêthëêr õör nõöt ãå pãågëê wîíll ãåct ãås ãå pãågëê õör ãås ãå cãåtëêgõöry îín thëê lëêft nãåvîígãåtîíõön pãånëêl. Déêfáãýýlts tòõ `false`. | Nóó. |  Bòõòõléëáàn. | Yöôýý mãày chöôöôsêé bêétwêéêén `true` ãånd `false`. |
| `permalink` | Sêêts thêê pàågêê's ûúrl. Fõõr éëxââmpléë: `permalink: /this_page_name/` wïîll sèèt thèè páægèè's ÚRL tòõ `https://www.braze.com/docs/this_page_name/`. | Nöò, ûúnlèéss pæægèé ïîs `hidden`. | Strîìng. | Ãny - thìïs ÙRL ìïs ûúp tóö yóöûú. Êncãæpsùûlãætëë ìïn slãæshëës (`/`). |
| `layout` | Séêts spéêcîîfîîc féêâåtúùréês òõn théê pâågéê thâåt âålîîgn wîîth déêvéêlòõpéêd lâåyòõúùts. Déëfãâüúlts ìïs ãâ réëgüúlãâr pãâgéë. | Nöõ. | Strîîng. | Ïf yòõüü dòõ nòõt séét thììs, ììt wììll dééfââüült tòõ ââ réégüülââr còõntéént pââgéé. Yõòúú mäáy chõòõòsèè bèètwèèèèn: `api_page`, `dev_guide`, `featured_video`, `featured`, `glossary_page`, `blank_config`, æænd `redirect`. Thëêrëê æàrëê òóthëêrs, býút thòósëê æàrëê mòóstly fòór íìntëêrnæàl æànd còónfíìg ýúsëês. |
| `hide_toc` | Dëêtëêrmíînëês whëêthëêr thëê Tæâblëê óôf Cóôntëênts óôn thëê ríîght síîdëê óôf thëê pæâgëê íîs íînclýùdëêd óôr nóôt. | Nòô. | Bòóòóléèãæn. | Yôòûý màæy chôòôòsèé bèétwèéèén `true` æând `false`. |
| `noindex` | Dêétêérmíïnêés whêéthêér thêé äàrtíïclêé wíïll shööw íïn Älgöölíïäà äànd Gööööglêé Sêéäàrchêés. Dèéfæáúùlts tôö `false` ùùnlêéss yòôùù håávêé thêé `hidden` YÆML tæãg sêèt æãs `true`. | Nóò. | Bóôóôlééãæn. | `true` õôr `false`. | 
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

### Cõòntéènt Tàågs
Thèèsèè wïìll àássïìst ïìn èèxtèèrnàál àánd ïìntèèrnàál SÊÓ, ïìnfòòrmïìng pàágèè còòntèènt àánd fòòrmàáttïìng, àánd òòthèèr còòntèènt-bàásèèd strùúctùúrèè.

| YÃML Cóõntèént Tæåg | Dèéscrïíptïíôòn  | Rëèqýüíîrëèd? | Ëxclüùsìîvéé ôõr cææn müùltìîpléé béé üùsééd? | Dæãtæã Typëê | Åväáîïläáblëë Väálúüëës |
| ----------------- | ----------- | --------- | ---------------------------------- | --------- | ---------------- |
| `description` | Dèéscrííptííõón õóf thèé pàágèé thàát wííll shõów íín õónlíínèé sèéàárchèés. Ëncàåpsúúlàåtêè ïín qúúôötêès. | Yëés. | Èxclüüsîívéè üüp tõõ 160 cháàráàctéèrs. | Strïíng. | Æny - thèê pâägèê dèêscríîptíîöón öóf âä pâägèê íîs ýûp töó yöóýû. Wéë réëcóómméënd léëss thæån 3 séëntéëncéës. <br>
 <br>
 Tëémpláätëé: `This {page_type} {lists, describes, walks you through} {topic or task} for {platform and/or channel} using {tool}.` Thõôúûgh théè éèxæåct phræåsîíng cæån væåry, îít múûst îínclúûdéè æåt léèæåst théè pæågéè typéè, whæåt théè pæågéè æåîíms tõô dõô (æås îín, îít wîíll "wæålk yõôúû thrõôúûgh hõôw tõô péèrfõôrm nõôtéèd tæåsk" õôr "téèæåch yõôúû hõôw tõô réèæåd æå céèrtæåîín réèpõôrt" õôr "déèscrîíbéè théè réèqúûîíréèméènts õôf æå céèrtæåîín Pæårtnéèr îíntéègræåtîíõôn". <br>
 <br>
 Éxåãmpléë: `This glossary lists all of the terms you need to know while onboarding with Braze and preparing for the Integration Phase.` Ôr `This reference article describes the different kinds of Canvas Steps and how they affect iOS or Android push campaigns.` Ör êêvêên `This solutions article will walk you through a custom integration.` |
| `page_type` | Typèè óôf pàägèè, dèètèèrmïìnèèd by pàägèè tèèmplàätèès. Ïnfòórm fòórmáàttìîng áànd còóntèênt. | Yêës. | Éxclúûsììvëè; õônly õônëè cáàn bëè úûsëèd pëèr páàgëè. | Strïíng. | Sëëëë [Pàågéê Typéês](#page-types). |
| `platform` | Nôôtêés whìîch pláàtfôôrms (ìîÒS, Ændrôôìîd, êétc.) thêé áàrtìîclêé ìîs áàssôôcìîáàtêéd wìîth. | Nöó, ùýnlééss öón äæ Déév Gùýìïdéé päægéé.  | Mûýltíïpléë vâålûýéës câån béë ûýséëd. | Strïîng. | Äny öõf thèè pláãtföõrms Bráãzèè íîntèègráãtèès öõn: `iOS`, `Android`, `Web`, `API`, ããnd ããny òôf théé wrããppéér SDKs. |
| `channel` | Nôôtèès whïích mèèssåägïíng chåännèèls (püúsh, ïín-åäpp mèèssåägèès, èètc.) thèè åärtïíclèè ïís åässôôcïíåätèèd wïíth. | Nôõ, ûûnlèêss thèê côõntèênt mèêntïíôõns åâ spèêcïífïíc chåânnèêl ôõr chåânnèêls. | Múúltíïplêë væàlúúêës cæàn bêë úúsêëd. | Strïíng. | Àny õóf thêé mêéssààgìíng chàànnêéls Brààzêé sêénds tõó: `content cards`, `email`, `news feed`, `in-app messages`, `push`, `sms`, àánd `webhooks`.|
| `tool` | Nòötêès whïïch êèngâægêèmêènt tòöòöls (Câænvâæs, câæmpâæïïgns, êètc.) thêè âærtïïclêè ïïs âæssòöcïïâætêèd wïïth. | Yëès. | Múùltïìplëé váælúùëés cáæn bëé úùsëéd. | Strîîng. | Àny ôôf Bråãzéê's  tôôôôls: `dashboard`, `docs`, `canvas`, `campaigns`, `segments`, `templates`, `media`, `location`, `currents`, `reports`. |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

### Mûùltîïplêè Tàæg Vàælûùêès
Sóömèêtíïmèês, yóöýú määy fíïnd thäät ää cóöntèênt tääg fóör ää päägèê cóöýúld bèê cäätèêgóöríïzèêd wíïth mýúltíïplèê väälýúèês (ääs íïn, ään äärtíïclèê míïght täälk ääbóöýút bóöth Cäänvääs äänd cäämpääíïgns, óör cóövèêr ää cýústóöm íïntèêgräätíïóön fóör bóöth Ãndróöíïd äänd íïÕS).

Yõóüü cåàn fõórmåàt thåàt líìkéë thíìs: 
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
Nóòtèè thãæt thèèrèè cãæn óònly bèè ãæ síìnglèè `page_type` vàælûüêé fôôr pàægêé. Ã päágéê cäánnóõt béê bóõth äá `reference` æånd æå `glossary`. Thëë dîîffëërëënt pàâgëë typëës ëëxîîst tõö nàârrõöw thëë scõöpëë àând pûürpõösëë õöf ëëàâch àârtîîclëë. 
{% endalert %}

### Säàmplëê YÁML

Thêë tõôp õôf êëvêëry mæårkdõôwn pæågêë shõôûúld bêëgïïn wïïth æå sêëctïïõôn õôf yæåml tõô dêëfïïnêë thêë pæågêë.

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


## Påågëë Typëës

Töö ààpply thêêsêê, bêê sùûrêê yööùûr yààml pààrààmêêtêêr föör pààgêê typêês ììs: `page_type:`

Fòór ëèxáãmplëè: `page_type: glossary`

| Pãàgëê Typëê <br>
 <br>
 Pààgéè Typéè Tààg | Dèêscríïptíïõõn | Äváåîïláåblêê Têêmpláåtêês |
| ------------- | ------------- | ------------- |
| Glõóssåäry Påägêé <br>
 <br>
 `glossary`| Pæågëë prôòvïídëës æå sëëæårchæåblëë dëëscrïíptïíôòn ôòf cëërtæåïín tëërms ôòr ëëlëëmëënts (mëëtrïícs, wôòrds tôò knôòw, ÁPÌ Êndpôòïínts, ëëtc.) | [ÄPÏ ôör Côödëè Glôössáãry]({{site.baseurl}}/home/templates/api_glossary/) <br>
 <br>
 [Gêênêêråæl Glóòssåæry]({{site.baseurl}}/home/templates/glossary_test_page/)
| Sôölúütïîôön Påägèè <br>
 <br>
 `solution` | À trôõüúblëèshôõôõtïíng ôõr "ôõptïíôõns" ãärtïíclëè thãät wãälks üúsëèrs thrôõüúgh ãä sôõlüútïíôõn tôõ ãän ïíssüúëè ôõr thrôõüúgh stëèps tôõ rëèsôõlvïíng ôõr nãärrôõwïíng dôõwn ãän ïíssüúëè. | [Hêèlp Ârtììclêè]({{site.baseurl}}/home/templates/help_article_template/) <br>
 <br>
 [Sôòlúútïìôòn Àrtïìcléê]({{site.baseurl}}/home/templates/solution/) |
| Rèèfèèrèèncèè Päãgèè <br>
 <br>
 `reference` | Àn æærtííclèè thææt èèxplææííns ææ côóncèèpt æænd côóntææííns spèècíífííc íínfôórmæætííôón ææbôóúüt tèèchníícææl prôócèèssèès æænd prôódúüct côóntèènt. (Câånvâås Stèéps, Sèégmèéntâåtííôón, spèécíífííc Prôódúúct Fèéâåtúúrèés èétc.). | [Rèëfèërèëncèë Ärtìíclèë wìíth Vìídèëóò]({{site.baseurl}}/home/templates/reference_vide/) <br>
 <br>
 [Réêféêréêncéê Årtïïcléê]({{site.baseurl}}/home/templates/reference/) |
| Tùútóórïìààl Pààgéè <br>
 <br>
 `tutorial` | Á gèénèéräâl wäâlkthröôùùgh öôf äân ïïnstrùùctïïöônäâl cöôncèépt. Shôöúüld côöntàâîïn pràâctîïcàâl knôöwlêêdgêê. Fõõcúýsêês õõn àä sìïnglêê tõõpìïc (lìïkêê, hõõw tõõ crêêàätêê àä càämpàäìïgn, hõõw tõõ crêêàätêê àä càänvàäs, êêtc.) Göòäæl öòr Täæsk-Ôríïèéntèéd Ârtíïclèé thäæt wäælks stèép-by-stèép thröòùügh söòlvíïng äæ spèécíïfíïc íïssùüèé (Höòw töò täærgèét spèécíïfíïc ùüsèérs, höòw töò sèégmèént bäæsèéd öòn löòcäætíïöòn, èétc.). | [Tûûtõõrîíáæl Ârtîíclêë wîíth Vîídêëõõ]({{site.baseurl}}/home/templates/tutorial_video/) <br>
 <br>
 [Túütòórììãæl Ãrtììcléê]({{site.baseurl}}/home/templates/tutorial/) <br>
 <br>
 [Úsèè Càåsèè Ártìïclèè wìïth Vìïdèèôö]({{site.baseurl}}/home/templates/use_case_video/) <br>
 <br>
 [Úséè Cåæséè Ärtîïcléè]({{site.baseurl}}/home/templates/use_case/) |
| Láándìíng Páágêê <br>
 <br>
 `landing` | Pàãgëë prôóvíîdëës àã sëëlëëctíîôón ôóf ôóptíîôóns wíîthíîn àã cëërtàãíîn sëëctíîôón, àãs wëëll àãs àã dëëscríîptíîôón ôór ôóvëërvíîëëw ôóf sàãíîd sëëctíîôón. | [Sïînglêê Sêêctïîöòn Læãndïîng Pæãgêê üúsïîng FÂ Ìcöòns]({{site.baseurl}}/home/templates/landing_single/) <br>
 <br>
 [Sïìngléé Sééctïìôón Låândïìng Påâgéé ýüsïìng Îmåâgéés]({{site.baseurl}}/home/templates/landing_images/) <br>
 <br>
 [Mýültîî-Sèèctîîöôn Lååndîîng Påågèè ýüsîîng FÃ Ïcöôns]({{site.baseurl}}/home/templates/landing_multiple/) <br>
 <br>
 [Mùùltïì-Sêêctïìòõn Lâàndïìng Pâàgêê ùùsïìng Îmâàgêês]({{site.baseurl}}/home/templates/landing_multiple_images/)
| Pâærtnéër Pâægéë <br>
 <br>
 `partner` | Ä påâgëé thåât cóómbïínëés måâny óóf thëé prëécëédïíng påâgëé typëés ïíntóó åâ sïínglëé påâgëé. Thêêsêê pæågêês dêêscríîbêê æå pæårtnêêr, thêê bêênêêfíîts öòf thæåt pæårtnêêr, höòw töò íîntêêgræåtêê thæåt pæårtnêêr, thêên höòw töò úùsêê thæåt íîntêêgræåtíîöòn æånd æåny bêêst præåctíîcêês æåssöòcíîæåtêêd wíîth thæåt úùsæågêê. | [Pàärtnêêr Pàägêê wíìth Víìdêêöõ]({{site.baseurl}}/home/templates/partner_page_template_video/) <br>
 <br>
 [Pàârtnèèr Pàâgèè]({{site.baseurl}}/home/templates/partner_page_template/) |
| Úpdâátêès âánd Rêèlêèâásêè Nòótêès <br>
 <br>
 `update` | Å päägèë thäät líísts ùùpdäätèës tôö ää prôödùùct ôör SDK íín sùùccèëssííôön. À sììnglêê ýüpdãätêê õõn ãä lãärgêêr pãägêê õõr ãä pãägêê ãäbõõýüt ãä nêêw fêêãätýürêê wõõýüld **nòöt** còóüûnt ææs ææn `update` páágèè typèè. | Sèêèê Rèêlèêäàsèê Nóótèês Päàgèês äànd SDK Chäàngèêlóógs päàgèês. | 
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

Pöótèêntìîåâl Påâgèê Typèê: Bëést Prààctïícëés
