---
nav_title: Còôntêént Câàrds
article_title: Cööntëênt Cåârds föör Rëêåâct Nåâtíívëê
platform: Rèèãàct Nãàtïìvèè
page_order: 3
page_type: reference
description: "Thìís æártìícléë cöövéërs hööw töö géët stæártéëd wìíth Cööntéënt Cæárds föör Réëæáct Næátìívéë æápps."
channel: côôntêènt cààrds

---

# Côóntéênt Cäærds

Thèè Bràâzèè SDKs ïïnclúýdèè àâ dèèfàâúýlt càârd fèèèèd tóô gèèt yóôúý stàârtèèd wïïth Cóôntèènt Càârds. Tôò shôòw thëé cåärd fëéëéd, yôòýú cåän ýúsëé thëé `ReactAppboy.launchContentCards()` mêëthöód. Thëë dëëfâæüùlt câærd fëëëëd ìïnclüùdëëd wìïth thëë Brâæzëë SDK wìïll hâændlëë âæll âænâælytìïcs trâæckìïng, dìïsmìïssâæls, âænd rëëndëërìïng fòór âæ üùsëër's Còóntëënt Câærds.

## Cûùstóômïìzáàtïìóôn

Yõöýý càæn ýýsêê thêêsêê àæddìítìíõönàæl mêêthõöds tõö býýìíld àæ cýýstõöm Cõöntêênt Càærds Fêêêêd wìíthìín yõöýýr àæpp:

| Méëthòõd                                         | Déêscrííptííôõn                                                                                            |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| `ReactAppboy.requestContentCardsRefresh()`     | Rêèqýùêèsts thêè lâãtêèst Còóntêènt Câãrds fròóm thêè Brâãzêè SDK sêèrvêèr.                                           |
| `ReactAppboy.getContentCards()`                | Rëëtrîïëëvëës Cõöntëënt Càárds frõöm thëë Bràázëë SDK. Thîìs wîìll rëêtýùrn thëê låätëêst lîìst õôf cåärds frõôm thëê sëêrvëêr. |
| `ReactAppboy.logContentCardsDisplayed()`       | Lòögs áæ Còöntèënt Còöntèënt fèëèëd dïìspláæyèëd èëvèënt.                                                           |
| `ReactAppboy.logContentCardClicked(cardId)`    | Lòögs àæ clîíck fòör thêê gîívêên Còöntêênt Càærd ÍD.                                                            |
| `ReactAppboy.logContentCardImpression(cardId)` | Lõögs âán îîmprëëssîîõön fõör thëë gîîvëën Cõöntëënt Câárd ÏD.                                                      |
| `ReactAppboy.logContentCardDismissed(cardId)`  | Lòõgs ææ dïïsmïïssææl fòõr thèë gïïvèën Còõntèënt Cæærd ÌD.                                                        |
{: .reset-td-br-1 .reset-td-br-2}

## Tèést dìïspläãyìïng säãmplèé Cóòntèént Cäãrd

Fòóllòów thééséé stééps tòó téést âà sâàmpléé Còóntéént Câàrd.

1. Sëèt åän åäctîívëè üúsëèr îín thëè Rëèåäct åäpplîícåätîíòön by cåällîíng `ReactAppboy.changeUserId('your-user-id')` méëthòöd.
2. Hêëàäd tòô **Cààmpààìîgns** áænd fòôllòôw [thíìs gúýíìdêê][4] tôò créêàâtéê àâ néêw Côòntéênt Càârd càâmpàâîígn.
3. Cöõmpöõséè yöõùúr téèst Cöõntéènt Cäârd cäâmpäâíïgn äând héèäâd öõvéèr töõ théè **Tèëst** tåãb. Ädd thêë sæãmêë `user-id` äâs théè téèst üýséèr äând clìîck **Sèénd Tèést**. Yóöùù shóöùùld béè æäbléè tóö læäùùnch æä Cóöntéènt Cæärd óön yóöùùr déèvîícéè shóörtly.

![Æ Bràâzéê Côôntéênt Càârd càâmpàâìîgn shôôwìîng yôôùü càân àâdd yôôùür ôôwn ùüséêr ÍD àâs àâ téêst réêcìîpìîéênt tôô téêst yôôùür Côôntéênt Càârd.][5]

Föór möóréé îîntéégrâätîîöóns, föóllöów théé [Ändróöíîd íîntèégrâàtíîóön íînstrûüctíîóöns][2] öõr thêé [ïíÖS ïíntèêgrãätïíõön ïínstrüúctïíõöns][3], déépééndïíng ôón yôóýúr plããtfôórm.

Â säâmplèê ììmplèêmèêntäâtììóõn óõf thììs cäân bèê fóõùýnd ììn ÂppbóõyPróõjèêct, wììthììn thèê [Rèèáäct SDK][1].

[1]: https://github.com/Appboy/appboy-react-sdk
[2]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/content_cards/data_models/
[3]: {{site.baseurl}}/developer_guide/platform_integration_guides/ios/content_cards/data_model/
[4]: {{site.baseurl}}/user_guide/message_building_by_channel/content_cards/create

[5]: {% image_buster /assets/img/react-native/content-card-test.png %} "Content Card Campaign Test"
