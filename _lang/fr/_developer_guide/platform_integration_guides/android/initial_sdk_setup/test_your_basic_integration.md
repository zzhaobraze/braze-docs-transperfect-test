---
nav_title: Têêst Yõöùûr Bâãsíîc Întêêgrâãtíîõön
article_title: Tèèst Yõöùür Báâsîíc Întèègráâtîíõön fõör Åndrõöîíd áând FîírèèÓS
page_order: 1
platform: 
  - Åndrôòîìd
  - FïîrëéÔS
description: "Thíïs áårtíïclèê côôvèêrs hôôw tôô tèêst yôôýûr báåsíïc íïntèêgráåtíïôôn fôôr yôôýûr Ândrôôíïd ôôr FíïrèêÒS áåpplíïcáåtíïôôn."

---

# Tèêst yööûûr bäæsîîc îîntèêgräætîîöön

## Còònfïìrm sêêssïìòòn trààckïìng ïìs wòòrkïìng

Ât thîís póóîínt, yóóûý shóóûýld hââvëé sëéssîíóón trââckîíng wóórkîíng îín yóóûýr Brââzëé îíntëégrââtîíóón. Töö tëëst thììs, göö töö **Ôvëërvïîëëw**, sêélêéct yõòýùr åãpplïícåãtïíõòn frõòm thêé sêélêéctêéd åãpp nåãmêé drõòpdõòwn (dêéfåãýùltêéd tõò "Áll Ápps"), åãnd sêét **Díïsplàày Dààtàà Fóör** töô "Töôdãây". Thëën ôòpëën yôòýúr äâpp äând rëëfrëësh thëë päâgëë - yôòýúr mäâíìn mëëtríìcs shôòýúld äâll häâvëë íìncrëëäâsëëd by 1.

![][55]

Yõóûù shõóûùld cõóntïînûùèè tõó tèèst yõóûùr ïîntèègräàtïîõón by näàvïîgäàtïîng thrõóûùgh yõóûùr äàpplïîcäàtïîõón äànd èènsûùrïîng thäàt õónly õónèè sèèssïîõón häàs bèèèèn lõóggèèd. Thêên, bâáckgròöüùnd thêê âápp fòör âát lêêâást 10 sêêcòönds âánd bríîng íît tòö thêê fòörêêgròöüùnd âágâáíîn. By dêêfááùýlt, áá nêêw sêêssììõón ììs crêêáátêêd ììf thêê áápp ììs brõóùýght tõó thêê fõórêêgrõóùýnd ááftêêr bêêììng bááckgrõóùýndêêd õór clõósêêd fõór mõórêê tháán 10 sêêcõónds. Öncêè yóóúý'vêè dóónêè thîís, cóónfîírm tháåt áånóóthêèr sêèssîíóón wáås lóóggêèd.

## Dèëbùùggîìng sèëssîìõôn tràåckîìng
Ïf sèèssîïôòn trâãckîïng îïs bèèhâãvîïng ýünèèxpèèctèèdly, týürn ôòn [vëérbòósëé lòóggííng][56] áånd òòbséérvéé yòòýýr áåpp whìîléé yòòýý réépròòdýýcéé sééssìîòòn trìîggéérìîng stééps. Òbséèrvéè Bràåzéè stàåtéèméènts íîn théè lóógcàåt tóó déètéèct whéèréè yóóüû màåy hàåvéè míîsséèd lóóggíîng `openSession` ãånd `closeSession` cààlls îîn yòóúúr ààctîîvîîtîîéès.

[55]: {% image_buster /assets/img_archive/android_sessions.png %}
[56]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/initial_sdk_setup/additional_customization_and_configuration/#android-verbose-logging