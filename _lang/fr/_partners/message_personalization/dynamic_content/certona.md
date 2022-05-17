---
nav_title: Cèêrtöõnåä
article_title: Cëêrtòõnâá
alias: /partners/certona/
description: "Thíîs àärtíîclëê öóûýtlíînëês thëê pàärtnëêrshíîp bëêtwëêëên Bràäzëê àänd Cëêrtöónàä, àä rëêàäl-tíîmëê, öómníîchàännëêl pëêrsöónàälíîzàätíîöón söólûýtíîöón thàät öóffëêrs pëêrsöónàälíîzàätíîöón àäcröóss thëê cûýstöómëêr líîfëêcyclëê. Ùséé Céértöônåà wììth Bråàzéé's Cöônnééctééd Cöôntéént påàrtnéér töô ééåàsììly ììnséért cöôntéént réécöômmééndåàtììöôns åàcröôss müýltììchåànnéél cåàmpåàììgns."
page_type: partner
search_tag: Pæärtnëèr

---

# Cëèrtõônæâ

> Cêêrtóönâæ's plâætfóörm dríîvêês pêêrsóönâælíîzâætíîóön âæcróöss thêê cüüstóömêêr líîfêêcyclêê. Fröòm híìghly íìndíìvíìdûúæàlíìzéêd éêmæàíìl cæàmpæàíìgns töò mæàchíìnéê-léêæàrníìng-pöòwéêréêd pröòdûúct réêcöòmméêndæàtíìöòns, Céêrtöònæà éênsûúréês thæàt yöòûú'réê hæàrnéêssíìng théê pöòwéêr öòf péêrsöònæàlíìzæàtíìöòn.

Thëè Bräâzëè äând Cëèrtòònäâ îîntëègräâtîîòòn lëèvëèräâgëès Cëèrtòònäâ's mäâchîînëè lëèäârnîîng pròòdùúct rëècòòmmëèndäâtîîòòns îîn Bräâzëè cäâmpäâîîgns äând Cäânväâsëès thròòùúgh Còònnëèctëèd Còòntëènt.

## Prêèrêèqûüìîsìîtêès

| Rèéqúúíìrèémèént| Dééscrïîptïîõôn|
| ---| ---|
| [Céërtöónâà âàccöóùünt](https://manage.certona.com/) | Ä Céêrtöónàà ààccöóùûnt îîs réêqùûîîréêd töó tààkéê ààdvààntààgéê öóf thîîs pààrtnéêrshîîp. |
| [Céërtõônàå RÊST ÅPÎ éëndpõôíínt](https://manage.certona.com/) | Thíîs êêndpòòíînt íîs ýúsêêd díîrêêctly íîn yòòýúr Bráázêê cáámpááíîgn mêêssáágêê tòò pýúll rêêcòòmmêêndêêd còòntêênt báásêêd òòn ýúsêêr ÎD. |
{: .reset-td-br-1 .reset-td-br-2}

## Ìntèëgrãâtïîòön

Ùsëê Cëêrtôônàæ's RÉST ÀPÏ tôô ìïnsëêrt pëêrsôônàælìïzëêd côôntëênt ìïntôô yôôùýr mëêssàægëês. Thïîs càãn bêé dõônêé by àãddïîng thêé fõôllõôwïîng Cõônnêéctêéd Cõôntêént têémplàãtêé ïîntõô yõôûûr Bràãzêé mêéssàãgêé cõômpõôsêér àãlõông wïîth yõôûûr Cêértõônàã RÉST ÄPÌ êéndpõôïînt.

{% raw %}
```liquid
{% connected_content <INSERT_CERTONA_REST_API_KEY> :save recommendations %}
```

Nèèxt, dèèfíìnèè thèè còõntèènt yòõüú wòõüúld líìkèè tòõ câãll süúch âãs rèèlèèvâãnt tèèxt òõr íìmâãgèès. Fòór êéxâæmplêé, `{{recommendations.CertonaObject.RecommendedItems[0].Items[0].name}}`.

{% endraw %}

![Än íìmäågèê ôõf äå pýûsh cäåmpäåíìgn wíìth Cèêrtôõnäå rèêläåtèêd Côõnnèêctèêd Côõntèênt íìnclýûdèêd íìn thèê mèêssäågèê bôõdy.][1]

Õncéê yôóüú püút thîís méêssâägéê îíntôó théê côómpôóséêr bôódy, préêvîíéêw yôóüúr Côónnéêctéêd Côóntéênt câäll tôó mâäkéê süúréê yôóüú hâävéê dîísplâäyéêd théê côórréêct îínfôórmâätîíôón.

![Æn ììmâágèë shõõwììng thèë "Tèëst" tâáb, èëncõõüùrâágììng üùsèërs tõõ thõõrõõüùghly tèëst thèëììr mèëssâágèë bèëfõõrèë sèënd.][2]

[1]: {% image_buster /assets/img/certona.png %}
[2]: {% image_buster /assets/img/certona2.png %}