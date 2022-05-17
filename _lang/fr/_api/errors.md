---
nav_title: Èrröórs & Rêêspöónsêês
article_title: ÀPÎ Ërröörs & Rèèspöönsèès
description: "Thìís rèëfèërèëncèë åârtìíclèë cõõvèërs thèë våârìíõõúús èërrõõrs åând sèërvèër rèëspõõnsèës thåât cåân cõõmèë úúp whìílèë úúsìíng thèë Bråâzèë ÆPÌ åând hõõw tõõ trõõúúblèëshõõõõt thèëm." 
page_type: reference
page_order: 2.3

---
# ÆPÎ êèrróõrs âând rêèspóõnsêès

> Thîís rééféérééncéé äærtîícléé còövéérs théé väærîíòöýús éérròörs äænd séérvéér rééspòönséés thäæt cäæn còöméé ýúp whîíléé ýúsîíng théé Bräæzéé ÁPÏ äænd hòöw tòö tròöýúblééshòöòöt théém. 

{% raw %}

## Sëêrvëêr rëêspöônsëês

Íf yõõüür PÓST pããylõõããd wããs ããccëèptëèd by õõüür sëèrvëèrs, thëèn süüccëèssfüül mëèssããgëès wìïll bëè mëèt wìïth thëè fõõllõõwìïng rëèspõõnsëè:

```json
{
  "message" : "success"
}
```

