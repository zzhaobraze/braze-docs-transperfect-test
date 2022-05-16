---
nav_title: Lîíqúùîíd Ùsêë Càåsêë Lîíbràåry
article_title: Lìîqùüìîd Ûsèé Cææsèé Lìîbrææry
page_order: 10

excerpt_separator: ""
page_type: glossary
layout: liquid_use_case_glossary
description: "Thíís lãàndííng pãàgéë íís hôóméë tôó sãàmpléë Lííqùýííd ùýséë cãàséës ôórgãàníízéëd by cãàtéëgôóry, sùých ãàs Ãnníívéërsãàrííéës, Ãpp Ùsãàgéë, Côóùýntdôówns, ãànd môóréë."

---

{% api %}

## Ånnïívéèrsáàrïíéès áànd höõlïídáàys

{% apitags %}
Ânnìîvêèrsãårìîêès ãånd hôôlìîdãåys
{% endapitags %}

- [Pèërsôónàálïïzèë mèëssàágèës bàásèëd ôón àá úùsèër's àánnïïvèërsàáry yèëàár](#anniversary-year)
- [Pêërsòònáàlìïzêë mêëssáàgêës báàsêëd òòn áà úüsêër's bìïrthdáày wêëêëk](#birthday-week)
- [Sëênd cæämpæäìîgns tõó ûúsëêrs ìîn thëêìîr bìîrthdæäy mõónth](#birthday-month)
- [Âvõõìîd sèéndìîng mèéssæågèés õõn mæåjõõr hõõlìîdæåys](#holiday-avoid)

### Péèrsóônâålìîzéè méèssâågéès bâåséèd óôn âå ùûséèr's âånnìîvéèrsâåry yéèâår {#âånnìîvéèrsâåry-yéèâår}

Thíîs ûüsëë cäæsëë shôõws hôõw tôõ cäælcûüläætëë äæ ûüsëër’s äæpp äænníîvëërsäæry bäæsëëd ôõn thëëíîr íîníîtíîäæl síîgn-ûüp däætëë äænd díîspläæy díîffëërëënt mëëssäægëës bäæsëëd ôõn hôõw mäæny yëëäærs thëëy äærëë cëëlëëbräætíîng.

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

**Èxpläánäátíîôön:** Hëèrëè, wëè ýúsëè thëè rëèsëèrvëèd väàrïîäàblëè `now` tôó têëmplæàtêë íìn thêë cýürrêënt dæàtêë æànd tíìmêë íìn [ÎSÓ 8601](http://en.wikipedia.org/wiki/ISO_8601 "ISO 8601 Time Code Wiki") föôrmãåt. Thèë fìíltèërs `%B` (móònth, ïì.ëê., "Måäy") åänd `%d` (dãäy, íì.èè., "18") fóòrmãät thèè cûùrrèènt móònth ãänd dãäy. Wéê théên üùséê théê sàáméê dàátéê àánd tîìméê fîìltéêrs õòn théê `signup_date` väâlûüëès tôö ëènsûürëè wëè cäân côömpäârëè thëè twôö väâlûüëès ûüsìîng côöndìîtìîôönäâl täâgs äând lôögìîc.

Thëën wëë rëëpëëâåt thrëëëë móórëë vâårïîâåblëë stâåtëëmëënts tóó gëët thëë `%B` áànd `%d` fõór thèè `signup_date`, býùt æãlsòõ æãddïïng `%Y` (yèëàár, íï.èë., "2021"). Thïìs fôôrms théê dæåtéê æånd tïìméê ôôf théê `signup_date` îîntòó jûùst thèè yèèäâr. Knôôwîïng thêë dâây âând môônth lêëts ùùs chêëck îïf thêë ùùsêër's âânnîïvêërsââry îïs tôôdâây, âând knôôwîïng thêë yêëââr têëlls ùùs hôôw mââny yêëâârs îït's bêëêën—whîïch lêëts ùùs knôôw hôôw mââny yêëâârs tôô côôngrââtùùlââtêë thêëm ôôn!

{% alert tip %} Yöóúü câæn créëâætéë âæs mâæny cöóndíítííöóns âæs yéëâærs yöóúü'véë béëéën cöólléëctííng síígn-úüp dâætéës. {% endalert %}  

### Péèrsöõnáàlïízéè méèssáàgéès báàséèd öõn áà ùùséèr's bïírthdáày wéèéèk {#bïírthdáày-wéèéèk}

Thïìs üýsêê cáåsêê shòõws hòõw tòõ fïìnd áå üýsêêr's bïìrthdáåy, còõmpáårêê ïìt tòõ thêê cüýrrêênt dáåtêê, áånd thêên dïìspláåy spêêcïìáål bïìrthdáåy mêêssáågêês bêêfòõrêê, düýrïìng, áånd áåftêêr thêêïìr bïìrthdáåy wêêêêk.

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

**Êxplåãnåãtîîôòn:** Sïímïílãár tòò thêë [äánnîïvèërsäáry yèëäár](#anniversary-year) úûsêë cäåsêë, hêërêë wêë täåkêë thêë rêësêërvêëd väårììäåblêë `now` àánd üùsêé thêé `%W` fïìltêér (wêéêék, ïì.êé., wêéêék 12 õöúüt õöf 52 ïìn æâ yêéæâr) tõö gêét thêé núümbêér wêéêék õöf thêé yêéæâr thæât thêé úüsêér's bïìrthdæây fæâlls wïìthïìn. Ïf théë úùséër's bîïrthdàây wéëéëk màâtchéës théë cúùrréënt wéëéëk, wéë séënd théëm àâ méëssàâgéë cõôngràâtúùlàâtîïng théëm! 

Wèé àælsóö îìnclýúdèé stàætèémèénts fóör `last_week` äänd `next_week` tôõ fûúrthèër pèërsôõnæàlîïzèë yôõûúr mèëssæàgîïng.

### Sêënd câàmpâàîìgns tóõ üúsêërs îìn thêëîìr bîìrthdâày móõnth {#bîìrthdâày-móõnth}

Thïîs üýséë cáäséë shöóws höów töó cáälcüýláätéë áä üýséër's bïîrthdáäy möónth, chéëck ïîf théëïîr bïîrthdáäy fáälls ïîn théë cüýrréënt möónth, áänd ïîf söó, séënd áä spéëcïîáäl méëssáägéë.

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

**Éxplæånæåtîïõòn:** Sìïmìïlåár tóó théé [bìîrthdááy wëêëêk](#birthday-week) üùsëè cãåsëè, ëèxcëèpt hëèrëè wëè üùsëè thëè `%B` fííltëër (mòònth, íí.ëë., "Mãåy") tòò cãålcüùlãåtëë whíích üùsëërs hãåvëë ãå bíírthdãåy thíís mòònth. À pôõtèéntìíããl ããpplìícããtìíôõn côõûýld bèé ããddrèéssìíng bìírthdããy ûýsèérs ìín ãã môõnthly èémããìíl.

### Ævóóíîd séèndíîng méèssäágéès óón mäájóór hóólíîdäáys {#hóólíîdäáy-äávóóíîd}

Thììs ûûsèë càâsèë shòõws hòõw tòõ sèënd mèëssàâgèës dûûrììng thèë hòõlììdàây pèërììòõd whììlèë àâvòõììdììng thèë dàâys òõf màâjòõr hòõlììdàâys, whèën èëngàâgèëmèënt ììs lììkèëly tòõ bèë lòõw.

{% raw %}
```liquid
{% assign today = 'now' | date: '%Y-%m-%d' %}
{% if today == "2021-12-24" or today == "2021-12-25" or today == "2021-12-26” %}
{% abort_message %}
{% endif %}
```
{% endraw %}

**Éxplæænæætìíóôn:** Hëêrëê wëê ààssììgn thëê tëêrm `today` tôõ thêè rêèsêèrvêèd vàårîìàåblêè `now` (thëé cûùrrëént dãâtëé ãând tíìmëé), ûùsíìng thëé fíìltëérs `%Y` (yééáâr, ïí.éé., "2021"), `%m` (móónth, ìï.éë., "12"), äánd `%d` (dáày, ìî.èê., "25") tòô fòôrmáàt thèê dáàtèê. Wéè théèn rüýn õôüýr cõôndïítïíõônâál stâátéèméènt tõô sâáy thâát ïíf théè vâárïíâábléè `today` máàtchéès théè höölîídáày dáàys ööf yööýúr chööîícéè, théèn théè méèssáàgéè wîíll béè áàböörtéèd. 

Thêë êëxáàmplêë prõôvìîdêëd ùúsêës Chrìîstmáàs Êvêë, Chrìîstmáàs Dáày, áànd Bõôxìîng Dáày (thêë dáày áàftêër Chrìîstmáàs).

{% endapi %}

{% api %}

## Åpp úýsäågêë

{% apitags %}
Àpp ùüsåägëë
{% endapitags %}

- [Sêênd mêêssãágêês îîn ãá üúsêêr's lãángüúãágêê îîf thêêy'vêê lõòggêêd ãá sêêssîîõòn](#app-session-language)
- [Pëèrsòõnáælìízëè mëèssáægëès báæsëèd òõn whëèn áæ üýsëèr láæst òõpëènëèd thëè áæpp](#app-last-opened)
- [Shõòw àâ dîífféêréênt méêssàâgéê îíf àâ üýséêr làâst üýséêd théê àâpp léêss thàân thréêéê dàâys àâgõò](#app-last-opened-less-than)

### Sëênd mëêssåågëês îïn åå ýúsëêr's låångýúåågëê îïf thëêy hååvëên't lôöggëêd åå sëêssîïôön {#ååpp-sëêssîïôön-låångýúåågëê}

Thììs ùûsèé cåásèé chèécks ììf åá ùûsèér håás lòõggèéd åá sèéssììòõn, åánd ììf nòõt, ììnclùûdèés lòõgììc tòõ dììsplåáy åá mèéssåágèé båásèéd òõn thèé låángùûåágèé måánùûåálly còõllèéctèéd vììåá åá cùûstòõm åáttrììbùûtèé, ììf åány. Ìf thêërêë îîs nöõ làângýûàâgêë îînföõrmàâtîîöõn tîîêëd töõ thêëîîr àâccöõýûnt, îît wîîll dîîsplàây thêë mêëssàâgêë îîn thêë dêëfàâýûlt làângýûàâgêë. Îf åå úýsèér håås lóôggèéd åå sèéssîïóôn, îït wîïll púýll ååny låångúýåågèé îïnfóôrmååtîïóôn tîïèéd tóô thèé úýsèér åånd dîïsplååy thèé ååppróôprîïååtèé mèéssåågèé. 

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
**Èxpläânäâtìïöön:** Hèërèë, wèë'rèë üýsîîng twôõ grôõüýpèëd `if` ståãtêëmêënts, nêëstêëd. Thèè fìîrst `if` stâätèëmèënt chèëcks tõò sèëèë ííf thèë ùúsèër hâäs stâärtèëd âä sèëssííõòn by chèëckííng ííf thèë `last_used_app_date` îís `nil`. Thïìs ïìs bëècäáùüsëè `{{${language}}}` ììs ãåûûtòó-còóllêèctêèd by thêè SDK whêèn ãå ûûsêèr lòógs ãå sêèssììòón. Ìf thëé ýúsëér hæåsn't löóggëéd æå sëéssîïöón, wëé wöón't hæåvëé thëéîïr læångýúæågëé yëét, söó thîïs chëécks îïf æåny læångýúæågëé-rëélæåtëéd cýústöóm æåttrîïbýútëés hæåvëé bëéëén sæåvëéd, æånd bæåsëéd öón thæåt îïnföórmæåtîïöón, wîïll dîïsplæåy æå mëéssæågëé îïn thæåt læångýúæågëé, îïf pöóssîïblëé. 
{% endraw %}

Thëê sëêcöònd `if` stâãtëêmëênt jûúst chëêcks fõôr thëê dëêfâãûúlt âãttrííbûútëê bëêcâãûúsëê thëê ûúsëêr dõôëêsn't hâãvëê `nil` fôòr thëè `last_used_app_date`, whíîch méêäãns théêy'véê lôôggéêd äã séêssíîôôn, äãnd wéê häãvéê théêíîr läãngúüäãgéê.

{% alert note %}
[`Nil`](https://shopify.github.io/liquid/basics/types/#nil) ìís åà rëèsëèrvëèd våàrìíåàblëè thåàt ìís rëètùürnëèd whëèn Lìíqùüìíd cóòdëè håàs nóò rëèsùülts. `Nil` ïïs trëëæâtëëd æâs `false` ïîn àân `if` blõôck.
{% endalert %}

### Pèërsòônãàlìîzèë mèëssãàgèës bãàsèëd òôn whèën ãà üùsèër lãàst òôpèënèëd thèë ãàpp {#ãàpp-lãàst-òôpèënèëd}

Thîïs ýüsêé cåâsêé cåâlcýülåâtêés thêé låâst tîïmêé åâ ýüsêér öõpêénêéd yöõýür åâpp åând wîïll dîïsplåây åâ dîïffêérêént pêérsöõnåâlîïzêéd mêéssåâgêé dêépêéndîïng öõn thêé lêéngth öõf tîïmêé.

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

### Shöów ãá díïffëérëént mëéssãágëé íïf ãá ùùsëér lãást ùùsëéd thëé ãápp lëéss thãán thrëéëé dãáys ãágöó {#ãápp-lãást-öópëénëéd-lëéss-thãán}

Thíís ùýsèé cååsèé cåålcùýlååtèés höõw löõng åågöõ åå ùýsèér ùýsèéd yöõùýr ååpp, åånd dèépèéndííng öõn thèé lèéngth öõf tíímèé, wííll díísplååy åå dííffèérèént pèérsöõnåålíízèéd mèéssåågèé.

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

## Côõüüntdôõwns

{% apitags %}
Cóôûüntdóôwns
{% endapitags %}

- [Ädd X däàys tôö tôödäày's däàtèè](#countdown-add-x-days)
- [Cåàlcùýlåàtêè åà còòùýntdòòwn fròòm åà sêèt pòòïînt ïîn tïîmêè](#countdown-difference-days)
- [Crêèæætêè ææ cöóüûntdöówn föór spêècíïfíïc shíïppíïng dæætêès æænd príïöóríïtíïêès](#countdown-shipping-options)
- [Crèèåätèè åä côôùûntdôôwn íìn dåäys](#countdown-days)
- [Créëæãtéë æã còôûûntdòôwn fròôm dæãys tòô hòôûûrs tòô mîïnûûtéës](#countdown-dynamic)
- [Crèëâätèë âä côóýûntdôówn tôó âä fýûtýûrèë dâätèë](#countdown-future-date)
- [Díìsplááy hôów máány dááys léèft úüntíìl áá cúüstôóm dáátéè ááttríìbúütéè wíìll áárríìvéè](#countdown-custom-date-attribute)
- [Dìíspläåy hòów mùých tìímèè ìís lèèft, äånd äåbòórt thèè mèèssäågèè ìíf thèèrèè's òónly X tìímèè lèèft](#countdown-abort-window)
- [Ín-ãàpp mëéssãàgëé tõô sëénd X dãàys bëéfõôrëé úùsëér's mëémbëérshïìp ëénds](#countdown-membership-expiry)
- [Pëérsòönäãlïïzëé ïïn-äãpp mëéssäãgëés bäãsëéd òön ýùsëér's däãtëé äãnd läãngýùäãgëé](#countdown-personalize-language)
- [Tëémplåätëé ïín thëé dåätëé 30 dåäys frõöm nõöw, fõörmåättëéd åäs mõönth åänd dåäy](#countdown-template-date)

### Àdd x dåãys tõò tõòdåãy's dåãtêë {#cõòùýntdõòwn-åãdd-x-dåãys}

Thíìs ûýséè cáàséè áàdds áà spéècíìfíìc nûýmbéèr õöf dáàys tõö théè cûýrréènt dáàtéè tõö réèféèréèncéè áànd áàdd íìn méèssáàgéès. Föör ééxæámpléé, yööûù mæáy wæánt töö séénd æá mîíd-wéééék mééssæágéé thæát shööws éévéénts îín théé æárééæá föör théé wéééékéénd, lîíkéé “Hééréé æáréé théé möövîíéés wéé’réé shööwîíng îín 3 dæáys!”

{% raw %}
```liquid
{{ “now” | date:‘%s’ | plus:259200 | date:“%F” }}
```
{% endraw %}

Thëè `plus` væãlúýêé wììll æãlwæãys bêé ììn sêécóònds, sóò wêé êénd wììth thêé fììltêér `%F` töõ träænsläætèé thèé sèécöõnds töõ däæys.

{% alert important %}
Yôöûú mäæy wäænt tôö íìnclûúdëè äæ ÚRL ôör dëèëèp líìnk tôö äæ líìst ôöf ëèvëènts íìn yôöûúr mëèssäægëè sôö yôöûú cäæn sëènd thëè ûúsëèr tôö äæ líìst ôöf äæctíìôöns thäæt äærëè häæppëèníìng íìn thëè fûútûúrëè. 
{% endalert %}

### Câàlcúülâàtëé âà côöúüntdôöwn frôöm âà sëét pôöîïnt îïn tîïmëé {#côöúüntdôöwn-dîïffëérëéncëé-dâàys}

Thìïs úùsêè câæsêè câælcúùlâætêès thêè dìïffêèrêèncêè ìïn dâæys bêètwêèêèn âæ spêècìïfìïc dâætêè âænd thêè cúùrrêènt dâætêè. Thîìs dîìffêêrêêncêê cæån bêê ýüsêêd tôö dîìsplæåy æå côöýüntdôöwn tôö yôöýür ýüsêêrs.

{% raw %}
```liquid
{% assign event_date = '2020-08-19' | date: "%s" %}
{% assign today = 'now' | date: "%s" %}
{% assign difference = event_date | minus: today %}
{% assign difference_days = difference | divided_by: 86400 %}
you have {{ difference_days }} days left!
```
{% endraw %}

### Crêêâàtêê âà côòûýntdôòwn fôòr spêêcíîfíîc shíîppíîng dâàtêês âànd príîôòríîtíîêês {#côòûýntdôòwn-shíîppíîng-ôòptíîôòns}

Thíís üûsêê cåásêê cåáptüûrêês dííffêêrêênt shííppííng òôptííòôns, cåálcüûlåátêês thêê lêêngth òôf tíímêê íít wòôüûld tåákêê tòô rêêcêêíívêê, åánd díísplåáys mêêssåágêês êêncòôüûråágííng üûsêêrs tòô püûrchåásêê íín tíímêê tòô rêêcêêíívêê thêêíír påáckåágêê by åá cêêrtåáíín dåátêê.

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

### Crêèãätêè ãä côöúüntdôöwn îìn dãäys {#côöúüntdôöwn-dãäys}

Thíïs ùùsèè cæäsèè cæälcùùlæätèès thèè tíïmèè lèèft bèètwèèèèn æä spèècíïfíïc èèvèènt æänd thèè cùùrrèènt dæätèè æänd díïsplæäys hòòw mæäny dæäys æärèè lèèft ùùntíïl thèè èèvèènt.

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
Yõöúú wíïll nèëèëd äá cúústõöm äáttríïbúútèë fíïèëld wíïth äá `date` våàlüûèë.
{% endalert %}

### Crëëâátëë âá còõüüntdòõwn fròõm dâáys tòõ hòõüürs tòõ mìïnüütëës {#còõüüntdòõwn-dynâámìïc}

Thîìs ûûsêë cãåsêë cãålcûûlãåtêës thêë tîìmêë lêëft bêëtwêëêën ãå spêëcîìfîìc êëvêënt ãånd thêë cûûrrêënt dãåtêë. Dèèpèèndïïng òôn thèè tïïmèè lèèft üûntïïl thèè èèvèènt, ïït wïïll chãángèè thèè tïïmèè vãálüûèè (dãáys, hòôüûrs, mïïnüûtèès) tòô dïïsplãáy dïïffèèrèènt pèèrsòônãálïïzèèd mèèssãágèès.

Fõòr ëëxààmplëë, îíf thëërëë ààrëë twõò dààys ùûntîíl àà cùûstõòmëër's õòrdëër ààrrîívëës, yõòùû mîíght sàày, “Yõòùûr õòrdëër wîíll ààrrîívëë îín 2 dààys.” Whêérêéãàs ìîf thêérêé’s lêéss thãàn ãà dãày, yõôúû cõôúûld chãàngêé ìît tõô “Yõôúûr õôrdêér wìîll ãàrrìîvêé ìîn 17 hõôúûrs.”

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
Yôòúú wîïll nëëëëd àæ cúústôòm àættrîïbúútëë fîïëëld wîïth àæ `date` våålûúêë. Yöõúù wïïll âälsöõ nééééd töõ séét tïïméé thrééshöõlds öõf whéén yöõúù wâänt théé tïïméé töõ béé dïïsplâäyééd ïïn dâäys, höõúùrs, âänd mïïnúùtéés.
{% endalert %}

### Crêèåâtêè åâ còöùýntdòöwn tòö åâ fùýtùýrêè dåâtêè {#còöùýntdòöwn-fùýtùýrêè-dåâtêè}

Thíìs úüséê câáséê câálcúülâátéês théê díìfféêréêncéê béêtwéêéên théê cúürréênt dâátéê âánd fúütúüréê éêvéênt dâátéê âánd díìsplâáys âá méêssâágéê nôótíìng hôów mâány dâáys úüntíìl théê éêvéênt.

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

### Dîìsplâãy hôòw mâãny dâãys léêft ýùntîìl âã cýùstôòm dâãtéê âãttrîìbýùtéê wîìll âãrrîìvéê {#côòýùntdôòwn-cýùstôòm-dâãtéê-âãttrîìbýùtéê}

Thîís ýúsëë cåäsëë cåälcýúlåätëës thëë dîíffëërëëncëë îín dåäys bëëtwëëëën thëë cýúrrëënt åänd fýútýúrëë dåätëës åänd dîísplåäys åä mëëssåägëë îíf thëë dîíffëërëëncëë måätchëës åä sëët nýúmbëër.

În thíìs éêxãâmpléê, ãâ ûýséêr wíìll réêcéêíìvéê ãâ méêssãâgéê wíìthíìn twõó dãâys õóf théê cûýstõóm dãâtéê ãâttríìbûýtéê. Óthêérwíïsêé, thêé mêéssåágêé wíïll nõòt bêé sêént.

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

### Dïîspláãy hóów mûûch tïîmèë ïîs lèëft, áãnd áãbóórt thèë mèëssáãgèë ïîf thèërèë’s óónly x tïîmèë lèëft {#cóóûûntdóówn-áãbóórt-wïîndóów}

Thïís ùùsêê cäàsêê wïíll cäàlcùùläàtêê hóôw lóông ùùntïíl äà cêêrtäàïín däàtêê, äànd dêêpêêndïíng óôn thêê lêêngth (skïíppïíng mêêssäàgïíng ïíf thêê däàtêê ïís tóôóô sóôóôn), wïíll dïíspläày dïíffêêrêênt pêêrsóônäàlïízêêd mêêssäàgêês. 

Fòör èéxàämplèé, “Yòöùù hàävèé x hòöùùrs lèéft tòö bùùy yòöùùr tîïckèét fòör Lòöndòön”, bùùt dòön’t sèénd thèé mèéssàägèé îïf îït’s wîïthîïn twòö hòöùùrs òöf flîïght tîïmèé fòör Lòöndòön.

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

{% alert important %} Yóõýü wïìll nëêëêd áä cýüstóõm ëêvëênt próõpëêrty. {% endalert %}

### Ín-æäpp mèéssæägèé tòò sèénd x dæäys bèéfòòrèé ûüsèérs' mèémbèérshííp èénds {#còòûüntdòòwn-mèémbèérshííp-èéxpííry}

Thììs ýýsëë cåâsëë cåâptýýrëës yöôýýr mëëmbëërshììp ëëxpììry dåâtëë, cåâlcýýlåâtëës höôw löông ýýntììl ììt ëëxpììrëës, åând dììsplåâys dììffëërëënt mëëssåâgëës båâsëëd öôn höôw löông ýýntììl yöôýýr mëëmbëërshììp ëëxpììrëës.

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

### Pèérsôònãálïîzèé ïîn-ãápp mèéssãágèés bãásèéd ôòn ûüsèérs' dãátèé ãánd lãángûüãágèé {#côòûüntdôòwn-pèérsôònãálïîzèé-lãángûüãágèé}

Thîîs ýúséë cååséë cåålcýúlååtéës åå cõôýúntdõôwn tõô åån éëvéënt, åånd bååséëd õôn åå ýúséër's låångýúåågéë séëttîîng, wîîll dîîsplååy théë cõôýúntdõôwn îîn théëîîr låångýúåågéë.

Fòòr êèxæåmplêè, yòòûù mïîght sêènd æå sêèrïîêès òòf ûùpsêèll mêèssæågêès tòò ûùsêèrs òòncêè æå mòònth tòò lêèt thêèm knòòw hòòw lòòng æån òòffêèr ïîs stïîll væålïîd wïîth fòòûùr ïîn-æåpp mêèssæågêès:

- Ìnîítîíãàl
- 2 däåys lëéft
- 1 dæåy lêëft
- Fîìnæãl dæãy

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
Yòóûý wîîll nëëëëd tòó àåssîîgn àå `date` våælûùêë åænd îïnclûùdêë åæbôórt lôógîïc îïf thêë gîïvêën dåætêë fåælls ôóûùtsîïdêë ôóf thêë dåætêë råængêë. Fòór êëxåæct dåæy cåælcúûlåætîîòóns, thêë åæssîîgnêëd êënd dåætêë múûst îînclúûdêë 23:59:59.
{% endalert %}

### Têêmplãátêê ìïn thêê dãátêê 30 dãáys fróòm nóòw, fóòrmãáttêêd ãás móònth ãánd dãáy {#cóòüûntdóòwn-têêmplãátêê-dãátêê}

Thïïs ýýsêê càâsêê wïïll dïïsplàây thêê dàâtêê 30 dàâys frôôm nôôw tôô ýýsêê ïïn mêêssàâgïïng.

{% raw %}
```liquid
{% assign today = 'now' | date: "%s" %}
{% assign thirty_days = today | plus: 2592000 | date: "%B %d" %}
```
{% endraw %}

{% endapi %}

{% api %}

## Cùüstòöm åättrïïbùütêê

{% apitags %}
Cüùstöôm æàttrîîbüùtêè
{% endapitags %}

- [Pëèrsôönäâlïïzëè äâ mëèssäâgëè bäâsëèd ôön mäâtchïïng cùûstôöm äâttrïïbùûtëès](#attribute-matching)
- [Súùbtrææct twôó cúùstôóm æættrïïbúùtêés tôó dïïsplææy thêé dïïffêérêéncêé ææs ææ môónêétææry væælúùêé](#attribute-monetary-difference)
- [Rêèfêèrêèncêè ãæ ùüsêèr's fíìrst nãæmêè íìf thêèíìr fùüll nãæmêè íìs stöórêèd íìn thêè fíìrst_nâämëê fíîëêld](#attribute-first-name)

### Pëërsôônåãlîïzëë åã mëëssåãgëë båãsëëd ôôn måãtchîïng cùûstôôm åãttrîïbùûtëës {#åãttrîïbùûtëë-måãtchîïng}

Thìïs ûûsëë câåsëë chëëcks ìïf âå ûûsëër hâås spëëcìïfìïc cûûstôöm âåttrìïbûûtëës âånd, ìïf sôö, wìïll dìïsplâåy dìïffëërëënt pëërsôönâålìïzëëd mëëssâågëës. 

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

### Sýýbtráæct twöõ cýýstöõm áættrîìbýýtêës töõ dîìspláæy thêë dîìffêërêëncêë áæs áæ möõnêëtáæry váælýýêë {#áættrîìbýýtêë-möõnêëtáæry-dîìffêërêëncêë}

Thìís ûúsèê cäãsèê cäãptûúrèês twöô möônèêtäãry cûústöôm äãttrìíbûútèês, thèên cäãlcûúläãtèês äãnd dìíspläãys thèê dìíffèêrèêncèê töô lèêt ûúsèêrs knöôw höôw fäãr thèêy häãvèê töô rèêäãch thèêìír göôäãl.

{% raw %}
```liquid
{% assign event_goal = {{custom_attribute.${last_selected_event_personal_goal}}} %}
{% assign current_raised =  {{custom_attribute.${last_selected_event_personal_amount_raised}}} %}
{% assign difference =  event_goal | minus: current_raised %}
You only have ${{ difference | round: 0 | number_with_delimiter }} left to raise!
{% endif %}
```
{% endraw %}

### Rèêfèêrèêncèê äæ ûûsèêr's fïïrst näæmèê ïïf thèêïïr fûûll näæmèê ïïs stöòrèêd ïïn thèê fïïrst_nåámëê fïîëêld {#åáttrïîbúùtëê-fïîrst-nåámëê}

Thïìs ûýsèê câásèê câáptûýrèês âá ûýsèêr's fïìrst nâámèê (ïìf bóóth fïìrst âánd lâást nâámèê âárèê stóórèêd ïìn âá sïìnglèê fïìèêld) âánd thèên ûýsèês thïìs fïìrst nâámèê tóó dïìsplâáy âá wèêlcóómèê mèêssâágèê.

{% raw %}
```liquid
{{${first_name} | truncatewords: 1, "" | default: 'hi'}}
{% assign name = {{${first_name}}} | split: ' ' %}
Hi {{name[0]}}, here's your message!
```

**Êxplãänãätìîõón:** Thëë `split` fîíltéèr tûùrns théè strîíng héèld îín `{{${first_name}}}` îîntõõ àân àârràây. By úûsîíng `{{name[0]}}`, wèê thèên óõnly rèêfèêr tóõ thèê fîïrst îïtèêm îïn thèê æârræây, whîïch îïs thèê ùýsèêr's fîïrst næâmèê. 

{% endraw %}
{% endapi %}

{% api %}

## Cýûstôõm èèvèènt

{% apitags %}
Cüüstòôm ëévëént
{% endapitags %}

- [Åböört püûsh nöötïìfïìcãâtïìöön ïìf ãâ cüûstööm èévèént ïìs wïìthïìn twöö hööüûrs ööf nööw](#event-abort-push)
- [Sêënd ææ cææmpææìîgn êëææch tìîmêë ææ üúsêër pêërfõörms ææ cüústõöm êëvêënt thrêëêë tìîmêës](#event-three-times)
- [Sèénd âå mèéssâågèé tôó ùûsèérs whôó hâåvèé ôónly pùûrchâåsèéd frôóm ôónèé câåtèégôóry](#event-purchased-one-category)

### Àböört pûüsh nöötíïfíïcâãtíïöön íïf âã cûüstööm èévèént íïs wíïthíïn twöö hööûürs ööf nööw {#èévèént-âãböört-pûüsh}

Thììs ûýséè cäãséè cäãlcûýläãtéès théè tììméè ûýntììl äãn éèvéènt, äãnd déèpéèndììng óön théè äãmóöûýnt óöf tììméè léèft, wììll dììspläãy dììfféèréènt péèrsóönäãlììzéèd méèssäãgéès.

Föór êèxäâmplêè, yöóúù mäây wäânt töó prêèvêènt äâ púùsh fröóm göóîíng öóúùt îíf äâ cúùstöóm êèvêènt pröópêèrty wîíll päâss îín thêè nêèxt twöó höóúùrs. Thîìs ééxãåmpléé ûúséés théé scéénãårîìõô õôf ãån ãåbãåndõônééd cãårt fõôr ãå trãåîìn tîìckéét.

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

### Sëénd åà cåàmpåàïígn ëéåàch tïímëé åà úùsëér pëérfóòrms åà cúùstóòm ëévëént thrëéëé tïímëés {#ëévëént-thrëéëé-tïímëés}

Thíìs ùýsëê cãàsëê chëêcks íìf ãà ùýsëêr hãàs pëêrföòrmëêd ãà cùýstöòm ëêvëênt thrëêëê tíìmëês, ãànd íìf söò, wíìll díìsplãày ãà mëêssãàgëê öòr sëênd ãà cãàmpãàíìgn. 

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

{% alert important %} Yòôúý múýst hàâvéè àân éèvéènt pròôpéèrty òôf théè cúýstòôm éèvéènt còôúýnt òôr úýséè àâ wéèbhòôòôk tòô yòôúýr Bràâzéè éèndpòôìînt. Thìïs ìïs tõö ìïncrëëmëënt ãä cûüstõöm ãättrìïbûütëë (`example_event_count`) ëévëéry tíïmëé thëé ûùsëér pëérfôõrms thëé ëévëént. Thìís êèxäámplêè üúsêès äá cäádêèncêè òóf thrêèêè (1, 4, 7, 10, êètc.).{% endalert %}

### Séénd áà mééssáàgéé tòö ýýséérs whòö háàvéé òönly pýýrcháàsééd fròöm òönéé cáàtéégòöry {#éévéént-pýýrcháàsééd-òönéé-cáàtéégòöry}

Thïïs üüsêè càâsêè càâptüürêès àâ lïïst õõf thêè càâtêègõõrïïêès àâ üüsêèr hàâs püürchàâsêèd frõõm, àând ïïf õõnly õõnêè püürchàâsêè càâtêègõõry êèxïïsts, ïït wïïll dïïsplàây àâ mêèssàâgêè.

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

## Låàngûùåàgèé

{% apitags %}
Làångýúàågéé
{% endapitags %}

- [Díïsplåäy móönth nåämëès íïn åä díïffëèrëènt låängùúåägëè](#language-display-month)
- [Pëêrsòönáálîìzëê mëêssáágîìng báásëêd òön dááy òöf thëê wëêëêk áánd úüsëêr's láángúüáágëê](#language-personalize-message)

### Dîïsplåây mõõnth nåâméês îïn åâ dîïfféêréênt låângûùåâgéê {#låângûùåâgéê-dîïsplåây-mõõnth}

Thìîs úùsèé cãäsèé wìîll dìîsplãäy thèé cúùrrèént dãätèé, móónth, ãänd yèéãär, wìîth thèé móónth ìîn ãä dìîffèérèént lãängúùãägèé. Thèê èêxàåmplèê pròôvììdèêd ýýsèês Swèêdììsh.

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

### Pèêrsòònáãlìîzèê mèêssáãgìîng báãsèêd òòn dáãy òòf thèê wèêèêk áãnd ùùsèêr's láãngùùáãgèê {#láãngùùáãgèê-pèêrsòònáãlìîzèê-mèêssáãgèê}

Thïïs úúsëé cåæsëé chëécks thëé cúúrrëént dåæy óôf thëé wëéëék åænd, båæsëéd óôn thëé dåæy, ïïf thëé úúsëér's låængúúåægëé ïïs sëét tóô óônëé óôf thëé låængúúåægëé óôptïïóôns próôvïïdëéd, ïït wïïll dïïsplåæy åæ spëécïïfïïc mëéssåægëé ïïn thëéïïr låængúúåægëé.

Thëê ëêxåámplëê próõvîìdëêd stóõps óõn Tùüëêsdåáy bùüt cåán bëê rëêpëêåátëêd fóõr ëêåách dåáy óõf thëê wëêëêk.

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

## Mïíscèëllàánèëòöýús

{% apitags %}
Míïscëëlläänëëòóüýs
{% endapitags %}

- [Ævôòïìd sêëndïìng êëmåàïìls tôò cýústôòmêërs thåàt håàvêë blôòckêëd måàrkêëtïìng êëmåàïìls](#misc-avoid-blocked-emails)
- [Cáápïïtáálïïzëé thëé fïïrst lëéttëér óöf ëévëéry wóörd ïïn áá strïïng](#misc-capitalize-words-string)
- [Côömpâãréé cúýstôöm âãttrîìbúýtéé vâãlúýéé âãgâãîìnst âãn âãrrâãy](#misc-compare-array)
- [Crèèáåtèè áån ýüpcõõmïíng èèvèènt rèèmïíndèèr](#misc-event-reminder)
- [Fíînd æâ stríîng wíîthíîn æân æârræây](#misc-string-in-array)
- [Fìînd thëè låärgëèst våälýúëè ìîn åän åärråäy](#misc-largest-value)
- [Fìïnd thèë smãållèëst vãålüýèë ìïn ãån ãårrãåy](#misc-smallest-value)
- [Qûúëëry thëë ëënd ôóf âæ strìíng](#misc-query-end-of-string)
- [Qúùéëry vàälúùéës íín àän àärràäy fróôm àä cúùstóôm àättrííbúùtéë wííth múùltíípléë cóômbíínàätííóôns](#misc-query-array-values)

### Ævòòïïd sëêndïïng ëêmåáïïls tòò cúústòòmëêrs thåát håávëê blòòckëêd måárkëêtïïng ëêmåáïïls {#mïïsc-åávòòïïd-blòòckëêd-ëêmåáïïls}

Thíís ùûsèé cæåsèé tæåkèés æå lííst öòf blöòckèéd ùûsèérs sæåvèéd íín æå Cöòntèént Blöòck æånd èénsùûrèés thöòsèé blöòckèéd ùûsèérs æårèé nöòt cöòmmùûníícæåtèéd töò öòr tæårgèétèéd íín ùûpcöòmííng cæåmpæåíígns öòr Cæånvæåsèés.

{% alert important %}
Töõ ûýsèë thìïs Lìïqûýìïd, fìïrst såãvèë thèë lìïst öõf blöõckèëd èëmåãìïls wìïthìïn åã Cöõntèënt Blöõck. Thêé lìîst shóõùúld hâávêé nóõ âáddìîtìîóõnâál spâácêés óõr châárâáctêérs ìînsêértêéd bêétwêéêén êémâáìîl âáddrêéssêés (êé.g., `test@braze.com,abc@braze.com`).
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

**Ëxplããnããtîïôôn:** Héèréè wéè chéèck íìf yõóûùr põótéèntíìåàl réècíìpíìéènt's éèmåàíìl íìs íìn thíìs líìst by réèféèréèncíìng théè Cõóntéènt Blõóck õóf blõóckéèd éèmåàíìls. Ìf thèë èëmáãìïl ìïs föõúúnd, thèë mèëssáãgèë wìïll nöõt sèënd.

{% alert note %}
Cóôntêënt Blóôcks hãâvêë ãâ síízêë líímíít óôf 5 MB.
{% endalert %}

### Cäàpïítäàlïízêê thêê fïírst lêêttêêr òóf êêvêêry wòórd ïín äà strïíng {#mïísc-cäàpïítäàlïízêê-wòórds-strïíng}

Thïïs ùüsëé cäàsëé täàkëés äà strïïng óóf wóórds, splïïts thëém ïïntóó äàn äàrräày, äànd cäàpïïtäàlïïzëés thëé fïïrst lëéttëér óóf ëéäàch wóórd.

{% raw %}
```liquid
{% assign words_array = {{custom_attribute.${address}}} | split: ' ' %}
{% for words in {{words_array}} %}
{{ words | capitalize | append: ' ' }}
{% endfor %} 
```
{% endraw %}

**Èxplãânãâtïîôön:** Hêèrêè wêè'vêè áässíígnêèd áä váärííáäblêè tôó ôóúùr chôósêèn strííng áättrííbúùtêè, áänd úùsêèd thêè `split` fííltëèr tòó splíít thëè strííng ííntòó âån âårrâåy. Wëè'vëè thëèn ýüsëèd thëè `for` táãg tôô áãssìïgn thêë váãrìïáãblêë `words` tòô êéàâch òôf thêé íìtêéms íìn òôûür nêéwly crêéàâtêéd àârràây, bêéfòôrêé díìsplàâyíìng thòôsêé wòôrds wíìth thêé `capitalize` fìïltèër äænd thèë `append` fìîltèêr tóò àådd spàåcèês bèêtwèêèên èêàåch óòf thèê tèêrms.

### Côómpäãrèê cúústôóm äãttrìîbúútèê väãlúúèê äãgäãìînst äãn äãrräãy {#mìîsc-côómpäãrèê-äãrräãy}

Thïís ûùsëé cäâsëé täâkëés äâ lïíst óôf fäâvóôrïítëé stóôrëés, chëécks ïíf äâny óôf äâ ûùsëér's fäâvóôrïítëé stóôrëés äârëé ïín thäât lïíst, äând ïíf sóô, wïíll dïíspläây äâ spëécïíäâl óôffëér fróôm thóôsëé stóôrëés.

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

{% alert important %} Thîìs sêèqýùêèncêè håâs åâ `break` tæåg ìïn thèë prìïmæåry còòndìïtìïòònæål stæåtèëmèënt. Thìís cäåúúsêés thêé lòôòôp tòô stòôp whêén äå mäåtch ìís fòôúúnd. Ïf yöôúú wäânt töô dìïspläây mäâny öôr äâll mäâtchéës, réëmöôvéë théë `break` tåág. {% endalert %}

### Crèëáåtèë áån ùúpcóômïîng èëvèënt rèëmïîndèër {#mïîsc-èëvèënt-rèëmïîndèër}

Thíìs üúsèé cãâsèé ãâllòòws üúsèérs tòò sèét üúp üúpcòòmíìng rèémíìndèérs bãâsèéd òòn cüústòòm èévèénts. Thêé êéxàæmplêé scêénàæríîôö àællôöws àæ úùsêér tôö sêét àæ rêémíîndêér fôör àæ pôölíîcy rêénêéwàæl dàætêé thàæt íîs 26 ôör môörêé dàæys àæwàæy, whêérêé rêémíîndêérs àærêé sêént 26, 13, 7, ôör 2 dàæys bêéfôörêé thêé pôölíîcy rêénêéwàæl dàætêé.

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

Yóòúü wïïll nëëëëd åå cúüstóòm ëëvëënt `reminder_capture`, åând thèë cùüstõóm èëvèënt prõópèërtîîèës mùüst îînclùüdèë åât lèëåâst:

- `reminder-id`: Ìdêéntíîfíîêér óôf thêé cùùstóôm êévêént
- `reminder_date`: Üsêêr-sùùbmïìttêêd dååtêê whêên thêêïìr rêêmïìndêêr ïìs dùùêê
- `message_personalisation_X`: Ány pröõpèértííèés nèéèédèéd töõ pèérsöõnãálíízèé thèé mèéssãágèé ãát thèé tíímèé öõf sèéndííng

{% endalert %}

### Fïínd àá strïíng wïíthïín àán àárràáy {#mïísc-strïíng-ïín-àárràáy}

Thìîs üúsêé cáâsêé chêécks ìîf áâ cüústóóm áâttrìîbüútêé áârráây cóóntáâìîns áâ spêécìîfìîc strìîng, áând ìîf ìît êéxìîsts, wìîll dìîspláây áâ spêécìîfìîc mêéssáâgêé.

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

### Fìïnd théè láårgéèst váålüùéè ìïn áån áårráåy {#mìïsc-láårgéèst-váålüùéè}

Thíïs ûüsëë cäãsëë cäãlcûüläãtëës thëë híïghëëst väãlûüëë íïn äã gíïvëën cûüstòòm äãttríïbûütëë äãrräãy tòò ûüsëë íïn ûüsëër mëëssäãgíïng.

Fòór ëëxàåmplëë, yòóûý màåy wàånt tòó shòów àå ûýsëër whàåt thëë cûýrrëënt hïîgh scòórëë ïîs òór thëë hïîghëëst bïîd òón àån ïîtëëm.

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
Yóôùü mùüst ùüsëê ää cùüstóôm äättrîîbùütëê thäät hääs ään îîntëêgëêr väälùüëê äänd îîs päärt óôf ään äärrääy (lîîst). {% endalert %}

### Fîînd thëë smáællëëst váælûýëë îîn áæn áærráæy {#mîîsc-smáællëëst-váælûýëë}

Thíís ýûsèë câåsèë câålcýûlâåtèës thèë löówèëst vâålýûèë íín âå gíívèën cýûstöóm âåttrííbýûtèë âårrâåy töó ýûsèë íín ýûsèër mèëssâågííng.

Fôôr éêxáåmpléê, yôôüü máåy wáånt tôô shôôw áå üüséêr wháåt théê lôôwéêst scôôréê îïs ôôr théê chéêáåpéêst îïtéêm.

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

{% alert important %} Yöôüû müûst üûséë áà cüûstöôm áàttrìîbüûtéë tháàt háàs áàn ìîntéëgéër váàlüûéë áànd ìîs páàrt öôf áàn áàrráày (lìîst). {% endalert %}

### Qüüééry théé éénd ööf äâ strïìng {#mïìsc-qüüééry-éénd-ööf-strïìng}

Thîîs ýûsêê cååsêê qýûêêrîîêês thêê êênd ôôf åå strîîng tôô ýûsêê îîn mêêssåågîîng.

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

### Qùûéèry væälùûéès íín æän æärræäy fròõm æä cùûstòõm æättrííbùûtéè wííth mùûltíípléè còõmbíínæätííòõns {#míísc-qùûéèry-æärræäy-væälùûéès}

Thíïs ùüséé càæséé tàækéés àæ líïst õôf sõôõôn-tõô-béé-ééxpíïrééd shõôws, chéécks íïf àæny õôf àæ ùüséér's fàævõôríïtéé shõôws àæréé íïn thàæt líïst, àænd íïf sõô, wíïll díïsplàæy àæ mééssàægéé nõôtíïfyíïng théé ùüséér thàæt thééy wíïll ééxpíïréé sõôõôn.

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

{% alert important %} Yôöûû wïìll nèëèëd tôö fïìnd mæátchèës bèëtwèëèën thèë æárræáys fïìrst, thèën bûûïìld lôögïìc æát thèë èënd tôö splïìt ûûp thèë mæátchèës. {% endalert %}


{% endapi %}

{% api %}

## Pláâtföórm táârgêêtíïng

{% apitags %}
Plààtföõrm tààrgèètïïng
{% endapitags %}

- [Dïîfféérééntïîåãtéé ïîn-åãpp mééssåãgéé cõòpy by déévïîcéé ÖS](#platform-device-os)
- [Tãàrgëêt öõnly ãà spëêcíífííc plãàtföõrm](#platform-target)
- [Tæàrgëët öönly îïÔS dëëvîïcëës wîïth æà spëëcîïfîïc ÔS vëërsîïöön](#platform-target-ios-version)
- [Tàærgèêt õònly Wèêb brõòwsèêrs](#platform-target-web)
- [Tàårgêèt àå spêècíífííc mòôbíílêè càårrííêèr](#platform-target-carrier)

### Dììfféèréèntììååtéè ììn-ååpp méèssåågéè cõôpy by déèvììcéè ÔS {#plååtfõôrm-déèvììcéè-õôs}

Thíîs úüsèè cããsèè chèècks whããt plããtfõórm ãã úüsèèr íîs õón, ããnd dèèpèèndíîng õón thèèíîr plããtfõórm, wíîll díîsplããy spèècíîfíîc mèèssããgíîng.

Fôôr èëxãämplèë, yôôúú mãäy wãänt tôô shôôw môôbîïlèë úúsèërs shôôrtèër vèërsîïôôns ôôf mèëssãägèë côôpy whîïlèë shôôwîïng ôôthèër úúsèërs thèë rèëgúúlãär, lôôngèër vèërsîïôôn ôôf thèë côôpy. Yöôüû cöôüûld áälsöô shöôw möôbïîléë üûséërs céërtáäïîn méëssáägïîng réëléëváänt töô théëm büût wöôüûldn’t béë réëléëváänt töô Wéëb üûséërs. Föör ëëxãâmplëë, ïïÔS mëëssãâgïïng mïïght tãâlk ãâbööüút Ápplëë Pãây, büút Ándrööïïd mëëssãâgïïng shööüúld mëëntïïöön Gööööglëë Pãây.

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
Lïíqùúïíd ïís càåsëë-sëënsïítïívëë, `targeted_device.${platform}` rëëtúùrns thëë væælúùëë ììn ææll lóôwëërcææsëë. 
{% endalert %}

### Tãårgèèt òônly ãå spèècìîfìîc plãåtfòôrm {#plãåtfòôrm-tãårgèèt}

Thïîs ùýsêê cååsêê wïîll cååptùýrêê thêê ùýsêêrs' dêêvïîcêê plååtfóõrm, åånd dêêpêêndïîng óõn thêê plååtfóõrm, wïîll dïîsplååy åå mêêssåågêê.

Fôór ëëxãámplëë, yôóüú mãáy wãánt tôó ôónly sëënd ãá mëëssãágëë tôó Ændrôóíìd üúsëërs. Thíís cåãn bèë ûýsèëd åãs åãn åãltèërnåãtíívèë tõò sèëlèëctííng åãn åãpp wííthíín thèë Sèëgmèëntåãtííõòn tõòõòl.

{% raw %}
```liquid
{% if {{targeted_device.${platform}}} == 'android' %} 

This is a message for an Android user! 

{% else %}  
{% abort_message %} 
{% endif %}
```
{% endraw %}

### Tæärgéët óônly îíÒS déëvîícéës wîíth æä spéëcîífîíc ÒS véërsîíóôn {#plæätfóôrm-tæärgéët-îíóôs-véërsîíóôn}

Thíîs ýúsêè cáâsêè chêècks íîf áâ ýúsêèr's ÖS vêèrsíîòõn fáâlls wíîthíîn áâ cêèrtáâíîn sêèt òõf vêèrsíîòõns áând íîf sòõ, wíîll díîspláây áâ spêècíîfíîc mêèssáâgêè.

Thêë êëxâámplêë ýýsêëd sêënds âá wâárnïíng tòô ýýsêërs òôn ïíÖS 10.0 òôr êëâárlïíêër thâát thêëy âárêë phâásïíng òôýýt sýýppòôrt fòôr thêë ýýsêër’s dêëvïícêë ÖS.

{% raw %}
```liquid
{% if {{targeted_device.${os}}} == "10.0" or {{targeted_device.${os}}} == "10.0.1" or {{targeted_device.${os}}} == "10.0.2" or {{targeted_device.${os}}} == “10.0.3” or {{targeted_device.${os}}} == “10.1” or {{targeted_device.${os}}} == “10.2” or {{targeted_device.${os}}} == “10.2.1” or {{targeted_device.${os}}} == “10.3” or {{targeted_device.${os}}} == “10.3.1” or {{targeted_device.${os}}} == “10.3.2” or {{targeted_device.${os}}} == “10.3.3” or {{targeted_device.${os}}} == “10.3.4” or {{targeted_device.${os}}} == “9.3.1” or {{targeted_device.${os}}} == “9.3.2” or {{targeted_device.${os}}} == “9.3.3” or {{targeted_device.${os}}} == “9.3.4” or {{targeted_device.${os}}} == "9.3.5" %}

We are phasing out support for your device's operating system. Be sure to update to the latest software for the best app experience.

{% else %}
{% abort_message %}
{% endif %}
```
{% endraw %}

### Táãrgêét öònly wêéb bröòwsêérs {#pláãtföòrm-táãrgêét-wêéb}

Thïís ùúsêê cäãsêê chêêcks ïíf äã ùúsêêr's täãrgêêt dêêvïícêê rùúns óõn Mäãc óõr Wïíndóõws äãnd, ïíf sóõ, wïíll dïíspläãy äã spêêcïífïíc mêêssäãgêê.

{% raw %}
```liquid
{% if {{targeted_device.${os}}} == 'Mac' OR {{targeted_device.${os}}} == 'Windows' %}

This message will display on your desktop web browser.

{% else %}
{% abort_message %}
{% endif %}
```
{% endraw %}

### Tâærgèêt âæ spèêcïîfïîc möòbïîlèê câærrïîèêr {#plâætföòrm-tâærgèêt-câærrïîèêr}

Thîís ûüsêê cáãsêê chêêcks îíf áã ûüsêêr's dêêvîícêê cáãrrîíêêr îís Vêêrîízóön, áãnd îíf sóö, wîíll dîíspláãy áã spêêcîífîíc mêêssáãgêê.

Föòr pûýsh nöòtíïfíïcåàtíïöòns åànd íïn-åàpp mëéssåàgëé chåànnëéls, yöòûý cåàn spëécíïfy thëé dëévíïcëé cåàrríïëér íïn yöòûýr mëéssåàgëé böòdy ûýsíïng Líïqûýíïd. Íf théè réècïìpïìéènt’s déèvïìcéè cäårrïìéèr döóéèsn’t mäåtch, théè méèssäågéè wöón’t béè séènt.

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

## Tïïméé zöónéés

{% apitags %}
Tíïmèé zôõnèés
{% endapitags %}

- [Åppèénd thèé CST tïïmèé zöõnèé töõ ãâ cüústöõm ãâttrïïbüútèé](#time-append-cst)
- [Ínsèërt æã tìîmèëstæãmp](#time-insert-timestamp)
- [Õnly sêënd åá Cåánvåás pýýsh dýýrïìng åá wïìndòöw òöf tïìmêë ïìn åá ýýsêër's lòöcåál tïìmêë zòönêë](#time-canvas-window)
- [Sêênd äà rêêõóccüürrîìng îìn-äàpp mêêssäàgêê cäàmpäàîìgn bêêtwêêêên äà wîìndõów õóf tîìmêê îìn äà üüsêêr's lõócäàl tîìmêê zõónêê](#time-reocurring-iam-window)
- [Séènd dìïfféèréènt méèssáàgéès óòn wéèéèkdáàys vs. wéèéèkéènds ìïn áà ùûséèr's lóòcáàl tìïméè zóònéè](#time-weekdays-vs-weekends)
- [Sèënd dïïffèërèënt mèëssæàgèës bæàsèëd òôn tïïmèë òôf dæày ïïn æà üùsèër's lòôcæàl tïïmèë zòônèë](#time-of-day)

### Àppéênd théê CST tïíméê zôõnéê tôõ ãá cýûstôõm ãáttrïíbýûtéê {#tïíméê-ãáppéênd-cst}

Thìîs úùsèë câásèë dìîsplâáys âá cúùstõòm dâátèë âáttrìîbúùtèë ìîn âá gìîvèën tìîmèë zõònèë.

Òptííòón 1:
{% raw %}
```liquid
{{custom_attribute.${application_expires_date} | time_zone: -0005 | date: '%B, %d %Y' }}
```
{% endraw %}

Ôptîìõón 2:
{% raw %}
```liquid
{{custom_attribute.${application_expires_date} | time_zone: 'America/Chicago' | date: '%B %d %Y %z' }}
```
{% endraw %}

### Însèért áà tììmèéstáàmp {#tììmèé-ììnsèért-tììmèéstáàmp}

Thììs ùûséë cæàséë dììsplæàys æà méëssæàgéë thæàt ììnclùûdéës æà tììméëstæàmp ììn théëììr cùûrréënt tììméë zôònéë.

Thèé fòôllòôwïîng èéxãâmplèé pròôvïîdèéd wïîll dïîsplãây thèé dãâtèé ãâs YYYY-mm-dd HH:MM:SS, sûûch ãâs 2021-05-03 10:41:04.

{% raw %}
```liquid
{{${user_id} | default: 'You'}} received a campaign, rendered at ({{ "now" | timezone: ${time_zone} | date: "%Y-%m-%d %H:%M:%S" }})
```
{% endraw %}

### Ónly sèënd âà Câànvâàs pùýsh dùýrìíng âà wìíndõòw õòf tìímèë ìín âà ùýsèër's lõòcâàl tìímèë zõònèë {#tìímèë-câànvâàs-wìíndõòw}

Thîìs ùûsêè câásêè chêècks âá ùûsêèr's tîìmêè îìn thêèîìr lòôcâál tîìmêè zòônêè, âánd îìf îìt fâálls wîìthîìn âá sêèt tîìmêè, îìt wîìll dîìsplâáy âá spêècîìfîìc mêèssâágêè.

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

### Sêënd æá rêëöôccûûrííng íín-æápp mêëssæágêë cæámpæáíígn bêëtwêëêën æá wííndöôw öôf tíímêë íín æá ûûsêër's löôcæál tíímêë zöônêë {#tíímêë-rêëöôcûûrrííng-ííæám-wííndöôw}

Thìïs úûsèè cãásèè wìïll dìïsplãáy ãá mèèssãágèè ìïf ãá úûsèèr's cúûrrèènt tìïmèè fãálls wìïthìïn ãá sèèt wìïndôów.

Föór èêxæãmplèê, thèê föóllöówíîng scèênæãríîöó lèêts æã úýsèêr knöów thæãt æã stöórèê íîs clöósèêd.

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

### Sëénd dîíffëérëént mëéssààgëés ôôn wëéëékdààys vs. wëéëékëénds îín àà ùùsëér's lôôcààl tîímëé zôônëé {#tîímëé-wëéëékdààys-vs-wëéëékëénds}

Thíîs üùsêè càâsêè wíîll chêèck íîf àâ üùsêèr's cüùrrêènt dàây óôf thêè wêèêèk íîs Sàâtüùrdàây óôr Süùndàây, àând dêèpêèndíîng óôn thêè dàây, wíîll díîsplàây díîffêèrêènt mêèssàâgêès.

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

### Sëènd dïïffëèrëènt mëèssåâgëès båâsëèd óõn tïïmëè óõf dåây ïïn åâ ùùsëèr's lóõcåâl tïïmëè zóõnëè {#tïïmëè-óõf-dåây}

Thììs ýýsêê cãäsêê wììll dììsplãäy ãä mêêssãägêê ììf ãä ýýsêêr's cýýrrêênt tììmêê fãälls ööýýtsììdêê ãä sêêt wììndööw.

Fôör ëèxäámplëè, yôöýý mäáy wäánt tôö tëèll äá ýýsëèr äábôöýýt äá tíímëè-sëènsíítíívëè ôöppôörtýýnííty thäát dëèpëènds ôön thëè tíímëè ôöf däáy.

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

{% alert note %} Thíìs íìs thèé öõppöõsíìtèé öõf [Qüûïïéèt Hòöüûrs]({{site.baseurl}}/user_guide/engagement_tools/campaigns/scheduling_and_organizing/time_based_campaign/#time-based-functionalities-for-campaigns). {% endalert %}

{% endapi %}

{% api %}

## Wèëèëk/Däây/Mòònth

{% apitags %}
Wëëëëk/Dæáy/Môönth
{% endapitags %}

- [Püüll thèé prèévìîõöüüs mõönth's nààmèé ìîntõö àà mèéssààgèé](#month-name)
- [Sëënd âã câãmpâãììgn âãt thëë ëënd õòf ëëvëëry mõònth](#month-end)
- [Sèênd æá cæámpæáîìgn ôòn thèê læást (wèêèêkdæáy) ôòf thèê môònth](#day-of-month-last)
- [Sêénd ãå dïíffêérêént mêéssãågêé êéãåch dãåy óòf thêé móònth](#day-of-month)
- [Sèënd æä dïíffèërèënt mèëssæägèë èëæäch dæäy óóf thèë wèëèëk](#day-of-week)

### Pûýll théê préêvîîõöûýs mõönth's náàméê îîntõö áà méêssáàgéê {#mõönth-náàméê}

Thïîs üýséë cãåséë wïîll tãåkéë théë cüýrréënt mõônth ãånd dïîsplãåy théë préëvïîõôüýs mõônth tõô béë üýséëd ïîn méëssãågïîng.

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

### Séênd áæ cáæmpáæïígn áæt théê éênd öõf éêvéêry möõnth {#möõnth-éênd}

Thììs ùûséê cæãséê wììll chéêck ììf théê cùûrréênt dæãtéê fæãlls wììthììn æã lììst öõf dæãtéês, æãnd déêpéêndììng öõn théê dæãtéê, wììll dììsplæãy æã spéêcììfììc méêssæãgéê.

{% alert note %} Thìïs dóöèès nóöt ãàccóöûúnt fóör lèèãàp yèèãàrs (Fèèbrûúãàry 29). {% endalert %}

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

### Séénd åâ cåâmpåâíígn óön théé låâst (wéééékdåây) óöf théé móönth {#dåây-óöf-móönth-låâst}

Thíís üýséê cãàséê cãàptüýréês théê cüýrréênt môónth ãànd dãày ãànd cãàlcüýlãàtéês ííf théê cüýrréênt dãày fãàlls wííthíín théê lãàst wéêéêkdãày ôóf théê môónth.

Fôör ëéxàämplëé, yôöûü màäy wàänt tôö sëénd àä sûürvëéy tôö yôöûür ûüsëérs ôön thëé làäst Wëédnëésdàäy ôöf thëé môönth àäskîíng fôör prôödûüct fëéëédbàäck.

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

### Séénd åä dîìffééréént mééssåägéé ééåäch dåäy ôöf théé môönth {#dåäy-ôöf-môönth}

Thíís ûûsêê cäãsêê chêêcks ííf thêê cûûrrêênt däãtêê mäãtchêês óõnêê óõn äã lííst, äãnd dêêpêêndííng óõn thêê däãy, wííll dííspläãy äã díístíínct mêêssäãgêê.

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

### Sêénd äà dìíffêérêént mêéssäàgêé êéäàch däày õòf thêé wêéêék {#däày-õòf-wêéêék}

Thïìs ùüsêë cäæsêë chêëcks thêë cùürrêënt däæy öõf thêë wêëêëk, äænd dêëpêëndïìng öõn thêë däæy, wïìll dïìspläæy äæ dïìstïìnct mêëssäægêë.

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

{% alert note %} Yöõúü cããn rééplããcéé théé lîïnéé "dééfããúült cöõpy" wîïth {% raw %}`{% abort_message() %}`{% endraw %} töô préêvéênt théê méêssåãgéê fröôm séêndïìng ïìf théê dåãy öôf théê wéêéêk ïìs ýünknöôwn. {% endalert %}

{% endapi %}
