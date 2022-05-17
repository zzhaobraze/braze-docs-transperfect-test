---
nav_title: Sùúppòòrtéêd Péêrsòònáâlíízáâtííòòn Táâgs
article_title: Súýppòörtèêd Lïïqúýïïd Pèêrsòönãålïïzãåtïïòön Tãågs
page_order: 1
description: "Thíìs rèêfèêrèêncèê åârtíìclèê cõõvèêrs åâ cõõmplèêtèê líìst õõf sýùppõõrtèêd Líìqýùíìd pèêrsõõnåâlíìzåâtíìõõn tåâgs."

---

# Süýppõörtèèd pèèrsõönäälïïzäätïïõön täägs

Às æä cóönvëéníïëéncëé, æä süümmæäry óöf süüppóörtëéd pëérsóönæälíïzæätíïóön tæägs æärëé próövíïdëéd. Fôôr môôréë déëtæåííl ôôn éëæåch kíínd ôôf tæåg æånd béëst præåctíícéës, côôntíínûúéë réëæådííng.

{% raw %}

| Pëërsöönãâlïïzãâtïïöön Tãâg Typëë | Tæãgs |
| -------------  | ---- |
| Dêêfàáúúlt Ättrîïbúútêês | `{{${city}}}` <br> `{{${country}}}` <br> `{{${date_of_birth}}}` <br> `{{${email_address}}}` <br> `{{${first_name}}}` <br> `{{${gender}}}` <br> `{{${language}}}` <br> `{{${last_name}}}` <br> `{{${last_used_app_date}}}` <br> `{{${most_recent_app_version}}}` <br> `{{${most_recent_locale}}}` <br> `{{${most_recent_location}}}` <br> `{{${phone_number}}}` <br> `{{${time_zone}}}` <br> `{{${twitter_handle}}}` <br> `{{${user_id}}}` <br> `{{${braze_id}}}` <br> `{{${random_bucket_number}}}` |
| Dèêvîìcèê Ãttrîìbúútèês | `{{most_recently_used_device.${carrier}}}` <br> `{{most_recently_used_device.${id}}}` <br> `{{most_recently_used_device.${idfa}}}` <br> `{{most_recently_used_device.${model}}}` <br> `{{most_recently_used_device.${os}}}` <br> `{{most_recently_used_device.${platform}}}` <br> `{{most_recently_used_device.${google_ad_id}}}` <br> `{{most_recently_used_device.${roku_ad_id}}}` <br> `{{most_recently_used_device.${windows_ad_id}}}` <br> `{{most_recently_used_device.${foreground_push_enabled}}}`|
| [Ëmääîìl Lîìst Ättrîìbùûtèès][43] | `{{${set_user_to_unsubscribed_url}}}` <br> `{{${set_user_to_subscribed_url}}}` <br> `{{${set_user_to_opted_in_url}}}`|
| [SMS Åttrïíbýütéês][48] | `{{sms.${inbound_message_body}}}` <br> `{{sms.${inbound_media_urls}}}` |
| Cáâmpáâìîgn Ættrìîbûùtèês | `{{campaign.${api_id}}}` <br> `{{campaign.${dispatch_id}}}` <br> `{{campaign.${name}}}` <br> `{{campaign.${message_name}}}` <br> `{{campaign.${message_api_id}}}` |
| Càânvàâs Åttrîîbýùtéës | `{{canvas.${name}}}` <br> `{{canvas.${api_id}}}` <br> `{{canvas.${variant_name}}}` <br> `{{canvas.${variant_api_id}}}` |
| Càänvàäs Stéép Ättrïíbýùtéés | `{{campaign.${api_id}}}` <br> `{{campaign.${dispatch_id}}}` <br> `{{campaign.${name}}}` <br> `{{campaign.${message_name}}}` <br> `{{campaign.${message_api_id}}}` |
| Cáãrd Àttrïîbùütêès | `{{card.${api_id}}}` <br> `{{card.${name}}}` |
| Gèéööfèéncìîng Èvèénts | `{{event_properties.${geofence_name}}}` <br> `{{event_properties.${geofence_set_name}}}` |
| Évéènt Prõòpéèrtîíéès <br>
 (Théêséê àâréê cúústôöm tôö yôöúúr àâpp grôöúúp.)| `{{event_properties.${your_custom_event_property}}}` |
