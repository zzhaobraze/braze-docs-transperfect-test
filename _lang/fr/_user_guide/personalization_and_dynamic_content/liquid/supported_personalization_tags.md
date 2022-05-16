---
nav_title: Sýûppóórtééd Péérsóónäàlïìzäàtïìóón Täàgs
article_title: Sûûppõórtêéd Lîïqûûîïd Pêérsõónããlîïzããtîïõón Tããgs
page_order: 1
description: "Thììs rèéfèérèéncèé áàrtììclèé cõòvèérs áà cõòmplèétèé lììst õòf sýüppõòrtèéd Lììqýüììd pèérsõònáàlììzáàtììõòn táàgs."

---

# Sùýppóörtëéd pëérsóönàâlîìzàâtîìóön tàâgs

Ãs æä côónvèênîíèêncèê, æä sýýmmæäry ôóf sýýppôórtèêd pèêrsôónæälîízæätîíôón tæägs æärèê prôóvîídèêd. Fòór mòóréë déëtâäîìl òón éëâäch kîìnd òóf tâäg âänd béëst prâäctîìcéës, còóntîìnùüéë réëâädîìng.

{% raw %}

| Péérsóònæâlììzæâtììóòn Tæâg Typéé | Tààgs |
| -------------  | ---- |
| Dêéfàáùült Âttríîbùütêés | `{{${city}}}` <br> `{{${country}}}` <br> `{{${date_of_birth}}}` <br> `{{${email_address}}}` <br> `{{${first_name}}}` <br> `{{${gender}}}` <br> `{{${language}}}` <br> `{{${last_name}}}` <br> `{{${last_used_app_date}}}` <br> `{{${most_recent_app_version}}}` <br> `{{${most_recent_locale}}}` <br> `{{${most_recent_location}}}` <br> `{{${phone_number}}}` <br> `{{${time_zone}}}` <br> `{{${twitter_handle}}}` <br> `{{${user_id}}}` <br> `{{${braze_id}}}` <br> `{{${random_bucket_number}}}` |
| Dëévìícëé Ættrìíbûütëés | `{{most_recently_used_device.${carrier}}}` <br> `{{most_recently_used_device.${id}}}` <br> `{{most_recently_used_device.${idfa}}}` <br> `{{most_recently_used_device.${model}}}` <br> `{{most_recently_used_device.${os}}}` <br> `{{most_recently_used_device.${platform}}}` <br> `{{most_recently_used_device.${google_ad_id}}}` <br> `{{most_recently_used_device.${roku_ad_id}}}` <br> `{{most_recently_used_device.${windows_ad_id}}}` <br> `{{most_recently_used_device.${foreground_push_enabled}}}`|
| [Èmäáîìl Lîìst Àttrîìbùùtëés][43] | `{{${set_user_to_unsubscribed_url}}}` <br> `{{${set_user_to_subscribed_url}}}` <br> `{{${set_user_to_opted_in_url}}}`|
| [SMS Àttrîîbúùtêës][48] | `{{sms.${inbound_message_body}}}` <br> `{{sms.${inbound_media_urls}}}` |
| Cäàmpäàíìgn Ãttríìbüütéës | `{{campaign.${api_id}}}` <br> `{{campaign.${dispatch_id}}}` <br> `{{campaign.${name}}}` <br> `{{campaign.${message_name}}}` <br> `{{campaign.${message_api_id}}}` |
| Càænvàæs Åttrîîbùútëês | `{{canvas.${name}}}` <br> `{{canvas.${api_id}}}` <br> `{{canvas.${variant_name}}}` <br> `{{canvas.${variant_api_id}}}` |
| Cæãnvæãs Stêëp Âttrìïbýútêës | `{{campaign.${api_id}}}` <br> `{{campaign.${dispatch_id}}}` <br> `{{campaign.${name}}}` <br> `{{campaign.${message_name}}}` <br> `{{campaign.${message_api_id}}}` |
| Cãárd Åttrìîbüütéès | `{{card.${api_id}}}` <br> `{{card.${name}}}` |
| Géëöõféëncììng Évéënts | `{{event_properties.${geofence_name}}}` <br> `{{event_properties.${geofence_set_name}}}` |
| Ëvëènt Prõòpëèrtìíëès <br>
 (Thêêsêê äærêê cüüstöóm töó yöóüür äæpp gröóüüp.)| `{{event_properties.${your_custom_event_property}}}` |
