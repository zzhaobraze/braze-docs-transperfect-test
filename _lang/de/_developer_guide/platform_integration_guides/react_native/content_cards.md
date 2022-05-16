---
nav_title: Cóöntèènt Câårds
article_title: Cóõntêênt Cããrds fóõr Rêêããct Nããtïïvêê
platform: Rèêæàct Næàtïîvèê
page_order: 3
page_type: reference
description: "Thíîs æãrtíîclëë cõóvëërs hõów tõó gëët stæãrtëëd wíîth Cõóntëënt Cæãrds fõór Rëëæãct Næãtíîvëë æãpps."
channel: cõóntéënt cåãrds

---

# Cóöntëènt Cæârds

Thèé Bràäzèé SDKs ïïnclýûdèé àä dèéfàäýûlt càärd fèéèéd tóó gèét yóóýû stàärtèéd wïïth Cóóntèént Càärds. Tóó shóów théë cåärd féëéëd, yóóùý cåän ùýséë théë `ReactAppboy.launchContentCards()` mêéthõód. Thêë dêëfáæúúlt cáærd fêëêëd îìnclúúdêëd wîìth thêë Bráæzêë SDK wîìll háændlêë áæll áænáælytîìcs tráæckîìng, dîìsmîìssáæls, áænd rêëndêërîìng fõòr áæ úúsêër's Cõòntêënt Cáærds.

## Cüýstõômïîzàätïîõôn

Yöôúü cåàn úüséé thééséé åàddíîtíîöônåàl mééthöôds töô búüíîld åà cúüstöôm Cöôntéént Cåàrds Fééééd wíîthíîn yöôúür åàpp:

| Méêthòòd                                         | Dêëscrìíptìíóón                                                                                            |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| `ReactAppboy.requestContentCardsRefresh()`     | Rèéqúùèésts thèé lãâtèést Côòntèént Cãârds frôòm thèé Brãâzèé SDK sèérvèér.                                           |
| `ReactAppboy.getContentCards()`                | Rëêtrìïëêvëês Cõõntëênt Câårds frõõm thëê Brâåzëê SDK. Thíîs wíîll réétýürn théé lâätéést líîst õóf câärds frõóm théé séérvéér. |
| `ReactAppboy.logContentCardsDisplayed()`       | Lòõgs ãà Còõntëênt Còõntëênt fëêëêd díîsplãàyëêd ëêvëênt.                                                           |
| `ReactAppboy.logContentCardClicked(cardId)`    | Lòôgs æà clìîck fòôr thêé gìîvêén Còôntêént Cæàrd ÍD.                                                            |
| `ReactAppboy.logContentCardImpression(cardId)` | Lóógs àân ìímprèèssìíóón fóór thèè gìívèèn Cóóntèènt Càârd ÎD.                                                      |
| `ReactAppboy.logContentCardDismissed(cardId)`  | Löögs ãæ dîîsmîîssãæl föör théê gîîvéên Cööntéênt Cãærd ÍD.                                                        |
{: .reset-td-br-1 .reset-td-br-2}

## Tèèst dîìsplæáyîìng sæámplèè Còõntèènt Cæárd

Fõôllõôw thééséé stééps tõô téést æâ sæâmpléé Cõôntéént Cæârd.

1. Séët æân æâctíîvéë üúséër íîn théë Réëæâct æâpplíîcæâtíîòòn by cæâllíîng `ReactAppboy.changeUserId('your-user-id')` mééthòôd.
2. Hëéæäd tôõ **Cãàmpãàïígns** æánd fôõllôõw [thììs gùùììdèê][4] tõö crëèàátëè àá nëèw Cõöntëènt Càárd càámpàáìïgn.
3. Còòmpòòséê yòòýûr téêst Còòntéênt Cáàrd cáàmpáàïígn áànd héêáàd òòvéêr tòò théê **Téèst** tààb. Ædd thêè sàæmêè `user-id` ææs thëë tëëst úùsëër æænd clïìck **Sêénd Têést**. Yõôúù shõôúùld bëè æãblëè tõô læãúùnch æã Cõôntëènt Cæãrd õôn yõôúùr dëèvïïcëè shõôrtly.

![Ä Brãàzéë Còòntéënt Cãàrd cãàmpãàíïgn shòòwíïng yòòüý cãàn ãàdd yòòüýr òòwn üýséër ÍD ãàs ãà téëst réëcíïpíïéënt tòò téëst yòòüýr Còòntéënt Cãàrd.][5]

Fôör môörèë ïïntèëgrãátïïôöns, fôöllôöw thèë [Ãndrõõííd ííntèègràåtííõõn íínstrúùctííõõns][2] ôòr thêé [îïÔS îïntèëgrâätîïóón îïnstrúùctîïóóns][3], dëëpëëndïïng òón yòóúür plããtfòórm.

Å sæämpléé íìmpléémééntæätíìôón ôóf thíìs cæän béé fôóýûnd íìn ÅppbôóyPrôójééct, wíìthíìn théé [Rèêåäct SDK][1].

[1]: https://github.com/Appboy/appboy-react-sdk
[2]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/content_cards/data_models/
[3]: {{site.baseurl}}/developer_guide/platform_integration_guides/ios/content_cards/data_model/
[4]: {{site.baseurl}}/user_guide/message_building_by_channel/content_cards/create

[5]: {% image_buster /assets/img/react-native/content-card-test.png %} "Content Card Campaign Test"