| Cùústõôm Ættrïìbùútëès <br>
 (Thëësëë àärëë cüústòòm tòò yòòüúr àäpp gròòüúp.) | `{{custom_attribute.${your_custom_attribute}}}` |
{: .reset-td-br-1 .reset-td-br-2}

{% endraw %}

{% alert important %}
Cäæmpäæíïgn, Cäærd, äænd Cäænväæs äættríïbüûtêës äærêë öönly süûppöörtêëd íïn thêëíïr cöörrêëspööndíïng mêëssäægíïng têëmpläætêës (föör êëxäæmplêë, `dispatch_id` îís nòöt áàváàîíláàblëè îín îín-áàpp mëèssáàgëè cáàmpáàîígns).
{% endalert %}

#### Cåænvåæs åænd cåæmpåæìîgn tåæg dìîffèêrèêncèês 

Thêé bêéhæãvïìöór föór thêé föóllöówïìng tæãgs dïìffêérs bêétwêéêén Cæãnvæãs æãnd cæãmpæãïìgns:
{% raw %}
- `dispatch_id` dìîfféêrs béêtwéêéên Cáænváæs áænd cáæmpáæìîgns béêcáæüüséê Bráæzéê tréêáæts Cáænváæs stéêps áæs trìîggéêréêd éêvéênts, éêvéên whéên théêy áæréê "schéêdüüléêd" (éêxcéêpt fòòr Ëntry Stéêps, whìîch cáæn béê schéêdüüléêd). Tóõ lêèæårn móõrêè, rêèfêèr tóõ [Dîìspáætch ÎD bëêháævîìôör]({{site.baseurl}}/help/help_articles/data/dispatch_id/).
- Ûsííng thêè `{{campaign.${name}}}` tæàg wìíth Cæànvæàs wìíll dìísplæày thêè Cæànvæàs stêèp næàmêè. Whéèn ýùsïïng thïïs täãg wïïth cäãmpäãïïgns, ïït wïïll dïïspläãy théè cäãmpäãïïgn näãméè.
{% endraw %}

## Môöst rêëcêëntly ýüsêëd dêëvíîcêë íînfôörmàãtíîôön

Yõòûý cáân tèémpláâtèé îìn thèé fõòllõòwîìng áâttrîìbûýtèés fõòr thèé ûýsèér's mõòst rèécèént dèévîìcèé áâcrõòss áâll pláâtfõòrms. Íf æà úúsêér hæàs nôõt úúsêéd yôõúúr æàpplìïcæàtìïôõn (êé.g., yôõúú ìïmpôõrtêéd thêé úúsêér vìïæà RÈST ÁPÍ), thêén thêésêé væàlúúêés wìïll æàll bêé `null`.

{% raw %}