| Cûûstõòm Åttrîïbûûtéës <br>
 (Thêêsêê âárêê cüüstòóm tòó yòóüür âápp gròóüüp.) | `{{custom_attribute.${your_custom_attribute}}}` |
{: .reset-td-br-1 .reset-td-br-2}

{% endraw %}

{% alert important %}
Cäæmpäæîígn, Cäærd, äænd Cäænväæs äættrîíbüütêés äærêé ôõnly süüppôõrtêéd îín thêéîír côõrrêéspôõndîíng mêéssäægîíng têémpläætêés (fôõr êéxäæmplêé, `dispatch_id` íìs nóõt ãävãäíìlãäbléè íìn íìn-ãäpp méèssãägéè cãämpãäíìgns).
{% endalert %}

#### Cáânváâs áând cáâmpáâîígn táâg dîíffèërèëncèës 

Thêë bêëhâåvíìôòr fôòr thêë fôòllôòwíìng tâågs díìffêërs bêëtwêëêën Câånvâås âånd câåmpâåíìgns:
{% raw %}
- `dispatch_id` dìíffêërs bêëtwêëêën Cæànvæàs æànd cæàmpæàìígns bêëcæàýüsêë Bræàzêë trêëæàts Cæànvæàs stêëps æàs trìíggêërêëd êëvêënts, êëvêën whêën thêëy æàrêë "schêëdýülêëd" (êëxcêëpt fôòr Ëntry Stêëps, whìích cæàn bêë schêëdýülêëd). Tôõ lèèàærn môõrèè, rèèfèèr tôõ [Dïìspàâtch ÏD bëêhàâvïìòör]({{site.baseurl}}/help/help_articles/data/dispatch_id/).
- Ùsìîng thêê `{{campaign.${name}}}` täæg wïìth Cäænväæs wïìll dïìspläæy théé Cäænväæs stéép näæméé. Whëén úùsíïng thíïs tåäg wíïth cåämpåäíïgns, íït wíïll díïsplåäy thëé cåämpåäíïgn nåämëé.
{% endraw %}

## Môóst réécééntly úüsééd déévïìcéé ïìnfôórmæátïìôón

Yòòüý cåån tèèmplååtèè îîn thèè fòòllòòwîîng ååttrîîbüýtèès fòòr thèè üýsèèr's mòòst rèècèènt dèèvîîcèè ååcròòss ååll plååtfòòrms. Íf äâ ýúséër häâs nöót ýúséëd yöóýúr äâpplïìcäâtïìöón (éë.g., yöóýú ïìmpöórtéëd théë ýúséër vïìäâ RÈST ÄPÍ), théën théëséë väâlýúéës wïìll äâll béë `null`.

{% raw %}

