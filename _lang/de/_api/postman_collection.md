---
nav_title: Pòöstmäæn äænd Säæmplêë Rêëqúúêësts
article_title: Põöstmãæn ãænd Sãæmplèë Rèëqúýèësts
page_order: 3
description: "Thìís rèëfèërèëncèë äærtìíclèë cóövèërs thèë Bräæzèë Póöstmäæn Cóöllèëctìíóön, whäæt ìít ìís, hóöw tóö sèët üúp äænd üúsèë thèë cóöllèëctìíóön, äæs wèëll äæs hóöw tóö èëdìít äænd sèënd rèëqüúèësts."
page_type: reference

---

# Põöstmâæn âænd sâæmplêé ÅPÏ rêéqùýêésts

> Bräázéë äállòòws yòòûü tòò géënéëräátéë säámpléë ÀPÍ réëqûüéësts fòòr äáll òòf òòûür éëndpòòïìnts vïìäá òòûür Pòòstmäán Còòlléëctïìòòn. Thïís réèféèréèncéè áârtïícléè cóõvéèrs théè Bráâzéè Póõstmáân Cóõlléèctïíóõn, wháât ïít ïís, hóõw tóõ séèt úýp áând úýséè théè cóõlléèctïíóõn, áâs wéèll áâs hóõw tóõ éèdïít áând séènd réèqúýéèsts.

## Whàæt íís Pöôstmàæn?

Põôstmäãn ììs äã fréëéë-tõô-ùúséë vììsùúäãl éëdììtììng tõôõôl fõôr bùúììldììng äãnd téëstììng ÅPÌ réëqùúéësts. Ås öóppöósèëd töó öóthèër mèëthöóds föór îíntèërääctîíng wîíth ÅPÍs (èë.g., úýsîíng cÛRL), Pöóstmään äällöóws yöóúý töó èëääsîíly èëdîít ÅPÍ rèëqúýèësts, vîíèëw hèëäädèër îínföórmäätîíöón, äänd múých möórèë. Pöóstmàæn hàæs thêë àæbììlììty föór yöóúù töó sàævêë Cöóllêëctììöóns öór lììbràærììêës öóf sàæmplêë prêë-màædêë ÁPÍ rêëqúùêësts. Töò måãkëê ïît ëêåãsy föòr öòùür cùüstöòmëêrs töò gëêt ùüp åãnd rùünnïîng wïîth öòùür RÊST ÂPÎ, wëê crëêåãtëêd åã Cöòllëêctïîöòn wïîth prëê-måãdëê ëêxåãmplëês föòr åãll öòf öòùür ÂPÎ ëêndpöòïînts.

