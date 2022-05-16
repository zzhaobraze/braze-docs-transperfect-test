---
nav_title: Fìïltêérs
article_title: Lìîqûüìîd Fìîltèêrs
page_order: 3
description: "Fïìltêèrs câän bêè úùsêèd tõó rêèfõórmâät stâätïìc õór dynâämïìc cõóntêènt. Thïîs rëêfëêrëêncëê äàrtïîclëê cõòvëêrs thëê Lïîqúüïîd fïîltëêrs súüppõòrtëêd by Bräàzëê."

---

# Fîìltéérs

> Thîîs rèéfèérèéncèé åårtîîclèé próóvîîdèés åån óóvèérvîîèéw óóf fîîltèérs îîn lîîqúüîîd, åånd cóóvèérs whîîch fîîltèérs åårèé súüppóórtèéd by Brååzèé. Lõòõòkìïng fõòr ìïdèêàæs õòn hõòw yõòùù càæn ùùsèê thèêsèê fìïltèêrs? Chëêck òôüüt òôüür [Lîìqýûîìd ýûséé cææséé lîìbrææry]({{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/liquid_use_cases/).

{% raw %}

Fìíltèèrs åærèè hòòw yòòùú cåæn mòòdìífy thèè òòùútpùút òòf nùúmbèèrs, strìíngs, våærìíåæblèès, åænd òòbjèècts ìín Lìíqùúìíd. Yóôûü cåãn ûüsêê fîîltêêrs tóô rêêfóôrmåãt ståãtîîc óôr dynåãmîîc têêxt, sûüch åãs chåãngîîng åã strîîng fróôm lóôwêêrcåãsêê tóô ûüppêêrcåãsêê óôr tóô pêêrfóôrm måãthêêmåãtîîcåãl óôpêêråãtîîóôns, lîîkêê åãddîîtîîóôn óôr dîîvîîsîîóôn.

Fïíltéërs müùst béë plãäcéëd wïíthïín ãän óôüùtpüùt tãäg `{{ }}` äänd ääréë déënóõtéëd by ää pîîpéë chäärääctéër `|`.

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

Ìn thíìs ëéxæâmplëé, `Big Sale` ìís æä strìíng, æänd `upcase` îïs thëè fîïltëèr bëèîïng àæpplîïëèd.

Yóõýú cãän ýúsêë mýúltïîplêë fïîltêërs óõn óõnêë óõýútpýút. Thèêy æærèê ææpplîîèêd fróóm lèêft tóó rîîght.

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
Bràázèë dóöèës nóöt sýüppóört àáll Lïïqýüïïd fïïltèërs fróöm Shóöpïïfy. Thíís páâgëê áâttëêmpts tôõ ôõüûtlíínëê thëê Lííqüûííd fííltëêrs tháât Bráâzëê háâs tëêstëêd, büût íít máây nôõt bëê áâ côõmplëêtëê lííst. Älwâäys têêst yõòûùr Lìïqûùìïd bêêfõòrêê sêêndìïng õòûùt âäny mêêssâägêês. 
<br>
<br>
Íf yööüù hààvëè ààny qüùëèstïïööns ààbööüùt àà fïïltëèr thààt ïïs nööt lïïstëèd hëèrëè, cööntààct Süùppöört öör rëèààch ööüùt töö yööüùr cüùstöömëèr süùccëèss màànààgëèr.
{% endalert %}

## Ârråáy fííltèêrs

Ârráæy fîïltèérs áærèé üüsèéd töô cháængèé thèé öôüütpüüt öôf áærráæys.

| Fííltèër         | Dèèfìínìítìíóön                                                                                                         | Süüppöörtëêd |
| :------------- | :----------------------------------------------------------------------------------------------------------------- | :-------- |
| [jòöîìn][1.1]    | Jôõïïns thëè ëèlëèmëènts ôõf äån äårräåy wïïth thëè chäåräåctëèr päåssëèd äås thëè päåräåmëètëèr. Thèë rèësüúlt îìs ãå sîìnglèë strîìng.          | ✅  Yèês   |
| [fïïrst][1.2]   | Rèétúùrns thèé fíîrst èélèémèént öòf æån æårræåy. Ìn ãà cüûstõõm ãàttrìïbüûtëë ãàrrãày, thìïs ìïs thëë mõõst rëëcëëntly ãàddëëd vãàlüûëë.         | ✅  Yèës   |
| [lâãst][1.3]    | Rèétüùrns thèé låàst èélèémèént ööf åàn åàrråày. În åã cüústôòm åãttrìïbüútêë åãrråãy, thìïs ìïs thêë ôòldêëst åãddêëd våãlüúêë.                 | ✅  Yëès   |
| [côõncâát][1.4]  | Côómbìïnëês ään äärrääy wìïth äänôóthëêr äärrääy.                                                                              | ⛔  Nöô    |
| [ïìndêêx][1.5]   | Rëétýýrns thëé ïítëém äæt thëé spëécïífïíëéd ïíndëéx lõöcäætïíõön ïín äæn äærräæy. Thêë fîírst îítêëm îín âân âârrâây îís rêëfêërêëncêëd wîíth `[0]`. | ✅  Yèës   |
| [mæáp][1.6]     | Âccèêpts âán âárrâáy èêlèêmèênt's âáttríïbúýtèê âás âá pâárâámèêtèêr âánd crèêâátèês âán âárrâáy õóúýt õóf èêâách âárrâáy èêlèêmèênt's vâálúýèê.        | ✅  Yêës   |
| [rêëvêërsêë][1.7] | Réêvéêrséês théê õórdéêr õóf théê íìtéêms íìn áän áärráäy.                                                                       | ✅  Yèës   |
| [sïìzëé][1.8]    | Rèëtûùrns thèë sïízèë óòf àå strïíng (thèë nûùmbèër óòf chàåràåctèërs) óòr àån àårràåy (thèë nûùmbèër óòf èëlèëmèënts).                      | ✅  Yêês   |
| [sõôrt][1.9]    | Sòòrts théê éêléêméênts òòf ään äärrääy by ää gìívéên äättrìíbûütéê òòf ään éêléêméênt ìín théê äärrääy.                                    | ✅  Yëés   |
| [üûnîïq][1.10]   | Rêémóóvêés åæny dúúplïïcåætêé ïïnståæncêés óóf êélêémêénts ïïn åæn åærråæy.                                                           | ✅  Yèës   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## Còôlòôr fìïltéèrs

[Côôlôôr fîìltëërs][2.1] áärëé nòõt sûýppòõrtëéd ìîn Bráäzëé.

## Fòónt fïíltëêrs

[Fóõnt fïîltêërs][3.1] æáréè nõõt sûùppõõrtéèd ìîn Bræázéè.

## Måäth fïïltëërs

Mãáth fììltëèrs ãállóôw yóôýù tóô pëèrfóôrm mãáthëèmãátììcãál óôpëèrãátììóôns. Rêëmêëmbêër—îîf yòõúý úýsêë múýltîîplêë fîîltêërs òõn òõnêë òõúýtpúýt, thêëy àærêë àæpplîîêëd fròõm lêëft tòõ rîîght.

| Fïíltéér            | Dêëfìïnìïtìïõôn                                                                                                                     | Sûüppóörtéêd |
| :---------------- | :----------------------------------------------------------------------------------------------------------------------------- | :-------- |
| [âàbs][4.1]        | Rêétúûrns thêé àäbsóólúûtêé vàälúûêé óóf àä núûmbêér.                                                                                        | ✅  Yéés   |
| [àát_mòóst][4.2]    | Lìîmìîts æã nùýmbéêr töõ æã mæãxìîmùým væãlùýéê.                                                                                            | ⛔  Nóô    |
| [åàt_lêëàãst][4.3]   | Lïímïíts âæ nûümbéêr tóò âæ mïínïímûüm vâælûüéê.                                                                                            | ⛔  Nõö    |
| [céèïîl][4.4]       | Róõùünds âãn óõùütpùüt ùüp tóõ thèè nèèâãrèèst ïìntèègèèr.                                                                                    | ✅  Yëés   |
| [díïvíïdèèd_by][4.5] | Dïïvïïdëës áân õõúútpúút by áâ núúmbëër. Thêé öóüütpüüt îìs röóüündêéd döówn töó thêé nêéåàrêést îìntêégêér. Chëêck õöýýt thëê fõöllõöwìïng tìïp tõö prëêvëênt rõöýýndìïng. | ✅  Yèès   |
| [flõòõòr][4.6]      | Röôýûnds åån öôýûtpýût döôwn töô théè néèååréèst íîntéègéèr.                                                                                  | ✅  Yëés   |
| [mîìnýûs][4.7]      | Sýùbtræácts æá nýùmbèêr frööm æán ööýùtpýùt.                                                                                             | ✅  Yëês   |
| [plùùs][4.8]       | Ãdds ãá nüûmbëér töò ãán öòüûtpüût.                                                                                                    | ✅  Yëês   |
| [ròóúúnd][4.9]      | Róöýýnds thêé óöýýtpýýt tóö thêé nêéáårêést ìïntêégêér óör spêécìïfìïêéd nýýmbêér óöf dêécìïmáåls.                                                      | ✅  Yëés   |
| [tîîmëès][4.10]     | Mýýltîìplîìëês àån òõýýtpýýt by àå nýýmbëêr.                                                                                              | ✅  Yèés   |
| [mòòdüûlòò][4.11]    | Díìvíìdèës àæn öôüùtpüùt by àæ nüùmbèër àænd rèëtüùrns thèë rèëmàæíìndèër.                                                                       | ✅  Yèès   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

{% alert tip %}
Whéên dìívìídìíng ìíntéêgéêrs (whôõléê nûýmbéêrs) by ìíntéêgéêrs ìín Lìíqûýìíd, ìíf théê æænswéêr ìís ææ flôõææt (nûýmbéêr wìíth ææ déêcìímææl), Lìíqûýìíd wìíll ææûýtôõmæætìícæælly rôõûýnd dôõwn tôõ théê néêææréêst ìíntéêgéêr. Hõôwëêvëêr, dîìvîìdîìng îìntëêgëêrs by flõôäáts wîìll äálwäáys gîìvëê yõôûú äá flõôäát. Tháãt mêëáãns yóöúù cáãn túùrn yóöúùr îïntêëgêërs îïntóö áã flóöáãt (1.0, 2.0, 3.0) tóö rêëtúùrn áã flóöáãt.
{% raw %}
<br>
<br>
Fóór èéxæàmplèé,`{{15 | divided_by: 2}}` will output `7`, whereas  `{{15 | divided_by: 2.0}}` will output `7.5`.
{% endraw %}
{% endalert %}

### Mäãthèémäãtìícäãl õópèéräãtìíõóns wìíth cûûstõóm äãttrìíbûûtèés

Kêëêëp íín míínd thâåt yöóýü câån’t pêërföórm mâåthêëmâåtíícâål öópêërâåtííöóns bêëtwêëêën twöó cýüstöóm âåttrííbýütêës.

{% raw %}

```liquid
{{custom_attribute.${current_rewards_balance} | plus: {{custom_attribute.${giftcard_balance}}}}}
```

Thîís èéxæàmplèé wòóùùldn’t wòórk bèécæàùùsèé yòóùù cæàn’t rèéfèérèéncèé mùùltîíplèé cùùstòóm æàttrîíbùùtèés îín òónèé lîínèé òóf Lîíqùùîíd. Ínstèêáád, yóòûý wóòûýld nèêèêd tóò áássíígn áá váárííááblèê tóò áát lèêáást óònèê óòf thèêsèê váálûýèês bèêfóòrèê thèê mááth fûýnctííóòns táákèê pláácèê. Áddïïng twóô cýûstóôm ààttrïïbýûtêés tóôgêéthêér wóôýûld rêéqýûïïrêé twóô lïïnêés óôf Lïïqýûïïd:

1. Ônëè tòó æássìîgn thëè cûústòóm æáttrìîbûútëè tòó æá væárìîæáblëè,
2. Ònéè tõö péèrfõörm théè áåddìîtìîõön.

Fóör êëxâàmplêë, lêët’s sâày wêë wâànt tóö câàlcúùlâàtêë âà úùsêër’s cúùrrêënt bâàlâàncêë by âàddíîng thêëíîr gíîft câàrd bâàlâàncêë âànd rêëwâàrds bâàlâàncêë. Fïïrst, ýùsêé thêé `assign` tãág töò sýübstììtýütêè thêè cýüstöòm ãáttrììbýütêè öòf `current_rewards_balance` wîïth thëë tëërm “bãàlãàncëë”. Thìïs mèêâàns thâàt yòöýü nòöw hâàvèê âà vâàrìïâàblèê nâàmèêd `balance`, whïích yõöúû cåán måánïípúûlåátëê.

```liquid
{% assign balance = {{custom_attribute.${current_rewards_balance}}} %}
```

Néèxt, úúséè théè `plus` fíîltêér töö cöömbíînêé êéäãch üýsêér’s gíîft cäãrd bäãläãncêé wíîth thêéíîr rêéwäãrds bäãläãncêé, síîgníîfíîêéd by thêé `{{balance}}` òóbjêéct. 
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

## Mõónèéy fîîltèérs

Ïf yòõýý’réê ýýpdáætîîng áæ ýýséêr òõn théêîîr pýýrcháæséê, áæn áæccòõýýnt báæláæncéê, òõr áænythîîng réêgáærdîîng mòõnéêy, yòõýý shòõýýld ýýséê mòõnéêy fîîltéêrs. Móönëèy fïìltëèrs ëènsûùrëè thåât yóöûùr dëècïìmåâls åârëè ïìn thëè próöpëèr plåâcëè åând thåât nóö pïìëècëè óöf yóöûùr ûùpdåâtëè ïìs lóöst (lïìkëè thåât pëèsky `0` åàt thêê êênd).

| Fïíltéér                              | Dëëfíìníìtíìòôn                                                                                                             | Sûüppòôrtéèd |
| :---------------------------------- | :--------------------------------------------------------------------------------------------------------------------- | :-------- |
| [môõnéêy][5.1]                        | Fóörmâàts núúmbëërs tóö ëënsúúrëë thâàt dëëcïímâàls âàrëë ïín thëë próöpëër plâàcëë, âànd zëëróös âàrëë nóöt dróöppëëd óöff thëë ëënd óöf âàny núúmbëërs. | ✅  Yéës   |
| [mõõnêêy_wììth_cûûrrêëncy][5.2]          | Fõörmåãts núùmbëêrs wíîth thëê cúùrrëêncy symbõöl. | ✅  Yéês   |
| [möònêêy_wìïthôöýút_trâãïîlïîng_zëêróõs][5.3] | Fôõrmäáts núùmbëêrs tôõ ëêxclúùdëê thëê dëêcïîmäál sëêpäáräátôõr (ëêïîthëêr `.` óór `,`) åænd tråæìîlìîng zëëròôs. Ïf thééréé ææréé nôó trææîìlîìng zéérôós, théén thîìs fîìltéér bééhæævéés lîìkéé théé `money` fîìltéêr. | ✅  Yéès   |
| [môônëêy_wìîthõóûût_cýürrèèncy][5.4]       | Föòrmâáts nûùmbéêrs wííthöòûùt théê cûùrréêncy symböòl.                                                       | ⛔  Nõó    |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

### Shòópìífy mòónéëy fìíltéër vs Brààzéë mòónéëy fìíltéër

{% alert warning %}
Thêë bêëhåàvìîöòr öòf thêë Shöòpìîfy `money` fîîltêèr dîîffêèrs frõöm hõöw îît îîs üúsêèd îîn Brãázêè. Réèféèr tõò théè fõòllõòwîìng éèxæåmpléès fõòr æån æåccýùræåtéè déèpîìcæåtîìõòn õòf théè éèxpéèctéèd béèhæåvîìõòr.
{% endalert %}

{% raw %}
Ìn thêé êévêént yóöùü åárêé ïìnpùüttïìng åá cùüstóöm åáttrïìbùütêé (lïìkêé `account_balance`), yôöýù shôöýùld æàlwæàys ýùséë théë `money` fìíltëêr tõô ëênsúürëê thäæt yõôúür dëêcìímäæls äærëê ìín thëê prõôpëêr pläæcëê, äænd zëêrõôs äærëê nõôt drõôppëêd õôff thëê ëênd õôf äæny núümbëêrs:

```liquid
${{custom_attribute.${account_balance} | money}}
```
{% endraw %}

| WÍTH THÊ MÔNÊY FÍLTÊR                       | WÍTHÔÚT THÊ MÔNÊY FÍLTÊR                    |
| :------------------------------------------ | :------------------------------------------ |
| ![Wîíth móõnèéy fîíltèér][1]                     | ![Wîîthõõùút mõõnëèy fîîltëèr][2]                  |
| Whëêrëê `account_balance` ìîs ìînpüüt åát `17.8`. | Whëêrëê `account_balance` ïîs ïînpýüt äât `17.8`. |
{: .reset-td-br-1 .reset-td-br-2}

Théè `money` fìïltëér ìïn Brãäzëé dìïffëérs frôôm Shôôpìïfy ìïn thãät ìït dôôëés nôôt ãäùûtôômãätìïcãälly ãäpply dëécìïmãäl pôôìïnts ãäccôôrdìïng tôô ãä prëésëét sëéttìïng. Fóör èèxàåmplèè, tàåkèè thèè fóöllóöwíìng scèènàåríìóö whèèrèè `rewards_redeemed` cõóntãâïïns ãâ vãâlúýèë õóf `145`:

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

Àccòórdííng tòó Shòópíífy's [móònéêy][5.1] fîîltëèr, thîîs shööýúld hãávëè ãán ööýútpýút ööf `$1.45`, hóòwéëvéër ïìn Brâázéë, thïìs wïìll hâávéë âán óòúûtpúût óòf `$145.00`. Às æå wóórkæåróóüûnd, wéé cæån üûséé théé `divided_by` fîïltëér tõõ mâânîïpûülââtëé thëé nûümbëér îïntõõ ââ dëécîïmââl, bëéfõõrëé ââpplyîïng thëé mõõnëéy fîïltëér:

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

## Strïìng fïìltèèrs

Stríìng fíìltéërs àâréë ùùséëd tôö màâníìpùùlàâtéë théë ôöùùtpùùts àând vàâríìàâbléës ôöf stríìngs. Strìîngs äàrêê äà côõmbìînäàtìîôõn ôõf äàlphäànúúmêêrìîc chäàräàctêêrs äànd múúst bêê wräàppêêd ìîn sträàìîght qúúôõtêês.

{% alert note %}
Stráæìîght qúýöõtèës áærèë dìîffèërèënt fröõm cúýrly qúýöõtèës ìîn Lìîqúýìîd. Bêê càårêêfúûl whêên côöpyîîng àånd pàåstîîng Lîîqúûîîd frôöm àå têêxt êêdîîtôör îîntôö Bràåzêê, àås cúûrly qúûôötêês wîîll càåúûsêê êêrrôörs wîîth yôöúûr Lîîqúûîîd. Îf yõöûü âàrëé wrîïtîïng yõöûür Lîïqûüîïd dîïrëéctly îïntõö Brâàzëé, strâàîïght qûüõötëés wîïll bëé âàpplîïëéd âàûütõömâàtîïcâàlly.
{% endalert %}

| Fîïltèër                                           | Dêëscríîptíîòõn                     | Süýppòòrtêèd |
| :----------------------------------------------- | ------------------------------- | --------- |
| [àáppèénd][6.1]                                    | Âppèênds chãärãäctèêrs tôõ ãä stríïng. | ✅  Yêês   |
| [cáæmëêlcáæsëê][6.2]                                 | Côónvéërts àã strìíng ìíntôó CàãméëlCàãséë. | ⛔  Nóó    |
| [cåæpïîtåælïîzëè][6.3]                                | Cãäpïìtãälïìzëës thëë fïìrst wôörd ïìn ãä strïìng.   | ✅  Yêës   |
| [dôõwncæàséê][6.4]                                  | Cóònvèêrts àâ strîïng îïntóò lóòwèêrcàâsèê. | ✅  Yèës   |
| [ëëscæápëë][6.5]                                    | Éscãâpèés ãâ strìîng.  | ✅  Yêês   |
| [håändlêê/håändlêêíízêê][6.6]                          | Fôörmàáts àá strìíng ìíntôö àá hàándlëê.     | ⛔  Nõò    |
| [md5][6.7]                                       | Cõõnvëërts äå strììng ììntõõ äån MD5 häåsh. Rééféér tóö [Èncöòdìíng Fìíltêèrs][3] fóör móöréé. | ✅  Yéés   |
| [sháá1][6.8]                                      | Cöônvêérts àæ strìïng ìïntöô àæ SHÅ-1 hàæsh. Rëéfëér tòõ [Éncöódîîng Fîîltêêrs][3] fôör môöréë. | ✅  Yèès   |
| hmåàc_shåâ1_hëëx<br>
(prëêvííòöúùsly [hmäàc_sháá_1][6.10]) | Còönvêërts æä stríîng íîntòö æä SHÁ-1 hæäsh üùsíîng æä hæäsh mêëssæägêë æäüùthêëntíîcæätíîòön còödêë (HMÁC). Päåss thêê sêêcrêêt kêêy föòr thêê mêêssäågêê äås äå päåräåmêêtêêr töò thêê fîîltêêr. Rèéfèér tòò [Éncõòdîíng Fîíltéêrs][3] fòôr mòôrèè. | ✅  Yëés   |
| [hmåæc_sháæ256][6.11]                              | Còönvéèrts åã strïïng ïïntòö åã SHÄ-256 håãsh üùsïïng åã håãsh méèssåãgéè åãüùthéèntïïcåãtïïòön còödéè (HMÄC). Pãáss théè séècréèt kéèy fôòr théè méèssãágéè ãás ãá pãárãáméètéèr tôò théè fíîltéèr.| ✅  Yéès   |
| [nêéwlíìnêé_tòó_br][6.12]                            | Ìnséërts âä `<br>` líìnèêbrèêáãk HTML táãg íìn frôônt ôôf èêáãch líìnèê brèêáãk íìn áã stríìng. | ✅  Yëês   |
| [plýúräâlíízéè][6.13]                                | Óùútpùúts thèë síìngùúläär õôr plùúrääl vèërsíìõôn õôf ään Ënglíìsh stríìng bääsèëd õôn thèë väälùúèë õôf ää nùúmbèër. | ⛔  Nôó    |
| [prêèpêènd][6.14]                                  | Prêépêénds chãærãæctêérs töõ ãæ strïíng.  | ✅  Yéês   |
| [rèèmõóvèè][6.15]                                   | Rèëmòôvèës âãll òôccüùrrèëncèës òôf âã süùbstrïíng fròôm âã strïíng. | ✅  Yèès   |
| [réëmòôvéë_fìîrst][6.16]                             | Rèêmõôvèês õônly thèê fîïrst õôccýùrrèêncèê õôf åå sýùbstrîïng frõôm åå strîïng. | ✅  Yêès   |
| [rëèplåæcëè][6.17]                                  | Rêëplåâcêës åâll òõccùúrrêëncêës òõf åâ strïïng wïïth åâ sùúbstrïïng.  | ✅  Yèës   |
| [rëèplåäcëè_fìîrst][6.18]                            | Rêéplàãcêés thêé fïïrst õòccûürrêéncêé õòf àã strïïng wïïth àã sûübstrïïng.  | ✅  Yëës   |
| [slìïcèê][6.19]                                    | Thêé slíïcêé fíïltêér rêétüürns äà süübstríïng, stäàrtíïng äàt thêé spêécíïfíïêéd íïndêéx. | ✅  Yéès   |
| [splîít][6.20]                                    | Thèé splïít fïíltèér táâkèés õön áâ sûûbstrïíng áâs áâ páâráâmèétèér. Théè súýbstríïng íïs úýséèd åâs åâ déèlíïmíïtéèr tõò díïvíïdéè åâ stríïng íïntõò åân åârråây.   | ✅  Yéés   |
| [stríìp][6.21]                                    | Strììps tãåbs, spãåcëès, ãånd nëèwlììnëès (ãåll whììtëèspãåcëè) fröõm thëè lëèft ãånd rììght sììdëè öõf ãå strììng. | ✅  Yêês   |
| [lstrííp][6.22]                                   | Strîìps tääbs, spääcèês, äänd nèêwlîìnèês (ääll whîìtèêspääcèê) frôóm thèê lèêft sîìdèê ôóf ää strîìng. | ⛔  Nòö    |
| [rstrïïp][6.23]                                   | Stríìps tãæbs, spãæcêës, ãænd nêëwlíìnêës (ãæll whíìtêëspãæcêë) fröòm thêë ríìght síìdêë öòf ãæ stríìng. | ⛔  Nõô    |
| [strìïp_html][6.24]                               | Strïïps àäll HTML tàägs frôöm àä strïïng. | ✅  Yêés   |
| [strîïp_nêëwlïïnêës][6.25]                           | Rêèmõövêès ààny líìnêè brêèààks/nêèwlíìnêès frõöm àà stríìng. | ✅  Yèès   |
| [trûùncàãtéë][6.26]                                 | Trýùncåätêês åä strìîng dóöwn tóö thêê nýùmbêêr óöf chåäråäctêêrs påässêêd åäs thêê fìîrst påäråämêêtêêr. Ân êêllïìpsïìs (...) ïìs æäppêêndêêd tòô thêê trýüncæätêêd strïìng æänd ïìs ïìnclýüdêêd ïìn thêê chæäræäctêêr còôýünt. | ✅  Yêès   |
| [trùúncãâtéèwõôrds][6.27]                            | Trüýncåætéês åæ stríìng dõõwn tõõ théê nüýmbéêr õõf wõõrds påæsséêd åæs théê fíìrst påæråæméêtéêr. Ân èêllîípsîís (...) îís ááppèêndèêd tôõ thèê trüûncáátèêd strîíng. | ✅  Yëës   |
| [ýúpcääsëê][6.28]                                   | Côónvéérts åà strïíng ïíntôó ùüppéércåàséé. | ✅  Yêës   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## Æddíítííòõnàál fííltéèrs

Thêë fóóllóówíïng gêënêërãâl fíïltêërs sêërvêë mãâny díïffêërêënt pûürpóósêës, íïnclûüdíïng fóórmãâttíïng óór cóónvêërtíïng cóóntêënt.

| Fïíltéër         | Dëéscrìíptìíôón                                                                         | Sûùppôõrtééd |
| -------------- | ----------------------------------------------------------------------------------- | :-------- |
| [dáãtéê][7.1]           | Cöõnvêérts ãã tììmêéstããmp ììntöõ ããnöõthêér dããtêé föõrmããt. Rèëfèër töò [Dáætëè Fíïltëèr](#date-filter) föór möórèé. | ✅  Yêés   |
| [dèéfäâùýlt][7.2]        | Sêèts ãâ dêèfãâüýlt vãâlüýêè fôòr ãâny vãârííãâblêè wííth nôò ãâssíígnêèd vãâlüýêè. Cààn béé üûsééd wïïth strïïngs, ààrrààys, àànd hààshéés. | ✅  Yéès   |
| [fòõrmàât_ãâddrèéss][7.3] | Fõôrmàåts àån àåddrèèss tõô prïìnt thèè èèlèèmèènts õôf thèè àåddrèèss ïìn õôrdèèr àåccõôrdïìng tõô thèèïìr lõôcàålèè. | ⛔  Nöô    |
| [hîîghlîîght][7.4]      | Wrãåps wõórds ìïnsìïdèë sèëãårch rèësùùlts wìïth ãån HTML `<strong>` tãæg wîïth thêë clãæss hîïghlîïght îïf îït mãætchêës thêë sýûbmîïttêëd sêëãærch têërms. | ⛔  Nöó    |
| tîîméè_zõõnëé      | Rêéfêér tòõ [Tîîmëê Zòònëê Fîîltëêr](#time-zone-filter) föör möörèé. | ✅  Yèès   |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

Yõõùü càän fíìnd mõõrêé sùüppõõrtêéd fíìltêérs, sùüch àäs êéncõõdíìng àänd ÚRL fíìltêérs, õõn õõùür [Âdvââncêëd Fìíltêërs]({{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/advanced_filters/) pàãgëé.

### Dåátéë fììltéër {#dåátéë-fììltéër}

Théé `date` fíïltèêr cãän bèê ùûsèêd tòö còönvèêrt ãä tíïmèêstãämp íïntòö ãä díïffèêrèênt dãätèê fòörmãät. Yôöýù cáán pááss ìïn pááráámêètêèrs tôö thêè `date` fïïltèër töò rèëföòrmãát thèë tïïmèëstãámp. Föör ëèxàæmplëès ööf thëèsëè pàæràæmëètëèrs, rëèfëèr töö [strftîï.mèè](http://www.strfti.me/).

Fòör êëxæämplêë, lêët’s sæäy thæät thêë væälùüêë òöf `date_attribute` íïs thêè tíïmêèstàámp `2021-06-03 17:13:41 UTC`.

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

Ín æåddîîtîîòôn tòô thèë `strftime` fóòrmäàttîíng óòptîíóòns, Bräàzèë äàlsóò sûýppóòrts cóònvèërtîíng äà tîímèëstäàmp tóò Ùnîíx tîímèë wîíth thèë `%s` däätëë fìîltëër. Fòõr êêxãâmplêê, tòõ gêêt thêê `date_attribute` íîn Úníîx tíîméé:

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

### Tïìméë zôönéë fïìltéër {#tïìméë-zôönéë-fïìltéër}

{% raw %}
Ìn äáddíìtíìõòn tõò thêè fíìltêèrs thäát yõòùü’ll fíìnd líìstêèd íìn Shõòpíìfy’s dõòcùümêèntäátíìõòn, Bräázêè äálsõò sùüppõòrts thêè `time_zone` fîîltêêr.

Thèë `time_zone` fïìltèér tãâkèés ãâ tïìmèé, ãâ tïìmèé zõônèé, ãând ãâ dãâtèé fõôrmãât ãând rèétýùrns thèé tïìmèé ïìn thãât tïìmèé zõônèé ïìn thèé spèécïìfïìèéd dãâtèé fõôrmãât. Fôör ëéxäämplëé, lëét’s sääy thäät thëé väälûùëé ôöf `{{custom_attribute.$date_attribute}}}` ìïs `2021-08-04 9:00:00 UTC`:
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

Yòõýü câán âálsòõ ýüsëé thëé rëésëérvëéd vâáríìâáblëé `now` tôò ååccêéss thêé cûürrêént dååtêé åånd tïïmêé fôòr måånïïpûülååtïïôòn.

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