|Tååg | Dêëscrííptííóôn |
|---|---|
|`{{most_recently_used_device.${browser}}}` | Thêê mõöst rêêcêêntly ûüsêêd brõöwsêêr õön thêê ûüsêêr's dêêvíïcêê. Ëxäämplèès ïînclûüdèè "Chróömèè" äänd "Sääfäärïî". |
|`{{most_recently_used_device.${id}}}` | Thîïs îïs Bräâzêê's dêêvîïcêê îïdêêntîïfîïêêr. Òn ïìÒS, thïìs ïìs thèê Ãpplèê Îdèêntïìfïìèêr fôôr Vèêndôôr (ÎDFV). Fòòr Ândròòîîd âänd òòthéër plâätfòòrms, îît îîs Brâäzéë's déëvîîcéë îîdéëntîîfîîéër, âä râändòòmly géënéërâätéëd GÙÍD. |
| `{{most_recently_used_device.${carrier}}}` | Théë mõóst réëcéëntly ýùséëd déëvîícéë's téëléëphõónéë séërvîícéë cáærrîíéër, îíf áæváæîíláæbléë. Èxãåmpléès ììnclüûdéè "Véèrììzóón" ãånd "Örãångéè". |
| `{{most_recently_used_device.${ad_tracking_enabled}}}` | Îf théé déévìîcéé hãäs ãäd trãäckìîng éénãäblééd ôör nôöt. Thíïs íïs ãá bóôóôléêãán vãálûûéê (`true` õör `false`). |
| `{{most_recently_used_device.${idfa}}}` | Föör îîÒS dëëvîîcëës, thîîs váãlúüëë wîîll bëë thëë Îdëëntîîfîîëër föör Ädvëërtîîsîîng (ÎDFÄ) îîf yööúür áãpplîîcáãtîîöön îîs cöönfîîgúürëëd wîîth Bráãzëë's [òôptîïòônàål ÍDFÁ còôllëêctîïòôn][40]. Fòór nòón-ìîÕS dèëvìîcèës, thìîs väâlûûèë wìîll bèë nûûll. |
| `{{most_recently_used_device.${google_ad_id}}}` | Fòór Åndròóïïd dëévïïcëés, thïïs væálýúëé wïïll bëé thëé Gòóòóglëé Plæáy Ådvëértïïsïïng Îdëéntïïfïïëér ïïf yòóýúr æápplïïcæátïïòón ïïs còónfïïgýúrëéd wïïth Bræázëé's òóptïïòónæál Gòóòóglëé Plæáy Ådvëértïïsïïng ÎD còóllëéctïïòón. Föõr nöõn-Ãndröõîíd dêévîícêés, thîís väælùýêé wîíll bêé nùýll. |
| `{{most_recently_used_device.${roku_ad_id}}}` | Fòór Ròóküü dèêvíícèês, thíís vââlüüèê wííll bèê thèê Ròóküü Ádvèêrtíísííng Ídèêntíífííèêr thâât íís còóllèêctèêd whèên yòóüür ââpplíícââtííòón íís còónfíígüürèêd wííth Brââzèê. Fóòr nóòn-Róòkýý dèèvîîcèès, thîîs væãlýýèè wîîll bèè nýýll. |
| `{{most_recently_used_device.${windows_ad_id}}}` | Föör Wîíndööws dèëvîícèës, thîís vâãlùùèë wîíll bèë thèë Wîíndööws Âdvèërtîísîíng Ïdèëntîífîíèër thâãt îís cööllèëctèëd whèën yööùùr âãpplîícâãtîíöön îís cöönfîígùùrèëd wîíth Brâãzèë. Fóör nóön-Wïïndóöws dëévïïcëés, thïïs våãlûüëé wïïll bëé nûüll. |
| `{{most_recently_used_device.${model}}}` | Thèê dèêvïîcèê's môõdèêl náåmèê, ïîf áåváåïîláåblèê. Éxàâmplêës ìïnclýùdêë "ìïPhöönêë 6S" àând "Nêëxýùs 6P" àând "Fìïrêëfööx". |
| `{{most_recently_used_device.${os}}}` | Thëê dëêvíícëê's óôpëêræàtííng systëêm, ííf æàvæàíílæàblëê. Êxáæmplêés îìnclýûdêé "îìÖS 9.2.1" áænd "Àndróõîìd (Lóõllîìpóõp)" áænd "Wîìndóõws". |
| `{{most_recently_used_device.${platform}}}` | Thèë dèëvïícèë's plààtfòórm, ïíf ààvààïílààblèë. Ìf sèét, thèé väàlüüèé wííll bèé õônèé õôf `ios`, `android`, `windows`, `windows8`, `kindle`, `android_china`, `web`, öôr `tvos`. |
{: .reset-td-br-1 .reset-td-br-2}


Bêècàåûúsêè thêèrêè àårêè sûúch àå wììdêè ràångêè ôöf dêèvììcêè càårrììêèrs, môödêèl nàåmêès, àånd ôöpêèràåtììng systêèms, wêè àådvììsêè thàåt yôöûú thôörôöûúghly têèst àåny Lììqûúììd thàåt côöndììtììôönàålly dêèpêènds ôön àåny ôöf thôösêè vàålûúêès. Thëêsëê vãâlúùëês wìíll bëê `null` íîf thëëy ãårëë nòõt ãåvãåíîlãåblëë òõn ãå pãårtíîcùýlãår dëëvíîcëë.

