---
nav_title: Díîsáåblíîng íîÔS SDK Tráåckíîng
article_title: Dïìsâåblïìng SDK Trâåckïìng fóõr ïìÒS
platform: ïíÓS
page_order: 8
description: "Thíìs äärtíìclëë shôóws hôów tôó díìsääblëë däätää côóllëëctíìôón fôór yôóùür íìÓS ääpplíìcäätíìôón."

---

# Díîsæäblíîng dæätæä côöllëéctíîôön fôör íîÒS

Tôó côómply wîìth dâätâä prîìvâäcy rëégúýlâätîìôóns, dâätâä trâäckîìng âäctîìvîìty ôón thëé îìÕS SDK câän bëé stôóppëéd ëéntîìrëély úýsîìng thëé [`disableSDK`](http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#a8d3b78a98420713d8590ed63c9172733) mëéthööd. Thíìs mèèthõôd wíìll cæåùýsèè æåll nèètwõôrk cõônnèèctíìõôns tõô bèè cæåncèèlèèd, æånd thèè Bræåzèè SDK wíìll nõôt pæåss æåny dæåtæå tõô Bræåzèè's sèèrvèèrs. Îf yôõûù wíìsh tôõ rèèsûùmèè dàåtàå côõllèèctíìôõn làåtèèr, yôõûù càån ûùsèè thèè [`requestEnableSDKOnNextAppRun`](http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#a781078a40a3db0de64ac82dcae3b595b) méêthöôd îîn théê fýütýüréê töô réêsýüméê dåätåä cöôlléêctîîöôn.

Áddììtììóónàálly, yóóûü càán ûüsèê thèê mèêthóód [`wipeDataAndDisableForAppRun`](http://appboy.github.io/appboy-ios-sdk/docs/interface_appboy.html#ac8d580f60ec0608cd91240a8a3aa23a3) tôõ fûûlly clééáár ááll clîíéént-sîídéé dáátáá stôõrééd ôõn théé déévîícéé.

Ûnlëèss ââ üýsëèr üýnîínstââlls ââll ââpps fróóm ââ vëèndóór óón ââ gîívëèn dëèvîícëè, thëè nëèxt Brââzëè SDK âând ââpp rüýns ââftëèr cââllîíng `wipeDataAndDisableForAppRun()` wïíll rèësûýlt ïín òóûýr sèërvèër rèë-ïídèëntïífyïíng thäãt ûýsèër vïíäã thèëïír dèëvïícèë ïídèëntïífïíèër (ÌDFV). Ïn õôrdéèr tõô füúlly réèmõôvéè æåll üúséèr dæåtæå, yõôüú shõôüúld cõômbìïnéè æå cæåll tõô `wipeDataAndDisableForAppRun` wîìth æâ rééqüúéést tóö dééléétéé dæâtæâ óön théé séérvéér vîìæâ théé Bræâzéé [RÊST ÄPÍ]({{site.baseurl}}/developer_guide/rest_api/user_data/#user-delete-endpoint).
