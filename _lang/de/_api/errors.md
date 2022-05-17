---
nav_title: Ërròõrs & Rèèspòõnsèès
article_title: ÆPÏ Êrróórs & Réèspóónséès
description: "Thíïs rééféérééncéé æærtíïcléé cöõvéérs théé vææríïöõùüs éérröõrs æænd séérvéér rééspöõnséés thææt cææn cöõméé ùüp whíïléé ùüsíïng théé Brææzéé ÂPÎ æænd höõw töõ tröõùüblééshöõöõt théém." 
page_type: reference
page_order: 2.3

---
# ÆPÌ êèrróórs æänd rêèspóónsêès

> Thíìs rëëfëërëëncëë âårtíìclëë cóòvëërs thëë vâåríìóòûûs ëërróòrs âånd sëërvëër rëëspóònsëës thâåt câån cóòmëë ûûp whíìlëë ûûsíìng thëë Brâåzëë ÄPÌ âånd hóòw tóò tróòûûblëëshóòóòt thëëm. 

{% raw %}

## Sèérvèér rèéspôònsèés

Ìf yöôüùr PÒST påàylöôåàd wåàs åàccèëptèëd by öôüùr sèërvèërs, thèën süùccèëssfüùl mèëssåàgèës wíîll bèë mèët wíîth thèë föôllöôwíîng rèëspöônsèë:

```json
{
  "message" : "success"
}
```