## Tæærgéëtéëd déëvììcéë ììnföôrmæætììöôn

Fôòr pûúsh nôòtíîfíîcâàtíîôòn âànd íîn-âàpp méêssâàgéê châànnéêls, yôòûú câàn téêmplâàtéê íîn théê fôòllôòwíîng âàttríîbûútéês fôòr théê déêvíîcéê tôò whíîch âà méêssâàgéê íîs béêíîng séênt. Thâàt îîs, âà púúsh nõôtîîfîîcâàtîîõôn õôr îîn-âàpp mèèssâàgèè câàn îînclúúdèè dèèvîîcèè âàttrîîbúútèès õôf thèè dèèvîîcèè õôn whîîch thèè mèèssâàgèè îîs bèèîîng rèèâàd. Nõõtëè thâæt thëèsëè âættrîîbûùtëès wîîll nõõt wõõrk fõõr Cõõntëènt Câærds. 

|Tääg | Dëëscríïptíïõón |
|------------------|---|
| `{{targeted_device.${id}}}` | Thíìs íìs Bràãzëë's dëëvíìcëë íìdëëntíìfíìëër. Òn ìïÒS, thìïs ìïs thëè Ápplëè Ídëèntìïfìïëèr fòòr Vëèndòòr (ÍDFV). Fôór Ândrôóíìd äánd ôóthéèr pläátfôórms, íìt íìs Bräázéè's déèvíìcéè íìdéèntíìfíìéèr, äá räándôómly géènéèräátéèd GÚÍD. |
| `{{targeted_device.${carrier}}}` | Thêë mööst rêëcêëntly ùüsêëd dêëvîícêë's têëlêëphöönêë sêërvîícêë cäàrrîíêër, îíf äàväàîíläàblêë. Ëxãæmpléês ïïnclýýdéê "Véêrïïzóòn" ãænd "Ôrãængéê". |
| `{{targeted_device.${idfa}}}` | Föòr ìïÒS dëëvìïcëës, thìïs väàlûýëë wìïll bëë thëë Ìdëëntìïfìïëër föòr Ãdvëërtìïsìïng (ÌDFÃ) ìïf yöòûýr äàpplìïcäàtìïöòn ìïs cöònfìïgûýrëëd wìïth Bräàzëë's [óõptïìóõnåæl ÍDFÃ cóõllëêctïìóõn][40]. Fôõr nôõn-ììÓS déèvììcéès, thììs vãälüûéè wììll béè nüûll. |
| `{{targeted_device.${google_ad_id}}}` | Fóór Åndróóìïd déèvìïcéès, thìïs väãlýýéè wìïll béè théè Góóóógléè Pläãy Ådvéèrtìïsìïng Îdéèntìïfìïéèr ìïf yóóýýr äãpplìïcäãtìïóón ìïs cóónfìïgýýréèd wìïth Bräãzéè's [õõptìïõõnäål Gõõõõglëê Pläåy Àdvëêrtìïsìïng ÏD cõõllëêctìïõõn]. Fòór nòón-Ændròóìïd dëévìïcëés, thìïs váálúýëé wìïll bëé núýll. |
| `{{targeted_device.${roku_ad_id}}}` | Fôôr Rôôkúù dèévïícèés, thïís váãlúùèé wïíll bèé thèé Rôôkúù Ädvèértïísïíng Ïdèéntïífïíèér tháãt ïís côôllèéctèéd whèén yôôúùr áãpplïícáãtïíôôn ïís côônfïígúùrèéd wïíth Bráãzèé. Fõör nõön-Rõöküú dêèvîîcêès, thîîs vàãlüúêè wîîll bêè nüúll. |
| `{{targeted_device.${windows_ad_id}}}` | Fõõr Wïïndõõws dêèvïïcêès, thïïs væålùýêè wïïll bêè thêè Wïïndõõws Àdvêèrtïïsïïng Ìdêèntïïfïïêèr thæåt ïïs cõõllêèctêèd whêèn yõõùýr æåpplïïcæåtïïõõn ïïs cõõnfïïgùýrêèd wïïth Bræåzêè. Föõr nöõn-Wïîndöõws déèvïîcéès, thïîs vàælúüéè wïîll béè núüll. |
| `{{targeted_device.${model}}}` | Théè déèvïícéè's môõdéèl nàãméè, ïíf àãvàãïílàãbléè. Éxââmplèës íînclúúdèë "íîPhõönèë 6S" âând "Nèëxúús 6P" âând "Fíîrèëfõöx". |
| `{{targeted_device.${os}}}` | Thêè dêèvïîcêè's öõpêèràätïîng systêèm, ïîf àävàäïîlàäblêè. Êxããmplëês íìnclúùdëê "íìÒS 9.2.1" ããnd "Åndrôôíìd (Lôôllíìpôôp)" ããnd "Wíìndôôws". |
| `{{targeted_device.${platform}}}` | Thèê dèêvïícèê's plåàtföòrm, ïíf åàvåàïílåàblèê. Íf sêët, thêë væålúúêë wììll bêë ôõnêë ôõf `ios`, `android`, `windows`, `windows8`, `kindle`, `android_china`, `web`, óòr `tvos`. Yôöûü càãn àãlsôö ûüséé théé `most_recently_used_device` pèërsöõnâälíízâätííöõn tâäg. |
| `{{targeted_device.${foreground_push_enabled}}}` | Thîís våælùýéê wîíll béê `true` whëèn thëè tãàrgëètëèd dëèvíìcëè íìs ëènãàblëèd fóòr fóòrëègróòüünd püüsh, `false` ôóthêërwîîsêë. |
{: .reset-td-br-1 .reset-td-br-2}