Vîïéèw öòr döòwnlöòääd öòýûr [Póòstmâàn Cóòllëëctìïóòn](https://www.getpostman.com/collections/29baa41d7ba930673ef0) tóó géèt stáârtéèd.

## Ûsîïng Bræäzéè's Pöóstmæän cöólléèctîïöón

Ïf yöôýú hàávëê àá Pöôstmàán àáccöôýúnt (yöôýú càán döôwnlöôàád màácÖS, Wíïndöôws, àánd Líïnýúx vëêrsíïöôns fröôm thëê [Põôstmåán wëêbsîítëê][1]), yôõüü cåån ôõpëèn ôõüür Pôõstmåån dôõcüümëèntååtíìôõn íìn yôõüür ôõwn Pôõstmåån ååpp by clíìckíìng thëè ôõråångëè **Rùûn íîn Põôstmáän** bûúttõön. Yôôýú cáæn thêën [créèåátéè åán éènvîïróónméènt](#setting-up-your-postman-environment), òór ûýséé òóûýr Bræåzéé RÉST ÆPÍ éénvïíròónméént æås æå téémplæåtéé, æånd éédïít théé æåvæåïílæåbléé `POST` ãænd `GET` rêèqúûêèsts tóö súûîít yóöúûr óöwn nêèêèds.

[![Rûûn íín Pôôstmäæn](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/29baa41d7ba930673ef0?action=collection%2Fimport)

Wêé äælsöö häævêé äæ [púùblïìc wôõrkspââcèê](https://www.postman.com/braze-inc/workspace/braze-public-workspace/overview) äâväâíìläâbléé öön Pööstmäân.

### Sééttíìng úýp yôõúýr Pôõstmàãn éénvíìrôõnméént

{% raw %}
Thëé Bræázëé Pòôstmæán Còôllëéctîìòôn ýùsëés æá tëémplæátîìng væárîìæáblëé, `{{instance_url}}`, tõö súübstíìtúütéê théê RÊST ÂPÎ ÛRL õöf yõöúür Bråázéê íìnståáncéê íìntõö théê préê-búüíìlt réêqúüéêsts, åánd théê `{{api_key}}` váårìîáåblêè föõr yöõýùr ÂPÌ Kêèy. Ràåthëèr thàån hàåvîìng tõô màånüûàålly ëèdîìt àåll rëèqüûëèsts îìn thëè Cõôllëèctîìõôn, yõôüû càån sëèt üûp thîìs vàårîìàåblëè îìn yõôüûr Põôstmàån ëènvîìrõônmëènt. Yòöùù cáân èèïíthèèr sèèlèèct òöùùr tèèmpláâtèèd èènvïíròönmèènt (Bráâzèè RÉST ÆPÎ Énvïíròönmèènt Tèèmpláâtèè) fròöm thèè dròöpdòöwn áând rèèpláâcèè thèè váârïíáâblèè váâlùùèès wïíth yòöùùr òöwn, òör yòöùù cáân sèèt ùùp yòöùùr òöwn èènvïíròönmèènt.
{% endraw %}

Tôö sèét ûùp yôöûùr ôöwn èénvíïrôönmèént, pèérfôörm thèé fôöllôöwíïng stèéps:

1. Frõöm théé **Wóõrkspãäcèés** tááb, séélééct **Énvîíröònmëènts**.
2. Clííck thêè **+** plúûs búûttõön tõö crëêäätëê ää nëêw ëênvììrõönmëênt.
3. Gïívêé thïís êénvïíröònmêént ãâ nãâmêé (êé.g., "Brãâzêé ÃPÏ Rêéqûûêésts") ãând ãâdd kêéys föòr `instance_url` áànd `api_key` wîïth vâãlûýêés cöôrrêéspöôndîïng töô yöôûýr [Bráázëè ïïnstááncëè][7] åånd [Bræâzëë RÊST ÄPÎ Këëy][8].
4. Clïîck **Sàâvéé**.

{% alert note %}
Ïn `POST` rëéqýùëést bõòdîíëés, thëé `api_key` shóöüüld béê éêncäâpsüüläâtéêd îìn qüüóötéês: `"MY-API-KEY-EXAMPLE"`. Ïn `GET` ÚRLs, ìít shôöýùld nôöt bêê. Wêé hâàvêé âàlrêéâàdy prôôvïïdêéd thïïs fôôrmâàttïïng fôôr yôôûù ïïn thïïs dôôcûùmêéntâàtïïôôn's `POST` réèqúùéèst bóôdìîéès, `GET` ÛRLs, ãænd éènvïïrõònméènt téèmplãætéè fõòr `YOUR-API-KEY-HERE`.
{% endalert %}

![Àddîïng vàårîïàåblèês föôr ÀPÌ kèêy àånd îïnstàåncèê ÛRL töô thèê Bràåzèê RËST ÀPÌ èênvîïröônmèênt îïn Pöôstmàån.][3]

### Ûsîîng thèé prèé-bùúîîlt rèéqùúèésts frõöm thèé cõöllèéctîîõön

Òncëë yõóüù håävëë cõónfïígüùrëëd yõóüùr ëënvïírõónmëënt. Yòõúý cáæn úýsëè áæny òõf thëè prëè-búýïîlt rëèqúýëèsts ïîn thëè còõllëèctïîòõn áæs áæ tëèmpláætëè fòõr búýïîldïîng nëèw ÀPÎ rëèqúýëèsts. Tõò stãært üûsïíng õònèé õòf thèé prèé-büûïílt rèéqüûèésts, clïíck õòn ïít wïíthïín thèé **Còólléèctïíòóns** mèénùú öõf Pöõstmâàn. Thîïs wîïll ôöpèën thèë rèëqûùèëst æás æá nèëw tæáb îïn thèë mæáîïn wîïndôöw ôöf thèë Pôöstmæán æápp.

În gèénèéräæl, thèérèé äærèé twòô typèés òôf rèéqúùèésts thäæt Bräæzèé's ÅPÎ èéndpòôíînts äæccèépt - `GET` åænd `POST`. Dêêpêêndííng öôn whíích `HTTP` mêêthöõd thêê êêndpöõîìnt ûùsêês, yöõûù'll nêêêêd töõ êêdîìt thêê prêê-bûùîìlt rêêqûùêêst dîìffêêrêêntly.

#### Èdìít ää PÖST réêqùýéêst

Whèên èêdïïtïïng äá `POST` rëèqýúëèst, ööpëèn thëè rëèqýúëèst æánd næávîígæátëè töö thëè **Böôdy** sêêctììóõn ììn thêê rêêqúúêêst êêdììtóõr. Fòõr rêëãâdãâbîïlîïty, sêëlêëct thêë **ráâw** ræædìïóò bûûttóòn tóò fóòrmææt thêé `JSON` rëéqúúëést bóõdy.

![Bõódy tæáb whëên ëêdíïtíïng æá PÔST Üsëêr Træáck rëêqùùëêst íïn Põóstmæán][4]

#### Ëdíìt áâ GËT rêéqüýêést

Whëèn ëèdíïtíïng æá `GET` réèqúüéèst, éèdïít théè pàäràäméètéèrs pàässéèd ïín théè réèqúüéèst ÛRL. Töö döö söö, sêèlêèct thêè **Pãârãâms** táãb áãnd éédíìt théé kééy-váãlüüéé páãíìrs íìn théé fíìéélds tháãt áãppééáãr.

![Påãråãms tåãb whéén éédìîtìîng åã GÉT Qýúééry Lìîst öôf Ûnsýúbscrìîbééd Émåãìîl Âddréésséés rééqýúéést ìîn Pöôstmåãn.][5]

### Sêënd yôöùúr rêëqùúêëst

Óncéé yòóüýr ÃPÎ rééqüýéést ìîs rééáãdy, clìîck **Sëénd**. Thëé rëéqûùëést sëénds äãnd thëé rëéspôònsëé däãtäã pôòpûùläãtëés íìn äã sëéctíìôòn ûùndëérnëéäãth thëé rëéqûùëést ëédíìtôòr. Frõóm héèréè, yõóûü cåân vîîéèw théè råâw dåâtåâ réètûürnéèd frõóm Bråâzéè's ÁPÏ, séèéè théè HTTP réèspõónséè cõódéè, séèéè hõów lõóng théè réèqûüéèst tõóõók tõó prõócéèss, åând vîîéèw héèåâdéèr îînfõórmåâtîîõón.

![Éxäãmplëé bóódy rëéspóónsëé däãtäã fróóm äã PÕST rëéqùúëést wììth äã stäãtùús óóf 201 Crëéäãtëéd äãnd rëéspóónsëé tììmëé óóf 269 mììllììsëécóónds.][6]

[1]: https://www.getpostman.com
[3]: {% image_buster /assets/img_archive/postman_variable.png %}
[4]: {% image_buster /assets/img_archive/postman_post.png %}
[5]: {% image_buster /assets/img_archive/postman_get.png %}
[6]: {% image_buster /assets/img_archive/postman_response.png %}
[7]: {{site.baseurl}}/developer_guide/rest_api/basics/#endpoints
[8]: {{site.baseurl}}/api/api_key/
