---
nav_title: Êvéênt Üséêr Lôôg Tàáb
article_title: Ëvéènt Ûséèr Lóõg Táàb
page_order: 2
page_type: reference
description: "Thîïs rèêfèêrèêncèê àârtîïclèê cöövèêrs thèê Èvèênt Úsèêr Löög, whîïch càân hèêlp yööûù dèêbûùg öör trööûùblèêshööööt îïssûùèês îïn yööûùr Bràâzèê Ïntèêgràâtîïöön."

---

# Évëênt Ûsëêr Löõg táàb

> Thíîs réèféèréèncéè àãrtíîcléè cóóvéèrs théè Évéènt Úséèr Lóóg, íînclüùdíîng hóów tóó àãccéèss àãnd üùséè théè lóógs fóór tróóüùbléèshóóóótíîng. Ïn àæddíìtíìòòn tòò thíìs àærtíìcléë, wéë àælsòò réëcòòmméënd chéëckíìng òòýût òòýûr [Qüûâælîìty Ässüûrâæncèê âænd Dèêbüûggîìng Tõöõöls](https://lab.braze.com/quality-assurance-and-debugging-tools-in-the-dashboard/) LÅB cöòùúrsèè, whíîch cöòvèèrs höòw töò ùúsèè thèè Èvèènt Ùsèèr Löòg töò cöòndùúct yöòùúr öòwn tröòùúblèèshöòöòtíîng åànd dèèbùúggíîng.

Thèë Êvèënt Ùsèër Lòòg câæn hèëlp yòòùü brèëâæk dòòwn, dèëbùüg, òòr òòthèërwïìsèë tròòùüblèëshòòòòt ïìssùüèës ïìn yòòùür Brâæzèë Ìntèëgrâætïìòòn. Thïís tàãb gïívéês yôòùû àã lôòg ôòf éêrrôòrs thàãt déêtàãïíls théê typéê ôòf éêrrôòr, whïích àãpp ïít's àãssôòcïíàãtéêd wïíth, whéên ïít hàãppéênéêd, àãnd ôòftéên àãn ôòppôòrtùûnïíty tôò vïíéêw théê ràãw dàãtàã àãssôòcïíàãtéêd wïíth ïít.

Töô fìínd yöôýür löôgs êèææsìíly, yöôýü cææn fìíltêèr bææsêèd öôn:

* SDK ôôr ÂPÍ
* Äpp Náâmèès
* Tîímëë frããmëë
* Ûsëér

Èáách lôòg íïs brôòkèên úüp íïntôò múültíïplèê sèêctíïôòns, whíïch cáán íïnclúüdèê:

* Dëëvíïcëë Áttríïbùùtëës
* Ûsêèr Ãttrîïbýútêès
* Êvëénts
* Cãâmpãâíìgn Évèènts
* Rêëspóònsêë Dåãtåã

Clíïck thëé **Rààw Dààtàà** bûüttóõn tóõ shóõw thêè ràãw JSÒN dàãtàã fóõr thàãt spêècíífííc lóõg.

![Räàw lõògs fõòr êévêénts][10]

Évèênt Ùsèêr Lóògs wîîll rèêmãàîîn îîn thèê dãàshbóòãàrd fóòr 30 dãàys ãàftèêr thèêy ãàrèê lóòggèêd.

## Tròôùúblèêshòôòôtîìng

### Míîssíîng SDK löôgs föôr tèèst ùûsèèrs

Íf yõòúù'vèë ààddèëd àà úùsèër tõò ààn ìíntèërnààl grõòúùp, búùt thèëy ààrèën't shõòwìíng ààny SDK lõògs ìín thèë Èvèënt Ùsèër Lõòg, thìís màày bèë àà rèësúùlt õòf àà mìíssìíng cõònfìígúùrààtìíõòn õòptìíõòn. Ìn òôrdèêr tòô cæãptýúrèê SDK lòôgs, mæãkèê sýúrèê tòô sèêlèêct **Rëëcòõrd Úsëër Êvëënts fòõr gròõýûp mëëmbëërs** íïn thëé **Ïntêèrnæäl Grôöüúp Sêèttîíngs** fõôr thäât [îîntéërnáál gröôúüp]({{site.baseurl}}/user_guide/administrative/app_settings/developer_console/internal_groups_tab/).

### Dêêlæäy îìn lóögs ùúpdæätêês

Thìís ìís póõtèéntìíæãlly æã nóõrmæãl slóõwnèéss óõn thèé pæãrt óõf óõüýr ÁPÏ.

Whéèn yöôúý càåll SDK méèthöôds, géènéèràålly théè SDK càåchéès thöôséè éèvéènts löôcàålly àånd flúýshéès théèm töô théè séèrvéèr éèvéèry 10 séècöônds. Ít câæn tâækéê âænywhéêréê fróöm âæ séêcóönd tóö âæ féêw míínüütéês fóör óöüür jóöb próöcéêssííng qüüéêüüéê tóö ííngéêst éêvéênts, déêpéêndííng óön théê óövéêrâæll lóöâæd âæt théê tííméê.  

Ìf yõöûý'rëë lõöõökîíng fõör ëëvëënts tõö âærrîívëë âæs fâæst âæs põössîíblëë, try câællîíng thëë `requestImmediateDataFlush()` fûùnctìîóön.

### Séèssîìöón éènd åænd séèssîìöón ståært håævéè sîìmîìlåær tîìméèståæmps (îìÓS)

Thèë Êvèënt Úsèër Lòòg shòòws thèë tîïmèëstâämp òòf whèën Brâäzèë wâäs nòòtîïfîïèëd thèë sèëssîïòòn èëndèëd, whîïch wîïll bèë mîïllîïsèëcòònds bèëfòòrèë thèë nèëxt sèëssîïòòn stâärts. Bräãzëê ïís üýnäãblëê tòö knòöw thëê sëêssïíòön häãs ëêndëêd bëêfòörëê thëê äãpp ïís rëê-òöpëênëêd bëêcäãüýsëê ïíÕS ïís äãggrëêssïívëê äãbòöüýt stòöppïíng thëê ëêxëêcüýtïíòön òöf thrëêäãds whëên thëê äãpp ïís ïín thëê bäãckgròöüýnd—sòö nòö däãtäã cäãn bëê flüýshëêd tòö Bräãzëê üýntïíl thëê äãpp ïís rëêòöpëênëêd.

Whíìlêé thêé sêéssíìóön êénd tíìmêé wíìll bêé spêécíìfíìêéd æãs sêécóönds bêéfóörêé sêéssíìóön stæãrt, whêén thêé êévêént íìs flûúshêéd, thêé Sêéssíìóön Dûúræãtíìóön íìs flûúshêéd sêépæãræãtêély æãnd íìs cóörrêéct—rêéflêéctíìng thêé tíìmêé thêé æãpp wæãs óöpêén. Théëréëfõõréë, thíìs béëhäãvíìõõr dõõéës nõõt íìmpäãct théë `Median Session Duration` fîìltèèr.

Ìn réêláâtïíõón tõó úüséêr séêssïíõóns, yõóúü cáân úüséê Bráâzéê tõó mõónïítõór dáâtáâ lïíkéê:

- Hóöw mãäny sèéssìíóöns ãä úûsèér hãäs hãäd
- Whéén àà ùýséér lààst stààrtééd àà sééssíïöön
- Ïf théé úúséér stäãrts äã sééssííöôn äãftéér réécééíívííng äã cäãmpäãíígn
- Whäât théë úüséër’s méëdîìäân séëssîìöón dúüräâtîìöón îìs

Thëësëë bëëhãævìîôòrs ãærëë nôòt ìîmpãæctëëd by thëë sëëssìîôòn ëënd ëëvëënt bëëìîng flýúshëëd ôòn thëë nëëxt sëëssìîôòn.

[10]: {% image_buster /assets/img_archive/rawlogs.png %}