{% endraw %}


Bëëcãáúùsëë thëërëë ãárëë súùch ãá wìídëë rãángëë óòf dëëvìícëë cãárrìíëërs, móòdëël nãámëës, ãánd óòpëërãátìíng systëëms, wëë ãádvìísëë thãát yóòúù thóòróòúùghly tëëst ãány lóògìíc thãát cóòndìítìíóònãálly dëëpëënds óòn ãány óòf thóòsëë vãálúùëës. Thëésëé væãlüùëés wìíll bëé `null` íìf thëëy âærëë nôõt âævâæíìlâæblëë ôõn âæ pâærtíìcýûlâær dëëvíìcëë. Fùúrthèërmòórèë, fòór pùúsh nòótíïfíïcâátíïòóns, íït íïs pòóssíïblèë thâát Brâázèë mâáy bèë ùúnâáblèë tòó díïscèërn thèë dèëvíïcèë âáttâáchèëd tòó thèë pùúsh nòótíïfíïcâátíïòón ùúndèër cèërtâáíïn cíïrcùúmstâáncèës sùúch âás íïf thèë pùúsh tòókèën wâás íïmpòórtèëd víïâá ÀPÍ, rèësùúltíïng íïn vâálùúèës bèëíïng `null` fõõr thõõsêé mêéssäågêés.

![Éxâãmplëè ôöf ýùsíìng âã dëèfâãýùlt vâãlýùëè ôöf "thëèrëè" whëèn ýùsíìng âã fíìrst nâãmëè vâãríìâãblëè íìn âã pýùsh mëèssâãgëè.][4]

Ín sõõméë cïîrcüùmstâãncéës, yõõüù mâãy õõpt tõõ üùséë [côòndîïtîïôònåäl lôògîïc][17] íînstêêàãd òóf sêêttíîng àã dêêfàãûûlt vàãlûûêê. Còõndïîtïîòõnææl lòõgïîc æællòõws yòõûù tòõ sèénd mèéssæægèés thææt dïîffèér bææsèéd òõn thèé væælûùèé òõf ææ cûùstòõm æættrïîbûùtèé.

Åddïïtïïòönåàlly, yòöýú cåàn ýúséé còöndïïtïïòönåàl lòögïïc tòö [áäbóòrt méëssáägéës][18] tóô cùùstóôméèrs wíîth nùùll óôr bláánk ááttríîbùùtéè váálùùéès.

