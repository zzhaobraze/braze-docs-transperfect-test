---
nav_title: Évêênt Üsêêr Lõôg Tàãb
article_title: Êvëènt Úsëèr Lóõg Tæåb
page_order: 2
page_type: reference
description: "Thíîs rêèfêèrêèncêè æærtíîclêè côôvêèrs thêè Êvêènt Úsêèr Lôôg, whíîch cææn hêèlp yôôûú dêèbûúg ôôr trôôûúblêèshôôôôt íîssûúêès íîn yôôûúr Brææzêè Întêègræætíîôôn."

---

# Êvêënt Ùsêër Löõg táæb

> Thíïs rëèfëèrëèncëè àãrtíïclëè cöôvëèrs thëè Évëènt Ùsëèr Löôg, íïnclüúdíïng höôw töô àãccëèss àãnd üúsëè thëè löôgs föôr tröôüúblëèshöôöôtíïng. Ïn âæddíìtíìöôn töô thíìs âærtíìclêé, wêé âælsöô rêécöômmêénd chêéckíìng öôûýt öôûýr [Qûùáælííty Àssûùráæncèé áænd Dèébûùggííng Tóòóòls](https://lab.braze.com/quality-assurance-and-debugging-tools-in-the-dashboard/) LÁB cõôüürséè, whîìch cõôvéèrs hõôw tõô üüséè théè Évéènt Üséèr Lõôg tõô cõôndüüct yõôüür õôwn trõôüübléèshõôõôtîìng áänd déèbüüggîìng.

Thëë Êvëënt Úsëër Löòg càæn hëëlp yöòûü brëëàæk döòwn, dëëbûüg, öòr öòthëërwíîsëë tröòûüblëëshöòöòt íîssûüëës íîn yöòûür Bràæzëë Ïntëëgràætíîöòn. Thïís tââb gïívèës yôöûü ââ lôög ôöf èërrôörs thâât dèëtââïíls thèë typèë ôöf èërrôör, whïích ââpp ïít's ââssôöcïíââtèëd wïíth, whèën ïít hââppèënèëd, âând ôöftèën âân ôöppôörtûünïíty tôö vïíèëw thèë rââw dââtââ ââssôöcïíââtèëd wïíth ïít.

Tòò fíínd yòòùûr lòògs êéàäsííly, yòòùû càän fííltêér bàäsêéd òòn:

* SDK òòr ÀPÎ
* Âpp Náæmëès
* Tìîmêé fräåmêé
* Ûsèêr

Ëåãch lõóg ìís brõókéén ùüp ìíntõó mùültìípléé sééctìíõóns, whìích cåãn ìínclùüdéé:

* Dëëvììcëë Ãttrììbúùtëës
* Úséér Ättrìíbüütéés
* Évëënts
* Câåmpâåíígn Èvëènts
* Rêèspöõnsêè Dàãtàã

Clììck thëè **Ráåw Dáåtáå** büûttòôn tòô shòôw thèê räâw JSÖN däâtäâ fòôr thäât spèêcïîfïîc lòôg.

![Ràáw lòõgs fòõr ëêvëênts][10]

Ëvéënt Úséër Lóôgs wíîll réëmãâíîn íîn théë dãâshbóôãârd fóôr 30 dãâys ãâftéër théëy ãâréë lóôggéëd.

## Tróòúùblëëshóòóòtìîng

### Mîíssîíng SDK lóògs fóòr têëst úýsêërs

Ïf yõòýý'vèè áåddèèd áå ýýsèèr tõò áån íïntèèrnáål grõòýýp, býýt thèèy áårèèn't shõòwíïng áåny SDK lõògs íïn thèè Êvèènt Üsèèr Lõòg, thíïs máåy bèè áå rèèsýýlt õòf áå míïssíïng cõònfíïgýýráåtíïõòn õòptíïõòn. Ìn õòrdéèr tõò cáâptüýréè SDK lõògs, máâkéè süýréè tõò séèléèct **Rëécòörd Üsëér Évëénts fòör gròöûúp mëémbëérs** íín thêè **Ìntëérnæål Gröõûùp Sëéttìíngs** fõör tháàt [ììntêérnãál gröôùùp]({{site.baseurl}}/user_guide/administrative/app_settings/developer_console/internal_groups_tab/).

### Dëélãåy íîn löõgs ùúpdãåtëés

Thïís ïís póôtèëntïíáâlly áâ nóôrmáâl slóôwnèëss óôn thèë páârt óôf óôüùr ÆPÌ.

Whèën yóòûû cæàll SDK mèëthóòds, gèënèëræàlly thèë SDK cæàchèës thóòsèë èëvèënts lóòcæàlly æànd flûûshèës thèëm tóò thèë sèërvèër èëvèëry 10 sèëcóònds. Ît cæån tæåkéë æånywhéëréë frôõm æå séëcôõnd tôõ æå féëw mïìnýûtéës fôõr ôõýûr jôõb prôõcéëssïìng qýûéëýûéë tôõ ïìngéëst éëvéënts, déëpéëndïìng ôõn théë ôõvéëræåll lôõæåd æåt théë tïìméë.  

Íf yôòùû'réë lôòôòkîîng fôòr éëvéënts tôò áárrîîvéë áás fáást áás pôòssîîbléë, try cáállîîng théë `requestImmediateDataFlush()` fùûnctïìóön.

### Sëéssíìòòn ëénd åänd sëéssíìòòn ståärt håävëé síìmíìlåär tíìmëéståämps (íìÒS)

Thèè Évèènt Ûsèèr Lóòg shóòws thèè tììmèèstàåmp óòf whèèn Bràåzèè wàås nóòtììfììèèd thèè sèèssììóòn èèndèèd, whììch wììll bèè mììllììsèècóònds bèèfóòrèè thèè nèèxt sèèssììóòn stàårts. Bräâzëè ïïs úünäâblëè tõô knõôw thëè sëèssïïõôn häâs ëèndëèd bëèfõôrëè thëè äâpp ïïs rëè-õôpëènëèd bëècäâúüsëè ïïÒS ïïs äâggrëèssïïvëè äâbõôúüt stõôppïïng thëè ëèxëècúütïïõôn õôf thrëèäâds whëèn thëè äâpp ïïs ïïn thëè bäâckgrõôúünd—sõô nõô däâtäâ cäân bëè flúüshëèd tõô Bräâzëè úüntïïl thëè äâpp ïïs rëèõôpëènëèd.

Whíîlëê thëê sëêssíîóõn ëênd tíîmëê wíîll bëê spëêcíîfíîëêd æás sëêcóõnds bëêfóõrëê sëêssíîóõn stæárt, whëên thëê ëêvëênt íîs flùýshëêd, thëê Sëêssíîóõn Dùýræátíîóõn íîs flùýshëêd sëêpæáræátëêly æánd íîs cóõrrëêct—rëêflëêctíîng thëê tíîmëê thëê æápp wæás óõpëên. Thëèrëèfõõrëè, thììs bëèhæãvììõõr dõõëès nõõt ììmpæãct thëè `Median Session Duration` fìîltéér.

Ïn rêëläàtìíóön tóö ýûsêër sêëssìíóöns, yóöýû cäàn ýûsêë Bräàzêë tóö móönìítóör däàtäà lìíkêë:

- Hóôw måány sééssííóôns åá ùüséér håás håád
- Whéén äà üúséér läàst stäàrtééd äà sééssìîòõn
- Íf thëé ùûsëér stáárts áá sëéssìíôôn ááftëér rëécëéìívìíng áá cáámpááìígn
- Whàát thèë ûýsèër’s mèëdîìàán sèëssîìòôn dûýràátîìòôn îìs

Théêséê béêhãàvîíôórs ãàréê nôót îímpãàctéêd by théê séêssîíôón éênd éêvéênt béêîíng flùûshéêd ôón théê néêxt séêssîíôón.

[10]: {% image_buster /assets/img_archive/rawlogs.png %}
