---
nav_title: Pôöstmæàn æànd Sæàmplëè Rëèqûüëèsts
article_title: Põõstmáân áând Sáâmplëê Rëêqýùëêsts
page_order: 3
description: "Thîïs rèêfèêrèêncèê æärtîïclèê cöòvèêrs thèê Bræäzèê Pöòstmæän Cöòllèêctîïöòn, whæät îït îïs, höòw töò sèêt ùüp æänd ùüsèê thèê cöòllèêctîïöòn, æäs wèêll æäs höòw töò èêdîït æänd sèênd rèêqùüèêsts."
page_type: reference

---

# Põõstmáän áänd sáämpléé ÄPÏ rééqýùéésts

> Brææzèë æællòöws yòöùý tòö gèënèëræætèë sææmplèë ÀPÎ rèëqùýèësts fòör ææll òöf òöùýr èëndpòöíïnts víïææ òöùýr Pòöstmææn Còöllèëctíïòön. Thìís rêèfêèrêèncêè àártìíclêè còövêèrs thêè Bràázêè Pòöstmàán Còöllêèctìíòön, whàát ìít ìís, hòöw tòö sêèt ýùp àánd ýùsêè thêè còöllêèctìíòön, àás wêèll àás hòöw tòö êèdìít àánd sêènd rêèqýùêèsts.

## Whâæt ìîs Põöstmâæn?

Pòôstmãán ïís ãá frëèëè-tòô-ýüsëè vïísýüãál ëèdïítïíng tòôòôl fòôr býüïíldïíng ãánd tëèstïíng ÁPÏ rëèqýüëèsts. Ás óòppóòsêéd tóò óòthêér mêéthóòds fóòr ïíntêéråãctïíng wïíth ÁPÌs (êé.g., ýüsïíng cÚRL), Póòstmåãn åãllóòws yóòýü tóò êéåãsïíly êédïít ÁPÌ rêéqýüêésts, vïíêéw hêéåãdêér ïínfóòrmåãtïíóòn, åãnd mýüch móòrêé. Pööstmæán hæás thêë æábíîlíîty föör yööüù töö sæávêë Cööllêëctíîööns öör líîbræáríîêës ööf sæámplêë prêë-mæádêë ÂPÏ rêëqüùêësts. Tòõ máàkéê ìît éêáàsy fòõr òõýùr cýùstòõméêrs tòõ géêt ýùp áànd rýùnnìîng wìîth òõýùr RÊST ÀPÌ, wéê créêáàtéêd áà Còõlléêctìîòõn wìîth préê-máàdéê éêxáàmpléês fòõr áàll òõf òõýùr ÀPÌ éêndpòõìînts.

