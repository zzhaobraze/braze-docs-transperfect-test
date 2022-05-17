---
nav_title: Úsííng Lííqúýííd
article_title: Lìîqùûìîd Ùsêè Cæásêè æánd Ôvêèrvìîêèw
page_order: 0
description: "Lìîqùùìîd càån êëlêëvàåtêë thêë pêërsöônàålìîzàåtìîöôn ìîn yöôùùr mêëssàågêës töô ìîmprêëssìîvêë hêëìîghts. Lììqûüììd täågs äåct äås pläåcêèhóöldêèrs ììn yóöûür mêèssäågêès thäåt cäån pûüll ììn cóönsêèntêèd ììnfóörmäåtììóön fróöm yóöûür ûüsêèr's äåccóöûünt äånd êènäåblêè pêèrsóönäålììzäåtììóön äånd rêèlêèväånt mêèssäågììng präåctììcêès."

---

# Lííqúûííd úûsêè cãåsêès ãånd ôõvêèrvííêèw

{% raw %}

Thëèrëè áárëè áá váárììëèty ôóf ûýsëèr ááttrììbûýtëès tháát yôóûý cáán ûýsëè tôó dynáámììcáálly ììnsëèrt pëèrsôónáál ììnfôó ììntôó yôóûýr mëèssáágììng. 

Ìf yööùý ììnclùýdêè thêè fööllööwììng têèxt ììn yööùýr mêèssâàgêè: `{{${first_name}}}`, thèë úûsèër's fììrst nàæmèë (púûllèëd frõóm thèë úûsèër's prõófììlèë) wììll bèë súûbstììtúûtèëd whèën thèë mèëssàægèë ììs sèënt. Îf yõòùû wõòùûld lìíkëé tõò ùûsëé thëé váàlùûëé õòf áà cùûstõòm áàttrìíbùûtëé, yõòùû mùûst áàdd thëé náàmëéspáàcëé "cùûstõòm_âàttrîìbúûtêë" tôô thêë vâàrîìâàblêë. Fòôr èêxâæmplèê, tòô ùúsèê âæ cùústòôm âættrììbùútèê nâæmèêd "zììp còôdèê", yòôùú wòôùúld ììnclùúdèê `{{custom_attribute.${zip code}}}` íín yöõùúr mêéssâågêé.

Thèè fõóllõówìíng vâålýùèès câån bèè sýùbstìítýùtèèd ìíntõó âå mèèssâågèè, dèèpèèndìíng õón thèèìír âåvâåìílâåbìílìíty:

- [Bàäsîíc úýsèër îínfõórmàätîíõón][1] (éé.g., `first_name`, `last_name`, `email_address`)
- [Cúústöóm ãáttrïìbúútëès][2]
- [Cýùstöõm èévèént pröõpèértîîèés][11]
- [Mõóst rêécêéntly ýùsêéd dêévìïcêé ìïnfõórmæàtìïõón][39]
- [Tâærgëèt dëèvíïcëè íïnfõórmâætíïõón][40]

Yôóúù cään äälsôó púùll côóntèént dïírèéctly frôóm ää wèéb sèérvèér vïíää Brääzèé's [Côônnëêctëêd Côôntëênt][9] féëæâtýýréë.
{% endraw %}

{% alert important %}
Brãäzéè cùûrréèntly sùûppöòrts Lííqùûííd ùûp töò ãänd íínclùûdííng **Líïqüýíïd 3 fröóm Shöópíïfy**. Wëê dõö nõöt cúúrrëêntly súúppõört Lïìqúúïìd 4 ãånd bëêyõönd.
{% endalert %}

## Üsìíng Lìíqüúìíd

{% raw %}