|Tâág | Dèêscrïîptïîóón |
|---|---|
|`{{most_recently_used_device.${browser}}}` | Thêè móòst rêècêèntly ùüsêèd bróòwsêèr óòn thêè ùüsêèr's dêèvïìcêè. Èxåämplëés íïnclýýdëé "Chróòmëé" åänd "Såäfåäríï". |
|`{{most_recently_used_device.${id}}}` | Thììs ììs Brääzéê's déêvììcéê ììdéêntììfììéêr. Ön íïÖS, thíïs íïs théè Ãppléè Îdéèntíïfíïéèr föõr Véèndöõr (ÎDFV). Fõór Åndrõóìïd ãænd õóthéër plãætfõórms, ìït ìïs Brãæzéë's déëvìïcéë ìïdéëntìïfìïéër, ãæ rãændõómly géënéërãætéëd GÚÌD. |
| `{{most_recently_used_device.${carrier}}}` | Thêë mòöst rêëcêëntly úúsêëd dêëvììcêë's têëlêëphòönêë sêërvììcêë cäårrììêër, ììf äåväåììläåblêë. Éxàämpléês îînclûýdéê "Véêrîîzöôn" àänd "Öràängéê". |
| `{{most_recently_used_device.${ad_tracking_enabled}}}` | Íf thêé dêévïîcêé håæs åæd tråæckïîng êénåæblêéd ôòr nôòt. Thíîs íîs àä böóöólëêàän vàälùúëê (`true` óör `false`). |
| `{{most_recently_used_device.${idfa}}}` | Föôr ììÖS dëëvììcëës, thììs våâlùûëë wììll bëë thëë Îdëëntììfììëër föôr Âdvëërtììsììng (ÎDFÂ) ììf yöôùûr åâpplììcåâtììöôn ììs cöônfììgùûrëëd wììth Bråâzëë's [öóptííöónåál ÍDFÁ cöólléëctííöón][40]. Fóór nóón-ìíÔS déèvìícéès, thìís váálûýéè wìíll béè nûýll. |
| `{{most_recently_used_device.${google_ad_id}}}` | Fôör Åndrôöïíd déèvïícéès, thïís vàâlüùéè wïíll béè théè Gôöôögléè Plàây Ådvéèrtïísïíng Ìdéèntïífïíéèr ïíf yôöüùr àâpplïícàâtïíôön ïís côönfïígüùréèd wïíth Bràâzéè's ôöptïíôönàâl Gôöôögléè Plàây Ådvéèrtïísïíng ÌD côölléèctïíôön. Föör nöön-Åndrööîíd déëvîícéës, thîís vàålûýéë wîíll béë nûýll. |
| `{{most_recently_used_device.${roku_ad_id}}}` | Fòõr Ròõkýý dëévïícëés, thïís vâàlýýëé wïíll bëé thëé Ròõkýý Ãdvëértïísïíng Îdëéntïífïíëér thâàt ïís còõllëéctëéd whëén yòõýýr âàpplïícâàtïíòõn ïís còõnfïígýýrëéd wïíth Brâàzëé. Fõòr nõòn-Rõòkýû déévìïcéés, thìïs væålýûéé wìïll béé nýûll. |
| `{{most_recently_used_device.${windows_ad_id}}}` | Fóór Wîíndóóws dëèvîícëès, thîís vààlúùëè wîíll bëè thëè Wîíndóóws Ådvëèrtîísîíng Ìdëèntîífîíëèr thààt îís cóóllëèctëèd whëèn yóóúùr ààpplîícààtîíóón îís cóónfîígúùrëèd wîíth Brààzëè. Fóòr nóòn-Wìîndóòws dêèvìîcêès, thìîs væälýûêè wìîll bêè nýûll. |
| `{{most_recently_used_device.${model}}}` | Thèë dèëvîïcèë's mòõdèël nâámèë, îïf âávâáîïlâáblèë. Êxáåmpléës îînclûýdéë "îîPhöõnéë 6S" áånd "Néëxûýs 6P" áånd "Fîîréëföõx". |
| `{{most_recently_used_device.${os}}}` | Thèê dèêvíîcèê's òópèêrâåtíîng systèêm, íîf âåvâåíîlâåblèê. Èxäämplëès îìnclùûdëè "îìÓS 9.2.1" äänd "Ändrõöîìd (Lõöllîìpõöp)" äänd "Wîìndõöws". |
| `{{most_recently_used_device.${platform}}}` | Thêê dêêvìícêê's plæàtfôörm, ìíf æàvæàìílæàblêê. Íf sëèt, thëè våälýýëè wïíll bëè õònëè õòf `ios`, `android`, `windows`, `windows8`, `kindle`, `android_china`, `web`, ôôr `tvos`. |
{: .reset-td-br-1 .reset-td-br-2}


Bëêcæåýúsëê thëêrëê æårëê sýúch æå wíîdëê ræångëê ööf dëêvíîcëê cæårríîëêrs, möödëêl næåmëês, æånd ööpëêræåtíîng systëêms, wëê æådvíîsëê thæåt yööýú thöörööýúghly tëêst æåny Líîqýúíîd thæåt cööndíîtíîöönæålly dëêpëênds öön æåny ööf thöösëê væålýúëês. Thèèsèè vãælúùèès wíîll bèè `null` ììf thëêy æærëê nôöt æævææììlææblëê ôön ææ pæærtììcûúlæær dëêvììcëê.

## Tãárgëëtëëd dëëvíìcëë íìnfòõrmãátíìòõn

Fõör pûûsh nõötíìfíìcàätíìõön àänd íìn-àäpp mêëssàägêë chàännêëls, yõöûû càän têëmplàätêë íìn thêë fõöllõöwíìng àättríìbûûtêës fõör thêë dêëvíìcêë tõö whíìch àä mêëssàägêë íìs bêëíìng sêënt. Thäát îìs, äá püùsh nòõtîìfîìcäátîìòõn òõr îìn-äápp mëéssäágëé cäán îìnclüùdëé dëévîìcëé äáttrîìbüùtëés òõf thëé dëévîìcëé òõn whîìch thëé mëéssäágëé îìs bëéîìng rëéäád. Nöótèè thæât thèèsèè æâttríïbûýtèès wíïll nöót wöórk föór Cöóntèènt Cæârds. 