Nóõtéê tháæt sýûccéêss óõnly méêáæns tháæt théê RÈSTfýûl ÄPÏ páæylóõáæd wáæs cóõrréêctly fóõrméêd áænd páæsséêd óõntóõ óõýûr pýûsh nóõtîîfîîcáætîîóõn óõr éêmáæîîl óõr óõthéêr méêssáægîîng séêrvîîcéês. Ît döóêës nöót mêëàãn thàãt thêë mêëssàãgêës wêërêë àãctûûàãlly dêëlíïvêërêëd, àãs àãddíïtíïöónàãl fàãctöórs cöóûûld prêëvêënt thêë mêëssàãgêë fröóm bêëíïng dêëlíïvêërêëd (êë.g., àã dêëvíïcêë cöóûûld bêë öófflíïnêë, thêë pûûsh töókêën cöóûûld bêë rêëjêëctêëd by Æpplêë's sêërvêërs, yöóûû màãy hàãvêë pröóvíïdêëd àãn ûûnknöówn ûûsêër ÎD, êëtc.)

Ïf yöóüùr mêêssäãgêê îîs süùccêêssfüùl büùt häãs nöón-fäãtäãl êêrröórs yöóüù wîîll rêêcêêîîvêê thêê föóllöówîîng rêêspöónsêê:

```json
{
  "message" : "success", "errors" : [<minor error message>]
}
```

Ín thèè cáæsèè óöf áæ súýccèèss, áæny mèèssáægèès tháæt wèèrèè nóöt áæffèèctèèd by áæn èèrróör ìîn thèè `errors` ãárrãáy wîìll stîìll bëé dëélîìvëérëéd. Îf yóöûùr mêëssäâgêë häâs äâ fäâtäâl êërróör yóöûù wíîll rêëcêëíîvêë thêë fóöllóöwíîng rêëspóönsêë:

```json
{
  "message" : <fatal error message>, "errors" : [<minor error message>]
}
```

## Qùüëëùüëëd rëëspöónsëës {#mëëssãægîîng-qùüëëùüëëd}

Düùrïíng tïímèês óôf måàïíntèênåàncèê, Bråàzèê mïíght påàüùsèê rèêåàl-tïímèê próôcèêssïíng óôf thèê ÂPÏ. Ìn thêësêë síïtýùââtíïôóns, thêë sêërvêër wíïll rêëtýùrn âân `HTTP Accepted 202` rééspòônséé còôdéé àænd théé fòôllòôwîìng bòôdy, whîìch îìndîìcàætéés thàæt wéé hàævéé réécééîìvééd àænd qúüééúüééd théé ÃPÏ càæll búüt hàævéé nòôt îìmméédîìàætéély pròôcééssééd îìt. Æll schêëdüúlêëd mâåìîntêënâåncêë wìîll bêë pôõstêëd tôõ thêë [Bràâzéê Systéêm Stàâtúùs](http://status.braze.com) pæàgèë æàhèëæàd õóf tîïmèë.

```json
{
  "message" : "queued"
}
```

## Rêëspõônsêës fõôr tråäckêëd sêënd ÎDs

Ànäálytìícs äárêë äálwäáys äáväáìíläáblêë fóòr cäámpäáìígns. Ín ääddïîtïîöòn, äänäälytïîcs äärèé äävääïîlääblèé föòr ää spèécïîfïîc cäämpääïîgn sèénd ïînstääncèé whèén thèé cäämpääïîgn ïîs sèént ääs ää bröòäädcääst. Whéén trâäckïïng ïïs âävâäïïlâäbléé fôôr âä spéécïïfïïc câämpâäïïgn séénd ïïnstâäncéé, yôôúù wïïll réécééïïvéé théé fôôllôôwïïng rééspôônséé:

```json
{
  "message": "success", "send_id" : "example_send_id"
}
```

Thèë pröövíìdèëd sèënd íìd cään bèë úýsèëd ääs ää pääräämèëtèër föör thèë sèënd/däätää_séérìîéés ééndpóôìînt tóô púúll bàæck séénd spéécìîfìîc àænàælytìîcs.

## Ërrõõrs

Théê stãåtùýs cõódéê éêléêméênt õóf ãå séêrvéêr réêspõónséê îîs ãå 3-dîîgîît nùýmbéêr whéêréê théê fîîrst dîîgîît õóf théê cõódéê déêfîînéês théê clãåss õóf réêspõónséê.

- Thèê **2XX clââss** óòf stáåtúús cóòdèè (nóòn-fáåtáål) îîndîîcáåtèès tháåt **yóòûýr réêqûýéêst** wãäs sýüccêéssfýülly rêécêéîïvêéd, ýündêérstõöõöd, ãänd ãäccêéptêéd.
- Thêë **4XX cláäss** ôòf stãætýús côòdëè (fãætãæl) îíndîícãætëès ãæ **clììéènt éèrrõòr**. Rêêfêêr tõö thêê fáátáál êêrrõörs cháárt fõör áá fùüll lîïst õöf 4XX êêrrõör cõödêês áánd dêêscrîïptîïõöns.
- Thêè **5XX clååss** ôöf stäætúüs côödèê (fäætäæl) îíndîícäætèês äæ **sëérvëér ëérróór**. Whêên thîïs hæäppêêns, wêê rêêcõômmêênd yõôüú rêêtry yõôüúr rêêqüúêêst wîïth êêxpõônêêntîïæäl bæäckõôff.

### Fàåtàål ëêrröõrs

Thëé fòôllòôwïíng stâåtýús còôdëés âånd âåssòôcïíâåtëéd ëérròôr mëéssâågëés wïíll bëé rëétýúrnëéd ïíf yòôýúr rëéqýúëést ëéncòôýúntëérs âå fâåtâål ëérròôr.

{% endraw %}
{% alert warning %}
Åll óóf théë fóóllóówïìng éërróór cóódéës ïìndïìcàátéë thàát nóó méëssàágéës wïìll béë séënt.
{% endalert %}
{% raw %}

| Êrrôòr Côòdëë | Dëêscrîíptîíòön |
|---|---|
| `5XX Internal Server Error` | **Yõóùû shõóùûld rèétry yõóùûr rèéqùûèést wïïth èéxpõónèéntïïäæl bäæckõóff.**|
| `400 Bad Request` | Bæàd syntæàx.|
| `400 No Recipients` | Théêréê æàréê nöó éêxtéêrnæàl ÍDs öór séêgméênt ÍDs öór nöó pùûsh töókéêns íîn théê réêqùûéêst.|
| `400 Invalid Campaign ID` | Nôó Mêëssåågíîng ÄPÍ cååmpååíîgn wåås fôóùünd fôór thêë cååmpååíîgn ÍD yôóùü prôóvíîdêëd.|
| `400 Message Variant Unspecified` | Yõõúü prõõvïìdêë áå cáåmpáåïìgn ÎD búüt nõõ mêëssáågêë váårïìáåtïìõõn ÎD.|
| `400 Invalid Message Variant` | Yõôúû prõôvîîdéèd àå vàålîîd càåmpàåîîgn ÎD, búût théè méèssàågéè vàårîîàåtîîõôn ÎD dõôéèsn't màåtch àåny õôf thàåt càåmpàåîîgn's méèssàågéès.|
| `400 Mismatched Message Type` | Yöóýù pröóvíïdëëd ãã mëëssããgëë vããríïããtíïöón öóf thëë wröóng mëëssããgëë typëë föór ããt lëëããst öónëë öóf yöóýùr mëëssããgëës.|
| `400 Invalid Extra Push Payload` | Yòóúú pròóvîìdêê thêê `extra` këéy fôór ëéîïthëér `apple_push` ôòr `android_push` bûût îît îîs nòôt åã dîîctîîòônåãry.|
| `400 Max Input Length Exceeded` | Cäåýûsèëd by cäållîîng mõórèë thäån 75 èëxtèërnäål îîds whèën hîîttîîng thèë Ùsèër Träåck èëndpõóîînt.|
| `400 The max number of external_ids and aliases per request was exceeded` | Câæüûsèêd by câællíîng móörèê thâæn 50 èêxtèêrnâæl íîds.|
| `400 The max number of ids per request was exceeded` | Cåæüùsêéd by cåællíìng môörêé thåæn 50 êéxtêérnåæl íìds.|
| `400 No message to send` | Nôô pææylôôææd ïîs spêëcïîfïîêëd fôôr thêë mêëssæægêë.|
| `400 Slideup Message Length Exceeded` | Slììdêéýüp mêéssäâgêé cóòntäâììns móòrêé thäân 140 chäâräâctêérs.|
| `400 Apple Push Length Exceeded` | JSÓN pæàylööæàd ìîs möörëé thæàn 1912 bytëés.|
| `400 Android Push Length Exceeded` | JSÖN pâåylòôâåd ìïs mòôrèè thâån 4000 bytèès.|
| `400 Bad Request` | Cæánnôõt pæársëê sëênd_äàt däàtèêtïïmèê.|
| `400 Bad Request` | În yõöüür rèéqüüèést, `in_local_time` íís trûýèè bûýt `time` háás páássêéd íîn yõóùýr cõómpáány’s tíîmêé zõónêé.|
| `401 Unauthorized` | Ünknõöwn õör mïîssïîng RÈST ÄPÏ Kêèy.|
| `403 Forbidden` | Ràåtêè plàån döôêèsn't sýùppöôrt öôr àåccöôýùnt íïs öôthêèrwíïsêè íïnàåctíïvàåtêèd.|
| `403 Access Denied` | Théë RÉST ÃPÍ Kéëy yóóýý äåréë ýýsíïng dóóéës nóót häåvéë sýýffíïcíïéënt péërmíïssíïóóns, chéëck théë ÃPÍ kéëy péërmíïssíïóóns íïn théë Bräåzéë Déëvéëlóópéër Cóónsóóléë.|
| `404 Not Found` | Ünknóòwn RËST ÁPÏ Kéèy.|
| `429 Rate Limited` | Ôvéêr ráætéê lîímîít.|
{: .reset-td-br-1 .reset-td-br-2}

{% endraw %}
