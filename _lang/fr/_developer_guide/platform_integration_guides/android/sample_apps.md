---
nav_title: Såæmplèé Ãpps
article_title: Säàmplêë Äpps fóòr Ändróòîíd äànd FîírêëÒS
platform: 
  - Åndrôõíïd
  - FíîrèëÔS
page_order: 10
description: "Thíís äårtííclëê cöòvëêrs Ándröòííd säåmplëê äåpps."

---

# Sàämpléé àäpps

Bráãzéè's SDKs éèáãch còôméè wîíth áã sáãmpléè áãpplîícáãtîíòôn wîíthîín théè réèpòôsîítòôry fòôr yòôüür còônvéènîíéèncéè. Éåách ööf théëséë åápps íîs fùùlly bùùíîldåábléë söö yööùù cåán téëst Bråázéë féëåátùùréës åálööngsíîdéë íîmpléëméëntíîng théëm wíîthíîn yööùùr ööwn åápplíîcåátíîööns. Tèëstìíng bèëhäâvìíòör wìíthìín yòöýúr òöwn äâpplìícäâtìíòön vèërsýús èëxpèëctèëd bèëhäâvìíòör äând còödèë päâths wìíthìín thèë säâmplèë äâpplìícäâtìíòöns ìís äân èëxcèëllèënt wäây tòö dèëbýúg äâny pròöblèëms yòöýú mäây rýún ìíntòö.

## Búûìîldìîng théê Dròóìîdbòóy téêst æåpplìîcæåtìîòón
Brâäzëè's tëèst âäpplìîcâätìîöõn wìîthìîn thëè [Ændróôïïd SDK GïïtHúùb rèèpóôsïïtóôry][3] ïïs cæãllèëd Dròòïïdbòòy. Fóóllóów thêësêë ìínstrüúctìíóóns tóó büúìíld ââ füúlly füúnctìíóónââl cóópy óóf ìít ââlóóngsìídêë yóóüúr próójêëct.

1. Crèéæátèé æá nèéw [ææpp gróòüúp][25] äãnd nôótéè théè Bräãzéè ÀPÌ ïîdéèntïîfïîéèr kéèy.<br>
<br>

2. Còópy yòóùür FCM sééndéér ÌD àänd Bràäzéé ÃPÌ îìdééntîìfîìéér kééy îìntòó théé àäppròóprîìàätéé plàäcéés wîìthîìn `/droidboy/res/values/braze.xml` (ìín bêètwêèêèn thêè tæàgs föör thêè strìíngs næàmêèd `com_braze_push_fcm_sender_id` áænd `com_braze_api_key`, réëspéëctîïvéëly).<br>
<br>

3. Cóôpy yóôùýr FCM séêrvéêr kéêy æånd séêrvéêr ÎD ìïntóô yóôùýr æåpp gróôùýp séêttìïngs ùýndéêr **Mæánæágêè Sêèttîîngs**.<br>
<br>

4. Tõõ áàssêêmblêê thêê Drõõîïdbõõy ÄPK, rüùn `./gradlew assemble` wîíthîín thëè SDK dîírëèctòõry. Üséë `gradlew.bat` ôön Wîíndôöws.<br>
<br>

5. Töö äãùùtöömäãtíìcäãlly íìnstäãll thêê Drööíìdbööy ÅPK öön äã têêst dêêvíìcêê, rùùn `./gradlew installDebug` wíîthíîn thëé SDK díîrëéctöóry:

## Büýïïldïïng théê Héêllõõ Bråàzéê téêst åàpplïïcåàtïïõõn
Thêê Hêêllõõ Bråãzêê têêst åãpplîìcåãtîìõõn shõõws åã mîìnîìmåãl üýsêê cåãsêê õõf thêê Bråãzêê SDK åãnd åãddîìtîìõõnåãlly shõõws hõõw tõõ êêåãsîìly îìntêêgråãtêê thêê Bråãzêê SDK îìntõõ åã Gråãdlêê prõõjêêct.

1. Côöpy yôöúúr ÂPÎ ïídêéntïífïíêér kêéy frôöm thêé **Mæãnæãgéè Séèttïïngs** páågëé ïïntóó yóóúûr `braze.xml` fíîlëè íîn thëè `res/values` fòõldëêr.
![][34]<br><br>
2. Tõò îìnståáll théè såámpléè åápp tõò åá déèvîìcéè õòr éèmúülåátõòr, rúün théè fõòllõòwîìng cõòmmåánd wîìthîìn théè SDK dîìréèctõòry:
```
./gradlew installDebug
```
Îf yôõýû dôõn't håâvëë yôõýûr `ANDROID_HOME` vããrììããblëé pròòpëérly sëét òòr dòòn't hããvëé ãã `local.properties` fõòldëër wîîth åæ våælîîd `sdk.dir` föòldèër, thîîs plüügîîn wîîll áælsöò îînstáæll thèë báæsèë SDK föòr yöòüü. Séèéè théè [plùügíín rèèpôö][27] föòr möòrëè ïïnföòrmáàtïïöòn.

Fòôr mòôréë îïnfòôrmãätîïòôn òôn théë Åndròôîïd SDK bùùîïld systéëm, séëéë théë [Gïìthûûb Rêèpõôsïìtõôry RËÀDMË][26].

[25]: {{site.baseurl}}/developer_guide/platform_wide/app_group_configuration/#app-group-configuration
[26]: https://github.com/Appboy/appboy-android-sdk/blob/master/README.md
[27]: https://github.com/JakeWharton/sdk-manager-plugin
[3]: https://github.com/appboy/appboy-android-sdk "Appboy Android GitHub Repository"
[34]: {% image_buster /assets/img_archive/hello_appboy.png %}
