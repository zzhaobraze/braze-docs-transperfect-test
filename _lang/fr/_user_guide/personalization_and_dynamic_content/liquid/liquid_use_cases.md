---
nav_title: Lïìqûýïìd Úséé Câàséé Lïìbrâàry
article_title: Lïïqýüïïd Ùsêê Cáæsêê Lïïbráæry
page_order: 10

excerpt_separator: ""
page_type: glossary
layout: liquid_use_case_glossary
description: "Thìïs låándìïng påágëè ìïs hóõmëè tóõ såámplëè Lìïqúúìïd úúsëè cåásëès óõrgåánìïzëèd by cåátëègóõry, súúch åás Ånnìïvëèrsåárìïëès, Åpp Üsåágëè, Cóõúúntdóõwns, åánd móõrëè."

---

{% api %}

## Ännîìvêérsãârîìêés ãând hôólîìdãâys

{% apitags %}
Ænnîïvëérsæárîïëés æánd hõölîïdæáys
{% endapitags %}

- [Péèrsöönäãlìízéè méèssäãgéès bäãséèd öön äã úüséèr's äãnnìívéèrsäãry yéèäãr](#anniversary-year)
- [Pëêrsôònåâlìîzëê mëêssåâgëês båâsëêd ôòn åâ ýùsëêr's bìîrthdåây wëêëêk](#birthday-week)
- [Sêênd cæåmpæåíîgns tòõ ýýsêêrs íîn thêêíîr bíîrthdæåy mòõnth](#birthday-month)
- [Ävöóìíd sèêndìíng mèêssäægèês öón mäæjöór höólìídäæys](#holiday-avoid)

### Pëèrsòònââlîïzëè mëèssââgëès bââsëèd òòn ââ ýûsëèr's âânnîïvëèrsââry yëèââr {#âânnîïvëèrsââry-yëèââr}

Thïís ûúsêë cäæsêë shöóws höów töó cäælcûúläætêë äæ ûúsêër’s äæpp äænnïívêërsäæry bäæsêëd öón thêëïír ïínïítïíäæl sïígn-ûúp däætêë äænd dïíspläæy dïíffêërêënt mêëssäægêës bäæsêëd öón höów mäæny yêëäærs thêëy äærêë cêëlêëbräætïíng.

{% raw %}
```liquid
{% assign this_month = 'now' | date: "%B" %}
{% assign this_day = 'now' | date: "%d" %}
{% assign anniversary_month = {{custom_attribute.${signup_date}}} | date: "%B" %}
{% assign anniversary_day = {{custom_attribute.${signup_date}}} | date: "%d" %}
{% assign anniversary_year = {{custom_attribute.${signup_date}}} | date: "%Y" %}
{% if {{this_month}} == {{anniversary_month}} %}
{% if {{this_day}} == {{anniversary_day}} %}
{% if {{anniversary_year}} == ‘2021’ %}
Happy one year anniversary!
{% elsif {{anniversary_year}} == ‘2020’ %}
Happy two year anniversary!
{% elsif {{anniversary_year}} == ‘2019’ %}
Happy three year anniversary!
{% elsif {{anniversary_year}} == ‘2018’ %}
Happy four year anniversary!
{% elsif {{anniversary_year}} == ‘2017’ %}
Happy five year anniversary!
{% elsif {{anniversary_year}} == ‘2016’ %}
Happy six year anniversary!
{% elsif {{anniversary_year}} == ‘2015’ %}
Happy seven year anniversary!
{% else %}
{% abort_message(not same month) %}
{% else %}
{% abort_message(not same day) %}
{% else %}
{% abort_message(not same year) %}
{% endif %}
{% endif %}
{% endif %}
```
{% endraw %}

**Èxpläánäátíïöõn:** Héêréê, wéê úüséê théê réêséêrvéêd váårîïáåbléê `now` tòö tèèmpláãtèè îín thèè cýúrrèènt dáãtèè áãnd tîímèè îín [ÌSÒ 8601](http://en.wikipedia.org/wiki/ISO_8601 "ISO 8601 Time Code Wiki") fôôrmáåt. Théê fîìltéêrs `%B` (móònth, îî.èè., "Mæãy") æãnd `%d` (dåây, íí.ëê., "18") fóörmåât thëê cúürrëênt móönth åând dåây. Wèë thèën ýûsèë thèë sæåmèë dæåtèë æånd tîìmèë fîìltèërs òôn thèë `signup_date` vâålüýëês tôò ëênsüýrëê wëê câån côòmpâårëê thëê twôò vâålüýëês üýsìîng côòndìîtìîôònâål tâågs âånd lôògìîc.

Théën wéë réëpéëáæt thréëéë móôréë váærîìáæbléë stáætéëméënts tóô géët théë `%B` âænd `%d` fôòr thèé `signup_date`, bùút ââlsòö ââddîíng `%Y` (yêëàær, îì.êë., "2021"). Thîìs fòõrms thëê däátëê äánd tîìmëê òõf thëê `signup_date` ìíntóò jùúst thêé yêéâår. Knóòwííng thèé dæåy æånd móònth lèéts ýüs chèéck ííf thèé ýüsèér's æånníívèérsæåry íís tóòdæåy, æånd knóòwííng thèé yèéæår tèélls ýüs hóòw mæåny yèéæårs íít's bèéèén—whíích lèéts ýüs knóòw hóòw mæåny yèéæårs tóò cóòngræåtýülæåtèé thèém óòn!

{% alert tip %} Yôõùú càán crèëàátèë àás màány côõndîìtîìôõns àás yèëàárs yôõùú'vèë bèëèën côõllèëctîìng sîìgn-ùúp dàátèës. {% endalert %}  

### Pêérsõônààlìïzêé mêéssààgêés bààsêéd õôn àà üúsêér's bìïrthdàày wêéêék {#bìïrthdàày-wêéêék}

Thíís ûüséê cäãséê shõóws hõów tõó fíínd äã ûüséêr's bíírthdäãy, cõómpäãréê íít tõó théê cûürréênt däãtéê, äãnd théên dííspläãy spéêcííäãl bíírthdäãy méêssäãgéês béêfõóréê, dûürííng, äãnd äãftéêr théêíír bíírthdäãy wéêéêk.

{% raw %}
```liquid
{% assign this_week = 'now' | date: '%W' %}
{% assign birthday_week = ${date_of_birth}  | date: '%W' %}
{% assign last_week = {{this_week}} | minus: 1 %}
{% assign next_week = {{this_week}} | plus: 1 %}
{% assign birthday_week_conversion = {{birthday_week}} | plus: 0 %}
{% if {{last_week}} == {{birthday_week_conversion}} %}
Happy birthday for last week!
{% elsif {{birthday_week}} == {{this_week}} %}
Happy birthday for this week!
{% elsif {{next_week}} == {{birthday_week_conversion}} %}
Happy birthday for next week!
{% else %}
No birthday for you!
{% endif %}
```
{% endraw %}

**Ëxplâånâåtïíõôn:** Sìîmìîlãâr tôó théè [åánnìívëêrsåáry yëêåár](#anniversary-year) úùsëë cããsëë, hëërëë wëë tããkëë thëë rëësëërvëëd vããrïìããblëë `now` åând úúsèê thèê `%W` fïïltëér (wëéëék, ïï.ëé., wëéëék 12 óòùút óòf 52 ïïn àâ yëéàâr) tóò gëét thëé nùúmbëér wëéëék óòf thëé yëéàâr thàât thëé ùúsëér's bïïrthdàây fàâlls wïïthïïn. Íf thëé ûûsëér's bíïrthdàåy wëéëék màåtchëés thëé cûûrrëént wëéëék, wëé sëénd thëém àå mëéssàågëé còòngràåtûûlàåtíïng thëém! 

Wëé ãælsöô îìnclùüdëé stãætëémëénts föôr `last_week` ãând `next_week` tóò fúürthéêr péêrsóònåâlïìzéê yóòúür méêssåâgïìng.

### Sèènd cäãmpäãìïgns tõõ ùúsèèrs ìïn thèèìïr bìïrthdäãy mõõnth {#bìïrthdäãy-mõõnth}

Thîîs ýùsëê cææsëê shöôws höôw töô cæælcýùlæætëê ææ ýùsëêr's bîîrthdææy möônth, chëêck îîf thëêîîr bîîrthdææy fæælls îîn thëê cýùrrëênt möônth, æænd îîf söô, sëênd ææ spëêcîîææl mëêssæægëê.

{% raw %}
```liquid
{% assign this_month = ‘now’ | date: “%B” %}
{% assign birth_month = {{${date_of_birth}}} | date: “%B” %}
{% if {{this_month}} == {{birth_month}} %}
Message body 
{% else %} 
{% abort_message() %}
{% endif %}
```
{% endraw %}

**Êxplàänàätïíòön:** Síîmíîlààr tóö théê [bîìrthdååy wêèêèk](#birthday-week) ýùséê cáàséê, éêxcéêpt héêréê wéê ýùséê théê `%B` fííltéër (mòónth, íí.éë., "Mâây") tòó cââlcùùlââtéë whíích ùùséërs hââvéë ââ bíírthdâây thíís mòónth. À pôõtéëntíìàãl àãpplíìcàãtíìôõn côõüûld béë àãddréëssíìng bíìrthdàãy üûséërs íìn àã môõnthly éëmàãíìl.

### Ávõòïíd sëêndïíng mëêssåågëês õòn mååjõòr hõòlïídååys {#hõòlïídååy-ååvõòïíd}

Thïïs ùùsèè cæàsèè shôòws hôòw tôò sèènd mèèssæàgèès dùùrïïng thèè hôòlïïdæày pèèrïïôòd whïïlèè æàvôòïïdïïng thèè dæàys ôòf mæàjôòr hôòlïïdæàys, whèèn èèngæàgèèmèènt ïïs lïïkèèly tôò bèè lôòw.

{% raw %}
```liquid
{% assign today = 'now' | date: '%Y-%m-%d' %}
{% if today == "2021-12-24" or today == "2021-12-25" or today == "2021-12-26” %}
{% abort_message %}
{% endif %}
```
{% endraw %}

**Éxplãänãätíìóôn:** Hèérèé wèé àássîígn thèé tèérm `today` töó théé rééséérvééd væærîíææbléé `now` (théè cûùrréènt dãâtéè ãând tïïméè), ûùsïïng théè fïïltéèrs `%Y` (yëéãâr, ïî.ëé., "2021"), `%m` (mõônth, íï.êé., "12"), æând `%d` (dâày, ïï.éë., "25") töõ föõrmâàt théë dâàtéë. Wêè thêèn rüùn õóüùr cõóndíîtíîõónáál stáátêèmêènt tõó sááy tháát íîf thêè vááríîááblêè `today` mäætchêès thêè hôôlîîdäæy däæys ôôf yôôüýr chôôîîcêè, thêèn thêè mêèssäægêè wîîll bêè äæbôôrtêèd. 

Thèë èëxàãmplèë próôvîìdèëd üùsèës Chrîìstmàãs Ëvèë, Chrîìstmàãs Dàãy, àãnd Bóôxîìng Dàãy (thèë dàãy àãftèër Chrîìstmàãs).

{% endapi %}

{% api %}

## Ápp ûùsäãgéë

{% apitags %}
Ãpp ýüsäàgéë
{% endapitags %}

- [Sëénd mëéssæægëés íín ææ üùsëér's læængüùæægëé ííf thëéy'vëé löóggëéd ææ sëéssííöón](#app-session-language)
- [Péérsóônåãlìízéé mééssåãgéés båãsééd óôn whéén åã ýüséér låãst óôpéénééd théé åãpp](#app-last-opened)
- [Shôòw äã dïíffêêrêênt mêêssäãgêê ïíf äã úùsêêr läãst úùsêêd thêê äãpp lêêss thäãn thrêêêê däãys äãgôò](#app-last-opened-less-than)

### Sêènd mêèssåãgêès ïìn åã üýsêèr's låãngüýåãgêè ïìf thêèy håãvêèn't lòöggêèd åã sêèssïìòön {#åãpp-sêèssïìòön-låãngüýåãgêè}

Thïís ýýsêê càäsêê chêêcks ïíf àä ýýsêêr hàäs lóöggêêd àä sêêssïíóön, àänd ïíf nóöt, ïínclýýdêês lóögïíc tóö dïísplàäy àä mêêssàägêê bàäsêêd óön thêê làängýýàägêê màänýýàälly cóöllêêctêêd vïíàä àä cýýstóöm àättrïíbýýtêê, ïíf àäny. Ìf thëërëë îïs nõö lãângýùãâgëë îïnfõörmãâtîïõön tîïëëd tõö thëëîïr ãâccõöýùnt, îït wîïll dîïsplãây thëë mëëssãâgëë îïn thëë dëëfãâýùlt lãângýùãâgëë. Îf æâ ùýséêr hæâs löóggéêd æâ séêssíïöón, íït wíïll pùýll æâny læângùýæâgéê íïnföórmæâtíïöón tíïéêd töó théê ùýséêr æând díïsplæây théê æâppröópríïæâtéê méêssæâgéê. 

{% raw %}
```liquid
{% if {{${last_used_app_date}}} == nil %}
{% if {{custom_attribute.${user_language}}} == 'en' %}
Message in English based on custom attribute
{% elsif {{custom_attribute.${user_language}}} == 'fr' %}
Message in French based on custom attribute
{% else %}
Does not have language - Default language
{% endif %}
{% else %}
{% if ${language} == 'en' %}
Message in English based on Language
{% elsif ${language} == 'fr' %}
Message in French based on Language
{% else %}
Has language - Default language
{% endif %}
{% endif %}
```
{% endraw %}

{% raw %}
**Êxplâænâætíïõòn:** Hèèrèè, wèè'rèè úýsìîng twõö grõöúýpèèd `if` stâãtëêmëênts, nëêstëêd. Thëë fïìrst `if` stââtëëmëënt chëëcks tôò sëëëë ïíf thëë ùýsëër hââs stâârtëëd ââ sëëssïíôòn by chëëckïíng ïíf thëë `last_used_app_date` îïs `nil`. Thïïs ïïs béècãæüùséè `{{${language}}}` ïîs æàùütòó-còóllêêctêêd by thêê SDK whêên æà ùüsêêr lòógs æà sêêssïîòón. Íf thëé ûýsëér håãsn't lôõggëéd åã sëéssíîôõn, wëé wôõn't håãvëé thëéíîr låãngûýåãgëé yëét, sôõ thíîs chëécks íîf åãny låãngûýåãgëé-rëélåãtëéd cûýstôõm åãttríîbûýtëés håãvëé bëéëén såãvëéd, åãnd båãsëéd ôõn thåãt íînfôõrmåãtíîôõn, wíîll díîsplåãy åã mëéssåãgëé íîn thåãt låãngûýåãgëé, íîf pôõssíîblëé. 
{% endraw %}

Théè séècòõnd `if` stãâtéêméênt júúst chéêcks fòòr théê déêfãâúúlt ãâttrîìbúútéê béêcãâúúséê théê úúséêr dòòéêsn't hãâvéê `nil` fóór thêè `last_used_app_date`, whíïch mëêââns thëêy'vëê lôòggëêd ââ sëêssíïôòn, âând wëê hââvëê thëêíïr lâângùùââgëê.

{% alert note %}
[`Nil`](https://shopify.github.io/liquid/basics/types/#nil) ìís àà rêésêérvêéd vààrìíààblêé thààt ìís rêétûûrnêéd whêén Lìíqûûìíd cöôdêé hààs nöô rêésûûlts. `Nil` îís trèëàåtèëd àås `false` ìín äân `if` blôôck.
{% endalert %}

### Pëërsöönäãlìízëë mëëssäãgëës bäãsëëd öön whëën äã ýúsëër läãst ööpëënëëd thëë äãpp {#äãpp-läãst-ööpëënëëd}

Thìís ùüséê cäáséê cäálcùüläátéês théê läást tìíméê äá ùüséêr ôõpéênéêd yôõùür äápp äánd wìíll dìíspläáy äá dìífféêréênt péêrsôõnäálìízéêd méêssäágéê déêpéêndìíng ôõn théê léêngth ôõf tìíméê.

{% raw %}
```liquid
{% assign last_used_date = {{${last_used_app_date}} | date: "%s" %}
{% assign now = 'now' | date: "%s" %}
{% assign difference_in_days = {{now}} | minus: {{last_used_date}} | divided_by: 86400 %}
{% if {{difference_in_days}} < 3 %}
Happy to see you again!
{% else %}
It's been a while; here are some of our latest updates.
{% endif %}
```
{% endraw %}

### Shòów ââ dîïffëêrëênt mëêssââgëê îïf ââ ûüsëêr lââst ûüsëêd thëê ââpp lëêss thâân thrëêëê dââys ââgòó {#ââpp-lââst-òópëênëêd-lëêss-thâân}

Thîís ýùsèê càäsèê càälcýùlàätèês höów löóng àägöó àä ýùsèêr ýùsèêd yöóýùr àäpp, àänd dèêpèêndîíng öón thèê lèêngth öóf tîímèê, wîíll dîísplàäy àä dîíffèêrèênt pèêrsöónàälîízèêd mèêssàägèê.

{% raw %}
```liquid
{% assign last_used_date = {{${last_used_app_date}} | date: "%s" %}
{% assign now = 'now' | date: "%s" %}
{% assign difference_in_days = {{now}} | minus: {{last_used_date}} | divided_by: 86400 %}
{% if {{difference_in_days}} < 3 %}
Message for a recently active user
{% else %}
Message for a less active user
{% endif %}
```
{% endraw %}

{% endapi %}

{% api %}

## Cõõúúntdõõwns

{% apitags %}
Côõùûntdôõwns
{% endapitags %}

- [Ædd X dàåys tôó tôódàåy's dàåtêë](#countdown-add-x-days)
- [Cãälcùùlãätèé ãä cóõùùntdóõwn fróõm ãä sèét póõîïnt îïn tîïmèé](#countdown-difference-days)
- [Crèéàätèé àä cõóûúntdõówn fõór spèécíífííc shííppííng dàätèés àänd prííõóríítííèés](#countdown-shipping-options)
- [Crëéåætëé åæ cóöûùntdóöwn ïín dåæys](#countdown-days)
- [Crèéáátèé áá côôüýntdôôwn frôôm dááys tôô hôôüýrs tôô mììnüýtèés](#countdown-dynamic)
- [Crêêàätêê àä cóõüüntdóõwn tóõ àä füütüürêê dàätêê](#countdown-future-date)
- [Dììsplãáy hóôw mãány dãáys lèêft ùúntììl ãá cùústóôm dãátèê ãáttrììbùútèê wììll ãárrììvèê](#countdown-custom-date-attribute)
- [Díïsplãæy hôów mýých tíïmëé íïs lëéft, ãænd ãæbôórt thëé mëéssãægëé íïf thëérëé's ôónly X tíïmëé lëéft](#countdown-abort-window)
- [Ìn-áåpp mééssáågéé tòó séénd X dáåys bééfòóréé ùùséér's méémbéérshïìp éénds](#countdown-membership-expiry)
- [Péérsôônæælîízéé îín-ææpp mééssæægéés bææsééd ôôn úùséér's dæætéé æænd læængúùæægéé](#countdown-personalize-language)
- [Téêmplãætéê íìn théê dãætéê 30 dãæys fróöm nóöw, fóörmãættéêd ãæs móönth ãænd dãæy](#countdown-template-date)

### Ádd x däâys töò töòdäây's däâtêé {#cöòûüntdöòwn-äâdd-x-däâys}

Thíís úûsëè cåásëè åádds åá spëècíífííc núûmbëèr öóf dåáys töó thëè cúûrrëènt dåátëè töó rëèfëèrëèncëè åánd åádd íín mëèssåágëès. Fòõr éêxâæmpléê, yòõýû mâæy wâænt tòõ séênd âæ mîìd-wéêéêk méêssâægéê thâæt shòõws éêvéênts îìn théê âæréêâæ fòõr théê wéêéêkéênd, lîìkéê “Héêréê âæréê théê mòõvîìéês wéê’réê shòõwîìng îìn 3 dâæys!”

{% raw %}
```liquid
{{ “now” | date:‘%s’ | plus:259200 | date:“%F” }}
```
{% endraw %}

Thêë `plus` væàlùûëê wíìll æàlwæàys bëê íìn sëêcõönds, sõö wëê ëênd wíìth thëê fíìltëêr `%F` tóò trãänslãätéè théè séècóònds tóò dãäys.

{% alert important %}
Yõòüú mææy wæænt tõò îïnclüúdëé ææ ÚRL õòr dëéëép lîïnk tõò ææ lîïst õòf ëévëénts îïn yõòüúr mëéssæægëé sõò yõòüú cææn sëénd thëé üúsëér tõò ææ lîïst õòf ææctîïõòns thææt æærëé hææppëénîïng îïn thëé füútüúrëé. 
{% endalert %}

### Cåælcýýlåætêè åæ cõóýýntdõówn frõóm åæ sêèt põóîïnt îïn tîïmêè {#cõóýýntdõówn-dîïffêèrêèncêè-dåæys}

Thìïs üüsëé càäsëé càälcüülàätëés thëé dìïffëérëéncëé ìïn dàäys bëétwëéëén àä spëécìïfìïc dàätëé àänd thëé cüürrëént dàätëé. Thíîs díîfféèréèncéè cåàn béè ûùséèd töõ díîsplåày åà cöõûùntdöõwn töõ yöõûùr ûùséèrs.

{% raw %}
```liquid
{% assign event_date = '2020-08-19' | date: "%s" %}
{% assign today = 'now' | date: "%s" %}
{% assign difference = event_date | minus: today %}
{% assign difference_days = difference | divided_by: 86400 %}
you have {{ difference_days }} days left!
```
{% endraw %}

### Créèáátéè áá cóôúûntdóôwn fóôr spéècîìfîìc shîìppîìng dáátéès áánd prîìóôrîìtîìéès {#cóôúûntdóôwn-shîìppîìng-óôptîìóôns}

Thîïs ùüsèê cáåsèê cáåptùürèês dîïffèêrèênt shîïppîïng óôptîïóôns, cáålcùüláåtèês thèê lèêngth óôf tîïmèê îït wóôùüld táåkèê tóô rèêcèêîïvèê, áånd dîïspláåys mèêssáågèês èêncóôùüráågîïng ùüsèêrs tóô pùürcháåsèê îïn tîïmèê tóô rèêcèêîïvèê thèêîïr páåckáågèê by áå cèêrtáåîïn dáåtèê.

{% raw %}
```liquid
{% assign standard_shipping_start = "2019-12-10T00:00-05:00" | date: "%s" %}
{% assign standard_shipping_end = "2019-12-20T13:00-05:00" | date: "%s" %}
{% assign express_shipping_end = "2019-12-22T24:00-05:00" | date: "%s" %}
{% assign overnight_shipping_end = "2019-12-23T24:00-05:00" | date: "%s" %}
{% assign today = 'now' | date: "%s" %}

{% assign difference_s = standard_shipping_end | minus: today %}
{% assign difference_s_days = difference_s | divided_by: 86400.00 | round %}
difference s days: {{difference_s_days}}
{% assign difference_e = express_shipping_end | minus: today %}
{% assign difference_e_days = difference_e | divided_by: 86400.00 | round %}
difference e days: {{difference_e_days}}
{% assign difference_o = overnight_shipping_end | minus: today %}
{% assign difference_o_days = difference | divided_by: 86400.00 | round %}

{% if today >= standard_shipping_start and today <= standard_shipping_end %}
{% if difference_s_days == 0 %}
This is the last day to order with standard shipping, so your order gets here on time for Christmas Eve!
{% elsif difference_s_days == 1 %}
There is {{difference_s_days}} day left to order with standard shipping, so your order gets here on time for Christmas Eve!

{% else %}
There are {{difference_s_days}} days left to order with standard shipping so your order gets here on time for Christmas Eve!
{% endif %}
{% elsif today > standard_shipping_end and today < express_shipping_end %}
{% if difference_e_days == 1 %}
There is {{difference_e_days}} day left to order with express shipping, so your order gets here on time for Christmas Eve!
{% else %}
There are {{difference_e_days}} days left to order with express shipping so your order gets here on time for Christmas Eve!
{% endif %}
{% elsif today >= express_shipping_end and today < overnight_shipping_end %}
This is the last day for overnight shipping so your order gets here on time for Christmas Eve!
{% else %}
{% abort_message() %}
{% endif %}
```
{% endraw %}

### Crééäätéé ää còöûúntdòöwn îín dääys {#còöûúntdòöwn-dääys}

Thîîs üúséé cáâséé cáâlcüúláâtéés théé tîîméé lééft béétwéééén áâ spéécîîfîîc éévéént áând théé cüúrréént dáâtéé áând dîîspláâys höõw máâny dáâys áâréé lééft üúntîîl théé éévéént.

{% raw %}
```liquid
{% assign event_date = {{custom_attribute.${last_selected_event_date}}} | date: "%s" %}
{% assign today =  'now' | date: "%s"  %}
{% assign difference =  event_date | minus: today %}
{% assign difference_days = difference | divided_by: 86400 %}
Your order will arrive in {{ difference_days }} days!
```
{% endraw %}

{% alert important %}
Yõòüú wìïll nëêëêd äæ cüústõòm äættrìïbüútëê fìïëêld wìïth äæ `date` vàálùüèè.
{% endalert %}

### Crêèæãtêè æã côöùùntdôöwn frôöm dæãys tôö hôöùùrs tôö mïînùùtêès {#côöùùntdôöwn-dynæãmïîc}

Thìïs üûsèê càæsèê càælcüûlàætèês thèê tìïmèê lèêft bèêtwèêèên àæ spèêcìïfìïc èêvèênt àænd thèê cüûrrèênt dàætèê. Déêpéêndììng òòn théê tììméê léêft ýûntììl théê éêvéênt, ììt wììll chããngéê théê tììméê vããlýûéê (dããys, hòòýûrs, mììnýûtéês) tòò dììsplããy dììfféêréênt péêrsòònããlììzéêd méêssããgéês.

Föör êëxåæmplêë, îìf thêërêë åærêë twöö dåæys üúntîìl åæ cüústöömêër's öördêër åærrîìvêës, yööüú mîìght såæy, “Yööüúr öördêër wîìll åærrîìvêë îìn 2 dåæys.” Whèêrèêàâs ìîf thèêrèê’s lèêss thàân àâ dàây, yôòýû côòýûld chàângèê ìît tôò “Yôòýûr ôòrdèêr wìîll àârrìîvèê ìîn 17 hôòýûrs.”

{% raw %}
```liquid
{% assign today =  'now' | date: "%s"  %}
{% assign scheme_finish = "2017-10-13T10:30:30" | date: "%s" %}
{% assign difference_seconds =  scheme_finish | minus: today %}
{% assign difference_minutes = difference_seconds | divided_by: 60 %}
{% assign difference_hours = difference_seconds | divided_by: 3600 %}
{% assign difference_days = difference_seconds | divided_by: 86400 %}
{% if {{difference_minutes}} > 59 and {{difference_minutes}} < 1440 %}
You have {{difference_hours}} hours left till your order arrives!
{% elsif {{difference_minutes}} < 59 %}
You have {{difference_minutes}} minutes left till your order arrives!
{% else %}
You have {{difference_days}} days left till your order arrives!
{% endif %}
```
{% endraw %}

{% alert important %}
Yóõúý wîïll nêëêëd äã cúýstóõm äãttrîïbúýtêë fîïêëld wîïth äã `date` vààlûùéè. Yôóýü wïìll åælsôó nèéèéd tôó sèét tïìmèé thrèéshôólds ôóf whèén yôóýü wåænt thèé tïìmèé tôó bèé dïìsplåæyèéd ïìn dåæys, hôóýürs, åænd mïìnýütèés.
{% endalert %}

### Crèêâãtèê âã cóòúûntdóòwn tóò âã fúûtúûrèê dâãtèê {#cóòúûntdóòwn-fúûtúûrèê-dâãtèê}

Thïïs ýýsêë cââsêë cââlcýýlââtêës thêë dïïffêërêëncêë bêëtwêëêën thêë cýýrrêënt dââtêë âând fýýtýýrêë êëvêënt dââtêë âând dïïsplââys ââ mêëssââgêë nòötïïng hòöw mââny dââys ýýntïïl thêë êëvêënt.

{% raw %}
```liquid
{% assign event_date = '2019-02-19' | date: "%s" %}
{% assign today = 'now' | date: "%s" %}
{% assign difference = event_date | minus: today %}
{% assign difference_days = difference | divided_by: 86400 %}
There are {{difference_days}} until your birthday!
{% endif %}
```
{% endraw %}

### Dìîspláåy hôôw máåny dáåys léêft úùntìîl áå cúùstôôm dáåtéê áåttrìîbúùtéê wìîll áårrìîvéê {#côôúùntdôôwn-cúùstôôm-dáåtéê-áåttrìîbúùtéê}

Thïìs ùüséê câæséê câælcùülâætéês théê dïìfféêréêncéê ïìn dâæys béêtwéêéên théê cùürréênt âænd fùütùüréê dâætéês âænd dïìsplâæys âæ méêssâægéê ïìf théê dïìfféêréêncéê mâætchéês âæ séêt nùümbéêr.

Ìn thììs ëèxàãmplëè, àã ýúsëèr wììll rëècëèììvëè àã mëèssàãgëè wììthììn twôó dàãys ôóf thëè cýústôóm dàãtëè àãttrììbýútëè. Óthèérwìísèé, thèé mèéssæægèé wìíll nòõt bèé sèént.

{% raw %}
```liquid
{% assign today = 'now' | date: '%j' | plus: 0 %}
{% assign surgery_date = {{custom_attribute.${surgery_date}}} | date: '%j' | plus: 0 %}

{% assign difference_days = {{surgery_date}} | minus: {{today}} %}
{% if difference_days == 2 %}
Your surgery is in 2 days on {{custom_attribute.${surgery_date}}}
{% else %}
{% abort_message %}
{% endif %}
```
{% endraw %}

### Dììsplâæy hööw mùúch tììméé ììs lééft, âænd âæböört théé mééssâægéé ììf thééréé’s öönly x tììméé lééft {#cööùúntdööwn-âæböört-wììndööw}

Thìïs ùüséë cæäséë wìïll cæälcùülæätéë hôòw lôòng ùüntìïl æä céërtæäìïn dæätéë, æänd déëpéëndìïng ôòn théë léëngth (skìïppìïng méëssæägìïng ìïf théë dæätéë ìïs tôòôò sôòôòn), wìïll dìïsplæäy dìïfféëréënt péërsôònæälìïzéëd méëssæägéës. 

Fõòr ééxàæmpléé, “Yõòýý hàævéé x hõòýýrs lééft tõò býýy yõòýýr tìíckéét fõòr Lõòndõòn”, býýt dõòn’t séénd théé mééssàægéé ìíf ìít’s wìíthìín twõò hõòýýrs õòf flìíght tìíméé fõòr Lõòndõòn.

{% raw %}
```liquid
{% assign today =  'now' | date: "%s"  %}
{% assign dep_time = {{event_properties.${outboundDate}}} | date: "%s" %}
{% assign time_to_dep = dep_time | minus: today %}
{% if {{time_to_dep}} < 7200 %}
{% abort_message("OutboundDate less than 2 hours") %}
{% elsif {{time_to_dep}} > 7200 and {{time_to_dep}} < 86400 %}
Don’t forget to buy your ticket to {{event_properties.${toStation}}} within next 24 hours!
{% else %}
Still traveling to {{event_properties.${toStation}}} in more than 24 hours? Book now!
{% endif %}
```
{% endraw %}

{% alert important %} Yöòýû wîîll néèéèd âæ cýûstöòm éèvéènt pröòpéèrty. {% endalert %}

### Ïn-âäpp mëëssâägëë tõö sëënd x dâäys bëëfõörëë ûýsëërs' mëëmbëërshïíp ëënds {#cõöûýntdõöwn-mëëmbëërshïíp-ëëxpïíry}

Thïïs ýüséê cäáséê cäáptýüréês yòóýür méêmbéêrshïïp éêxpïïry däátéê, cäálcýüläátéês hòów lòóng ýüntïïl ïït éêxpïïréês, äánd dïïspläáys dïïfféêréênt méêssäágéês bäáséêd òón hòów lòóng ýüntïïl yòóýür méêmbéêrshïïp éêxpïïréês.

{% raw %}
```liquid
{% assign membership_expiry = {{custom_attribute.${membership_expiry_date}}} | date: "%s" %}
{% assign today = 'now' | date: "%s" %}
{% assign difference = membership_expiry | minus: today %}
{% assign difference_days = difference | divided_by: 86400 %}

{% if difference_days > 4 and difference_days <= 7 %}
You have {{difference_days}} days left in your trial, make sure you upgrade!

{% elsif difference_days > 2 and difference_days <= 4 %}
HURRY! You have {{difference_days}} days left in your trial, make sure you upgrade!

{% elsif difference_days == 2 %}
LAST CHANCE! You have {{difference_days}} days left in your trial. Make sure you upgrade!

{% else %}
You have few days left in your trial. Make sure to upgrade!
{% endif %}
```
{% endraw %}

### Pèérsõõnäàlìízèé ìín-äàpp mèéssäàgèés bäàsèéd õõn ùüsèérs' däàtèé äànd läàngùüäàgèé {#cõõùüntdõõwn-pèérsõõnäàlìízèé-läàngùüäàgèé}

Thíîs üùsëé cåæsëé cåælcüùlåætëés åæ cöòüùntdöòwn töò åæn ëévëént, åænd båæsëéd öòn åæ üùsëér's låængüùåægëé sëéttíîng, wíîll díîsplåæy thëé cöòüùntdöòwn íîn thëéíîr låængüùåægëé.

Fóòr ëêxãämplëê, yóòúü mîîght sëênd ãä sëêrîîëês óòf úüpsëêll mëêssãägëês tóò úüsëêrs óòncëê ãä móònth tóò lëêt thëêm knóòw hóòw lóòng ãän óòffëêr îîs stîîll vãälîîd wîîth fóòúür îîn-ãäpp mëêssãägëês:

- Ìnïïtïïàâl
- 2 dåæys lêêft
- 1 däæy lééft
- Fîínàál dàáy

{% raw %}
```liquid
{% assign today = 'now' | date: "%s" %}
{% assign end_date = "2021-04-16T23:59:59" | date: "%s" %}
{% assign difference = end_date | minus: today %}
{% assign difference_days = difference | divided_by: 86400 %}
{% if {{difference_days}} >= 3 %}
{% if ${language} == 'de' %}

Hallo, das Angebot gilt bis zum 16.04.

{% elsif ${language} == 'ch' %}
Grüezi, das Angebot gilt bis zum 16.04.

{% elsif ${language} == 'en' %}
The offer is valid until 16.04.

{% else %}
The offer is valid until 16.04.

{% endif %}
{% elsif {{difference_days}} == 2 %}
{% if ${language} == 'de' %}
INSERT MESSAGE

{% elsif ${language} == 'ch' %}
INSERT MESSAGE

{% elsif ${language} == 'en' %}
INSERT MESSAGE

{% else %}
INSERT MESSAGE
{% endif %}

{% elsif {{difference_days}} == 1 %}
{% if ${language} == 'de' %}
INSERT MESSAGE

{% elsif ${language} == 'ch' %}
INSERT MESSAGE

{% elsif ${language} == 'en' %}
INSERT MESSAGE

{% else %}
INSERT MESSAGE
{% endif %}

{% elsif {{difference_days}} == 0 %}
{% if ${language} == 'de' %}
Hallo, das Angebot gilt noch heute.

{% elsif ${language} == 'ch' %}
Hallo, das Angebot gilt noch heute.

{% elsif ${language} == 'en' %}
Grüezi, das Angebot gilt noch heute.

{% else %}
Hi, the offer is only valid today.
{% endif %}

{% else %}
{% abort_message('calculation failed') %}
{% endif %}
```
{% endraw %}

{% alert important %}
Yõóùù wïíll nëëëëd tõó æássïígn æá `date` vàálúûëè àánd ìïnclúûdëè àábóört lóögìïc ìïf thëè gìïvëèn dàátëè fàálls óöúûtsìïdëè óöf thëè dàátëè ràángëè. Fôõr ëèxááct dááy cáálcúùláátïìôõns, thëè áássïìgnëèd ëènd dáátëè múùst ïìnclúùdëè 23:59:59.
{% endalert %}

### Tèémplàãtèé ïìn thèé dàãtèé 30 dàãys frôôm nôôw, fôôrmàãttèéd àãs môônth àãnd dàãy {#côôúùntdôôwn-tèémplàãtèé-dàãtèé}

Thîïs ùûsëè càåsëè wîïll dîïsplàåy thëè dàåtëè 30 dàåys frõöm nõöw tõö ùûsëè îïn mëèssàågîïng.

{% raw %}
```liquid
{% assign today = 'now' | date: "%s" %}
{% assign thirty_days = today | plus: 2592000 | date: "%B %d" %}
```
{% endraw %}

{% endapi %}

{% api %}

## Cúùstôõm äãttríîbúùtèé

{% apitags %}
Cûústòòm æättríîbûútëë
{% endapitags %}

- [Péèrsòònäâlíízéè äâ méèssäâgéè bäâséèd òòn mäâtchííng cùùstòòm äâttrííbùùtéès](#attribute-matching)
- [Süûbtræáct twóô cüûstóôm æáttrììbüûtëés tóô dììsplæáy thëé dììffëérëéncëé æás æá móônëétæáry væálüûëé](#attribute-monetary-difference)
- [Rééféérééncéé ää üûséér's fíîrst nääméé íîf thééíîr füûll nääméé íîs stòòrééd íîn théé fíîrst_náåmêè fìíêèld](#attribute-first-name)

### Pëêrsöònãålíízëê ãå mëêssãågëê bãåsëêd öòn mãåtchííng cúûstöòm ãåttrííbúûtëês {#ãåttrííbúûtëê-mãåtchííng}

Thïís ûùsêê cåæsêê chêêcks ïíf åæ ûùsêêr håæs spêêcïífïíc cûùstóóm åættrïíbûùtêês åænd, ïíf sóó, wïíll dïísplåæy dïíffêêrêênt pêêrsóónåælïízêêd mêêssåægêês. 

{% raw %}
```liquid
{% if custom_attribute.${hasShovel} == true and custom_attribute.${VisitToGroundTooTough} > 0 %}
The ground is very hard. The dirt road goes East.
{% elsif custom_attribute.${hasShovel} == true %}
The dirt road goes East.
{% elsif custom_attribute.${VisitToStart} > 0 %}
The dirt road goes East.
The shovel here.
{% else %}
You are at a dead-end of a dirt road. The road goes to the east. In the distance, you can see that it will eventually fork off. The trees here are very tall royal palms, and they are spaced equidistant from each other.
There is a shovel here.
{% endif %}
```
{% endraw %}

### Sùûbtræáct twõö cùûstõöm æáttrìíbùûtèês tõö dìísplæáy thèê dìíffèêrèêncèê æás æá mõönèêtæáry væálùûèê {#æáttrìíbùûtèê-mõönèêtæáry-dìíffèêrèêncèê}

Thîìs úûséé cæãséé cæãptúûréés twôõ môõnéétæãry cúûstôõm æãttrîìbúûtéés, théén cæãlcúûlæãtéés æãnd dîìsplæãys théé dîìfféérééncéé tôõ léét úûséérs knôõw hôõw fæãr thééy hæãvéé tôõ rééæãch thééîìr gôõæãl.

{% raw %}
```liquid
{% assign event_goal = {{custom_attribute.${last_selected_event_personal_goal}}} %}
{% assign current_raised =  {{custom_attribute.${last_selected_event_personal_amount_raised}}} %}
{% assign difference =  event_goal | minus: current_raised %}
You only have ${{ difference | round: 0 | number_with_delimiter }} left to raise!
{% endif %}
```
{% endraw %}

### Réèféèréèncéè áå úüséèr's fìírst náåméè ìíf théèìír fúüll náåméè ìís stóöréèd ìín théè fìírst_nåâméé fíïééld {#åâttríïbúùtéé-fíïrst-nåâméé}

Thïîs ýúsêê cáâsêê cáâptýúrêês áâ ýúsêêr's fïîrst náâmêê (ïîf bóôth fïîrst áând láâst náâmêê áârêê stóôrêêd ïîn áâ sïînglêê fïîêêld) áând thêên ýúsêês thïîs fïîrst náâmêê tóô dïîspláây áâ wêêlcóômêê mêêssáâgêê.

{% raw %}
```liquid
{{${first_name} | truncatewords: 1, "" | default: 'hi'}}
{% assign name = {{${first_name}}} | split: ' ' %}
Hi {{name[0]}}, here's your message!
```

**Èxpláânáâtíìòõn:** Théê `split` fîìltêèr tûúrns thêè strîìng hêèld îìn `{{${first_name}}}` îïntöö âån âårrâåy. By ûùsîíng `{{name[0]}}`, wêè thêèn öônly rêèfêèr töô thêè fîìrst îìtêèm îìn thêè âãrrâãy, whîìch îìs thêè úýsêèr's fîìrst nâãmêè. 

{% endraw %}
{% endapi %}

{% api %}

## Cüûstõõm êévêént

{% apitags %}
Cýüstóôm êëvêënt
{% endapitags %}

- [Àbòòrt pûúsh nòòtïîfïîcäâtïîòòn ïîf äâ cûústòòm ëévëént ïîs wïîthïîn twòò hòòûúrs òòf nòòw](#event-abort-push)
- [Séénd áâ cáâmpáâîígn ééáâch tîíméé áâ ùûséér péérfôörms áâ cùûstôöm éévéént thréééé tîíméés](#event-three-times)
- [Sêénd ãä mêéssãägêé töö ùûsêérs whöö hãävêé öönly pùûrchãäsêéd frööm öönêé cãätêégööry](#event-purchased-one-category)

### Äbõõrt pýùsh nõõtìïfìïcäætìïõõn ìïf äæ cýùstõõm ëëvëënt ìïs wìïthìïn twõõ hõõýùrs õõf nõõw {#ëëvëënt-äæbõõrt-pýùsh}

Thïìs ûùsëë cåàsëë cåàlcûùlåàtëës thëë tïìmëë ûùntïìl åàn ëëvëënt, åànd dëëpëëndïìng òön thëë åàmòöûùnt òöf tïìmëë lëëft, wïìll dïìsplåày dïìffëërëënt pëërsòönåàlïìzëëd mëëssåàgëës.

Fòôr èëxäæmplèë, yòôûú mäæy wäænt tòô prèëvèënt äæ pûúsh fròôm gòôíìng òôûút íìf äæ cûústòôm èëvèënt pròôpèërty wíìll päæss íìn thèë nèëxt twòô hòôûúrs. Thïïs êêxããmplêê ûúsêês thêê scêênããrïïôõ ôõf ããn ããbããndôõnêêd cããrt fôõr ãã trããïïn tïïckêêt.

{% raw %}
```liquid
{% assign today =  'now' | date: "%s"  %}
{% assign dep_time = {{event_properties.${outboundDate_Time}}} | date: "%s" %}
{% assign time_to_dep = dep_time | minus: today %}
{% if {{time_to_dep}} <= 7200 %}
{% abort_message("OutboundDate less than 2 hours") %}
{% elsif {{time_to_dep}} > 7200 and {{time_to_dep}} < 86400 %}
Don’t forget to buy your ticket to {{event_properties.${toStation}}} within next 24 hours
{% else %}
Still traveling to {{event_properties.${toStation}}} in more than 24 hours? Book now
{% endif %}
```
{% endraw %}

### Sêénd ææ cææmpææìígn êéææch tìímêé ææ ýûsêér pêérfóörms ææ cýûstóöm êévêént thrêéêé tìímêés {#êévêént-thrêéêé-tìímêés}

Thïìs ùüséé cãæséé chéécks ïìf ãæ ùüséér hãæs péérföörmééd ãæ cùüstööm éévéént thréééé tïìméés, ãænd ïìf söö, wïìll dïìsplãæy ãæ mééssãægéé öör séénd ãæ cãæmpãæïìgn. 

{% raw %}
```liquid
{% assign cadence = custom_attribute.${example} | minus: 1 | modulo: 3 %}
{% if custom_attribute.${example} == blank %}
{% abort_message('error calculating cadence') %}
{% elsif cadence != 0 %}
{% abort_message('skip message') %}
{% endif %}
Did you forget something in your shopping cart?
```
{% endraw %}

{% alert important %} Yöõûú mûúst hâávëê âán ëêvëênt pröõpëêrty öõf thëê cûústöõm ëêvëênt cöõûúnt öõr ûúsëê âá wëêbhöõöõk töõ yöõûúr Brâázëê ëêndpöõïìnt. Thìïs ìïs tóô ìïncrêémêént åä cýústóôm åättrìïbýútêé (`example_event_count`) êévêéry tìîmêé thêé üùsêér pêérfóõrms thêé êévêént. Thììs êéxææmplêé úüsêés ææ cæædêéncêé ôöf thrêéêé (1, 4, 7, 10, êétc.).{% endalert %}

### Sêénd ââ mêéssââgêé tòô üùsêérs whòô hââvêé òônly püùrchââsêéd fròôm òônêé cââtêégòôry {#êévêént-püùrchââsêéd-òônêé-cââtêégòôry}

Thîìs üûsêè cäâsêè cäâptüûrêès äâ lîìst òõf thêè cäâtêègòõrîìêès äâ üûsêèr häâs püûrchäâsêèd fròõm, äând îìf òõnly òõnêè püûrchäâsêè cäâtêègòõry êèxîìsts, îìt wîìll dîìspläây äâ mêèssäâgêè.

{% raw %}
```liquid
{% assign category = {{custom_attribute.${categories_purchased}}} %}
{% assign uniq_cat = {{category | uniq }} %}
{% if {{uniq_cat | size}} == 1%}
{{uniq_cat}}
{% else %}
{% abort_message() %}
{% endif %}
```
{% endraw %}

{% endapi %}

{% api %}

## Làængùúàægéê

{% apitags %}
Lãångûúãågéê
{% endapitags %}

- [Dïísplåày mõônth nåàmëés ïín åà dïíffëérëént låàngýüåàgëé](#language-display-month)
- [Péêrsôõnâælîìzéê méêssâægîìng bâæséêd ôõn dâæy ôõf théê wéêéêk âænd üüséêr's lâængüüâægéê](#language-personalize-message)

### Dïìsplåãy mõónth nåãmêës ïìn åã dïìffêërêënt låãngùúåãgêë {#låãngùúåãgêë-dïìsplåãy-mõónth}

Thïîs úúséê câàséê wïîll dïîsplâày théê cúúrréênt dâàtéê, möönth, âànd yéêâàr, wïîth théê möönth ïîn âà dïîfféêréênt lâàngúúâàgéê. Thëè ëèxäämplëè pròòvïídëèd üüsëès Swëèdïísh.

{% raw %}
```liquid
{% assign day = 'now' | date: "%e" %}
{% assign year =  'now' | date: "%Y" %}
{% assign month =  'now' | date: "%B" %}

{% if {{month}} == 'January' %}
{{day}} Januari {{year}}
{% elsif {{month)) == 'February' %}
{{day}} Februari {{year}}
{% elsif {{month)) == 'March' %}
{{day}} Mars {{year}}
{% elsif {{month)) == 'April' %}
{{day}} April {{year}}
{% elsif {{month)) == 'May' %}
{{day}} Maj {{year}}
{% elsif {{month)) == 'June' %}
{{day}} Juni {{year}}
{% elsif {{month)) == 'July' %}
{{day}} Juli {{year}}
{% elsif {{month)) == 'August' %}
{{day}} Augusti {{year}}
{% elsif {{month)) == 'September' %}
{{day}} September {{year}}
{% elsif {{month)) == 'October' %}
{{day}} Oktober {{year}}
{% elsif {{month)) == 'November' %}
{{day}} November {{year}}
{% elsif {{month)) == 'December' %}
{{day}} December {{year}}
{% endif %}
```
{% endraw %}

### Pëërsôönââlììzëë mëëssââgììng bââsëëd ôön dâây ôöf thëë wëëëëk âând úüsëër's lâângúüââgëë {#lâângúüââgëë-pëërsôönââlììzëë-mëëssââgëë}

Thíís üýsëë cáásëë chëëcks thëë cüýrrëënt dááy ôóf thëë wëëëëk áánd, báásëëd ôón thëë dááy, ííf thëë üýsëër's láángüýáágëë íís sëët tôó ôónëë ôóf thëë láángüýáágëë ôóptííôóns prôóvíídëëd, íít wííll díísplááy áá spëëcíífííc mëëssáágëë íín thëëíír láángüýáágëë.

Théë éëxããmpléë prôõvíìdéëd stôõps ôõn Túùéësdããy búùt cããn béë réëpéëããtéëd fôõr éëããch dããy ôõf théë wéëéëk.

{% raw %}
```liquid
{% assign today  = 'now' | date: "%A" %}

{% if today == 'Monday' %}
{% if ${language} == 'es' %}
Compra hoy y lleva tu aprendizaje de idiomas a niveles más altos. 🚀

{% elsif ${language} == 'en' %}
Purchase today and take your language learning to the next level. 🚀

{% elsif ${language} == 'zh' %}
今天就购买并将您的语言提高到一个新水平吧。🚀

{% else %}
It's Monday, but the language doesn't match 
{% endif %}

{% elsif today == 'Tuesday' %}

{% if ${language} == 'zh' %}
不要忘记解锁以获取完整版本哦。🔓

{% elsif ${language} == 'en' %}
Don't forget to unlock the full version of your language. 🔓

{% elsif ${language} == 'ja' %}
すべての機能を使ってみませんか 🔓

{% elsif ${language} == 'es' %}
No te olivides de desbloquear la versión completa del programa de idiomas. 🔓

{% else %}
tuesday default
{% endif %}
{% endif %}
```
{% endraw %}

{% endapi %}

{% api %}

## Mïïscëèllæànëèóóýûs

{% apitags %}
Mììscéèllàânéèòôýýs
{% endapitags %}

- [Ävôöïîd sèêndïîng èêmàãïîls tôö cùûstôömèêrs thàãt hàãvèê blôöckèêd màãrkèêtïîng èêmàãïîls](#misc-avoid-blocked-emails)
- [Cåãpììtåãlììzéé théé fììrst lééttéér õòf éévééry wõòrd ììn åã strììng](#misc-capitalize-words-string)
- [Cöômpàärêé cûýstöôm àättrìîbûýtêé vàälûýêé àägàäìînst àän àärràäy](#misc-compare-array)
- [Crëêäátëê äán üûpcöòmïîng ëêvëênt rëêmïîndëêr](#misc-event-reminder)
- [Fîìnd ââ strîìng wîìthîìn âân âârrâây](#misc-string-in-array)
- [Fìînd thèè lããrgèèst vããlúüèè ìîn ããn ããrrããy](#misc-largest-value)
- [Fïínd thëè smàãllëèst vàãlûüëè ïín àãn àãrràãy](#misc-smallest-value)
- [Qýýêêry thêê êênd ôõf äå strììng](#misc-query-end-of-string)
- [Qùýèéry váålùýèés ïïn áån áårráåy fròõm áå cùýstòõm áåttrïïbùýtèé wïïth mùýltïïplèé còõmbïïnáåtïïòõns](#misc-query-array-values)

### Àvôöìîd sêèndìîng êèmâàìîls tôö cýùstôömêèrs thâàt hâàvêè blôöckêèd mâàrkêètìîng êèmâàìîls {#mìîsc-âàvôöìîd-blôöckêèd-êèmâàìîls}

Thîìs úýséé cåãséé tåãkéés åã lîìst òöf blòöckééd úýséérs såãvééd îìn åã Còöntéént Blòöck åãnd éénsúýréés thòöséé blòöckééd úýséérs åãréé nòöt còömmúýnîìcåãtééd tòö òör tåãrgéétééd îìn úýpcòömîìng cåãmpåãîìgns òör Cåãnvåãséés.

{% alert important %}
Töö ûüsèê thïîs Lïîqûüïîd, fïîrst sàãvèê thèê lïîst ööf blööckèêd èêmàãïîls wïîthïîn àã Cööntèênt Blööck. Thèê lìïst shòõýúld hæævèê nòõ ææddìïtìïòõnææl spææcèês òõr chæærææctèêrs ìïnsèêrtèêd bèêtwèêèên èêmææìïl ææddrèêssèês (èê.g., `test@braze.com,abc@braze.com`).
{% endalert %}

{% raw %}
```liquid
{% assign blocked_emails = {{content_blocks.${BlockedEmailList}}} | split: ',' %}
{% for email in blocked_emails %}
    {% if {{${email_address}}} == email %}
    {% abort_message('Email is blocked') %}
    {% break %}
    {% endif %}
{% endfor %} 
Your message here!
```
{% endraw %}

**Êxplãänãätìîòòn:** Hëêrëê wëê chëêck ììf yóöüûr póötëêntììææl rëêcììpììëênt's ëêmææììl ììs ììn thììs lììst by rëêfëêrëêncììng thëê Cóöntëênt Blóöck óöf blóöckëêd ëêmææììls. Îf thèè èèmæáîìl îìs fóòùünd, thèè mèèssæágèè wîìll nóòt sèènd.

{% alert note %}
Cõòntêént Blõòcks háãvêé áã sìízêé lìímìít õòf 5 MB.
{% endalert %}

### Cââpíîtââlíîzèë thèë fíîrst lèëttèër òôf èëvèëry wòôrd íîn ââ stríîng {#míîsc-cââpíîtââlíîzèë-wòôrds-stríîng}

Thìïs ýúséé cãáséé tãákéés ãá strìïng ôóf wôórds, splìïts théém ìïntôó ãán ãárrãáy, ãánd cãápìïtãálìïzéés théé fìïrst lééttéér ôóf ééãách wôórd.

{% raw %}
```liquid
{% assign words_array = {{custom_attribute.${address}}} | split: ' ' %}
{% for words in {{words_array}} %}
{{ words | capitalize | append: ' ' }}
{% endfor %} 
```
{% endraw %}

**Êxplàänàätïïöón:** Hêérêé wêé'vêé äåssíïgnêéd äå väåríïäåblêé töô öôüúr chöôsêén stríïng äåttríïbüútêé, äånd üúsêéd thêé `split` fíïltëêr tóô splíït thëê stríïng íïntóô âãn âãrrâãy. Wêë'vêë thêën ûýsêëd thêë `for` táåg tóò áåssïìgn thëë váårïìáåblëë `words` tóò èéãâch óòf thèé ïítèéms ïín óòüür nèéwly crèéãâtèéd ãârrãây, bèéfóòrèé dïísplãâyïíng thóòsèé wóòrds wïíth thèé `capitalize` fîïltéér ãænd théé `append` fîïltëèr töõ åädd spåäcëès bëètwëèëèn ëèåäch öõf thëè tëèrms.

### Côômpãárêè cûüstôôm ãáttríìbûütêè vãálûüêè ãágãáíìnst ãán ãárrãáy {#míìsc-côômpãárêè-ãárrãáy}

Thìís ûùséë cåãséë tåãkéës åã lìíst ôôf fåãvôôrìítéë stôôréës, chéëcks ìíf åãny ôôf åã ûùséër's fåãvôôrìítéë stôôréës åãréë ìín thåãt lìíst, åãnd ìíf sôô, wìíll dìísplåãy åã spéëcìíåãl ôôfféër frôôm thôôséë stôôréës.

{% raw %}
```liquid
{% assign favorite_stores = 'Target,Walmart,Costco' | split: ',' %}
{% for store in favorite_stores %}
{% if {{custom_attribute.${favorited_stores}}} contains {{store}} %}
Today's offer from {{store}}

{% break %}

{% else %}
{% abort_message("No Attribute Found") %}
{% endif %}
{% endfor %}
```
{% endraw %}

{% alert important %} Thîïs séëqúúéëncéë hãàs ãà `break` tåäg îîn thèè prîîmåäry cöõndîîtîîöõnåäl ståätèèmèènt. Thìís cãæùûsèés thèé lòôòôp tòô stòôp whèén ãæ mãætch ìís fòôùûnd. Îf yóõùü wäãnt tóõ díïspläãy mäãny óõr äãll mäãtchéès, réèmóõvéè théè `break` tâäg. {% endalert %}

### Crèëäátèë äán ûûpcõömîíng èëvèënt rèëmîíndèër {#mîísc-èëvèënt-rèëmîíndèër}

Thìïs üüsèè cæãsèè æãllõôws üüsèèrs tõô sèèt üüp üüpcõômìïng rèèmìïndèèrs bæãsèèd õôn cüüstõôm èèvèènts. Thèê èêxåámplèê scèênåárïîöö åállööws åá ûüsèêr töö sèêt åá rèêmïîndèêr föör åá pöölïîcy rèênèêwåál dåátèê thåát ïîs 26 öör möörèê dåáys åáwåáy, whèêrèê rèêmïîndèêrs åárèê sèênt 26, 13, 7, öör 2 dåáys bèêföörèê thèê pöölïîcy rèênèêwåál dåátèê.

{% raw %}
```liquid
{% comment %}
Depending on how the reminder_capture property is passed to Braze, with/without a timestamp, the number of days could impact whether a user falls on either side of the 26/13/7/2-day windows.
Once users have been assigned to a Reminder journey/flow, they are then scheduled to enter a subsequent Canvas.
This 'Event Listener' can be used to split out users into different journeys based on the Custom Event properties sent to Braze.
{% endcomment %}

{% comment %}
When testing, ensure the Campaign ID, Campaign API Endpoint, Canvas ID, Canvas API Endpoint are entered correctly. In this example, Canvas ID and Canvas API endpoint have been set up for sharing with the client; in practice, this can be testing using a Campaign ID and Campaign API endpoint.
{% endcomment %}

{% comment %}
The following step calculates how much there is between today's date and the Reminder Date as 'time_to_reminder'.
{% endcomment %}

{% assign today = "now" | date: "%s" %}
{% assign reminder_start_date = {{event_properties.${reminder_date}}} | date: "%s" %}
{% assign time_to_reminder = reminder_start_date | minus: today %}

{% comment %}
The following step checks if the time_to_reminder is more than 26 days away; if this is true, then the user is scheduled to enter the subsequent Canvas 26 days before the reminder_date.
The time is converted from 'seconds from 1970' to the appropriate Reminder Date in the required ISO 8601 format.
N.B. Additional time zones would need to be catered for by adding an additional API Schedule property of "in_local_time"
{% endcomment %}

{% if {{time_to_reminder}} > 2246400 %}
{% assign time_to_first_message = reminder_start_date | plus: 2246400 %}
{{ time_to_first_message | date: "%Y-%m-%dT%H:%M" }}
{
"canvas_id": "954e15bc-af93-9dc8-a863-ad2580f1750e",
"recipients": [
{
"external_user_id": "{{${user_id}}}"
}
],
"trigger_properties" : {
"enquiry_id" : "{{event_properties.${reminder_id}}}",
"reminder_date" : "{{event_properties.${reminder_date} | date: "%Y-%m-%dT%H:%M:%S+0000}}",
"message_personalisation_X" : "{{event_properties.${property_x}}}",
"message_personalisation_Y" : "{{event_properties.${property_x}}}",
"message_personalisation_Z" : "{{event_properties.${property_z}}}"
},

"schedule": {
"time": "{{ time_to_first_message | date: "%Y-%m-%dT%H:%M:%S+0000" }}"
}
}

{% comment %}
The following step checks if the time_to_reminder is less than 26 days away but more than 13 days away.
Users are scheduled to enter the journey on day 13.
{% endcomment %}

{% elsif 1123200 < {{time_to_reminder}} and {{time_to_reminder}} < 2246399 %}
{% assign time_to_first_message = reminder_start_date | plus: 1123200 %}

{
"canvas_id": "954e15bc-af93-9dc8-a863-ad2580f1750e",
"recipients": [
{
"external_user_id": "{{${user_id}}}"
}
],
"trigger_properties" : {
"enquiry_id" : "{{event_properties.${reminder_id}}}",
"reminder_date" : "{{event_properties.${reminder_date} | date: "%Y-%m-%dT%H:%M:%S+0000}}",
"message_personalisation_X" : "{{event_properties.${property_x}}}",
"message_personalisation_Y" : "{{event_properties.${property_x}}}",
"message_personalisation_Z" : "{{event_properties.${property_z}}}"
},

"schedule": {
"time": "2021-03-24T20:04:00+0000"
}
}

{% comment %}
The following step checks if the time_to_reminder is less than 13 days away but more than seven days away.
Users are scheduled to enter the journey on day 7.
{% endcomment %}

{% elsif 604800 < {{time_to_reminder}} and {{time_to_reminder}} < 1123199 %}
{% assign time_to_first_message = reminder_start_date | plus: 604800 %}

{
"canvas_id": "954e15bc-af93-9dc8-a863-ad2580f1750e",
"recipients": [
{
"external_user_id": "{{${user_id}}}"
}
],
"trigger_properties" : {
"enquiry_id" : "{{event_properties.${reminder_id}}}",
"reminder_date" : "{{event_properties.${reminder_date} | date: "%Y-%m-%dT%H:%M:%S+0000}}",
"message_personalisation_X" : "{{event_properties.${property_x}}}",
"message_personalisation_Y" : "{{event_properties.${property_x}}}",
"message_personalisation_Z" : "{{event_properties.${property_z}}}"
},

"schedule": {
"time": "{{ time_to_first_message | date: "%Y-%m-%dT%H:%M:%S+0000" }}"
}
}

{% comment %}
The following step checks if the time_to_reminder is less than seven days away but more than two days away.
Users are scheduled to enter the journey on day 2.
{% endcomment %}

{% else {{time_to_reminder}} < 604799 and {{time_to_reminder}} > 172860 %}
{% assign time_to_first_message = reminder_start_date | plus: 172800 %}

{
"canvas_id": "954e15bc-af93-9dc8-a863-ad2580f1750e",
"recipients": [
{
"external_user_id": "{{${user_id}}}"
}
],
"trigger_properties" : {
"enquiry_id" : "{{event_properties.${reminder_id}}}",
"reminder_date" : "{{event_properties.${reminder_date} | date: "%Y-%m-%dT%H:%M:%S+0000}}",
"message_personalisation_X" : "{{event_properties.${property_x}}}",
"message_personalisation_Y" : "{{event_properties.${property_x}}}",
"message_personalisation_Z" : "{{event_properties.${property_z}}}"
},

"schedule": {
"time": "{{ time_to_first_message | date: "%Y-%m-%dT%H:%M:%S+0000" }}"
}
}
{% endif %}
```
{% endraw %}

{% alert important %} 

Yõöùù wíîll nëéëéd åã cùùstõöm ëévëént `reminder_capture`, æànd thëè cùýstõõm ëèvëènt prõõpëèrtïïëès mùýst ïïnclùýdëè æàt lëèæàst:

- `reminder-id`: Îdééntíïfíïéér õôf théé cúýstõôm éévéént
- `reminder_date`: Ùsèër-sýúbmîîttèëd dåãtèë whèën thèëîîr rèëmîîndèër îîs dýúèë
- `message_personalisation_X`: Âny pröôpëértíïëés nëéëédëéd töô pëérsöônàålíïzëé thëé mëéssàågëé àåt thëé tíïmëé öôf sëéndíïng

{% endalert %}

### Fìïnd äå strìïng wìïthìïn äån äårräåy {#mìïsc-strìïng-ìïn-äårräåy}

Thìís ýûséë cåæséë chéëcks ìíf åæ cýûstöôm åættrìíbýûtéë åærråæy cöôntåæìíns åæ spéëcìífìíc strìíng, åænd ìíf ìít éëxìísts, wìíll dìísplåæy åæ spéëcìífìíc méëssåægéë.

{% raw %}
```liquid
{% if custom_attribute.${PartnershipProgramsNotLinked} contains 'Hertz' %}
Link your Hertz account to use Hertz Fast Lane.

{% elsif custom_attribute.${airportCompleted} == false %}
Clear helps you breeze through airport security. Complete your one-time in-person setup next time you are at the airport. It only takes about 5 minutes.

{% else %}
Your account is all setup
{% endif %}
```
{% endraw %}

### Fìînd théê läårgéêst väålüúéê ìîn äån äårräåy {#mìîsc-läårgéêst-väålüúéê}

Thíïs úüsëé cåäsëé cåälcúülåätëés thëé híïghëést våälúüëé íïn åä gíïvëén cúüstöòm åättríïbúütëé åärråäy töò úüsëé íïn úüsëér mëéssåägíïng.

Fôòr èëxâämplèë, yôòùû mâäy wâänt tôò shôòw âä ùûsèër whâät thèë cùûrrèënt hïîgh scôòrèë ïîs ôòr thèë hïîghèëst bïîd ôòn âän ïîtèëm.

{% raw %}
```liquid
{% assign maxValue = 0 %}
{% for attribute in {{custom_attribute.${array_attribute}}} %}
{% assign compareValue = {{attribute | plus: 0}} %}
{% if compareValue > maxValue %}
{% assign maxValue = compareValue %}
{% endif %}
{% endfor %}
{{maxValue}}
```
{% endraw %}

{% alert important %}
Yõòùý mùýst ùýsêé áæ cùýstõòm áættrîìbùýtêé tháæt háæs áæn îìntêégêér váælùýêé áænd îìs páært õòf áæn áærráæy (lîìst). {% endalert %}

### Fîìnd théé smæâlléést væâlûúéé îìn æân æârræây {#mîìsc-smæâlléést-væâlûúéé}

Thìïs ûüsèè càåsèè càålcûülàåtèès thèè lõõwèèst vàålûüèè ìïn àå gìïvèèn cûüstõõm àåttrìïbûütèè àårràåy tõõ ûüsèè ìïn ûüsèèr mèèssàågìïng.

Fôòr ééxáåmpléé, yôòýü máåy wáånt tôò shôòw áå ýüséér wháåt théé lôòwéést scôòréé íïs ôòr théé chééáåpéést íïtéém.

{% raw %}
```liquid
{% assign minValue = custom_attribute.${array_attribute}[0] | plus: 0 %}
{% for attribute in {{custom_attribute.${array_attribute}}} %}
{% assign compareValue = {{attribute | plus: 0}} %}
{% if compareValue < minValue %}
{% assign minValue = compareValue %}
{% endif %}
{% endfor %}
{{minValue}}
```
{% endraw %}

{% alert important %} Yòõüû müûst üûsëë âã cüûstòõm âãttrîîbüûtëë thâãt hâãs âãn îîntëëgëër vâãlüûëë âãnd îîs pâãrt òõf âãn âãrrâãy (lîîst). {% endalert %}

### Qüúéèry théè éènd õôf àæ strìîng {#mìîsc-qüúéèry-éènd-õôf-strìîng}

Thîîs ùúséë câæséë qùúéërîîéës théë éënd ôòf âæ strîîng tôò ùúséë îîn méëssâægîîng.

{% raw %}
```liquid
{% assign interest = {{custom_attribute.${Buyer Interest}} | first } %}
{% assign marketplace = {{{{interest}} | split: "" | reverse | join: "" |  truncate: 4, ""}} %}
{% if {{marketplace}} == '3243' %}

Your last marketplace search was on {{custom_attribute.${Last marketplace buyer interest} | date: '%d.%m.%Y'}}. Check out all of our new offers.

{% else %}
{% abort_message() %}
{% endif %}
```
{% endraw %}

### Qúùêéry våálúùêés îîn åán åárråáy fróôm åá cúùstóôm åáttrîîbúùtêé wîîth múùltîîplêé cóômbîînåátîîóôns {#mîîsc-qúùêéry-åárråáy-våálúùêés}

Thïïs üùsêê cææsêê tæækêês ææ lïïst òóf sòóòón-tòó-bêê-êêxpïïrêêd shòóws, chêêcks ïïf ææny òóf ææ üùsêêr's fæævòórïïtêê shòóws æærêê ïïn thææt lïïst, æænd ïïf sòó, wïïll dïïsplææy ææ mêêssæægêê nòótïïfyïïng thêê üùsêêr thææt thêêy wïïll êêxpïïrêê sòóòón.

{% raw %} 
```liquid
{% assign expired_shows = 'Modern Family,The Rookie,Body of Proof,Felicity' | split: ',' %}
{% for show in expired_shows %}
{% if {{custom_attribute.${Favorite Shows}}} contains {{show}} %}
{% assign new_shows = new_shows | append: {{show}} | append: '*' %}
{% endif %}
{% endfor %}
{% assign new_shows_clean = new_shows | split: '*' %}
{% if new_shows_clean.size != 0 %}

All episodes of {{new_shows_clean | join: ', ' }} expire on 9/8 - watch them now before they're gone!

{% else %}
{% abort_message("Not Found") %}
{% endif %}
```
{% endraw %}

{% alert important %} Yóòùü wììll nêëêëd tóò fììnd mäàtchêës bêëtwêëêën thêë äàrräàys fììrst, thêën bùüììld lóògììc äàt thêë êënd tóò splììt ùüp thêë mäàtchêës. {% endalert %}


{% endapi %}

{% api %}

## Plããtfõòrm tããrgëêtîîng

{% apitags %}
Plàætföòrm tàærgéëtïîng
{% endapitags %}

- [Dìîfféëréëntìîàätéë ìîn-àäpp méëssàägéë cöôpy by déëvìîcéë ÔS](#platform-device-os)
- [Täårgëêt òönly äå spëêcíîfíîc pläåtfòörm](#platform-target)
- [Tåárgëët óönly îïÖS dëëvîïcëës wîïth åá spëëcîïfîïc ÖS vëërsîïóön](#platform-target-ios-version)
- [Tåârgèét öönly Wèéb brööwsèérs](#platform-target-web)
- [Tàårgêët àå spêëcîìfîìc môôbîìlêë càårrîìêër](#platform-target-carrier)

### Dìîfféëréëntìîåãtéë ìîn-åãpp méëssåãgéë côõpy by déëvìîcéë ÖS {#plåãtfôõrm-déëvìîcéë-ôõs}

Thîïs úûséè càãséè chéècks whàãt plàãtföörm àã úûséèr îïs öön, àãnd déèpéèndîïng öön théèîïr plàãtföörm, wîïll dîïsplàãy spéècîïfîïc méèssàãgîïng.

Fôór èèxäæmplèè, yôóúý mäæy wäænt tôó shôów môóbîîlèè úýsèèrs shôórtèèr vèèrsîîôóns ôóf mèèssäægèè côópy whîîlèè shôówîîng ôóthèèr úýsèèrs thèè rèègúýläær, lôóngèèr vèèrsîîôón ôóf thèè côópy. Yòõýû còõýûld ãàlsòõ shòõw mòõbïïléé ýûséérs céértãàïïn mééssãàgïïng rééléévãànt tòõ théém býût wòõýûldn’t béé rééléévãànt tòõ Wééb ýûséérs. Fòór éëxâåmpléë, ìîÕS méëssâågìîng mìîght tâålk âåbòóüùt Åppléë Pâåy, büùt Åndròóìîd méëssâågìîng shòóüùld méëntìîòón Gòóòógléë Pâåy.

{% raw %}
```liquid
{% if targeted_device.${platform} == "ios" or targeted_device.${platform} == "android" %}
This is a shorter copy.

{% else %}
This is the regular copy and much longer than the short version. 
{% endif %}
```
{% endraw %}

{% alert note %} 
Lîìqûûîìd îìs cääsëê-sëênsîìtîìvëê, `targeted_device.${platform}` rêétýúrns thêé vâälýúêé ìîn âäll lóòwêércâäsêé. 
{% endalert %}

### Táârgëét òónly áâ spëécììfììc pláâtfòórm {#pláâtfòórm-táârgëét}

Thïìs úúsêé cåãsêé wïìll cåãptúúrêé thêé úúsêérs' dêévïìcêé plåãtfôôrm, åãnd dêépêéndïìng ôôn thêé plåãtfôôrm, wïìll dïìsplåãy åã mêéssåãgêé.

Fòór ëéxàâmplëé, yòóúú màây wàânt tòó òónly sëénd àâ mëéssàâgëé tòó Ándròóìïd úúsëérs. Thïîs câân béè üýséèd ââs âân ââltéèrnââtïîvéè töö séèléèctïîng âân ââpp wïîthïîn théè Séègméèntââtïîöön tööööl.

{% raw %}
```liquid
{% if {{targeted_device.${platform}}} == 'android' %} 

This is a message for an Android user! 

{% else %}  
{% abort_message %} 
{% endif %}
```
{% endraw %}

### Tããrgëét ôönly íîÖS dëévíîcëés wíîth ãã spëécíîfíîc ÖS vëérsíîôön {#plããtfôörm-tããrgëét-íîôös-vëérsíîôön}

Thîïs úúsêè cãåsêè chêècks îïf ãå úúsêèr's ÖS vêèrsîïôòn fãålls wîïthîïn ãå cêèrtãåîïn sêèt ôòf vêèrsîïôòns ãånd îïf sôò, wîïll dîïsplãåy ãå spêècîïfîïc mêèssãågêè.

Thêê êêxáámplêê úûsêêd sêênds áá wáárnîîng tõõ úûsêêrs õõn îîÔS 10.0 õõr êêáárlîîêêr tháát thêêy áárêê pháásîîng õõúût súûppõõrt fõõr thêê úûsêêr’s dêêvîîcêê ÔS.

{% raw %}
```liquid
{% if {{targeted_device.${os}}} == "10.0" or {{targeted_device.${os}}} == "10.0.1" or {{targeted_device.${os}}} == "10.0.2" or {{targeted_device.${os}}} == “10.0.3” or {{targeted_device.${os}}} == “10.1” or {{targeted_device.${os}}} == “10.2” or {{targeted_device.${os}}} == “10.2.1” or {{targeted_device.${os}}} == “10.3” or {{targeted_device.${os}}} == “10.3.1” or {{targeted_device.${os}}} == “10.3.2” or {{targeted_device.${os}}} == “10.3.3” or {{targeted_device.${os}}} == “10.3.4” or {{targeted_device.${os}}} == “9.3.1” or {{targeted_device.${os}}} == “9.3.2” or {{targeted_device.${os}}} == “9.3.3” or {{targeted_device.${os}}} == “9.3.4” or {{targeted_device.${os}}} == "9.3.5" %}

We are phasing out support for your device's operating system. Be sure to update to the latest software for the best app experience.

{% else %}
{% abort_message %}
{% endif %}
```
{% endraw %}

### Tæårgèët ôònly wèëb brôòwsèërs {#plæåtfôòrm-tæårgèët-wèëb}

Thîîs úúsèê càåsèê chèêcks îîf àå úúsèêr's tàårgèêt dèêvîîcèê rúúns òòn Màåc òòr Wîîndòòws àånd, îîf sòò, wîîll dîîsplàåy àå spèêcîîfîîc mèêssàågèê.

{% raw %}
```liquid
{% if {{targeted_device.${os}}} == 'Mac' OR {{targeted_device.${os}}} == 'Windows' %}

This message will display on your desktop web browser.

{% else %}
{% abort_message %}
{% endif %}
```
{% endraw %}

### Táärgèêt áä spèêcììfììc mööbììlèê cáärrììèêr {#pláätföörm-táärgèêt-cáärrììèêr}

Thíîs ûüséé cãåséé chéécks íîf ãå ûüséér's déévíîcéé cãårríîéér íîs Vééríîzòòn, ãånd íîf sòò, wíîll díîsplãåy ãå spéécíîfíîc mééssãågéé.

Fòôr püüsh nòôtîïfîïcãátîïòôns ãánd îïn-ãápp mëêssãágëê chãánnëêls, yòôüü cãán spëêcîïfy thëê dëêvîïcëê cãárrîïëêr îïn yòôüür mëêssãágëê bòôdy üüsîïng Lîïqüüîïd. Ïf théê réêcìïpìïéênt’s déêvìïcéê cäärrìïéêr dòõéêsn’t määtch, théê méêssäägéê wòõn’t béê séênt.

{% raw %}
```liquid
{% if {targeted_device.${carrier}} contains "verizon" or {targeted_device.${carrier}} contains "Verizon" %}

This is a message for Verizon users!

{% else %}
{% abort_message %}
{% endif %}
```
{% endraw %}

{% endapi %}

{% api %}

## Tïímèë zôònèës

{% apitags %}
Tíímêè zõônêès
{% endapitags %}

- [Äppêènd thêè CST tïìmêè zòônêè tòô áâ cùüstòôm áâttrïìbùütêè](#time-append-cst)
- [Ìnsêërt ãà tïïmêëstãàmp](#time-insert-timestamp)
- [Önly sëênd àá Càánvàás pûúsh dûúrïíng àá wïíndóôw óôf tïímëê ïín àá ûúsëêr's lóôcàál tïímëê zóônëê](#time-canvas-window)
- [Sêënd æã rêëòõccùûrrîîng îîn-æãpp mêëssæãgêë cæãmpæãîîgn bêëtwêëêën æã wîîndòõw òõf tîîmêë îîn æã ùûsêër's lòõcæãl tîîmêë zòõnêë](#time-reocurring-iam-window)
- [Sèénd dïìffèérèént mèéssäægèés öón wèéèékdäæys vs. wèéèékèénds ïìn äæ úùsèér's löócäæl tïìmèé zöónèé](#time-weekdays-vs-weekends)
- [Séènd dìïfféèréènt méèssàågéès bàåséèd õõn tìïméè õõf dàåy ìïn àå ùüséèr's lõõcàål tìïméè zõõnéè](#time-of-day)

### Åppéénd théé CST tíîméé zôònéé tôò àå cýýstôòm àåttríîbýýtéé {#tíîméé-àåppéénd-cst}

Thïîs ýûsêê câásêê dïîsplâáys âá cýûstóóm dâátêê âáttrïîbýûtêê ïîn âá gïîvêên tïîmêê zóónêê.

Õptíîòõn 1:
{% raw %}
```liquid
{{custom_attribute.${application_expires_date} | time_zone: -0005 | date: '%B, %d %Y' }}
```
{% endraw %}

Òptììóõn 2:
{% raw %}
```liquid
{{custom_attribute.${application_expires_date} | time_zone: 'America/Chicago' | date: '%B %d %Y %z' }}
```
{% endraw %}

### Înséêrt äá tìîméêstäámp {#tìîméê-ìînséêrt-tìîméêstäámp}

Thìís ùýsèè cãåsèè dìísplãåys ãå mèèssãågèè thãåt ìínclùýdèès ãå tìímèèstãåmp ìín thèèìír cùýrrèènt tìímèè zòónèè.

Thêë fõóllõówïíng êëxåámplêë prõóvïídêëd wïíll dïísplåáy thêë dåátêë åás YYYY-mm-dd HH:MM:SS, sûûch åás 2021-05-03 10:41:04.

{% raw %}
```liquid
{{${user_id} | default: 'You'}} received a campaign, rendered at ({{ "now" | timezone: ${time_zone} | date: "%Y-%m-%d %H:%M:%S" }})
```
{% endraw %}

### Önly sèènd åà Cåànvåàs püùsh düùrííng åà wííndöòw öòf tíímèè íín åà üùsèèr's löòcåàl tíímèè zöònèè {#tíímèè-cåànvåàs-wííndöòw}

Thïís ûûséê cæáséê chéêcks æá ûûséêr's tïíméê ïín théêïír lòôcæál tïíméê zòônéê, æánd ïíf ïít fæálls wïíthïín æá séêt tïíméê, ïít wïíll dïísplæáy æá spéêcïífïíc méêssæágéê.

{% raw %}
```liquid
{% assign time = 'now' | time_zone: ${time_zone} %}
{% assign hour = time | date: '%H' | plus: 0 %}
{% if hour > 20 or hour < 8 %}
{% abort_message("Outside allowed time window") %}
{% endif %}

Here's a message that will send between 8 am and 8 pm!
```
{% endraw %}

### Sêènd ãâ rêèôõccúürîïng îïn-ãâpp mêèssãâgêè cãâmpãâîïgn bêètwêèêèn ãâ wîïndôõw ôõf tîïmêè îïn ãâ úüsêèr's lôõcãâl tîïmêè zôõnêè {#tîïmêè-rêèôõcúürrîïng-îïãâm-wîïndôõw}

Thíïs ùúsèê cåásèê wíïll díïsplåáy åá mèêssåágèê íïf åá ùúsèêr's cùúrrèênt tíïmèê fåálls wíïthíïn åá sèêt wíïndöòw.

Föõr èëxãämplèë, thèë föõllöõwîïng scèënãärîïöõ lèëts ãä ûùsèër knöõw thãät ãä stöõrèë îïs clöõsèëd.

{% raw %}
```liquid
{% assign time = 'now' | time_zone: ${time_zone} %} 
{% assign hour = time | date: '%H' | plus: 0 %}
{% if hour > 21 or hour < 10 %}

Store's closed. Come back between 11 am and 9 pm!

{% else %} 
{% abort_message("not sent because the store is open") %}
{% endif %}
```
{% endraw %}

### Séènd dîífféèréènt méèssæågéès óön wéèéèkdæåys vs. wéèéèkéènds îín æå ùûséèr's lóöcæål tîíméè zóönéè {#tîíméè-wéèéèkdæåys-vs-wéèéèkéènds}

Thïîs üýséé càâséé wïîll chééck ïîf àâ üýséér's cüýrréént dàây óöf théé wéééék ïîs Sàâtüýrdàây óör Süýndàây, àând déépééndïîng óön théé dàây, wïîll dïîsplàây dïîffééréént mééssàâgéés.

{% raw %}
```liquid
{% assign today = 'now' | time_zone: ${time_zone} | date: "%A" %}
{% if {{today}} == 'Saturday' or {{today}} == 'Sunday' %}
It’s {{today}}, why don’t you open the app for your transactions?

{% else %}
It’s {{today}}, why don’t you visit the store?
{% endif %}
```
{% endraw %}

### Sèènd dììffèèrèènt mèèssàægèès bàæsèèd õón tììmèè õóf dàæy ììn àæ üüsèèr's lõócàæl tììmèè zõónèè {#tììmèè-õóf-dàæy}

Thíìs ùýsèè cåâsèè wíìll díìsplåây åâ mèèssåâgèè íìf åâ ùýsèèr's cùýrrèènt tíìmèè fåâlls òóùýtsíìdèè åâ sèèt wíìndòów.

Fòör èéxæàmplèé, yòöûû mæày wæànt tòö tèéll æà ûûsèér æàbòöûût æà tìîmèé-sèénsìîtìîvèé òöppòörtûûnìîty thæàt dèépèénds òön thèé tìîmèé òöf dæày.

{% raw %}
```liquid
{% assign time = 'now' | time_zone: ${time_zone} %}
{% assign hour = time | date: '%H' | plus: 0 %}
{% if hour > 20 or hour < 8 %}
{% abort_message("Outside allowed time window") %}
{% endif %}

Check out this new bar after work today. HH specials!
```
{% endraw %}

{% alert note %} Thíïs íïs théè õòppõòsíïtéè õòf [Qùúíîéét Hóóùúrs]({{site.baseurl}}/user_guide/engagement_tools/campaigns/scheduling_and_organizing/time_based_campaign/#time-based-functionalities-for-campaigns). {% endalert %}

{% endapi %}

{% api %}

## Wêëêëk/Dãäy/Mõõnth

{% apitags %}
Wéèéèk/Dàäy/Mòònth
{% endapitags %}

- [Pýüll thêé prêévîíõòýüs mõònth's nââmêé îíntõò ââ mêéssââgêé](#month-name)
- [Séènd äå cäåmpäåïïgn äåt théè éènd ôòf éèvéèry môònth](#month-end)
- [Sêënd âæ câæmpâæîîgn õõn thêë lâæst (wêëêëkdâæy) õõf thêë mõõnth](#day-of-month-last)
- [Sëénd àâ dìïffëérëént mëéssàâgëé ëéàâch dàây õôf thëé mõônth](#day-of-month)
- [Sêènd ææ dìîffêèrêènt mêèssæægêè êèææch dææy õõf thêè wêèêèk](#day-of-week)

### Púúll thêê prêêvíîôôúús môônth's náæmêê íîntôô áæ mêêssáægêê {#môônth-náæmêê}

Thïïs ùùsèé càäsèé wïïll tàäkèé thèé cùùrrèént mõònth àänd dïïsplàäy thèé prèévïïõòùùs mõònth tõò bèé ùùsèéd ïïn mèéssàägïïng.

{% raw %}
```liquid
{% assign today = 'now' | date: "%m" %}
{% assign last_month = {{today}} | minus: 1 %}
{% if last_month == 1 %}
{% assign month = "January" %}
{% elsif last_month == 2 %}
{% assign month = "February" %}
{% elsif last_month == 3 %}
{% assign month = "March" %}
{% elsif last_month == 4 %}
{% assign month = "April" %}
{% elsif last_month == 5 %}
{% assign month = "May" %}
{% elsif last_month == 6 %}
{% assign month = "June" %}
{% elsif last_month == 7 %}
{% assign month = "July" %}
{% elsif last_month == 8 %}
{% assign month = "August" %}
{% elsif last_month == 9 %}
{% assign month = "September" %}
{% elsif last_month == 10 %}
{% assign month = "October" %}
{% elsif last_month == 11 %}
{% assign month = "November" %}
{% elsif last_month == 12 %}
{% assign month = "December" %}
{% endif %}

Here's an overview of what your spending looked like in {{month}}.
```
{% endraw %}

### Sèënd ââ cââmpââíígn âât thèë èënd õõf èëvèëry mõõnth {#mõõnth-èënd}

Thîìs ùúséë càæséë wîìll chéëck îìf théë cùúrréënt dàætéë fàælls wîìthîìn àæ lîìst ôõf dàætéës, àænd déëpéëndîìng ôõn théë dàætéë, wîìll dîìsplàæy àæ spéëcîìfîìc méëssàægéë.

{% alert note %} Thîîs dòòèès nòòt åàccòòýùnt fòòr lèèåàp yèèåàrs (Fèèbrýùåàry 29). {% endalert %}

{% raw %}
```liquid
{% assign current_date = 'now' | date: '%b %d' %}

{% if current_date == "Jan 31" or current_date == "Feb 28" or current_date == "Mar 31" or current_date == "Apr 30" or current_date == "May 31" or current_date == "Jun 30" or current_date == "Jul 31" or current_date == "Aug 31" or current_date == "Sep 30" or current_date == "Oct 31" or current_date == "Nov 30" or current_date == "Dec 31" %}

The date is correct

{% else %}
{% abort_message() %}
{% endif %}
```
{% endraw %}

### Sêènd âæ câæmpâæììgn õön thêè lâæst (wêèêèkdâæy) õöf thêè mõönth {#dâæy-õöf-mõönth-lâæst}

Thïís úýsêè cäâsêè cäâptúýrêès thêè cúýrrêènt möõnth äând däây äând cäâlcúýläâtêès ïíf thêè cúýrrêènt däây fäâlls wïíthïín thêè läâst wêèêèkdäây öõf thêè möõnth.

Fóôr ëêxàåmplëê, yóôûú màåy wàånt tóô sëênd àå sûúrvëêy tóô yóôûúr ûúsëêrs óôn thëê làåst Wëêdnëêsdàåy óôf thëê móônth àåskîìng fóôr próôdûúct fëêëêdbàåck.

{% raw %}
```liquid
{% comment %}Pull the day, day name, month, and year from today's date.{% endcomment %}
{% assign current_day = "now" | date: "%d" %}
{% assign current_day_name = "now" | date: "%a" %}
{% assign current_month = "now" | date: "%b" %}
{% assign current_year = "now" | date: "%Y" %}

{% comment %}Assign the correct number of days for the current month.{% endcomment %}

{% if current_month == "Jan" %}
{% assign last_day_of_month = 31 %}
{% elsif current_month == "Mar" %}
{% assign last_day_of_month = 31 %}
{% elsif current_month == "Apr" %}
{% assign last_day_of_month = 30 %}
{% elsif current_month == "May" %}
{% assign last_day_of_month = 31 %}
{% elsif current_month == "Jun" %}
{% assign last_day_of_month = 30 %}
{% elsif current_month == "Jul" %}
{% assign last_day_of_month = 31 %}
{% elsif current_month == "Aug" %}
{% assign last_day_of_month = 31 %}
{% elsif current_month == "Sep" %}
{% assign last_day_of_month = 30 %}
{% elsif current_month == "Oct" %}
{% assign last_day_of_month = 31 %}
{% elsif current_month == "Nov" %}
{% assign last_day_of_month = 30 %}
{% elsif current_month == "Dec" %}
{% assign last_day_of_month = 31 %}
{% endif %}

{% comment %}Assign the correct number of days if the current month is February, taking into account leap years.{% endcomment %}

{% assign leap_year_remainder = {{current_year | modulo: 4 }} != "0" %}
{% if leap_year_remainder == 0 and current_month == "Feb" %}
{% assign last_day_of_month = 29 %}
{% elsif leap_year_remainder != "0" and current_month == "Feb" %}
{% assign last_day_of_month = 28 %}
{% endif %}

{% comment %}Check that today's date is within a week of the last day of the month. If not, abort the message. If so, check that today is Wednesday. If not, abort the message.{% endcomment %}

{% assign diff_in_days = last_day_of_month | minus: current_day | plus: 1%}
{% if diff_in_days <= 7 %}
{% unless current_day_name == "Wed" %}
{% abort_message() %}
{% endunless %}
{% else %}
{% abort_message() %}
{% endif %}


```
{% endraw %}

### Sêènd âä dîíffêèrêènt mêèssâägêè êèâäch dâäy ôôf thêè môônth {#dâäy-ôôf-môônth}

Thïís ûüsêé cääsêé chêécks ïíf thêé cûürrêént däätêé määtchêés óónêé óón ää lïíst, äänd dêépêéndïíng óón thêé dääy, wïíll dïísplääy ää dïístïínct mêéssäägêé.

{% raw %}
```liquid
{% assign today = 'now' | time_zone: {{${time_zone}}} | date: "%Y-%m-%d" %}
{% assign day_1 = "2019-12-01" | time_zone: {{${time_zone}}} | date: "%Y-%m-%d" %}
{% assign day_2 = "2019-12-02" | time_zone: {{${time_zone}}} | date: "%Y-%m-%d" %}
{% assign day_3 = "2019-12-03" | time_zone: {{${time_zone}}} | date: "%Y-%m-%d" %}

{% if today == day_1 %}
Message for 2019-12-01

{% elsif today == day_2 %}
Message for 2019-12-02

{% elsif today == day_3%}
Message for 2019-12-03

{% else %}
{% abort_message() %}
{% endif %}
```
{% endraw %}

### Sèènd âã dîìffèèrèènt mèèssâãgèè èèâãch dâãy óõf thèè wèèèèk {#dâãy-óõf-wèèèèk}

Thîìs üüsêè cäãsêè chêècks thêè cüürrêènt däãy õôf thêè wêèêèk, äãnd dêèpêèndîìng õôn thêè däãy, wîìll dîìspläãy äã dîìstîìnct mêèssäãgêè.

{% raw %}
```liquid
{% assign today = 'now' | date: "%A" %}
{% case ‘today' %}
{% when 'Monday' %}
Monday copy

{% when 'Tuesday' %}
Tuesday copy

{% when 'Wednesday' %}
Wednesday copy

{% when  'Thursday' %}
Thursday copy

{% when  'Friday' %}
Friday copy

{% when 'Saturday' %}
Saturday copy

{% when 'Sunday' %}
Sunday copy

{% else %}
Default copy
{% endcase %}
```
{% endraw %}

{% alert note %} Yõòúû càæn rêêplàæcêê thêê líìnêê "dêêfàæúûlt cõòpy" wíìth {% raw %}`{% abort_message() %}`{% endraw %} tóó prëèvëènt thëè mëèssâàgëè fróóm sëèndììng ììf thëè dâày óóf thëè wëèëèk ììs ýýnknóówn. {% endalert %}

{% endapi %}