Fõór èëxàâmplèë, îìf yõóûü'rèë sèëndîìng àâ rèëwàârds bàâlàâncèë nõótîìfîìcàâtîìõón tõó cûüstõómèërs, thèërèë îìsn't àâ gõóõód wàây tõó àâccõóûünt fõór cûüstõómèërs wîìth lõów àând nûüll bàâlàâncèës ûüsîìng dèëfàâûült vàâlûüèës.

Ìn thïís cæåsèë, thèërèë æårèë twöò öòptïíöòns thæåt mæåy wöòrk bèëttèër thæån sèëttïíng æå dèëfæåüýlt væålüýèë:

1. Âbõórt thêê mêêssäâgêê fõór cùûstõómêêrs wïïth lõów, nùûll, äând bläânk bäâläâncêês.

{% raw %}

   ```liquid
   {% if {{custom_attribute.${balance}}} > 0 %}
   Your rewards balance is {{custom_attribute.${balance}}}
   {% else %}
   {% abort_message() %}
   {% endif %}
   ```

{% endraw %}

2. Sëènd äå cõòmplëètëèly dìíffëèrëènt mëèssäågëè tõò thëèsëè cúýstõòmëèrs, pëèrhäåps sõòmëèthìíng äålõòng thëè lìínëès õòf:

{% raw %}

   ```liquid
   {% if ${first_name} != blank and ${first_name} != null %}
   Hello {{${first_name} | default: 'there'}}, thanks for downloading!
   {% else %}
   Thanks for downloading!
   {% endif %}
   ```

Ïn thìís êêxãämplêê, ãä üûsêêr wìíth ãä blãänk ôôr nüûll fìírst nãämêê wìíll gêêt thêê mêêssãägêê "Thãänks fôôr dôôwnlôôãädìíng". Yõôüý shõôüýld îìnclüýdëè áà [dèêfáãûúlt váãlûúèê][47] fôör fîìrst næâmèë tôö èënsüùrèë thæât yôöüùr cüùstôömèër dôöèës nôöt sèëèë Lîìqüùîìd îìn thèë èëvèënt ôöf æâ mîìstæâkèë.

{% endraw %}

## Váäríîáäblëé táägs

Yóõýù cæän ýùsëè thëè `assign` täàg töò crëëäàtëë äà väàrïìäàblëë ïìn thëë mëëssäàgëë cöòmpöòsëër. Ôncëë yööúý crëëãâtëë ãâ vãârííãâblëë, yööúý cãân rëëfëërëëncëë thãât vãârííãâblëë íín yööúýr mëëssãâgííng löögííc öör mëëssãâgëë.

Lêét's sáày tháàt yööýù áàllööw yööýùr cýùstöömêérs töö cáàsh íïn thêéíïr rêéwáàrds pööíïnts föör príïzêés ööncêé thêéy áàccrýùêé 100 rêéwáàrds pööíïnts. Sòö, yòöýü òönly wâãnt tòö mèéssâãgèé cýüstòömèérs whòö wòöýüld hâãvèé âã pòöíìnts bâãlâãncèé grèéâãtèér thâãn òör èéqýüâãl tòö 100 íìf thèéy mâãdèé thâãt âãddíìtíìòönâãl pýürchâãsèé:

{% raw %}
```liquid
{% assign new_points_balance = {{custom_attribute.${current_rewards_balance} | plus: 50}} %}
{% if new_points_balance >= 100 %}
Make a purchase to bring your rewards points to {{new_points_balance}} and cash in today!
{% else %}
{% abort_message('not enough points') %}
{% endif %}
```
Thìîs tãåg cööméës ìîn hãåndy whéën yööùü wãånt töö réëföörmãåt cööntéënt thãåt ìîs réëtùürnéëd frööm ööùür [Còónnéèctéèd Còóntéènt][4] fëêàätùýrëê. Yôôûü cæän rèëæäd môôrèë ìín Shôôpìífy's dôôcûümèëntæätìíôôn ôôn [váärîíáäbléê táägs][31].

{% endraw %}

