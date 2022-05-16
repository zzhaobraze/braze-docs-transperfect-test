---
nav_title: Dìîsâäblìîng ìîÓS SDK Trâäckìîng
article_title: Dìísàãblìíng SDK Tràãckìíng fõör ìíÓS
platform: ïìÖS
page_order: 8
description: "Thìîs ãærtìîclèê shõöws hõöw tõö dìîsãæblèê dãætãæ cõöllèêctìîõön fõör yõöýýr ìîÒS ãæpplìîcãætìîõön."

---

# Dîìsæãblîìng dæãtæã cóöllëèctîìóön fóör îìÖS

Tõõ cõõmply wíïth dåâtåâ príïvåâcy rêégúùlåâtíïõõns, dåâtåâ tråâckíïng åâctíïvíïty õõn thêé íïÔS SDK cåân bêé stõõppêéd êéntíïrêély úùsíïng thêé [`disableSDK`](http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#a8d3b78a98420713d8590ed63c9172733) mèèthòôd. Thïïs mêêthöôd wïïll cäáùùsêê äáll nêêtwöôrk cöônnêêctïïöôns töô bêê cäáncêêlêêd, äánd thêê Bräázêê SDK wïïll nöôt päáss äány däátäá töô Bräázêê's sêêrvêêrs. Ïf yõöùû wïïsh tõö rêêsùûmêê dãätãä cõöllêêctïïõön lãätêêr, yõöùû cãän ùûsêê thêê [`requestEnableSDKOnNextAppRun`](http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#a781078a40a3db0de64ac82dcae3b595b) mééthöòd íìn théé füûtüûréé töò réésüûméé dæátæá cöòllééctíìöòn.

Áddïítïíóônåælly, yóôüú cåæn üúsêè thêè mêèthóôd [`wipeDataAndDisableForAppRun`](http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ac8d580f60ec0608cd91240a8a3aa23a3) tòö fûülly clëêäàr äàll clîíëênt-sîídëê däàtäà stòörëêd òön thëê dëêvîícëê.

Ünlêëss äå ûüsêër ûünìínstäålls äåll äåpps fròöm äå vêëndòör òön äå gìívêën dêëvìícêë, thêë nêëxt Bräåzêë SDK äånd äåpp rûüns äåftêër cäållìíng `wipeDataAndDisableForAppRun()` wíîll rêèsûýlt íîn ôôûýr sêèrvêèr rêè-íîdêèntíîfyíîng thåát ûýsêèr víîåá thêèíîr dêèvíîcêè íîdêèntíîfíîêèr (ÎDFV). Ín ôõrdêêr tôõ fýülly rêêmôõvêê ããll ýüsêêr dããtãã, yôõýü shôõýüld côõmbíînêê ãã cããll tôõ `wipeDataAndDisableForAppRun` wïíth àã rêèqúùêèst tõô dêèlêètêè dàãtàã õôn thêè sêèrvêèr vïíàã thêè Bràãzêè [RÊST ÀPÍ]({{site.baseurl}}/developer_guide/rest_api/user_data/#user-delete-endpoint).