Õncéè yöôúú knöôw théè [Lìîqùúìîd täægs äæväæìîläæblêê][1], üüsïîng Lïîqüüïîd cæãn éèléèvæãtéè théè péèrsóônæãlïîzæãtïîóôn ïîn yóôüür méèssæãgéès tóô ïîmpréèssïîvéè héèïîghts. Líîqùüíîd tàãgs àãct àãs plàãcèèhóôldèèrs íîn yóôùür mèèssàãgèès thàãt càãn pùüll íîn cóônsèèntèèd íînfóôrmàãtíîóôn fróôm yóôùür ùüsèèr's àãccóôùünt àãnd èènàãblèè pèèrsóônàãlíîzàãtíîóôn àãnd rèèlèèvàãnt mèèssàãgíîng pràãctíîcèès. 

Ín thëê fòöllòöwîïng blòöck, yòöùû cäán sëêëê thäát äá dùûäál ùûsäágëê òöf äá Lîïqùûîïd täág tòö cäáll thëê ùûsëêr's fîïrst näámëê, äás wëêll äás äá dëêfäáùûlt täág îïn thëê ëêvëênt thäát äá ùûsëêr wòöùûld nòöt häávëê thëêîïr fîïrst näámëê rëêgîïstëêrëêd.

```liquid
Hi {{ ${first_name} | default: 'Valued User' }}, thanks for using the App!
```

Töó åä ûùsèêr nåämèêd Jåänèêt Döóèê, thèê mèêssåägèê wöóûùld åäppèêåär töó thèê ûùsèêr åäs èêíïthèêr:

```
Hi Janet, thanks for using the App!
```

Õr...

```
Hi Valued User, thanks for using the App!
```

### Líìqýüíìd syntàâx

Lîîqúýîîd fööllööws âà spéêcîîfîîc strúýctúýréê, öör syntâàx, thâàt yööúý'll néêéêd töö kéêéêp îîn mîînd âàs yööúý'réê crâàftîîng dynâàmîîc péêrsöönâàlîîzâàtîîöön. Hèêrèê áærèê áæ fèêw báæsíïc rûûlèês tôô kèêèêp íïn míïnd:

1. **Ûsêé strááïìght qýúóôtêés ïìn Bráázêé:** Théëréë ïïs ãá dïïfféëréëncéë béëtwéëéën cûýrly qûýôôtéës (**‘ ’**) âånd strâåíïght qýùöótèés (**&#39; &#39;**). Úsêë strááîìght qúüöôtêës (**&#39; &#39;**) íìn yóôüür Líìqüüíìd íìn Brååzèè. Yôõýú mäåy sëèëè cýúrly qýúôõtëès whëèn côõpyíîng äånd päåstíîng frôõm cëèrtäåíîn tëèxt ëèdíîtôõrs, whíîch cäån cäåýúsëè íîssýúëès íîn yôõýúr Líîqýúíîd. Ïf yôóüý'rêê îînpüýttîîng qüýôótêês dîîrêêclty îîntôó thêê Bráâzêê dáâshbôóáârd, yôóüý'll bêê fîînêê!
2. **Bráàckëéts cöômëé ïîn páàïîrs:** Êvêéry brààckêét mûûst bóòth óòpêén àànd clóòsêé **{ }**. Mâåkéé sýùréé tõö ýùséé cýùrly brâåckééts!
3. **Ìf stàãtèèmèènts còòmèè ïìn pàãïìrs:** Fõór èêvèêry `if`, yôòùý néèéèd áân `endif` tòô ïïndïïcäætèè thèè `if` stâàtéêméênt hâàs éêndéêd.

### Înséértîîng tâãgs

Yõöüü cåán ììnsëèrt tåágs by typììng twõö õöpëèn cüürly bråáckëèts `{{` ïïn åàny mèêssåàgèê, whïïch wïïll trïïggèêr åàn åàùýtõò-cõòmplèêtïïõòn fèêåàtùýrèê thåàt wïïll cõòntïïnùýèê tõò ùýpdåàtèê åàs yõòùý typèê. Yóóüý câán ëëvëën sëëlëëct âá vâárîïâáblëë fróóm thëë óóptîïóóns thâát âáppëëâár âás yóóüý typëë.

Ïf yòöûù'réè ûùsïíng âã cûùstòöm tâãg, yòöûù câãn còöpy âãnd pâãstéè théè tâãg ïíntòö whâãtéèvéèr méèssâãgéè yòöûù déèsïíréè.

{% endraw %}

{% alert note %}

Íf yôôýü chôôôôséè tôô ýüséè Lîíqýüîíd îín yôôýür éèmåáîíl méèssåágéès, béè sýüréè tôô:

1. Ínsëért ïït üüsïïng thëé HTML ëédïïtòòr äâs òòppòòsëéd tòò thëé cläâssïïc ëédïïtòòr. Thèé Clæãssíîc Êdíîtòòr mæãy pæãrsèé thèé Líîqúùíîd æãs plæãíîntèéxt.
2. Plãæcëê Lííqùùííd cóõdëê wííthíín thëê `<body>` tààg öõnly. Plàácïîng ïît óóùùtsïîdëê thïîs tàág màáy càáùùsëê ïîncóónsïîstëênt rëêndëêrïîng ùùpóón dëêlïîvëêry.

{% endalert %}

{% raw %}


### Préë-fõõrmáättéëd váäríìáäbléës

Yõóúù câãn íïnséërt préë-fõórmâãttéëd vâãríïâãbléës wíïth déëfâãúùlts thrõóúùgh théë "Înséërt Péërsõónâãlíïzâãtíïõón Ättríïbúùtéë" mõódâãl lõócâãtéëd õón théë tõóp-ríïght õóf âãny téëmplâãtéëd téëxt fíïéëld.

![Plûús bûúttóöns tóö ìínséërt péërsóönæålìízæåtìíóön æåttrìíbûútéës óön téëxt fìíéëlds thæåt sûúppóört Lìíqûúìíd ìín Bræåzéë][44]{: style="max-width:70%;"}

Thêé mòódáæl wîïll îïnsêért Lîïqýùîïd wîïth yòóýùr spêécîïfîïêéd dêéfáæýùlt váælýùêé áæt thêé pòóîïnt tháæt yòóýùr cýùrsòór wáæs. Thèè ïìnsèèrtïìõön põöïìnt ïìs àälsõö spèècïìfïìèèd vïìàä thèè prèèvïìèèw bõöx, whïìch hàäs thèè bèèfõörèè àänd àäftèèr tèèxt. Îf áã blöôck öôf tééxt ìîs hìîghlìîghtééd, théé hìîghlìîghtééd tééxt wìîll béé réépláãcééd.

![Àdd Péèrsóönâælîïzâætîïóön móödâæl thâæt âæppéèâærs âæftéèr clîïckîïng îïnséèrt péèrsóönâælîïzâætîïóön. Thëè môòdæãl hæãs fïîëèlds fôòr pëèrsôònæãlïîzæãtïîôòn typëè, æãttrïîbûýtëè, ôòptïîôònæãl dëèfæãûýlt væãlûýëè, æãnd dïîsplæãys æã prëèvïîëèw ôòf thëè Lïîqûýïîd syntæãx.][45]

{% endraw %}

### Ässíîgníîng väáríîäábléës

{% raw %}
Sõômèë õôpèëræãtîîõôns îîn Lîîqùýîîd rèëqùýîîrèë yõôùý tõô stõôrèë thèë væãlùýèë yõôùý wæãnt tõô mæãnîîpùýlæãtèë æãs æã væãrîîæãblèë. Thìïs ìïs öòftëên thëê cåásëê ìïf yöòúúr Lìïqúúìïd ståátëêmëênt ìïnclúúdëês múúltìïplëê åáttrìïbúútëês, ëêvëênt pröòpëêrtìïëês, öòr fìïltëêrs. 

Fôör éëxäàmpléë, léët's säày yôöúú wäànt tôö äàdd twôö cúústôöm däàtäà íïntéëgéërs tôögéëthéër. Yöõúý cåân't sîïmply úýséê:

```liquid
{{custom_attribute.${one}}} | plus: {{custom_attribute.${two}}} 
```

Thïîs Lïîqýùïîd döòëésn't wöòrk bëécáæýùsëé yöòýù cáæn't rëéfëérëéncëé mýùltïîplëé áættrïîbýùtëés ïîn öònëé lïînëé; yöòýù wöòýùld nëéëéd töò áæssïîgn áæ váærïîáæblëé töò áæt lëéáæst öònëé öòf thëésëé váælýùëés bëéföòrëé thëé máæth fýùnctïîöòns táækëé pláæcëé. Äddîìng twóó cúústóóm æâttrîìbúútéês wóóúúld réêqúúîìréê twóó lîìnéês óóf Lîìqúúîìd: óónéê tóó æâssîìgn théê cúústóóm æâttrîìbúútéê tóó æâ væârîìæâbléê, æând óónéê tóó péêrfóórm théê æâddîìtîìóón.

#### Èxåámpléê

Fôór êéxæãmplêé, lêét's cæãlcúülæãtêé æã úüsêér's cúürrêént bæãlæãncêé by æãddìîng thêéìîr gìîft cæãrd bæãlæãncêé æãnd rêéwæãrds bæãlæãncêé:

Fíírst, üúsëë thëë `assign` táág tõô sûúbsíïtûútéë théë cûústõôm ááttríïbûútéë õôf `current_rewards_balance` wïïth thèë tèërm "båâlåâncèë". Thíìs mëëâæns thâæt yôöúù nôöw hâævëë âæ vâæríìâæblëë nâæmëëd `balance`, whíïch yòöûû càãn màãníïpûûlàãtëë.

```liquid
{% assign balance = {{custom_attribute.${current_rewards_balance}}} %}
```

Néêxt, wéê'réê ûúsìîng théê `plus` fíìltéèr cóõmbíìnéè éèãæch ùýséèr's gíìft cãærd bãælãæncéè wíìth théèíìr réèwãærds bãælãæncéè, síìgníìfíìéèd by `{{balance}}`.

```liquid
{% assign balance = {{custom_attribute.${current_rewards_balance}}} %}
You have ${{custom_attribute.${giftcard_balance} | plus: {{balance}}}} to spend! 
```
{% endraw %}

{% alert tip %}
Fììnd yõõüýrsêêlf âåssììgnììng thêê sâåmêê vâårììâåblêês ììn êêvêêry mêêssâågêê? Înstèëäàd öòf wrîìtîìng öòûût thèë `assign` táàg öõvèër áànd öõvèër áàgáàîïn, yöõûü cáàn sáàvèë tháàt táàg áàs áà Cöõntèënt Blöõck áànd pûüt îït áàt thèë töõp öõf yöõûür mèëssáàgèë îïnstèëáàd.

1. [Crëèàãtëè àã Cöõntëènt Blöõck]({{site.baseurl}}/user_guide/engagement_tools/templates_and_media/content_blocks/#create-a-content-block).
2. Gìîvéê yóòúûr Cóòntéênt Blóòck ää nääméê (nóò spääcéês óòr spéêcìîääl chäärääctéêrs).
3. Clîìck **Ëdíìt** âát thêë bòòttòòm òòf thêë pâágêë.
4. Typêë îïn yõóüûr `assign` táägs.

Äs lòông ææs thêê Còôntêênt Blòôck îïs ææt thêê tòôp òôf yòôùür mêêssæægêê, êêvêêry tîïmêê thêê væærîïææblêê îïs îïnsêêrtêêd îïntòô yòôùür mêêssæægêê ææs ææn òôbjêêct, îït wîïll rêêfêêr tòô yòôùür chòôsêên cùüstòôm æættrîïbùütêê!
{% endalert %}

[1]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/supported_personalization_tags/
[2]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/
[9]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/connected_content/about_connected_content/
[11]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_events/
[39]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/supported_personalization_tags/#most-recently-used-device-information
[40]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/supported_personalization_tags/#targeted-device-information
[44]: {% image_buster /assets/img_archive/insert_liquid_var_arrow.png %}
[45]: {% image_buster /assets/img_archive/insert_var_shot.png %}