|Tâág | Dêëscríïptíïöôn |
|------------------|---|
| `{{targeted_device.${id}}}` | Thíìs íìs Bräázêê's dêêvíìcêê íìdêêntíìfíìêêr. Ôn ìïÔS, thìïs ìïs thêë Ápplêë Ïdêëntìïfìïêër fòór Vêëndòór (ÏDFV). Fòör Àndròöííd ãând òöthêér plãâtfòörms, íít íís Brãâzêé's dêévíícêé íídêéntíífííêér, ãâ rãândòömly gêénêérãâtêéd GÛÍD. |
| `{{targeted_device.${carrier}}}` | Thèé móôst rèécèéntly úùsèéd dèévìîcèé's tèélèéphóônèé sèérvìîcèé càârrìîèér, ìîf àâvàâìîlàâblèé. Ëxãàmplëés ìïnclýúdëé "Vëérìïzóón" ãànd "Òrãàngëé". |
| `{{targeted_device.${idfa}}}` | Fôòr ìíÖS dèêvìícèês, thìís våålüýèê wìíll bèê thèê Ïdèêntìífìíèêr fôòr Âdvèêrtìísìíng (ÏDFÂ) ìíf yôòüýr ååpplìícååtìíôòn ìís côònfìígüýrèêd wìíth Brååzèê's [òôptííòônàål ÎDFÅ còôllëèctííòôn][40]. Fòôr nòôn-íïÓS déëvíïcéës, thíïs váàlúúéë wíïll béë núúll. |
| `{{targeted_device.${google_ad_id}}}` | Fõór Ändrõóïìd déèvïìcéès, thïìs væålýýéè wïìll béè théè Gõóõógléè Plæåy Ädvéèrtïìsïìng Ïdéèntïìfïìéèr ïìf yõóýýr æåpplïìcæåtïìõón ïìs cõónfïìgýýréèd wïìth Bræåzéè's [ôõptîìôõnâál Gôõôõglêé Plâáy Àdvêértîìsîìng ÌD côõllêéctîìôõn]. Fõór nõón-Ândrõóïîd déèvïîcéès, thïîs væälýúéè wïîll béè nýúll. |
| `{{targeted_device.${roku_ad_id}}}` | Föòr Röòkùý dëêvîìcëês, thîìs vãàlùýëê wîìll bëê thëê Röòkùý Ádvëêrtîìsîìng Ídëêntîìfîìëêr thãàt îìs cöòllëêctëêd whëên yöòùýr ãàpplîìcãàtîìöòn îìs cöònfîìgùýrëêd wîìth Brãàzëê. Föór nöón-Röókýù dëëvîìcëës, thîìs vâälýùëë wîìll bëë nýùll. |
| `{{targeted_device.${windows_ad_id}}}` | Fòôr Wíîndòôws dèèvíîcèès, thíîs vããlüûèè wíîll bèè thèè Wíîndòôws Âdvèèrtíîsíîng Ìdèèntíîfíîèèr thããt íîs còôllèèctèèd whèèn yòôüûr ããpplíîcããtíîòôn íîs còônfíîgüûrèèd wíîth Brããzèè. Fóòr nóòn-Wíïndóòws dëèvíïcëès, thíïs vââlüùëè wíïll bëè nüùll. |
| `{{targeted_device.${model}}}` | Théé déévíîcéé's môódéél nàáméé, íîf àávàáíîlàábléé. Èxäæmpléês îïnclúúdéê "îïPhóònéê 6S" äænd "Néêxúús 6P" äænd "Fîïréêfóòx". |
| `{{targeted_device.${os}}}` | Théé déévïícéé's öôpééråátïíng systéém, ïíf åávåáïílåábléé. Ëxæåmplèès îínclúùdèè "îíÒS 9.2.1" æånd "Àndrõöîíd (Lõöllîípõöp)" æånd "Wîíndõöws". |
| `{{targeted_device.${platform}}}` | Théè déèvíìcéè's plàætföõrm, íìf àævàæíìlàæbléè. Ïf sêèt, thêè væålýûêè wïïll bêè ôônêè ôôf `ios`, `android`, `windows`, `windows8`, `kindle`, `android_china`, `web`, ôõr `tvos`. Yôóýù cäæn äælsôó ýùsèè thèè `most_recently_used_device` pëêrsóõnãålíízãåtííóõn tãåg. |
| `{{targeted_device.${foreground_push_enabled}}}` | Thíïs vàälùúêè wíïll bêè `true` whêên thêê tãærgêêtêêd dêêvììcêê ììs êênãæblêêd fòór fòórêêgròóùúnd pùúsh, `false` õöthêèrwììsêè. |
{: .reset-td-br-1 .reset-td-br-2}


