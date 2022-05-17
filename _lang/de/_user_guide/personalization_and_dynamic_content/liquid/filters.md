---
nav_title: Fîîltéêrs
article_title: Líîqûûíîd Fíîltèérs
page_order: 3
description: "Fììltèêrs câän bèê üùsèêd tõó rèêfõórmâät stâätììc õór dynâämììc cõóntèênt. Thíîs rêéfêérêéncêé âàrtíîclêé cóövêérs thêé Líîqýüíîd fíîltêérs sýüppóörtêéd by Brâàzêé."

---

# Fìîltêêrs

> Thíïs rêëfêërêëncêë äãrtíïclêë pröôvíïdêës äãn öôvêërvíïêëw öôf fíïltêërs íïn líïqýýíïd, äãnd cöôvêërs whíïch fíïltêërs äãrêë sýýppöôrtêëd by Bräãzêë. Lòöòökïìng fòör ïìdééäás òön hòöw yòöýú cäán ýúséé thééséé fïìltéérs? Chêëck öòûýt öòûýr [Lïìqýûïìd ýûsëé cæàsëé lïìbræàry]({{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/liquid_use_cases/).

{% raw %}

Fííltéérs âàréé hòôw yòôüú câàn mòôdíífy théé òôüútpüút òôf nüúmbéérs, strííngs, vâàrííâàbléés, âànd òôbjéécts íín Lííqüúííd. Yôôüû càän üûsëê fîïltëêrs tôô rëêfôôrmàät stàätîïc ôôr dynàämîïc tëêxt, süûch àäs chàängîïng àä strîïng frôôm lôôwëêrcàäsëê tôô üûppëêrcàäsëê ôôr tôô pëêrfôôrm màäthëêmàätîïcàäl ôôpëêràätîïôôns, lîïkëê àäddîïtîïôôn ôôr dîïvîïsîïôôn.

Fíîltèërs müùst bèë plæåcèëd wíîthíîn æån ôóüùtpüùt tæåg `{{ }}` æând æârèè dèènõôtèèd by æâ pïípèè chæâræâctèèr `|`.

{% endraw %}

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
{{"Big Sale" | upcase}}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
BIG SALE
```
{% endraw %}
{% endtab %}
{% endtabs %}

Ìn thìîs ëèxâæmplëè, `Big Sale` îîs àæ strîîng, àænd `upcase` îís thèè fîíltèèr bèèîíng æãpplîíèèd.

Yòôùý cáån ùýsèé mùýltìïplèé fìïltèérs òôn òônèé òôùýtpùýt. Thëéy àärëé àäpplìïëéd frôóm lëéft tôó rìïght.

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
 {{ "Big Sale" | upcase | remove: “BIG” }}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
SALE
```
{% endraw %}
{% endtab %}
{% endtabs %}

{% alert important %}
Bråàzèê dôöèês nôöt súûppôört åàll Lììqúûììd fììltèêrs frôöm Shôöpììfy. Thìïs pæágëê æáttëêmpts tõò õòýútlìïnëê thëê Lìïqýúìïd fìïltëêrs thæát Bræázëê hæás tëêstëêd, býút ìït mæáy nõòt bëê æá cõòmplëêtëê lìïst. Ãlwããys têèst yòóùýr Lííqùýííd bêèfòórêè sêèndííng òóùýt ããny mêèssããgêès. 
<br>
<br>
Ïf yôõùù hàãvèé àãny qùùèéstíîôõns àãbôõùùt àã fíîltèér thàãt íîs nôõt líîstèéd hèérèé, côõntàãct Sùùppôõrt ôõr rèéàãch ôõùùt tôõ yôõùùr cùùstôõmèér sùùccèéss màãnàãgèér.
{% endalert %}

## Àrræáy fïíltéêrs

Årræày fïîltèërs æàrèë ýýsèëd tòõ chæàngèë thèë òõýýtpýýt òõf æàrræàys.

| Fíïltêèr         | Dèêfìïnìïtìïóôn                                                                                                         | Süûppõòrtêéd |
| :------------- | :----------------------------------------------------------------------------------------------------------------- | :-------- |
| [jôöíìn][1.1]    | Jóöìîns thêë êëlêëmêënts óöf äán äárräáy wìîth thêë chäáräáctêër päássêëd äás thêë päáräámêëtêër. Thèë rèësúült ïïs ãä sïïnglèë strïïng.          | ✅  Yëés   |
| [fíírst][1.2]   | Réêtüûrns théê fîírst éêléêméênt õóf äán äárräáy. Ín ââ cüústôöm ââttrííbüútêè âârrâây, thíís íís thêè môöst rêècêèntly ââddêèd vââlüúêè.         | ✅  Yêês   |
| [läást][1.3]    | Rèêtûýrns thèê láæst èêlèêmèênt öóf áæn áærráæy. Ín áæ cüýstööm áættrïìbüýtëè áærráæy, thïìs ïìs thëè ööldëèst áæddëèd váælüýëè.                 | ✅  Yéès   |
| [cõôncæät][1.4]  | Còömbïïnèês ààn ààrràày wïïth àànòöthèêr ààrràày.                                                                              | ⛔  Nòô    |
| [ííndééx][1.5]   | Réêtùûrns théê ììtéêm àãt théê spéêcììfììéêd ììndéêx lôöcàãtììôön ììn àãn àãrràãy. Théê fîírst îítéêm îín âân âârrâây îís réêféêréêncéêd wîíth `[0]`. | ✅  Yëés   |
| [màåp][1.6]     | Æccèèpts áán áárrááy èèlèèmèènt's ááttríîbûûtèè áás áá pááráámèètèèr áánd crèèáátèès áán áárrááy öòûût öòf èèáách áárrááy èèlèèmèènt's váálûûèè.        | ✅  Yêès   |
| [rëévëérsëé][1.7] | Rèêvèêrsèês thèê ôôrdèêr ôôf thèê îìtèêms îìn àän àärràäy.                                                                       | ✅  Yêës   |
| [sïízéë][1.8]    | Rèétûýrns thèé sìîzèé ööf æà strìîng (thèé nûýmbèér ööf chæàræàctèérs) öör æàn æàrræày (thèé nûýmbèér ööf èélèémèénts).                      | ✅  Yëès   |
| [sóórt][1.9]    | Sõõrts thêé êélêémêénts õõf ããn ããrrããy by ãã gììvêén ããttrììbûútêé õõf ããn êélêémêént ììn thêé ããrrããy.                                    | ✅  Yéés   |
| [üýnîíq][1.10]   | Rëèmòòvëès åàny dùýplîîcåàtëè îînståàncëès òòf ëèlëèmëènts îîn åàn åàrråày.                                                           | ✅  Yêès   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## Còölòör fíïltéérs

[Còòlòòr fíïltëërs][2.1] ãærèé nóót súýppóórtèéd ìïn Brãæzèé.

## Fóônt fîîltéèrs

[Fóönt fîìltèêrs][3.1] ääréê nöòt sûúppöòrtéêd ïîn Brääzéê.

## Mãâth fìîltêérs

Mæäth fííltêërs æällööw yööùû töö pêërföörm mæäthêëmæätíícæäl ööpêëræätííööns. Rêèmêèmbêèr—îìf yöóùù ùùsêè mùùltîìplêè fîìltêèrs öón öónêè öóùùtpùùt, thêèy æârêè æâpplîìêèd fröóm lêèft töó rîìght.

| Fîîltêèr            | Dééfìínìítìíòön                                                                                                                     | Sýýppòòrtëëd |
| :---------------- | :----------------------------------------------------------------------------------------------------------------------------- | :-------- |
| [áåbs][4.1]        | Rèètûürns thèè ââbsõölûütèè vââlûüèè õöf ââ nûümbèèr.                                                                                        | ✅  Yêès   |
| [æåt_móôst][4.2]    | Lîímîíts áå núümbèèr tóò áå máåxîímúüm váålúüèè.                                                                                            | ⛔  Nóò    |
| [æàt_lèëâåst][4.3]   | Líïmíïts ãã nýûmbéêr tòó ãã míïníïmýûm vããlýûéê.                                                                                            | ⛔  Nóõ    |
| [cééííl][4.4]       | Ròòûünds àãn òòûütpûüt ûüp tòò théë néëàãréëst ííntéëgéër.                                                                                    | ✅  Yëès   |
| [dïívïídèèd_by][4.5] | Dïîvïîdéës ãån õòýýtpýýt by ãå nýýmbéër. Thèê öõûútpûút ïìs röõûúndèêd döõwn töõ thèê nèêäàrèêst ïìntèêgèêr. Chëëck óõúýt thëë fóõllóõwìíng tìíp tóõ prëëvëënt róõúýndìíng. | ✅  Yêês   |
| [flõòõòr][4.6]      | Rõöúünds ãân õöúütpúüt dõöwn tõö théê néêãâréêst îíntéêgéêr.                                                                                  | ✅  Yéès   |
| [mïînûüs][4.7]      | Sùùbtrãäcts ãä nùùmbëër fröóm ãän öóùùtpùùt.                                                                                             | ✅  Yëès   |
| [plýús][4.8]       | Ädds æã núúmbëér tõö æãn õöúútpúút.                                                                                                    | ✅  Yêès   |
| [röòùûnd][4.9]      | Róöüýnds thêè óöüýtpüýt tóö thêè nêèàãrêèst îíntêègêèr óör spêècîífîíêèd nüýmbêèr óöf dêècîímàãls.                                                      | ✅  Yéés   |
| [tìïmëés][4.10]     | Mýúltîîplîîêês àán òóýútpýút by àá nýúmbêêr.                                                                                              | ✅  Yèës   |
| [môôdûûlôô][4.11]    | Dîîvîîdëés ãæn òôûýtpûýt by ãæ nûýmbëér ãænd rëétûýrns thëé rëémãæîîndëér.                                                                       | ✅  Yèês   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

{% alert tip %}
Whèên dìívìídìíng ìíntèêgèêrs (whòòlèê nûýmbèêrs) by ìíntèêgèêrs ìín Lìíqûýìíd, ìíf thèê äänswèêr ìís ää flòòäät (nûýmbèêr wìíth ää dèêcìímääl), Lìíqûýìíd wìíll ääûýtòòmäätìícäälly ròòûýnd dòòwn tòò thèê nèêäärèêst ìíntèêgèêr. Hõôwëèvëèr, dììvììdììng ììntëègëèrs by flõôàæts wììll àælwàæys gììvëè yõôùü àæ flõôàæt. Thàát mëèàáns yöóûü càán tûürn yöóûür ïíntëègëèrs ïíntöó àá flöóàát (1.0, 2.0, 3.0) töó rëètûürn àá flöóàát.
{% raw %}
<br>
<br>
Föór éêxããmpléê,`{{15 | divided_by: 2}}` will output `7`, whereas  `{{15 | divided_by: 2.0}}` will output `7.5`.
{% endraw %}
{% endalert %}

### Màåthéêmàåtïìcàål òôpéêràåtïìòôns wïìth cüüstòôm àåttrïìbüütéês

Këêëêp íìn míìnd thåät yõóûù cåän’t pëêrfõórm måäthëêmåätíìcåäl õópëêråätíìõóns bëêtwëêëên twõó cûùstõóm åättríìbûùtëês.

{% raw %}

```liquid
{{custom_attribute.${current_rewards_balance} | plus: {{custom_attribute.${giftcard_balance}}}}}
```

Thîïs ééxââmpléé wòòúüldn’t wòòrk béécââúüséé yòòúü câân’t rééféérééncéé múültîïpléé cúüstòòm ââttrîïbúütéés îïn òònéé lîïnéé òòf Lîïqúüîïd. Ìnstëéååd, yööýù wööýùld nëéëéd töö ååssïïgn åå våårïïååblëé töö ååt lëéååst öönëé ööf thëésëé våålýùëés bëéföörëé thëé mååth fýùnctïïööns tååkëé plååcëé. Ãddìíng twóõ cúýstóõm áættrìíbúýtèës tóõgèëthèër wóõúýld rèëqúýìírèë twóõ lìínèës óõf Lìíqúýìíd:

1. Õnëé tõò æãssíígn thëé cûýstõòm æãttrííbûýtëé tõò æã væãrííæãblëé,
2. Önèé tóó pèérfóórm thèé ãåddììtììóón.

Fóôr èéxáãmplèé, lèét’s sáãy wèé wáãnt tóô cáãlcüùláãtèé áã üùsèér’s cüùrrèént báãláãncèé by áãddìîng thèéìîr gìîft cáãrd báãláãncèé áãnd rèéwáãrds báãláãncèé. Fììrst, ùùsêê thêê `assign` tââg tôò súùbstíìtúùtêè thêè cúùstôòm ââttríìbúùtêè ôòf `current_rewards_balance` wìîth théê téêrm “bäåläåncéê”. Thïìs mèèääns thäät yõôúû nõôw häävèè ää väärïìääblèè näämèèd `balance`, whìïch yóõüü cáæn máænìïpüüláætêé.

```liquid
{% assign balance = {{custom_attribute.${current_rewards_balance}}} %}
```

Nèëxt, üúsèë thèë `plus` fìîltëèr tóò cóòmbìînëè ëèäách üüsëèr’s gìîft cäárd bäáläáncëè wìîth thëèìîr rëèwäárds bäáläáncëè, sìîgnìîfìîëèd by thëè `{{balance}}` óöbjëêct. 
{% endraw %}
{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
{% assign balance = {{custom_attribute.${current_rewards_balance}}} %}
You have ${{custom_attribute.${giftcard_balance} | plus: {{balance}}}} to spend!
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
You have $35 to spend!
```
{% endraw %}
{% endtab %}
{% endtabs %}

## Môònêêy fìíltêêrs

Ïf yõõüú’rëè üúpdàátíîng àá üúsëèr õõn thëèíîr püúrchàásëè, àán àáccõõüúnt bàálàáncëè, õõr àánythíîng rëègàárdíîng mõõnëèy, yõõüú shõõüúld üúsëè mõõnëèy fíîltëèrs. Möónêéy fïíltêérs êénsüùrêé thàát yöóüùr dêécïímàáls àárêé ïín thêé pröópêér plàácêé àánd thàát nöó pïíêécêé öóf yöóüùr üùpdàátêé ïís löóst (lïíkêé thàát pêésky `0` æãt thèê èênd).

| Fïïltëêr                              | Déèfïïnïïtïïöòn                                                                                                             | Sýýppôõrtêëd |
| :---------------------------------- | :--------------------------------------------------------------------------------------------------------------------- | :-------- |
| [möónéëy][5.1]                        | Fòórmáåts nûümbëêrs tòó ëênsûürëê tháåt dëêcïîmáåls áårëê ïîn thëê pròópëêr pláåcëê, áånd zëêròós áårëê nòót dròóppëêd òóff thëê ëênd òóf áåny nûümbëêrs. | ✅  Yëês   |
| [mòònéèy_wíîth_cüûrrëëncy][5.2]          | Fòórmååts nûýmbèêrs wììth thèê cûýrrèêncy symbòól. | ✅  Yëës   |
| [móônêèy_wïíthõóýýt_trâáìïlìïng_zéêrõõs][5.3] | Fòörmãáts nýümbéërs tòö éëxclýüdéë théë déëcìîmãál séëpãárãátòör (éëìîthéër `.` òór `,`) âànd trâàìîlìîng zëêròõs. Ìf théèréè âåréè nôö trâåììlììng zéèrôös, théèn thììs fììltéèr béèhâåvéès lììkéè théè `money` fïíltéèr. | ✅  Yêès   |
| [mòõnéêy_wíïthõöúút_cýûrrèéncy][5.4]       | Fòórmãæts núúmbêërs wìíthòóúút thêë cúúrrêëncy symbòól.                                                       | ⛔  Nòò    |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

### Shõópíífy mõónêéy fííltêér vs Bràåzêé mõónêéy fííltêér

{% alert warning %}
Thèé bèéhãåvïìóòr óòf thèé Shóòpïìfy `money` fîìltéér dîìfféérs fröòm höòw îìt îìs ýùsééd îìn Bræãzéé. Rêèfêèr töõ thêè föõllöõwîìng êèxæãmplêès föõr æãn æãccûúræãtêè dêèpîìcæãtîìöõn öõf thêè êèxpêèctêèd bêèhæãvîìöõr.
{% endalert %}

{% raw %}
În théë éëvéënt yòôýû âåréë ìînpýûttìîng âå cýûstòôm âåttrìîbýûtéë (lìîkéë `account_balance`), yôöúù shôöúùld äàlwäàys úùsêê thêê `money` fîîltèér tòô èénsúýrèé thæàt yòôúýr dèécîîmæàls æàrèé îîn thèé pròôpèér plæàcèé, æànd zèéròôs æàrèé nòôt dròôppèéd òôff thèé èénd òôf æàny núýmbèérs:

```liquid
${{custom_attribute.${account_balance} | money}}
```
{% endraw %}

| WÍTH THË MÔNËY FÍLTËR                       | WÎTHÓÜT THÈ MÓNÈY FÎLTÈR                    |
| :------------------------------------------ | :------------------------------------------ |
| ![Wîîth môónéèy fîîltéèr][1]                     | ![Wïíthòöýýt mòönëéy fïíltëér][2]                  |
| Whéèréè `account_balance` ïïs ïïnpûýt âát `17.8`. | Whèërèë `account_balance` ìîs ìînpûýt áåt `17.8`. |
{: .reset-td-br-1 .reset-td-br-2}

Thêë `money` fîíltëêr îín Bráázëê dîíffëêrs fróóm Shóópîífy îín tháát îít dóóëês nóót ááúútóómáátîícáálly áápply dëêcîímáál póóîínts ááccóórdîíng tóó áá prëêsëêt sëêttîíng. Föõr ééxäämpléé, tääkéé théé föõllöõwîîng scéénäärîîöõ whééréé `rewards_redeemed` côöntàäîìns àä vàälùùéê ôöf `145`:

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
${{event_properties.${rewards_redeemed} | money }}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
$145.00
```
{% endraw %}
{% endtab %}
{% endtabs %}

Âccõòrdîïng tõò Shõòpîïfy's [môõnëêy][5.1] fíìltêêr, thíìs shôõýüld håævêê åæn ôõýütpýüt ôõf `$1.45`, hõôwêévêér îîn Bräåzêé, thîîs wîîll häåvêé äån õôùýtpùýt õôf `$145.00`. Ás ãá wöòrkãáröòûünd, wéè cãán ûüséè théè `divided_by` fïíltéër tõò måänïípùülåätéë théë nùümbéër ïíntõò åä déëcïímåäl, béëfõòréë åäpplyïíng théë mõònéëy fïíltéër:

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
${{event_properties.${rewards_redeemed} | divided_by: 100.00 | money }}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
$1.45
```
{% endraw %}
{% endtab %}
{% endtabs %}

## Strîîng fîîltéérs

Strîîng fîîltèêrs äãrèê ýüsèêd tóó mäãnîîpýüläãtèê thèê óóýütpýüts äãnd väãrîîäãblèês óóf strîîngs. Strìïngs äàrëé äà côõmbìïnäàtìïôõn ôõf äàlphäànûúmëérìïc chäàräàctëérs äànd mûúst bëé wräàppëéd ìïn sträàìïght qûúôõtëés.

{% alert note %}
Strãâíîght qúýôótëés ãârëé díîffëérëént frôóm cúýrly qúýôótëés íîn Líîqúýíîd. Bëê cåàrëêfüül whëên còòpyìíng åànd påàstìíng Lìíqüüìíd fròòm åà tëêxt ëêdìítòòr ìíntòò Bråàzëê, åàs cüürly qüüòòtëês wìíll cåàüüsëê ëêrròòrs wìíth yòòüür Lìíqüüìíd. Ìf yõöüü æàréê wrïïtïïng yõöüür Lïïqüüïïd dïïréêctly ïïntõö Bræàzéê, stræàïïght qüüõötéês wïïll béê æàpplïïéêd æàüütõömæàtïïcæàlly.
{% endalert %}

| Fíïltëèr                                           | Dèéscrïîptïîõón                     | Sùýppöôrtèéd |
| :----------------------------------------------- | ------------------------------- | --------- |
| [äâppèénd][6.1]                                    | Áppéênds chãärãäctéêrs töô ãä strììng. | ✅  Yêês   |
| [cäàmêêlcäàsêê][6.2]                                 | Cöönvêèrts àä strìíng ìíntöö CàämêèlCàäsêè. | ⛔  Nöò    |
| [cæãpîîtæãlîîzéè][6.3]                                | Càæpìítàælìízëês thëê fìírst wòõrd ìín àæ strìíng.   | ✅  Yêës   |
| [dööwncããsêê][6.4]                                  | Cöònvéérts ãä strîíng îíntöò löòwéércãäséé. | ✅  Yèés   |
| [èèscäàpèè][6.5]                                    | Ëscâåpèès âå stríïng.  | ✅  Yëés   |
| [hàändlèè/hàändlèèîìzèè][6.6]                          | Fòòrmæåts æå strïíng ïíntòò æå hæåndlèë.     | ⛔  Nòö    |
| [md5][6.7]                                       | Cóönvëérts æâ strìîng ìîntóö æân MD5 hæâsh. Rèêfèêr tòò [Ëncöódïíng Fïíltéërs][3] fôör môörêê. | ✅  Yéës   |
| [shåã1][6.8]                                      | Cóònvêèrts äæ strííng ííntóò äæ SHÀ-1 häæsh. Réèféèr tõó [Êncõôdîìng Fîìltèêrs][3] fôôr môôrêè. | ✅  Yéés   |
| hmåæc_sháæ1_héèx<br>
(prèëvîíöôúýsly [hmàåc_shäá_1][6.10]) | Côônvéèrts æä stríïng íïntôô æä SHÄ-1 hæäsh ýùsíïng æä hæäsh méèssæägéè æäýùthéèntíïcæätíïôôn côôdéè (HMÄC). Páàss thêê sêêcrêêt kêêy fõôr thêê mêêssáàgêê áàs áà páàráàmêêtêêr tõô thêê fíïltêêr. Rèèfèèr töó [Èncòödìîng Fìîltêérs][3] fôór môóréé. | ✅  Yêés   |
| [hmæãc_shåã256][6.11]                              | Cöônvèërts áä stríìng íìntöô áä SHÂ-256 háäsh úûsíìng áä háäsh mèëssáägèë áäúûthèëntíìcáätíìöôn cöôdèë (HMÂC). Páæss thêë sêëcrêët kêëy fõór thêë mêëssáægêë áæs áæ páæráæmêëtêër tõó thêë fíìltêër.| ✅  Yëës   |
| [néèwlîínéè_tóó_br][6.12]                            | Ìnsèèrts åå `<br>` lïínéëbréëáãk HTML táãg ïín frõónt õóf éëáãch lïínéë bréëáãk ïín áã strïíng. | ✅  Yëès   |
| [plüýræålììzéé][6.13]                                | Ôýütpýüts thêë sììngýülàár öór plýüràál vêërsììöón öóf àán Ènglììsh strììng bàásêëd öón thêë vàálýüêë öóf àá nýümbêër. | ⛔  Nõò    |
| [préëpéënd][6.14]                                  | Préëpéënds chäåräåctéërs tòõ äå strîïng.  | ✅  Yëès   |
| [rêémòôvêé][6.15]                                   | Rëêmõòvëês ååll õòccüúrrëêncëês õòf åå süúbstríîng frõòm åå stríîng. | ✅  Yéès   |
| [réèmõóvéè_fïïrst][6.16]                             | Rëëmóôvëës óônly thëë fïîrst óôccýürrëëncëë óôf æã sýübstrïîng fróôm æã strïîng. | ✅  Yèès   |
| [rèèplãäcèè][6.17]                                  | Rèéplààcèés ààll òõccüùrrèéncèés òõf àà strîìng wîìth àà süùbstrîìng.  | ✅  Yëés   |
| [rêèplæâcêè_fïîrst][6.18]                            | Rèépläåcèés thèé fììrst óôccýùrrèéncèé óôf äå strììng wììth äå sýùbstrììng.  | ✅  Yéés   |
| [slïîcéé][6.19]                                    | Théê slíícéê fííltéêr réêtùûrns âã sùûbstrííng, stâãrtííng âãt théê spéêcíífííéêd ííndéêx. | ✅  Yëés   |
| [splîît][6.20]                                    | Thëê splïìt fïìltëêr tãâkëês öôn ãâ sùûbstrïìng ãâs ãâ pãârãâmëêtëêr. Théè sûýbstrîîng îîs ûýséèd âæs âæ déèlîîmîîtéèr töö dîîvîîdéè âæ strîîng îîntöö âæn âærrâæy.   | ✅  Yêés   |
| [strïíp][6.21]                                    | Strîïps tãábs, spãácèës, ãánd nèëwlîïnèës (ãáll whîïtèëspãácèë) fròòm thèë lèëft ãánd rîïght sîïdèë òòf ãá strîïng. | ✅  Yêès   |
| [lstrîîp][6.22]                                   | Strîïps tãæbs, spãæcêés, ãænd nêéwlîïnêés (ãæll whîïtêéspãæcêé) fróôm thêé lêéft sîïdêé óôf ãæ strîïng. | ⛔  Nöö    |
| [rstrîîp][6.23]                                   | Strïìps tãàbs, spãàcêës, ãànd nêëwlïìnêës (ãàll whïìtêëspãàcêë) fróóm thêë rïìght sïìdêë óóf ãà strïìng. | ⛔  Nöó    |
| [strïìp_html][6.24]                               | Stríïps ãáll HTML tãágs fróòm ãá stríïng. | ✅  Yéès   |
| [strîíp_néêwlíïnéês][6.25]                           | Réêmòôvéês àâny líînéê bréêàâks/néêwlíînéês fròôm àâ stríîng. | ✅  Yëés   |
| [trúùncåætéë][6.26]                                 | Trùûncæàtëès æà strìíng dòówn tòó thëè nùûmbëèr òóf chæàræàctëèrs pæàssëèd æàs thëè fìírst pæàræàmëètëèr. Án èèllîîpsîîs (...) îîs áæppèèndèèd tóó thèè trúüncáætèèd strîîng áænd îîs îînclúüdèèd îîn thèè cháæráæctèèr cóóúünt. | ✅  Yêés   |
| [trûýncæåtèèwóôrds][6.27]                            | Trùüncáätéês áä strììng dõòwn tõò théê nùümbéêr õòf wõòrds páässéêd áäs théê fììrst páäráäméêtéêr. Ân èëllììpsììs (...) ììs áâppèëndèëd töõ thèë trüùncáâtèëd strììng. | ✅  Yêès   |
| [üúpcæåséè][6.28]                                   | Côönvëërts âä strîìng îìntôö úùppëërcâäsëë. | ✅  Yèês   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## Àddîîtîîöónâæl fîîltêërs

Thêé fòöllòöwîíng gêénêérääl fîíltêérs sêérvêé määny dîíffêérêént püùrpòösêés, îínclüùdîíng fòörmäättîíng òör còönvêértîíng còöntêént.

| Fïìltèër         | Déëscrîîptîîöön                                                                         | Süýppóòrtéêd |
| -------------- | ----------------------------------------------------------------------------------- | :-------- |
| [dàãtêé][7.1]           | Côònvéêrts æä tììméêstæämp ììntôò æänôòthéêr dæätéê fôòrmæät. Rêèfêèr tòò [Dâætèé Fïïltèér](#date-filter) fôór môórëë. | ✅  Yèês   |
| [dêëfãâùûlt][7.2]        | Sêêts ææ dêêfææýúlt væælýúêê fóór ææny væærìîææblêê wìîth nóó ææssìîgnêêd væælýúêê. Cããn bëè ùýsëèd wìîth strìîngs, ããrrããys, ããnd hããshëès. | ✅  Yêés   |
| [fóórmâàt_áäddrêëss][7.3] | Fòòrmäãts äãn äãddrêéss tòò prìïnt thêé êélêémêénts òòf thêé äãddrêéss ìïn òòrdêér äãccòòrdìïng tòò thêéìïr lòòcäãlêé. | ⛔  Nòõ    |
| [híïghlíïght][7.4]      | Wrâáps wóòrds íînsíîdëë sëëâárch rëësúýlts wíîth âán HTML `<strong>` täãg wìïth théè cläãss hìïghlìïght ìïf ìït mäãtchéès théè sýùbmìïttéèd séèäãrch téèrms. | ⛔  Nóò    |
| tïîmèé_zóônëè      | Rêëfêër tôò [Tîîmëè Zõõnëè Fîîltëèr](#time-zone-filter) fòõr mòõrèè. | ✅  Yèés   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

Yòöýý cäán fïínd mòöréé sýýppòörtééd fïíltéérs, sýých äás ééncòödïíng äánd ÜRL fïíltéérs, òön òöýýr [Àdvååncèêd Fîîltèêrs]({{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/advanced_filters/) påãgéè.

### Dàætèê fíìltèêr {#dàætèê-fíìltèêr}

Thêè `date` fîïltéèr cáán béè ùüséèd tôó côónvéèrt áá tîïméèstáámp îïntôó áá dîïfféèréènt dáátéè fôórmáát. Yòõûü càán pàáss ìïn pàáràáméètéèrs tòõ théè `date` fìíltëér tòô rëéfòôrmæãt thëé tìímëéstæãmp. Fóör èëxåâmplèës óöf thèësèë påâråâmèëtèërs, rèëfèër tóö [strftîí.mêë](http://www.strfti.me/).

Fòõr ééxæámpléé, léét’s sæáy thæát théé væálúýéé òõf `date_attribute` íìs thêè tíìmêèstàämp `2021-06-03 17:13:41 UTC`.

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
{{custom_attribute.${date_attribute} | date: '%b %d'}}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
03 June
```
{% endraw %}
{% endtab %}
{% endtabs %}

Ín åæddììtììôôn tôô thêé `strftime` fôórmâåttíïng ôóptíïôóns, Brâåzèê âålsôó sûýppôórts côónvèêrtíïng âå tíïmèêstâåmp tôó Üníïx tíïmèê wíïth thèê `%s` dæãtèè fíìltèèr. Fôôr èéxåämplèé, tôô gèét thèé `date_attribute` îín Ùnîíx tîíméë:

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
{{custom_attribute.${date_attribute} | date: '%s' }}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
1433351621
```
{% endraw %}
{% endtab %}
{% endtabs %}

### Tïîméê zôõnéê fïîltéêr {#tïîméê-zôõnéê-fïîltéêr}

{% raw %}
În àæddîîtîîòón tòó thêè fîîltêèrs thàæt yòóùý’ll fîînd lîîstêèd îîn Shòópîîfy’s dòócùýmêèntàætîîòón, Bràæzêè àælsòó sùýppòórts thêè `time_zone` fïìltëér.

Thèè `time_zone` fìïltëèr täákëès äá tìïmëè, äá tìïmëè zóônëè, äánd äá däátëè fóôrmäát äánd rëètùúrns thëè tìïmëè ìïn thäát tìïmëè zóônëè ìïn thëè spëècìïfìïëèd däátëè fóôrmäát. Fóõr ëèxàãmplëè, lëèt’s sàãy thàãt thëè vàãlùýëè óõf `{{custom_attribute.$date_attribute}}}` îís `2021-08-04 9:00:00 UTC`:
{% endraw %}

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
{{custom_attribute.${date_attribute} | time_zone: 'America/Los_Angeles' | date: '%a %b %e %T' }}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
Wed August 4 2:00:00
```
{% endraw %}
{% endtab %}
{% endtabs %}

Yôòüù câàn âàlsôò üùsëé thëé rëésëérvëéd vâàríìâàblëé `now` tõõ ââccëëss thëë cûúrrëënt dââtëë âând tìïmëë fõõr mâânìïpûúlââtìïõõn.

{% tabs local %}
{% tab Input %}
{% raw %}
```liquid
{{ 'now' | date: '%Y-%m-%d %H:%M:%S' }}
```
{% endraw %}
{% endtab %}
{% tab Output %}
{% raw %}
```liquid
2021-08-04 18:13:13
```
{% endraw %}
{% endtab %}
{% endtabs %}


[1.1]: https://shopify.dev/api/liquid/filters/array-filters#join
[1.2]: https://shopify.dev/api/liquid/filters/array-filters#first
[1.3]: https://shopify.dev/api/liquid/filters/array-filters#last
[1.4]: https://shopify.dev/api/liquid/filters/array-filters#concat
[1.5]: https://shopify.dev/api/liquid/filters/array-filters#index
[1.6]: https://shopify.dev/api/liquid/filters/array-filters#map
[1.7]: https://shopify.dev/api/liquid/filters/array-filters#reverse
[1.8]: https://shopify.dev/api/liquid/filters/array-filters#size
[1.9]: https://shopify.dev/api/liquid/filters/array-filters#sort
[1.10]: https://shopify.dev/api/liquid/filters/array-filters#uniq

[2.1]: https://shopify.dev/api/liquid/filters/color-filters
[3.1]: https://shopify.dev/api/liquid/filters/font-filters

[4.1]: https://shopify.dev/api/liquid/filters/math-filters#abs
[4.2]: https://shopify.dev/api/liquid/filters/math-filters#at_most
[4.3]: https://shopify.dev/api/liquid/filters/math-filters#at_least
[4.4]: https://shopify.dev/api/liquid/filters/math-filters#ceil
[4.5]: https://shopify.dev/api/liquid/filters/math-filters#divided_by
[4.6]: https://shopify.dev/api/liquid/filters/math-filters#floor
[4.7]: https://shopify.dev/api/liquid/filters/math-filters#minus
[4.8]: https://shopify.dev/api/liquid/filters/math-filters#plus
[4.9]: https://shopify.dev/api/liquid/filters/math-filters#round
[4.10]: https://shopify.dev/api/liquid/filters/math-filters#times
[4.11]: https://shopify.dev/api/liquid/filters/math-filters#modulo

[5.1]: https://shopify.dev/api/liquid/filters/money-filters#money
[5.2]: https://shopify.dev/api/liquid/filters/money-filters#money_with_currency
[5.3]: https://shopify.dev/api/liquid/filters/money-filters#money_without_trailing_zeros
[5.4]: https://shopify.dev/api/liquid/filters/money-filters#money_without_currency

[6.1]: https://shopify.dev/api/liquid/filters/string-filters#append
[6.2]: https://shopify.dev/api/liquid/filters/string-filters#camelcase
[6.3]: https://shopify.dev/api/liquid/filters/string-filters#capitalize
[6.4]: https://shopify.dev/api/liquid/filters/string-filters#downcase
[6.5]: https://shopify.dev/api/liquid/filters/string-filters#escape
[6.6]: https://shopify.dev/api/liquid/filters/string-filters#handle-handleize
[6.7]: https://shopify.dev/api/liquid/filters/string-filters#md5
[6.8]: https://shopify.dev/api/liquid/filters/string-filters#sha1
[6.10]: https://shopify.dev/api/liquid/filters/string-filters#hmac_sha1
[6.11]: https://shopify.dev/api/liquid/filters/string-filters#hmac_sha256
[6.12]: https://shopify.dev/api/liquid/filters/string-filters#newline_to_br
[6.13]: https://shopify.dev/api/liquid/filters/string-filters#pluralize
[6.14]: https://shopify.dev/api/liquid/filters/string-filters#prepend
[6.15]: https://shopify.dev/api/liquid/filters/string-filters#remove
[6.16]: https://shopify.dev/api/liquid/filters/string-filters#remove_first
[6.17]: https://shopify.dev/api/liquid/filters/string-filters#replace
[6.18]: https://shopify.dev/api/liquid/filters/string-filters#replace_first
[6.19]: https://shopify.dev/api/liquid/filters/string-filters#slice
[6.20]: https://shopify.dev/api/liquid/filters/string-filters#split
[6.21]: https://shopify.dev/api/liquid/filters/string-filters#strip
[6.22]: https://shopify.dev/api/liquid/filters/string-filters#lstrip
[6.23]: https://shopify.dev/api/liquid/filters/string-filters#rstrip
[6.24]: https://shopify.dev/api/liquid/filters/string-filters#strip_html
[6.25]: https://shopify.dev/api/liquid/filters/string-filters#strip_newlines
[6.26]: https://shopify.dev/api/liquid/filters/string-filters#truncate
[6.27]: https://shopify.dev/api/liquid/filters/string-filters#truncatewords
[6.28]: https://shopify.dev/api/liquid/filters/string-filters#upcase

[7.1]: https://shopify.dev/api/liquid/filters/additional-filters#date
[7.2]: https://shopify.dev/api/liquid/filters/additional-filters#default
[7.3]: https://shopify.dev/api/liquid/filters/additional-filters#format_address
[7.4]: https://shopify.dev/api/liquid/filters/additional-filters#highlight


[1]: {% image_buster /assets/img/with_money_filter.png %}
[2]: {% image_buster /assets/img/without_money_filter.png %}
[3]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/advanced_filters/#encoding-filters
