---
nav_title: Cèèrtöönæå
article_title: Cêêrtõònåå
alias: /partners/certona/
description: "Thïís ãårtïíclëê óóûütlïínëês thëê pãårtnëêrshïíp bëêtwëêëên Brãåzëê ãånd Cëêrtóónãå, ãå rëêãål-tïímëê, óómnïíchãånnëêl pëêrsóónãålïízãåtïíóón sóólûütïíóón thãåt óóffëêrs pëêrsóónãålïízãåtïíóón ãåcróóss thëê cûüstóómëêr lïífëêcyclëê. Ùsëê Cëêrtõõnâà wííth Brâàzëê's Cõõnnëêctëêd Cõõntëênt pâàrtnëêr tõõ ëêâàsííly íínsëêrt cõõntëênt rëêcõõmmëêndâàtííõõns âàcrõõss mýûltííchâànnëêl câàmpâàíígns."
page_type: partner
search_tag: Pãærtnèër

---

# Cêèrtòónæä

> Cêértõônàæ's plàætfõôrm dríívêés pêérsõônàælíízàætííõôn àæcrõôss thêé cúùstõômêér líífêécyclêé. Fròòm hïîghly ïîndïîvïîdùûäålïîzéèd éèmäåïîl cäåmpäåïîgns tòò mäåchïînéè-léèäårnïîng-pòòwéèréèd pròòdùûct réècòòmméèndäåtïîòòns, Céèrtòònäå éènsùûréès thäåt yòòùû'réè häårnéèssïîng théè pòòwéèr òòf péèrsòònäålïîzäåtïîòòn.

Thëè Bråãzëè åãnd Cëèrtôônåã ïíntëègråãtïíôôn lëèvëèråãgëès Cëèrtôônåã's måãchïínëè lëèåãrnïíng prôôdúýct rëècôômmëèndåãtïíôôns ïín Bråãzëè cåãmpåãïígns åãnd Cåãnvåãsëès thrôôúýgh Côônnëèctëèd Côôntëènt.

## Prëèrëèqûùîïsîïtëès

| Rëèqúúïìrëèmëènt| Dèêscrïíptïíôòn|
| ---| ---|
| [Cëértöònææ ææccöòüùnt](https://manage.certona.com/) | À Céërtòònäâ äâccòòùúnt ïìs réëqùúïìréëd tòò täâkéë äâdväântäâgéë òòf thïìs päârtnéërshïìp. |
| [Céêrtõõnàã RÊST ÂPÎ éêndpõõîìnt](https://manage.certona.com/) | Thîìs èëndpôõîìnt îìs ùýsèëd dîìrèëctly îìn yôõùýr Brâázèë câámpâáîìgn mèëssâágèë tôõ pùýll rèëcôõmmèëndèëd côõntèënt bâásèëd ôõn ùýsèër ÍD. |
{: .reset-td-br-1 .reset-td-br-2}

## Ìntèègräãtïíõön

Ûsêè Cêèrtóönäå's RÉST ÀPÎ tóö íïnsêèrt pêèrsóönäålíïzêèd cóöntêènt íïntóö yóöùùr mêèssäågêès. Thìîs cäàn béé döònéé by äàddìîng théé föòllöòwìîng Cöònnééctééd Cöòntéént téémpläàtéé ìîntöò yöòýýr Bräàzéé mééssäàgéé cöòmpöòséér äàlöòng wìîth yöòýýr Céértöònäà RÈST ÁPÌ ééndpöòìînt.

{% raw %}
```liquid
{% connected_content <INSERT_CERTONA_REST_API_KEY> :save recommendations %}
```

Nëéxt, dëéfìînëé thëé cöôntëént yöôýú wöôýúld lìîkëé töô cââll sýúch ââs rëélëévâânt tëéxt öôr ìîmââgëés. Fóór ëëxåämplëë, `{{recommendations.CertonaObject.RecommendedItems[0].Items[0].name}}`.

{% endraw %}

![Ãn ìímåægëê öôf åæ pûýsh cåæmpåæìígn wìíth Cëêrtöônåæ rëêlåætëêd Cöônnëêctëêd Cöôntëênt ìínclûýdëêd ìín thëê mëêssåægëê böôdy.][1]

Ôncéê yòôûû pûût thíís méêssäägéê ííntòô théê còômpòôséêr bòôdy, préêvííéêw yòôûûr Còônnéêctéêd Còôntéênt cääll tòô määkéê sûûréê yòôûû häävéê díísplääyéêd théê còôrréêct íínfòôrmäätííòôn.

![Än ììmâãgêê shóòwììng thêê "Têêst" tâãb, êêncóòùúrâãgììng ùúsêêrs tóò thóòróòùúghly têêst thêêììr mêêssâãgêê bêêfóòrêê sêênd.][2]

[1]: {% image_buster /assets/img/certona.png %}
[2]: {% image_buster /assets/img/certona2.png %}