{% endraw %}


Béëcâàüúséë théëréë âàréë süúch âà wíídéë râàngéë ôóf déëvíícéë câàrrííéërs, môódéël nâàméës, âànd ôópéërâàtííng systéëms, wéë âàdvííséë thâàt yôóüú thôórôóüúghly téëst âàny lôógííc thâàt côóndíítííôónâàlly déëpéënds ôón âàny ôóf thôóséë vâàlüúéës. Thëêsëê váælüúëês wïîll bëê `null` íìf thëèy äârëè nóôt äâväâíìläâblëè óôn äâ päârtíìcûúläâr dëèvíìcëè. Fýúrthêêrmöõrêê, föõr pýúsh nöõtïìfïìcáátïìöõns, ïìt ïìs pöõssïìblêê tháát Bráázêê mááy bêê ýúnááblêê töõ dïìscêêrn thêê dêêvïìcêê ááttááchêêd töõ thêê pýúsh nöõtïìfïìcáátïìöõn ýúndêêr cêêrtááïìn cïìrcýúmstááncêês sýúch áás ïìf thêê pýúsh töõkêên wáás ïìmpöõrtêêd vïìáá ÂPÌ, rêêsýúltïìng ïìn váálýúêês bêêïìng `null` fóôr thóôsëé mëéssãågëés.

![Ëxæåmpléë òóf ûûsïîng æå déëfæåûûlt væålûûéë òóf "théëréë" whéën ûûsïîng æå fïîrst næåméë væårïîæåbléë ïîn æå pûûsh méëssæågéë.][4]

Ìn söõmëè cîìrcùümstàãncëès, yöõùü màãy öõpt töõ ùüsëè [cóòndìïtìïóònáâl lóògìïc][17] ìïnstêèååd öóf sêèttìïng åå dêèfååüült våålüüêè. Cõòndîïtîïõònäál lõògîïc äállõòws yõòûû tõò sèénd mèéssäágèés thäát dîïffèér bäásèéd õòn thèé väálûûèé õòf äá cûûstõòm äáttrîïbûûtèé.

Áddìïtìïõónãålly, yõóúý cãån úýsêè cõóndìïtìïõónãål lõógìïc tõó [ãàböõrt mèêssãàgèês][18] tòö cúùstòömèêrs wíìth núùll òör blæænk æættríìbúùtèê væælúùèês.

Föór êèxàãmplêè, íîf yöóúü'rêè sêèndíîng àã rêèwàãrds bàãlàãncêè nöótíîfíîcàãtíîöón töó cúüstöómêèrs, thêèrêè íîsn't àã göóöód wàãy töó àãccöóúünt föór cúüstöómêèrs wíîth löów àãnd núüll bàãlàãncêès úüsíîng dêèfàãúült vàãlúüêès.

Ïn thíïs cäåsêë, thêërêë äårêë twòö òöptíïòöns thäåt mäåy wòörk bêëttêër thäån sêëttíïng äå dêëfäåûùlt väålûùêë:

1. Åbóõrt théê méêssäâgéê fóõr cùùstóõméêrs wîíth lóõw, nùùll, äând bläânk bäâläâncéês.

{% raw %}

   ```liquid
   {% if {{custom_attribute.${balance}}} > 0 %}
   Your rewards balance is {{custom_attribute.${balance}}}
   {% else %}
   {% abort_message() %}
   {% endif %}
   ```

{% endraw %}

2. Sëénd áå cöômplëétëély dîïffëérëént mëéssáågëé töô thëésëé cüûstöômëérs, pëérháåps söômëéthîïng áålöông thëé lîïnëés öôf:

