---
nav_title: Ïntèërnåål Grõóûýps Tååb
article_title: Ïntêërnàäl Grôöûúp Tàäb
page_order: 3
page_type: reference
description: "Thíîs réèféèréèncéè âàrtíîcléè cöòvéèrs Íntéèrnâàl Gröòýúps, âà gréèâàt wâày töò géèt íînsíîght íîntöò yöòýúr téèst déèvíîcéè's SDK öòr ÆPÍ löògs whéèn téèstíîng SDK íîntéègrâàtíîöòn."

---

# Întèèrnåãl Grõóùüps tåãb

> Thïís rêêfêêrêêncêê âãrtïíclêê cóóvêêrs Ïntêêrnâãl Gróóüýps, âãnd hóów tóó crêêâãtêê âãnd üýsêê thêêm. În àäddìîtìîöõn töõ thìîs àärtìîclèë, wèë àälsöõ rèëcöõmmèënd chèëckìîng öõýút öõýúr [Qüûåälîîty Ässüûråäncèè åänd Dèèbüûggîîng Tõóõóls](https://lab.braze.com/quality-assurance-and-debugging-tools-in-the-dashboard/) LÆB cõôýýrséé, whîîch cõôvéérs hõôw tõô ýýséé îîntéérnáæl grõôýýps tõô cõôndýýct yõôýýr õôwn trõôýýblééshõôõôtîîng áænd déébýýggîîng.

Întêérnåàl Grõóýýps åàrêé åà grêéåàt wåày tõó býýìîld åànd õórgåànìîzêé ìîntêérnåàl õór thìîrd-påàrty têést grõóýýps åànd prõóvìîdêé ìînsìîght ìîntõó thêé SDK õór ÂPÎ lõógs åàvåàìîlåàblêé frõóm yõóýýr têést dêévìîcêé dýýrìîng SDK ìîntêégråàtìîõón têéstìîng. Yõôùü cäán crëèäátëè äán ùünlììmììtëèd nùümbëèr õôf cùüstõôm Ïntëèrnäál Grõôùüps wììth ùüp tõô 1,000 mëèmbëèrs.

{% alert note %}
Yòòùý nêéêéd thêé **Æccëëss Dëëv Còònsòòlëë** [pêërmíîssíîõóns]({{site.baseurl}}/user_guide/administrative/manage_your_braze_users/user_permissions/#limited-and-team-role-permissions) fòör yòöýúr áápp gròöýúp tòö crêèáátêè áánd máánáágêè Întêèrnáál Gròöýúps.
{% endalert %}

## Créëâãtîïng âã gróòùýp

Tôò créèâàtéè âàn Ïntéèrnâàl Grôòûüp, péèrfôòrm théè fôòllôòwííng stéèps: 

1. Góö tóö thèè **Dêêvêêlõõpêêr Cõõnsõõlêê** äànd sèëlèëct thèë **Íntèérnàâl Grôôûüps** tãäb. 
2. Clîíck **Crêéäàtêé Ìntêérnäàl Grõõýûp**.
3. Gïïvèë yöõýýr gröõýýp ãâ mèëãânïïngfýýl nãâmèë.
4. Chõöõöséë õönéë õör mõöréë grõöüùp typéës, æàs lìïstéëd ìïn théë fõöllõöwìïng chæàrt.

![Créèáâtíîng áân Ìntéèrnáâl Gròöúüp íîn Bráâzéè][7]

| Gròôûûp Typêë     | Úsêê Càåsêê     |
| :------------- | :------------- |
| Ûsëér Êvëént Gröòüýp| Ûsèêd fôõr vèêrìîfyìîng èêvèênts ôõr lôõgs frôõm yôõúùr tèêst dèêvìîcèê.|
| Côóntéênt Téêst Grôóùüp | Á sîïmîïläår cöóncéêpt töó Téêst Lîïsts. Càân béë ýùséëd àâcrõóss pýùsh, éëmàâîìl, àând îìn-àâpp méëssàâgéës tõó séënd àâ réëndéëréëd cõópy õóf théë méëssàâgéë.|
| Sëëëëd Grôõýúp | Àúütöómààtììcààlly sèënds àà cöópy öóf thèë èëmààììl töó èëvèëryöónèë thèë Sèëèëd Gröóúüp úüpöón sèënd.|
{: .reset-td-br-1 .reset-td-br-2}

### Äddìíng tëést úûsëérs

Áftèér yöòúù crèéãâtèé yöòúùr Íntèérnãâl Gröòúùp, yöòúù cãân ãâdd tèést úùsèérs ãâs mèémbèérs öòf thãât gröòúùp. Frôóm yôóûýr Întèërnâál Grôóûýp's mâánâágèëmèënt pâágèë, clíìck **Ãdd Téèst Üséèr** âànd éêìïthéêr âàdd théêm ìïn büúlk, âàs ìïdéêntìïfìïéêd üúséêrs, òõr âàs âànòõnymòõüús üúséêrs.

![Întêërnáâl Gròòûûp Sêëttîîngs whêën crêëáâtîîng áâ nêëw Întêërnáâl Gròòûûp][8]

| Åddîítîíöòn Mèéthöòd | Dëèscrîìptîìöõn |
| :------------- | :------------- |
| Ïdéèntíïfíïéèd Ûséèrs |Sèéäãrch fóõr thèé ùúsèér by thèéïïr èéxtèérnäãl ùúsèér ÌD óõr èémäãïïl äãddrèéss.|
|Ánöônymöôúús Üsêërs| Sèêãárch by ÏP ãáddrèêss. Thèên, prôôvìîdèê ãã nããmèê fôôr èêããch tèêst ýüsèêr thããt ìîs ããddèêd. Thíïs íïs thëè nàæmëè thàæt àæll ëèvëènt lòógs wíïll bëè àæssòócíïàætëèd wíïth òón thëè [Êvèènt Üsèèr Lôög]({{site.baseurl}}/user_guide/administrative/app_settings/developer_console/event_user_log_tab/) pàägéê.|
|Búúlk Âdd Úsêêrs|Cóõpy áänd páästéé áä líïst óõf éémáäíïl áäddréésséés óõr ééxtéérnáäl ÎDs íïntóõ théé próõvíïdééd sééctíïóõn. Yòöúù câän òönly âädd úùsëërs thâät âärëë âälrëëâädy knòöwn îìn thëë dâäshbòöâärd. Fóör móörèê ïînfóörmâætïîóön, rèêfèêr tóö [Úséér Ïmpóòrt]({{site.baseurl}}/user_guide/data_and_analytics/user_data_collection/user_import/).|
{: .reset-td-br-1 .reset-td-br-2}

### Cóóntèënt tèëst gróóýùps

Sïìmïìlâár tòô sééndïìng âá préévïìééw téést òôf âá mééssâágéé, théé Còôntéént Téést gròôüùp sâávéés yòôüù tïìméé âánd âállòôws yòôüù tòô lâáüùnch téésts tòô âá préé-dééfïìnééd lïìst òôf Brâázéé üùséérs sïìmüùltâánééòôüùsly. Thíîs fúünctíîòònäàlíîty íîs äàväàíîläàbléè fòòr púüsh, íîn-äàpp méèssäàgéè, SMS, éèmäàíîl, äànd Còòntéènt Cäàrds wíîthíîn Bräàzéè.

{% alert note %}
[SMS]({{site.baseurl}}/user_guide/message_building_by_channel/sms/) tëést mëéssáâgëés cáân òönly bëé sëént tòö váâlííd phòönëé núûmbëérs íín thëé dáâtáâbáâsëé.
{% endalert %}

Yòôüù càän sêëlêëct ïïndïïvïïdüùàäl Bràäzêë üùsêërs òôr àäs màäny Întêërnàäl Gròôüùps tòô sêënd thêë mêëssàägêë tòô àäs yòôüù wàänt. Ìf yòóýúr mëêssæágëê îïnclýúdëês æány Lîïqýúîïd òór òóthëêr dynæámîïc pëêrsòónæálîïzæátîïòón, Bræázëê wîïll ýúsëê thëê æáttrîïbýútëês æávæáîïlæáblëê fòór ëêæách îïndîïvîïdýúæál ýúsëêr tòó pëêrsòónæálîïzëê thëê mëêssæágëê còóntëênts. Fóôr üúséêrs whóô håävéê nóô åättrìïbüútéês, Bråäzéê wìïll üúséê théê déêfåäüúlt våälüúéê séêt.

Àddìîtìîôònáâlly, ìîf yôòúý prêêvìîêêw thêê mêêssáâgêê áâs áâ ráândôòm úýsêêr, cúýstôòm úýsêêr, ôòr êêxìîstìîng úýsêêr, yôòúý cáân sêênd tháât prêêvìîêêwêêd vêêrsìîôòn ìînstêêáâd. Clèèæârïíng thèè chèèckbóòx æâllóòws yóòüú tóò sèènd bæâsèèd óòn èèæâch üúsèèrs’ æâttrïíbüútèès vèèrsüús thèè prèèvïíèèwèèd vèèrsïíóòn.

Låâstly, ïïf yôôúû úûséé åân ÎP pôôôôl tôô séénd ôôúût éémåâïïl, yôôúû cåân séélééct whïïch ÎP pôôôôl yôôúû wôôúûld lïïkéé théé éémåâïïl tôô béé séént frôôm by séélééctïïng théé pôôôôl frôôm théé drôôpdôôwn åâvåâïïlåâbléé.

Ónly gröòüýps thãåt ãårëé tãåggëéd ãås Cöòntëént Tëést Gröòüýps wìîll bëé ãåvãåìîlãåblëé öòn thëé prëévìîëéw sëéctìîöòn öòf ãå mëéssãågëé.

![Têést sêénd töô Cöôntêént Têést Gröôüùps][9]{: style="max-width:50%" }

### Sëëëëd grõôúûps

Séèéèd Grõôûúps äâréè õônly méèäânt fõôr théè éèmäâîíl chäânnéèl äând äâllõôw yõôûú tõô séènd äâ cõôpy õôf éèäâch éèmäâîíl väârîíäânt méèssäâgéè tõô méèmbéèrs õôf thäât grõôûúp. Sééééd Grõôüüps âáréé nõôt âávâáíílâábléé fõôr ÄPÎ câámpâáíígns, âálthõôüügh yõôüü câán íínclüüdéé Sééééd Grõôüüps vííâá âán ÄPÎ-trííggéérééd ééntry íín câámpâáíígn. Thíís fêêäàtüúrêê íís typíícäàlly üúsêêd wííth päàrtnêêrs süúch äàs Rêêtüúrn Päàth óôr 250ÔK tóô mêêäàsüúrêê dêêlíívêêräàbíílííty mêêtríícs. Ït càån bêè ûýsêèd tõõ kêèêèp àå rêècõõrd õõf thêè êèmàåîíl cõõntêènt fõõr hîístõõrîícàål àånd àårchîívàål pûýrpõõsêès. 

Òncêê yöòûù hâãvêê crêêâãtêêd âãn Ìntêêrnâãl Gröòûùp âãnd tâãggêêd íít töò bêê ûùsêêd âãs âã Sêêêêd Gröòûùp, yöòûù câãn sêêlêêct íít fröòm thêê **Täärgéèt Ûséèrs** stéëp ôòf théë cãàmpãàïígn côòmpôòséër, ôòr ôòn théë **Sèénd Sèéttïîngs** stéép ïìn æà Cæànvæàs. Sêèêèd êèmáåïìls wïìll háåvêè thêè ïìdêèntïìfïìêèr `[SEED]`, ãåppêêndêêd tôô thêê stãårt ôôf thêê êêmãåíïl sýýbjêêct líïnêê. Nôôtèé thãàt Sèéèéd èémãàïïls sèént dôôn't ïïncrèémèént sèénds ïïn dãàshbôôãàrd ãànãàlytïïcs, ãànd thèéy dôôn't úùpdãàtèé ãà úùsèér prôôfïïlèé's **Câãmpâãììgn Rëëcëëììvëëd** lîíst.

{% alert tip %}
Îf yõóùür Sèêèêd Grõóùüp mèêmbèêrs rèêpõórt nõót sèêèêìíng thèê mèêssáàgèê ìín thèêìír ìínbõóx, èênsùürèê tháàt thèêy áàrèê lìístèêd ìín thèê Întèêrnáàl Grõóùüp, vèêrìífy tháàt yõóùür sùübjèêct lìínèês áàrèê dìíffèêrèênt áànd tháàt Gmáàìíl háàs nõót bùündlèêd thèê èêmáàìíls tõógèêthèêr, õór háàvèê thèêm chèêck thèêìír SPÅM fõóldèêrs.
{% endalert %}

#### Fóòr cäámpäáïìgns

Séëéëd Grõôüýps câàn béë éëdíítéëd frõôm théë **Tæàrgéêtííng** päãgêè whêèn còömpòösïîng äãn êèmäãïîl cäãmpäãïîgn.

Sééééd Gróõýúps séénd tóõ ééãâch éémãâíîl vãâríîãânt óõncéé ãând ãâréé déélíîvéérééd théé fíîrst tíîméé yóõýúr ýúséér réécééíîvéés thãât pãârtíîcýúlãâr vãâríîãânt. Fõör schéédüýlééd mééssåàgéés thìís typìícåàlly ìís théé fìírst tìíméé théé cåàmpåàìígn låàüýnchéés. Föör áåctíîöön-báåsèëd öör ÆPÌ-tríîggèërèëd cáåmpáåíîgns, thíîs wíîll bèë thèë tíîmèë thèë fíîrst úùsèër íîs sèënt áå mèëssáågèë.

Ìf yõõüür cãåmpãåïïgn ïïs müültïïvãårïïãåtëè ãånd yõõüür vãårïïãånt hãås ãå 0% sëènd pëèrcëèntãågëè, ïït wïïll nõõt bëè sëènt tõõ sëèëèd grõõüüps. Áddìïtìïöönâælly, ìïf thëè vâærìïâænt hâæs âælrëèâædy bëèëèn sëènt âænd hâæs nööt bëèëèn ùýpdâætëèd töö rëèsëènd ìïn **Èdîît Sëèëèd Grööüúps** òõn thêê **Täârgëèt** stèép, îît wîîll nòôt sèénd ãágãáîîn by dèéfãáúült.

{% alert note %}
Íf théëréë îís æã réëcüúrrîíng cæãmpæãîígn æãnd æãn üúpdæãtéë îís cöõndüúctéëd öõn æãny öõnéë öõf théë væãrîíæãnts, yöõüú hæãvéë théë öõptîíöõn öõf réë-séëndîíng töõ öõnly théë üúpdæãtéëd væãrîíæãnts, æãll væãrîíæãnts, öõr töõ tüúrn öõff séëéëd gröõüúp séëndîíng üúpöõn üúpdæãtéë.
{% endalert %}

![Sèêèêd gröóûûps prèêvìïèêw föór ãã cããmpããìïgn][11]

#### Fóôr Cãânvãâs

Sêéêéd grõôùûps îïn Cæànvæàs wõôrk îïn æà sîïmîïlæàr fæàshîïõôn tõô thæàt õôf æàny trîïggêérêéd cæàmpæàîïgn. Brãàzêê ãàûùtóómãàtìïcãàlly dêêtêêcts ãàll stêêps thãàt cóóntãàìïn ãàn êêmãàìïl mêêssãàgêê ãànd wìïll sêênd tóó thêêsêê whêên yóóûùr ûùsêêr fìïrst rêêãàchêês thãàt pãàrtìïcûùlãàr êêmãàìïl stêêp.

Íf äån èèmäåïìl stèèp wäås ùúpdäåtèèd äåftèèr thèè Sèèèèd Grôòùúp wäås mäåïìlèèd, thèè ôòptïìôòn tôò ôònly sèènd tôò ùúpdäåtèèd stèèps, äåll stèèps, ôòr tùúrn ôòff sèèèèds wïìll bèè prèèsèèntèèd.


[7]: {% image_buster /assets/img_archive/internal_group.png %}
[8]: {% image_buster /assets/img_archive/UserLogs1.png %}
[9]: {% image_buster /assets/img_archive/content_test_preview.png %}
[11]: {% image_buster /assets/img_archive/seed_group_campaign.png %}
