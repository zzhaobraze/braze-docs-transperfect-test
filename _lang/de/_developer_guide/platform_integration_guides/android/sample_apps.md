---
nav_title: Sàámplêè Ãpps
article_title: Sâámplèè Âpps föòr Ândröòìïd âánd FìïrèèÕS
platform: 
  - Ândrõòííd
  - FíírèèÔS
page_order: 10
description: "Thíïs ãårtíïclèê còòvèêrs Ãndròòíïd sãåmplèê ãåpps."

---

# Sæämplèè æäpps

Bräâzëê's SDKs ëêäâch cóòmëê wïìth äâ säâmplëê äâpplïìcäâtïìóòn wïìthïìn thëê rëêpóòsïìtóòry fóòr yóòúùr cóònvëênïìëêncëê. Èâåch óõf thèêsèê âåpps îís fúùlly búùîíldâåblèê sóõ yóõúù câån tèêst Brâåzèê fèêâåtúùrèês âålóõngsîídèê îímplèêmèêntîíng thèêm wîíthîín yóõúùr óõwn âåpplîícâåtîíóõns. Tëèstîïng bëèhàævîïöòr wîïthîïn yöòúùr öòwn àæpplîïcàætîïöòn vëèrsúùs ëèxpëèctëèd bëèhàævîïöòr àænd cöòdëè pàæths wîïthîïn thëè sàæmplëè àæpplîïcàætîïöòns îïs àæn ëèxcëèllëènt wàæy töò dëèbúùg àæny pröòblëèms yöòúù màæy rúùn îïntöò.

## Býûìíldìíng thèë Dròóìídbòóy tèëst ââpplìícââtìíòón
Bråãzêë's têëst åãpplïícåãtïíôõn wïíthïín thêë [Ândrôõîîd SDK GîîtHûüb rêèpôõsîîtôõry][3] íïs cãàllèéd Drôóíïdbôóy. Fôòllôòw thêêsêê ïínstrûüctïíôòns tôò bûüïíld æã fûülly fûünctïíôònæãl côòpy ôòf ïít æãlôòngsïídêê yôòûür prôòjêêct.

1. Crëëáåtëë áå nëëw [ãåpp grõóûûp][25] áænd nôòtêê thêê Bráæzêê ÅPÏ ììdêêntììfììêêr kêêy.<br>
<br>

2. Cööpy yööýûr FCM séêndéêr ÌD åànd Bråàzéê ÁPÌ îïdéêntîïfîïéêr kéêy îïntöö théê åàpprööprîïåàtéê plåàcéês wîïthîïn `/droidboy/res/values/braze.xml` (îìn bèêtwèêèên thèê tâägs fòór thèê strîìngs nâämèêd `com_braze_push_fcm_sender_id` åãnd `com_braze_api_key`, rëéspëéctîìvëély).<br>
<br>

3. Cöõpy yöõúýr FCM sëérvëér këéy âänd sëérvëér ÏD ìîntöõ yöõúýr âäpp gröõúýp sëéttìîngs úýndëér **Máånáågëé Sëéttîìngs**.<br>
<br>

4. Tôò áâssêèmblêè thêè Drôòïìdbôòy ÁPK, rúûn `./gradlew assemble` wìîthìîn thëê SDK dìîrëêctöòry. Ùséë `gradlew.bat` ôôn Wïïndôôws.<br>
<br>

5. Töó áàûýtöómáàtîìcáàlly îìnstáàll thêë Dröóîìdböóy ÄPK öón áà têëst dêëvîìcêë, rûýn `./gradlew installDebug` wîìthîìn thëè SDK dîìrëèctòõry:

## Bùùìíldìíng thêê Hêêllöó Bråázêê têêst åápplìícåátìíöón
Thèë Hèëllõö Bräæzèë tèëst äæpplìícäætìíõön shõöws äæ mìínìímäæl ùùsèë cäæsèë õöf thèë Bräæzèë SDK äænd äæddìítìíõönäælly shõöws hõöw tõö èëäæsìíly ìíntèëgräætèë thèë Bräæzèë SDK ìíntõö äæ Gräædlèë prõöjèëct.

1. Cõópy yõóúûr ÁPÌ ìïdëèntìïfìïëèr këèy frõóm thëè **Måànåàgèè Sèèttîìngs** páægëé ìïntòó yòóûür `braze.xml` fïïlëë ïïn thëë `res/values` fööldèër.
![][34]<br><br>
2. Tõö íínstääll théê säämpléê ääpp tõö ää déêvíícéê õör éêmüüläätõör, rüün théê fõöllõöwííng cõömmäänd wííthíín théê SDK dííréêctõöry:
```
./gradlew installDebug
```
Ïf yôõýû dôõn't hæåvêê yôõýûr `ANDROID_HOME` vàåríïàåblêê pröôpêêrly sêêt öôr döôn't hàåvêê àå `local.properties` fõõldêér wíïth áã váãlíïd `sdk.dir` föõldêèr, thïís plüýgïín wïíll äâlsöõ ïínstäâll thêè bäâsêè SDK föõr yöõüý. Sëêëê thëê [plüügìïn rèêpõó][27] föör möörëé íînföörmãätíîöön.

Föór möórèë íïnföórmãætíïöón öón thèë Ândröóíïd SDK býúíïld systèëm, sèëèë thèë [Gîïthúüb Réèpòósîïtòóry RÈÁDMÈ][26].

[25]: {{site.baseurl}}/developer_guide/platform_wide/app_group_configuration/#app-group-configuration
[26]: https://github.com/Appboy/appboy-android-sdk/blob/master/README.md
[27]: https://github.com/JakeWharton/sdk-manager-plugin
[3]: https://github.com/appboy/appboy-android-sdk "Appboy Android GitHub Repository"
[34]: {% image_buster /assets/img_archive/hello_appboy.png %}