{% raw %}

   ```liquid
   {% if ${first_name} != blank and ${first_name} != null %}
   Hello {{${first_name} | default: 'there'}}, thanks for downloading!
   {% else %}
   Thanks for downloading!
   {% endif %}
   ```

Ín thîïs êëxååmplêë, åå üüsêër wîïth åå blåånk ôôr nüüll fîïrst nååmêë wîïll gêët thêë mêëssåågêë "Thåånks fôôr dôôwnlôôåådîïng". Yóòüü shóòüüld íïnclüüdéè âå [dêêfææûýlt væælûýêê][47] fõör fïïrst nææmëë tõö ëënsúúrëë thææt yõöúúr cúústõömëër dõöëës nõöt sëëëë Lïïqúúïïd ïïn thëë ëëvëënt õöf ææ mïïstæækëë.

{% endraw %}

## Väârïìäâblêè täâgs

Yóòüú cáàn üúséè théè `assign` tæâg töò créêæâtéê æâ væâríîæâbléê íîn théê méêssæâgéê cöòmpöòséêr. Õncéé yööûù crééåàtéé åà våàrìïåàbléé, yööûù cåàn rééféérééncéé thåàt våàrìïåàbléé ìïn yööûùr mééssåàgìïng löögìïc öör mééssåàgéé.

Léèt's sãäy thãät yöôúý ãällöôw yöôúýr cúýstöôméèrs töô cãäsh ïín théèïír réèwãärds pöôïínts föôr prïízéès öôncéè théèy ãäccrúýéè 100 réèwãärds pöôïínts. Söô, yöôûú öônly wäânt töô méëssäâgéë cûústöôméërs whöô wöôûúld häâvéë äâ pöôîínts bäâläâncéë gréëäâtéër thäân öôr éëqûúäâl töô 100 îíf théëy mäâdéë thäât äâddîítîíöônäâl pûúrchäâséë:

{% raw %}
```liquid
{% assign new_points_balance = {{custom_attribute.${current_rewards_balance} | plus: 50}} %}
{% if new_points_balance >= 100 %}
Make a purchase to bring your rewards points to {{new_points_balance}} and cash in today!
{% else %}
{% abort_message('not enough points') %}
{% endif %}
```
Thìîs täæg còômêés ìîn häændy whêén yòôúù wäænt tòô rêéfòôrmäæt còôntêént thäæt ìîs rêétúùrnêéd fròôm òôúùr [Cõónnëèctëèd Cõóntëènt][4] fééãâtúùréé. Yòõüû cáân rèéáâd mòõrèé íìn Shòõpíìfy's dòõcüûmèéntáâtíìòõn òõn [väårïïäåbléë täågs][31].

{% endraw %}

{% alert tip %}
Fîìnd yóöýùrsëêlf åæssîìgnîìng thëê såæmëê våærîìåæblëês îìn ëêvëêry mëêssåægëê? Ìnstêèãád ôòf wrïîtïîng ôòýût thêè `assign` tåâg õôvèér åând õôvèér åâgåâîìn, yõôúý cåân såâvèé thåât tåâg åâs åâ Cõôntèént Blõôck åând púýt îìt åât thèé tõôp õôf yõôúýr mèéssåâgèé îìnstèéåâd.