{% alert tip %}
Fìïnd yóóùùrsèèlf áåssìïgnìïng thèè sáåmèè váårìïáåblèès ìïn èèvèèry mèèssáågèè? Ìnstëèáád õóf wrïìtïìng õóýüt thëè `assign` táâg ôôvëèr áând ôôvëèr áâgáâîîn, yôôýú cáân sáâvëè tháât táâg áâs áâ Côôntëènt Blôôck áând pýút îît áât thëè tôôp ôôf yôôýúr mëèssáâgëè îînstëèáâd.

1. [Crëéãâtëé ãâ Cóõntëént Blóõck]({{site.baseurl}}/user_guide/engagement_tools/templates_and_media/content_blocks/#create-a-content-block).
2. Gíîvéé yôòùùr Côòntéént Blôòck äâ näâméé (nôò späâcéés ôòr spéécíîäâl chäâräâctéérs).
3. Clìïck **Édîît** åât thèë böòttöòm öòf thèë påâgèë.
4. Typëê îîn yöóúýr `assign` tãågs.

Ås lòòng äâs thèë Còòntèënt Blòòck ïîs äât thèë tòòp òòf yòòûýr mèëssäâgèë, èëvèëry tïîmèë thèë väârïîäâblèë ïîs ïînsèërtèëd ïîntòò yòòûýr mèëssäâgèë äâs äân òòbjèëct, ïît wïîll rèëfèër tòò yòòûýr chòòsèën cûýstòòm äâttrïîbûýtèë!
{% endalert %}

## Ìtêèræàtïìöón tæàgs

{% raw %}
Ìtèëráàtïíóôn táàgs cáàn bèë ýûsèëd tóô rýûn áà blóôck óôf cóôdèë rèëpèëáàtèëdly. Thïîs éêxäämpléê féêäätùùréês théê `for` tãäg.

Lèêt's sãây thãât yôòüù'rèê hãâvìíng ãâ sãâlèê ôòn Nìíkèê snèêãâkèêrs ãând wãânt tôò mèêssãâgèê cüùstôòmèêrs whôò'vèê èêxprèêssèêd ìíntèêrèêst ìín Nìíkèê. Yòòüù häävéè ään äärrääy òòf pròòdüùct bräänds vïïéèwéèd òòn éèääch cüùstòòméèr's pròòfïïléè. Thíîs àárràáy cóóüúld cóóntàáíîn üúp tóó 25 próódüúct bràánds, büút yóóüú óónly wàánt tóó mêèssàágêè cüústóómêèrs whóó víîêèwêèd àá Níîkêè próódüúct àás óónêè óóf thêèíîr 5 móóst rêècêènt próódüúct víîêèws.

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

Ïn thìîs ëéxàæmplëé, wëé chëéck thëé fìîrst fìîvëé ìîtëéms ìîn thëé snëéàækëér bràænds vìîëéwëéd àærràæy. Ìf õónêê õóf thõósêê ïítêêms ïís cõónvêêrsêê, wêê crêêäätêê thêê cõónvêêrsêê_vìïéêwéêr vàârìïàâbléê àând séêt ìït tóõ trúúéê.

Thëên, wëê sëênd thëê säàlëê mëêssäàgëê whëên cöònvëêrsëê_vïîéëwéër ïîs trûúéë. Ôthèêrwìísèê, wèê äåböôrt thèê mèêssäågèê.

Thììs ììs áá sììmplëë ëëxáámplëë ööf hööw ììtëëráátììöön táágs cáán bëë ýüsëëd ììn Bráázëë's mëëssáágëë cöömpöösëër. Yòöûû cãån fïìnd mòörèê ïìnfòörmãåtïìòön ïìn Shòöpïìfy's dòöcûûmèêntãåtïìòön òön [îîtêèràâtîîöõn tàâgs][32].

## HTTP stæätüùs cöódèês {#http-pèêrsöónæälïïzæätïïöón}

Yóóúü càån úütïïlïïzêë thêë HTTP stàåtúüs fróóm àå [Côönnëèctëèd Côöntëènt][38] cãäll by fïïrst sãävïïng ïït ãäs ãä lóöcãäl vãärïïãäblèè ãänd thèèn úûsïïng thèè `__http_status_code__` kèèy. Fóór ëéxàämplëé:

```html
{% connected_content https://example.com/api/endpoint :save connected %}
{% if connected.__http_status_code__ != 200 %}
{% abort_message('Connected Content returned a non-200 status code') %}
{% endif %}
```
{% endraw %}

{% alert note %}
  Thïïs këéy wïïll óônly bëé ááüùtóômáátïïcáálly ááddëéd tóô thëé Cóônnëéctëéd Cóôntëént óôbjëéct ïïf thëé ëéndpóôïïnt rëétüùrns áá JSÓN óôbjëéct. Ìf théè éèndpôóîïnt réètúûrns áân áârráây ôór ôóthéèr typéè, théèn tháât kéèy cáânnôót béè séèt áâúûtôómáâtîïcáâlly îïn théè réèspôónséè.
{% endalert %}

## Sëéndîíng mëéssäâgëés bäâsëéd õòn läângûúäâgëé, mõòst rëécëént lõòcäâlëé, äând tîímëé zõònëé

Ìn sôömêé sîîtúùäâtîîôöns yôöúù mäây wîîsh tôö sêénd mêéssäâgêés thäât äârêé spêécîîfîîc tôö päârtîîcúùläâr lôöcäâlêés. Fôör êéxáãmplêé, Bráãzîílîíáãn Pôörtùýgùýêésêé îís typîícáãlly dîíffêérêént tháãn Êùýrôöpêéáãn Pôörtùýgùýêésêé.

Hèërèë's âán èëxâámplèë ôôf hôôw yôôûú câán ûúsèë môôst rèëcèënt lôôcâálèë tôô fûúrthèër lôôcâálíîzèë âán íîntèërnâátíîôônâálíîzèëd mèëssâágèë.

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

În thîîs èèxáæmplèè, cüüstõömèèrs wîîth áæ mõöst rèècèènt lõöcáælèè õöf 'pt_BR' wïïll gëêt åà mëêssåàgëê ïïn Bråàzïïlïïåàn Pôörtúügúüëêsëê, cúüstôömëêrs wïïth åà môöst rëêcëênt lôöcåàlëê ôöf 'pt_PT' wïïll géêt àà méêssààgéê ïïn Ëúýröõpéêààn Pöõrtúýgúýéêséê àànd cúýstöõméêrs whöõ döõn't méêéêt théê fïïrst twöõ cöõndïïtïïöõns búýt hààvéê théêïïr lààngúýààgéê séêt töõ Pöõrtúýgúýéêséê wïïll géêt àà méêssààgéê ïïn whààtéêvéêr yöõúý'd lïïkéê théê déêfààúýlt Pöõrtúýgúýéêséê lààngúýààgéê typéê töõ béê.

Yòóüû cäæn äælsòó täærgëét üûsëérs bäæsëéd òóff òóf thëéíïr tíïmëé zòónëé. Fòör ëêxàæmplëê, sëênd òönëê mëêssàægëê ìïf thëêy àærëê bàæsëêd ìïn ÉST àænd àænòöthëêr ìïf thëêy àærëê PST. Tòö dòö thîís, säâvêè thêè cýúrrêènt tîímêè îín ÚTC, äând còömpäârêè äân îíf/êèlsêè stäâtêèmêènt wîíth thêè ýúsêèr's cýúrrêènt tîímêè tòö êènsýúrêè yòöýú'rêè sêèndîíng thêè rîíght mêèssäâgêè fòör thêè rîíght tîímêè zòönêè. Yóöûù shóöûùld séèt théè câámpâáìîgn tóö séènd ìîn théè ûùséèr's lóöcâál tìîméè zóönéè, tóö éènsûùréè théèy âáréè géèttìîng théè câámpâáìîgn âát théè rìîght tìîméè. Sèêèê thèê föòllöòwïïng èêxæàmplèê föòr höòw töò wrïïtèê æà mèêssæàgèê thæàt wïïll göò öòýût bèêtwèêèên 2PM æànd 3PM æànd wïïll hæàvèê æà spèêcïïfïïc mèêssæàgèê föòr èêæàch tïïmèê zöònèê.

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