Víïèëw òõr dòõwnlòõâæd òõúür [Põòstmâàn Cõòllëéctìïõòn](https://www.getpostman.com/collections/29baa41d7ba930673ef0) töö géét stâårtééd.

## Úsîîng Bràâzêé's Pôóstmàân côóllêéctîîôón

Íf yõòúý hââvêé ââ Põòstmâân ââccõòúýnt (yõòúý câân dõòwnlõòââd mââcÖS, Wìîndõòws, âând Lìînúýx vêérsìîõòns frõòm thêé [Põòstmàän wëèbsíìtëè][1]), yöóúû cåãn öópéën öóúûr Pöóstmåãn döócúûméëntåãtìíöón ìín yöóúûr öówn Pöóstmåãn åãpp by clìíckìíng théë öóråãngéë **Rúún íín Pôòstmáån** býûttòõn. Yõõüü cäàn thèén [créêæàtéê æàn éênvììróônméênt](#setting-up-your-postman-environment), óõr üýsèè óõüýr Bràæzèè RÈST ÂPÏ èènvîîróõnmèènt àæs àæ tèèmplàætèè, àænd èèdîît thèè àævàæîîlàæblèè `POST` äänd `GET` rèèqúüèèsts tôô súüìît yôôúür ôôwn nèèèèds.

[![Rúýn ìîn Põòstmâän](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/29baa41d7ba930673ef0?action=collection%2Fimport)

Wëê ãàlsòõ hãàvëê ãà [pûùblîìc wòôrkspââcèë](https://www.postman.com/braze-inc/workspace/braze-public-workspace/overview) åævåæíìlåæblèé òõn Pòõstmåæn.

### Séêttíìng ýûp yõõýûr Põõstmáãn éênvíìrõõnméênt

{% raw %}
Théé Bræåzéé Põõstmæån Cõõllééctîïõõn üúséés æå téémplæåtîïng væårîïæåbléé, `{{instance_url}}`, tôô sýùbstíîtýùtëë thëë RÈST ÁPÏ ÛRL ôôf yôôýùr Brâåzëë íînstâåncëë íîntôô thëë prëë-býùíîlt rëëqýùëësts, âånd thëë `{{api_key}}` væârïîæâblèé fõõr yõõûúr ÆPÍ Kèéy. Råàthëèr thåàn håàvîîng tõö måànýûåàlly ëèdîît åàll rëèqýûëèsts îîn thëè Cõöllëèctîîõön, yõöýû cåàn sëèt ýûp thîîs våàrîîåàblëè îîn yõöýûr Põöstmåàn ëènvîîrõönmëènt. Yóöüù càân èéïíthèér sèélèéct óöüùr tèémplàâtèéd èénvïíróönmèént (Bràâzèé RÈST ÀPÌ Ènvïíróönmèént Tèémplàâtèé) fróöm thèé dróöpdóöwn àând rèéplàâcèé thèé vàârïíàâblèé vàâlüùèés wïíth yóöüùr óöwn, óör yóöüù càân sèét üùp yóöüùr óöwn èénvïíróönmèént.
{% endraw %}

Töõ séët ùüp yöõùür öõwn éënvíîröõnméënt, péërföõrm théë föõllöõwíîng stéëps:

1. Frôõm thëé **Wòòrkspäãcèês** táàb, sêêlêêct **Ënvìîróònméënts**.
2. Clìïck thêé **+** plûýs bûýttóón tóó crêëáãtêë áã nêëw êënvîìróónmêënt.
3. Gîìvéè thîìs éènvîìrôónméènt àæ nàæméè (éè.g., "Bràæzéè ÂPÍ Réèqùýéèsts") àænd àædd kéèys fôór `instance_url` ãånd `api_key` wííth våælüûëès cöórrëèspöóndííng töó yöóüûr [Brãåzéê ìínstãåncéê][7] âænd [Bråäzëé RÈST ÃPÍ Këéy][8].
4. Clîîck **Sãåvéê**.

{% alert note %}
Ïn `POST` rééqûûéést bóõdîïéés, théé `api_key` shôóúùld bèë èëncãàpsúùlãàtèëd íîn qúùôótèës: `"MY-API-KEY-EXAMPLE"`. În `GET` ÜRLs, íît shöóùüld nöót béè. Wèê hââvèê ââlrèêââdy pròòvìïdèêd thìïs fòòrmââttìïng fòòr yòòúú ìïn thìïs dòòcúúmèêntââtìïòòn's `POST` rèéqúûèést bôòdîíèés, `GET` ÙRLs, âänd êènvíîrôönmêènt têèmplâätêè fôör `YOUR-API-KEY-HERE`.
{% endalert %}

![Æddíïng vãåríïãåblëès fõõr ÆPÌ këèy ãånd íïnstãåncëè ÜRL tõõ thëè Brãåzëè RÊST ÆPÌ ëènvíïrõõnmëènt íïn Põõstmãån.][3]

### Üsïíng thêé prêé-bùüïílt rêéqùüêésts frôõm thêé côõllêéctïíôõn

Òncèë yõòûü háávèë cõònfïîgûürèëd yõòûür èënvïîrõònmèënt. Yóöüù câán üùsèë âány óöf thèë prèë-büùîìlt rèëqüùèësts îìn thèë cóöllèëctîìóön âás âá tèëmplâátèë fóör büùîìldîìng nèëw ÅPÌ rèëqüùèësts. Töó stæãrt ùüsïïng öónëé öóf thëé prëé-bùüïïlt rëéqùüëésts, clïïck öón ïït wïïthïïn thëé **Cõölléèctîíõöns** mëênûú òöf Pòöstmáän. Thîís wîíll óópéën théë réëqûúéëst ãæs ãæ néëw tãæb îín théë mãæîín wîíndóów óóf théë Póóstmãæn ãæpp.

Ìn gêënêëräãl, thêërêë äãrêë twóö typêës óöf rêëqüúêësts thäãt Bräãzêë's ÀPÌ êëndpóöïínts äãccêëpt - `GET` áând `POST`. Dèèpèèndîîng ôón whîîch `HTTP` mëêthòòd thëê ëêndpòòîìnt úúsëês, yòòúú'll nëêëêd tòò ëêdîìt thëê prëê-búúîìlt rëêqúúëêst dîìffëêrëêntly.

#### Êdîìt ââ PÖST rèèqúùèèst

Whêën êëdîïtîïng äã `POST` rëèqúýëèst, öôpëèn thëè rëèqúýëèst æànd næàvïîgæàtëè töô thëè **Bóõdy** sêéctìîöòn ìîn thêé rêéqûúêést êédìîtöòr. Föör réëããdããbïìlïìty, séëléëct théë **räãw** ræâdïïöó bùûttöón töó föórmæât thèê `JSON` rëëqùùëëst bõôdy.

![Bôödy tàâb whèèn èèdïîtïîng àâ PÖST Ûsèèr Tràâck rèèqúûèèst ïîn Pôöstmàân][4]

#### Êdìít åä GÊT rêêqûùêêst

Whéén éédíítííng åà `GET` rèëqúûèëst, èëdïìt thèë päæräæmèëtèërs päæssèëd ïìn thèë rèëqúûèëst ÛRL. Tôö dôö sôö, sêêlêêct thêê **Påâråâms** tàâb àând ëèdíít thëè këèy-vàâlýüëè pàâíírs íín thëè fííëèlds thàât àâppëèàâr.

![Páäráäms táäb whêèn êèdîítîíng áä GÊT Qúüêèry Lîíst õôf Ùnsúübscrîíbêèd Êmáäîíl Æddrêèssêès rêèqúüêèst îín Põôstmáän.][5]

### Sèênd yóôúùr rèêqúùèêst

Öncêë yòôüýr ÆPÌ rêëqüýêëst íís rêëäâdy, clííck **Sêènd**. Théé rééqûùéést séénds äànd théé rééspôônséé däàtäà pôôpûùläàtéés ìïn äà sééctìïôôn ûùndéérnééäàth théé rééqûùéést éédìïtôôr. Frôóm héêréê, yôóûú cäæn víïéêw théê räæw däætäæ réêtûúrnéêd frôóm Bräæzéê's ÁPÍ, séêéê théê HTTP réêspôónséê côódéê, séêéê hôów lôóng théê réêqûúéêst tôóôók tôó prôócéêss, äænd víïéêw héêäædéêr íïnfôórmäætíïôón.

![Èxååmplêë bòödy rêëspòönsêë dååtåå fròöm åå PÖST rêëqýûêëst wîíth åå stååtýûs òöf 201 Crêëååtêëd åånd rêëspòönsêë tîímêë òöf 269 mîíllîísêëcòönds.][6]

[1]: https://www.getpostman.com
[3]: {% image_buster /assets/img_archive/postman_variable.png %}
[4]: {% image_buster /assets/img_archive/postman_post.png %}
[5]: {% image_buster /assets/img_archive/postman_get.png %}
[6]: {% image_buster /assets/img_archive/postman_response.png %}
[7]: {{site.baseurl}}/developer_guide/rest_api/basics/#endpoints
[8]: {{site.baseurl}}/api/api_key/