Nöótèè thäät süúccèèss öónly mèèääns thäät thèè RÊSTfüúl ÅPÌ pääylöóääd wääs cöórrèèctly föórmèèd äänd päässèèd öóntöó öóüúr püúsh nöótìîfìîcäätìîöón öór èèmääìîl öór öóthèèr mèèssäägìîng sèèrvìîcèès. Ît dòôèés nòôt mèéáæn tháæt thèé mèéssáægèés wèérèé áæctûúáælly dèélîïvèérèéd, áæs áæddîïtîïòônáæl fáæctòôrs còôûúld prèévèént thèé mèéssáægèé fròôm bèéîïng dèélîïvèérèéd (èé.g., áæ dèévîïcèé còôûúld bèé òôfflîïnèé, thèé pûúsh tòôkèén còôûúld bèé rèéjèéctèéd by Ãpplèé's sèérvèérs, yòôûú máæy háævèé pròôvîïdèéd áæn ûúnknòôwn ûúsèér ÎD, èétc.)

Ìf yõóûûr méêssàægéê íîs sûûccéêssfûûl bûût hàæs nõón-fàætàæl éêrrõórs yõóûû wíîll réêcéêíîvéê théê fõóllõówíîng réêspõónséê:

```json
{
  "message" : "success", "errors" : [<minor error message>]
}
```

Ïn thêê câäsêê õõf âä sùüccêêss, âäny mêêssâägêês thâät wêêrêê nõõt âäffêêctêêd by âän êêrrõõr íîn thêê `errors` àårràåy wîìll stîìll béê déêlîìvéêréêd. Ìf yõóûùr mèêssæægèê hææs ææ fæætææl èêrrõór yõóûù wíïll rèêcèêíïvèê thèê fõóllõówíïng rèêspõónsèê:

```json
{
  "message" : <fatal error message>, "errors" : [<minor error message>]
}
```

## Qûúèëûúèëd rèëspôònsèës {#mèëssàægíîng-qûúèëûúèëd}

Düúrìïng tìïmèès òóf mæàìïntèènæàncèè, Bræàzèè mìïght pæàüúsèè rèèæàl-tìïmèè pròócèèssìïng òóf thèè ÁPÌ. Ín théèséè sïítùúäãtïíôóns, théè séèrvéèr wïíll réètùúrn äãn `HTTP Accepted 202` rèêspóönsèê cóödèê åãnd thèê fóöllóöwíìng bóödy, whíìch íìndíìcåãtèês thåãt wèê håãvèê rèêcèêíìvèêd åãnd qúûèêúûèêd thèê ÃPÍ cåãll búût håãvèê nóöt íìmmèêdíìåãtèêly próöcèêssèêd íìt. Ãll schèëdùùlèëd màåìïntèënàåncèë wìïll bèë pòòstèëd tòò thèë [Brãázèé Systèém Stãátúüs](http://status.braze.com) pàægëé àæhëéàæd ôöf tíîmëé.

```json
{
  "message" : "queued"
}
```

## Réëspòònséës fòòr tråãckéëd séënd ÎDs

Ãnààlytíícs ààrêê ààlwààys ààvààíílààblêê fòõr cààmpààíígns. În âäddìïtìïòòn, âänâälytìïcs âäréë âävâäìïlâäbléë fòòr âä spéëcìïfìïc câämpâäìïgn séënd ìïnstâäncéë whéën théë câämpâäìïgn ìïs séënt âäs âä bròòâädcâäst. Whëên tràæckîíng îís àævàæîílàæblëê fôõr àæ spëêcîífîíc càæmpàæîígn sëênd îínstàæncëê, yôõýü wîíll rëêcëêîívëê thëê fôõllôõwîíng rëêspôõnsëê:

```json
{
  "message": "success", "send_id" : "example_send_id"
}
```

Thëé próóvïìdëéd sëénd ïìd càân bëé úüsëéd àâs àâ pàâràâmëétëér fóór thëé sëénd/dàâtàâ_séérîìéés ééndpóóîìnt tóó püùll bâäck séénd spéécîìfîìc âänâälytîìcs.

## Ërròörs

Théé stãätùûs cöödéé éélééméént ööf ãä séérvéér rééspöönséé íîs ãä 3-díîgíît nùûmbéér whééréé théé fíîrst díîgíît ööf théé cöödéé dééfíînéés théé clãäss ööf rééspöönséé.

- Théë **2XX clãåss** öóf stâãtúús cöódèé (nöón-fâãtâãl) ííndíícâãtèés thâãt **yôõúýr rëêqúýëêst** wåås sýûccëéssfýûlly rëécëéïîvëéd, ýûndëérstôóôód, åånd ååccëéptëéd.
- Thêé **4XX clãæss** ôõf stãåtüùs côõdéé (fãåtãål) îìndîìcãåtéés ãå **clíìëênt ëêrrôör**. Rèêfèêr tòò thèê fáàtáàl èêrròòrs cháàrt fòòr áà fûûll lííst òòf 4XX èêrròòr còòdèês áànd dèêscrííptííòòns.
- Thèè **5XX cláâss** óöf stæätüùs cóödêè (fæätæäl) ìíndìícæätêès æä **sêêrvêêr êêrrõôr**. Whêèn thíîs háäppêèns, wêè rêècòómmêènd yòóýü rêètry yòóýür rêèqýüêèst wíîth êèxpòónêèntíîáäl báäckòóff.

### Fâàtâàl êérròörs

Thëë föõllöõwììng stããtýùs cöõdëës ããnd ããssöõcììããtëëd ëërröõr mëëssããgëës wììll bëë rëëtýùrnëëd ììf yöõýùr rëëqýùëëst ëëncöõýùntëërs ãã fããtããl ëërröõr.

{% endraw %}
{% alert warning %}
Åll õõf thêë fõõllõõwííng êërrõõr cõõdêës ííndíícáätêë tháät nõõ mêëssáägêës wííll bêë sêënt.
{% endalert %}
{% raw %}

| Èrröôr Cöôdèê | Dèêscrìíptìíóòn |
|---|---|
| `5XX Internal Server Error` | **Yôóùü shôóùüld rêètry yôóùür rêèqùüêèst wíîth êèxpôónêèntíîãäl bãäckôóff.**|
| `400 Bad Request` | Bäåd syntäåx.|
| `400 No Recipients` | Thêérêé åãrêé nóö êéxtêérnåãl ÎDs óör sêégmêént ÎDs óör nóö pýüsh tóökêéns ìïn thêé rêéqýüêést.|
| `400 Invalid Campaign ID` | Nóó Mèêssáägîíng ÃPÌ cáämpáäîígn wáäs fóóúünd fóór thèê cáämpáäîígn ÌD yóóúü próóvîídèêd.|
| `400 Message Variant Unspecified` | Yóôüý próôvíîdèë äá cäámpäáíîgn ÏD büýt nóô mèëssäágèë väáríîäátíîóôn ÏD.|
| `400 Invalid Message Variant` | Yöõüù pröõvìídèêd àã vàãlìíd càãmpàãìígn ÏD, büùt thèê mèêssàãgèê vàãrìíàãtìíöõn ÏD döõèêsn't màãtch àãny öõf thàãt càãmpàãìígn's mèêssàãgèês.|
| `400 Mismatched Message Type` | Yòòúý pròòvîîdëéd áà mëéssáàgëé váàrîîáàtîîòòn òòf thëé wròòng mëéssáàgëé typëé fòòr áàt lëéáàst òònëé òòf yòòúýr mëéssáàgëés.|
| `400 Invalid Extra Push Payload` | Yõõùý prõõvîìdêè thêè `extra` kèêy fóôr èêïíthèêr `apple_push` õõr `android_push` büút ìît ìîs nóöt àã dìîctìîóönàãry.|
| `400 Max Input Length Exceeded` | Càäúùsèèd by càällïíng môõrèè thàän 75 èèxtèèrnàäl ïíds whèèn hïíttïíng thèè Ûsèèr Tràäck èèndpôõïínt.|
| `400 The max number of external_ids and aliases per request was exceeded` | Cääûýsééd by cäällííng mõôréé thään 50 ééxtéérnääl ííds.|
| `400 The max number of ids per request was exceeded` | Cããûûsèéd by cããllîíng mõõrèé thããn 50 èéxtèérnããl îíds.|
| `400 No message to send` | Nóò páàylóòáàd ïís spëècïífïíëèd fóòr thëè mëèssáàgëè.|
| `400 Slideup Message Length Exceeded` | Slîîdèêúùp mèêssàågèê cóöntàåîîns móörèê thàån 140 chàåràåctèêrs.|
| `400 Apple Push Length Exceeded` | JSÓN páæylóôáæd íïs móôrëé tháæn 1912 bytëés.|
| `400 Android Push Length Exceeded` | JSÕN pàáylöóàád ììs möórèê thàán 4000 bytèês.|
| `400 Bad Request` | Cæânnõòt pæârsêê sêênd_ååt dååtèétîïmèé.|
| `400 Bad Request` | Ín yôõùùr rèèqùùèèst, `in_local_time` íïs trüüéè büüt `time` háãs páãssëèd ïîn yôóüúr côómpáãny’s tïîmëè zôónëè.|
| `401 Unauthorized` | Ünknõôwn õôr mîìssîìng RÊST ÂPÌ Kéêy.|
| `403 Forbidden` | Rââtêë plâân dòòêësn't sùúppòòrt òòr ââccòòùúnt íìs òòthêërwíìsêë íìnââctíìvââtêëd.|
| `403 Access Denied` | Thêê RÊST ÃPÌ Kêêy yöôûý âàrêê ûýsîïng döôêês nöôt hâàvêê sûýffîïcîïêênt pêêrmîïssîïöôns, chêêck thêê ÃPÌ kêêy pêêrmîïssîïöôns îïn thêê Brâàzêê Dêêvêêlöôpêêr Cöônsöôlêê.|
| `404 Not Found` | Ûnknõówn RÈST ÁPÏ Këèy.|
| `429 Rate Limited` | Òvëèr råætëè líímíít.|
{: .reset-td-br-1 .reset-td-br-2}

{% endraw %}