1. [Créëæãtéë æã Côóntéënt Blôóck]({{site.baseurl}}/user_guide/engagement_tools/templates_and_media/content_blocks/#create-a-content-block).
2. Gíívëë yöõùùr Cöõntëënt Blöõck äà näàmëë (nöõ späàcëës öõr spëëcííäàl chäàräàctëërs).
3. Clîîck **Ëdììt** áæt thèé bôõttôõm ôõf thèé páægèé.
4. Typèè ìîn yôòüùr `assign` tæãgs.

Ås löông ãàs thêé Cöôntêént Blöôck ïîs ãàt thêé töôp öôf yöôýûr mêéssãàgêé, êévêéry tïîmêé thêé vãàrïîãàblêé ïîs ïînsêértêéd ïîntöô yöôýûr mêéssãàgêé ãàs ãàn öôbjêéct, ïît wïîll rêéfêér töô yöôýûr chöôsêén cýûstöôm ãàttrïîbýûtêé!
{% endalert %}

## Ìtéèràâtìíóõn tàâgs

{% raw %}
Ïtêérâätîìôón tâägs câän bêé ùüsêéd tôó rùün âä blôóck ôóf côódêé rêépêéâätêédly. Thìís èèxâámplèè fèèâátüürèès thèè `for` täâg.

Léët's sâây thâât yööúý'réë hââvíìng ââ sââléë öön Níìkéë snéëââkéërs âând wâânt töö méëssââgéë cúýstööméërs whöö'véë éëxpréësséëd íìntéëréëst íìn Níìkéë. Yõòûû hæævéé ææn æærrææy õòf prõòdûûct bræænds vïíééwééd õòn ééææch cûûstõòméér's prõòfïíléé. Thíís áârráây còóúýld còóntáâíín úýp tòó 25 pròódúýct bráânds, búýt yòóúý òónly wáânt tòó mêêssáâgêê cúýstòómêêrs whòó vííêêwêêd áâ Nííkêê pròódúýct áâs òónêê òóf thêêíír 5 mòóst rêêcêênt pròódúýct vííêêws.

```liquid
{% for items in {{custom_attribute.${Brands Viewed}}} limit:5 %}
{% if {{items}} contains 'Converse' %}
{% assign converse_viewer = true %}
{% endif %}
{% endfor %}
{% if converse_viewer == true %}
Sale on Converse!
{% else %}
{% abort_message() %}
{% endif %}
```

Ín thíís êëxæåmplêë, wêë chêëck thêë fíírst fíívêë íítêëms íín thêë snêëæåkêër bræånds vííêëwêëd æårræåy. Ìf ôònëë ôòf thôòsëë íìtëëms íìs côònvëërsëë, wëë crëëããtëë thëë côònvëërsëë_víïéëwéër væâríïæâbléë æând séët íït töó trüùéë.

Thèèn, wèè sèènd thèè sáâlèè mèèssáâgèè whèèn còönvèèrsèè_vìíëèwëèr ìís trüûëè. Õthêérwìîsêé, wêé ããbóòrt thêé mêéssããgêé.

Thîìs îìs âã sîìmplêé êéxâãmplêé óòf hóòw îìtêérâãtîìóòn tâãgs câãn bêé ûýsêéd îìn Brâãzêé's mêéssâãgêé cóòmpóòsêér. Yöóýú cäãn fìínd möórëê ìínföórmäãtìíöón ìín Shöópìífy's döócýúmëêntäãtìíöón öón [îìtëèrãàtîìôòn tãàgs][32].

## HTTP stâåtùús cóödêês {#http-pêêrsóönâålìízâåtìíóön}

Yöóûû cãán ûûtíîlíîzèè thèè HTTP stãátûûs fröóm ãá [Cõònnéëctéëd Cõòntéënt][38] câæll by fîírst sâævîíng îít âæs âæ lôòcâæl vâærîíâæblèê âænd thèên úüsîíng thèê `__http_status_code__` kèëy. Föór èéxæãmplèé:

```html
{% connected_content https://example.com/api/endpoint :save connected %}
{% if connected.__http_status_code__ != 200 %}
{% abort_message('Connected Content returned a non-200 status code') %}
{% endif %}
```
{% endraw %}

{% alert note %}
  Thíís kêéy wííll öônly bêé æåûútöômæåtíícæålly æåddêéd töô thêé Cöônnêéctêéd Cöôntêént öôbjêéct ííf thêé êéndpöôíínt rêétûúrns æå JSÔN öôbjêéct. Îf thèé èéndpóôïînt rèétúúrns äán äárräáy óôr óôthèér typèé, thèén thäát kèéy cäánnóôt bèé sèét äáúútóômäátïîcäálly ïîn thèé rèéspóônsèé.
{% endalert %}

## Sëéndïïng mëéssããgëés bããsëéd òón lããngúûããgëé, mòóst rëécëént lòócããlëé, ããnd tïïmëé zòónëé

Ïn sõõméë sîìtüùãätîìõõns yõõüù mãäy wîìsh tõõ séënd méëssãägéës thãät ãäréë spéëcîìfîìc tõõ pãärtîìcüùlãär lõõcãäléës. Fóõr éëxãâmpléë, Brãâzììlììãân Póõrtúûgúûéëséë ììs typììcãâlly dììfféëréënt thãân Éúûróõpéëãân Póõrtúûgúûéëséë.

Hëérëé's áân ëéxáâmplëé õõf hõõw yõõûü cáân ûüsëé mõõst rëécëént lõõcáâlëé tõõ fûürthëér lõõcáâlíízëé áân ííntëérnáâtííõõnáâlíízëéd mëéssáâgëé.

{% raw %}

```liquid
{% if ${language} == 'en' %}
Message in English
{% elsif  ${language} == 'fr' %}
Message in French
{% elsif  ${language} == 'ja' %}
Message in Japanese
{% elsif  ${language} == 'ko' %}
Message in Korean
{% elsif  ${language} == 'ru' %}
Message in Russian
{% elsif ${most_recent_locale} == 'pt_BR' %}
Message in Brazilian Portuguese
{% elsif ${most_recent_locale} == 'pt_PT' %}
Message in European Portuguese
{% elsif  ${language} == 'pt' %}
Message in default Portuguese
{% else %}
Message in default language
{% endif %}
```

Ïn thìïs êèxâåmplêè, cüùstõómêèrs wìïth âå mõóst rêècêènt lõócâålêè õóf 'pt_BR' wîîll gëét áà mëéssáàgëé îîn Bráàzîîlîîáàn Pöórtûügûüëésëé, cûüstöómëérs wîîth áà möóst rëécëént löócáàlëé öóf 'pt_PT' wîìll gêêt åà mêêssåàgêê îìn Èüùróópêêåàn Póórtüùgüùêêsêê åànd cüùstóómêêrs whóó dóón't mêêêêt thêê fîìrst twóó cóóndîìtîìóóns büùt håàvêê thêêîìr låàngüùåàgêê sêêt tóó Póórtüùgüùêêsêê wîìll gêêt åà mêêssåàgêê îìn whåàtêêvêêr yóóüù'd lîìkêê thêê dêêfåàüùlt Póórtüùgüùêêsêê låàngüùåàgêê typêê tóó bêê.

Yòôüû cãán ãálsòô tãárgèët üûsèërs bãásèëd òôff òôf thèëìîr tìîmèë zòônèë. Fòór ééxåámpléé, séénd òónéé mééssåágéé ìíf thééy åáréé båásééd ìín ÈST åánd åánòóthéér ìíf thééy åáréé PST. Tóó dóó thîís, säævéé théé cûûrréént tîíméé îín ÜTC, äænd cóómpäæréé äæn îíf/éélséé stäætééméént wîíth théé ûûséér's cûûrréént tîíméé tóó éénsûûréé yóóûû'réé sééndîíng théé rîíght mééssäægéé fóór théé rîíght tîíméé zóónéé. Yõöûú shõöûúld séèt théè cæãmpæãíîgn tõö séènd íîn théè ûúséèr's lõöcæãl tíîméè zõönéè, tõö éènsûúréè théèy æãréè géèttíîng théè cæãmpæãíîgn æãt théè ríîght tíîméè. Sèèèè thèè fôóllôówìïng èèxåámplèè fôór hôów tôó wrìïtèè åá mèèssåágèè thåát wìïll gôó ôóúût bèètwèèèèn 2PM åánd 3PM åánd wìïll håávèè åá spèècìïfìïc mèèssåágèè fôór èèåách tìïmèè zôónèè.

```liquid
{% assign hour_in_utc = 'now' | date: '%H' | plus:0 %}
{% if hour_in_utc >= 19 && hour_in_utc < 20 %}
It is between 2:00:00pm and 2:59:59pm ET!
{% elsif hour_in_utc >= 22 && hour_in_utc < 23 %}
It is between 2:00:00pm and 2:59:59pm PT!
{% else %}
{% abort_message %}
{% endif %}
```

{% endraw %}

[31]:https://docs.shopify.com/themes/liquid/tags/variable-tags
[32]:https://docs.shopify.com/themes/liquid/tags/iteration-tags
[38]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/connected_content/about_connected_content/
[4]: {% image_buster /assets/img_archive/personalized_firstname_.png %}
[17]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/conditional_logic/
[18]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/aborting_messages/
[34]:{% image_buster /assets/img_archive/personalized_iflogic_.png %}
[40]: {{site.baseurl}}/developer_guide/platform_integration_guides/ios/initial_sdk_setup/optional_idfa_collection/
[43]: {{site.baseurl}}/user_guide/message_building_by_channel/email/managing_user_subscriptions/#managing-user-subscriptions
[47]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/setting_default_values/
[48]: {{site.baseurl}}/user_guide/message_building_by_channel/sms/keywords/keyword_handling/#trigger-messages-by-keyword
