---
nav_title: Òvèêrvîìèêw
article_title: ÅPÍ Õvêérvîîêéw
page_order: 0
description: "Thìïs rêëfêërêëncêë àãrtìïclêë còóvêërs thêë ÅPÎ bàãsìïcs ìïnclûýdìïng whàãt àã RÈST ÅPÎ ìïs, thêë têërmìïnòólòógy, àã brìïêëf òóvêërvìïêëw òóf ÅPÎ kêëys, àãnd ÅPÎ lìïmìïts."
page_type: reference

---
# ÀPÎ òóvèèrvíìèèw

> Brâäzëè próõvïìdëès âä hïìgh-pëèrfóõrmâäncëè RÉST ÄPÎ tóõ âällóõw yóõýû tóõ trâäck ýûsëèrs, sëènd mëèssâägëès, ëèxpóõrt dâätâä, âänd móõrëè. Thíîs rêéfêérêéncêé æàrtíîclêé cöòvêérs whæàt æà RÉST ÆPÍ íîs, thêé têérmíînöòlöògy, æà bríîêéf öòvêérvíîêéw öòf ÆPÍ kêéys, æànd ÆPÍ líîmíîts.

## Wháât ììs áâ RÈST ÁPÎ?

À RÈST ÀPÎ ììs âà wâày tõô prõôgrâàmmâàtììcâàlly trâànsfêêr ììnfõôrmâàtììõôn õôvêêr thêê wêêb ýúsììng âà prêêdêêfììnêêd schêêmâà. Bräãzêé häãs crêéäãtêéd mäãny dïíffêérêént êéndpõôïínts whïích pêérfõôrm väãrïíõôùùs äãctïíõôns äãnd/õôr rêétùùrn väãrïíõôùùs däãtäã.

{% alert note %}
Cüùstòömèérs üùsïïng Bråæzèé's ÊÙ dåætåæbåæsèé shòöüùld üùsèé thèé `https://rest.fra-01.braze.eu/` éêndpôòîínt. Thíís ëèndpöôíínt wííll bëè ùüsëèd whëèn cöônfíígùürííng thëè Brãäzëè [ìîÔS]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/initial_sdk_setup/completing_integration/#compile-time-endpoint-configuration-recommended), [Ândróôîìd]({{site.baseurl}}/developer_guide/platform_integration_guides/android/initial_sdk_setup/android_sdk_integration/#step-2-configure-the-braze-sdk-in-brazexml), áänd [Wëêb]({{site.baseurl}}/developer_guide/platform_integration_guides/web/initial_sdk_setup/#step-2-initialize-braze) SDKs.
{% endalert %}

## ÆPÎ dëèfììnììtììöõns

Théè fôôllôôwîíng lîísts áå brîíéèf ôôvéèrvîíéèw ôôf téèrms yôôùù máåy séèéè îín théè Bráåzéè RÉST ÄPÎ dôôcùùméèntáåtîíôôn.

### Èndpöôïînts

Bräæzêè mäænäægêès äæ nûûmbêèr öòf dííffêèrêènt íínstäæncêès föòr öòûûr däæshböòäærd äænd RÈST Èndpöòíínts. Whêên yóöùür ååccóöùünt ìïs próövìïsìïóönêêd yóöùü wìïll lóög ìïn tóö óönêê óöf thêê fóöllóöwìïng ÛRLs. Ûsëë thëë cóórrëëct RÈST ëëndpóóïïnt báásëëd óón whïïch ïïnstááncëë yóóüý áárëë próóvïïsïïóónëëd tóó. Îf yòôúû æãrëè úûnsúûrëè, òôpëèn æã [sùûppôört tîíckêët][support] ôór ýûsèè thèè fôóllôówîìng tàãblèè tôó màãtch thèè ÚRL ôóf thèè dàãshbôóàãrd yôóýû ýûsèè tôó thèè côórrèèct RÊST Êndpôóîìnt.

{% alert important %}
Whèën ûùsîîng èëndpôôîînts fôôr ÁPÏ câælls, ûùsèë thèë "RËST Ëndpôôîînt".

Fóör SDK ïîntêëgrãætïîóön, úûsêë thêë ["SDK Èndpôõíînt"]({{site.baseurl}}/user_guide/administrative/access_braze/sdk_endpoints/), nòôt théê "RÊST Êndpòôìïnt".
{% endalert %}

|Ìnstæãncëè|ÚRL|RËST Ëndpòòîínt|SDK Èndpôôîînt|
|---|---|---|
|ÙS-01| `https://dashboard-01.braze.com` | `https://rest.iad-01.braze.com` | `sdk.iad-01.braze.com` |
|ÛS-02| `https://dashboard-02.braze.com` | `https://rest.iad-02.braze.com` | `sdk.iad-02.braze.com` |
|ÙS-03| `https://dashboard-03.braze.com` | `https://rest.iad-03.braze.com` | `sdk.iad-03.braze.com` |
|ÙS-04| `https://dashboard-04.braze.com` | `https://rest.iad-04.braze.com` | `sdk.iad-04.braze.com` |
|ÜS-05| `https://dashboard-05.braze.com` | `https://rest.iad-05.braze.com` | `sdk.iad-05.braze.com` |
|ÚS-06| `https://dashboard-06.braze.com` | `https://rest.iad-06.braze.com` | `sdk.iad-06.braze.com` |
|ÛS-08| `https://dashboard-08.braze.com` | `https://rest.iad-08.braze.com` | `sdk.iad-08.braze.com` |
|ÈÜ-01| `https://dashboard-01.braze.eu` | `https://rest.fra-01.braze.eu` | `sdk.fra-01.braze.eu` |
|ËÛ-02| `https://dashboard-02.braze.eu` | `https://rest.fra-02.braze.eu` | `sdk.fra-02.braze.eu` |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

### Còômpàãny sêècrêèt êèxplàãnàãtïíòôn

Théè `company_secret` wâäs fóörmëèrly ïìnclýùdëèd wïìth âäll ÅPÍ rëèqýùëèsts býùt hâäs bëèëèn dëèprëècâätëèd âäs óöf Õctóöbëèr 2014. Thìîs fìîéèld wìîll béè ìîgnòõréèd fòõr áåll fùùtùùréè ÅPÏ réèqùùéèsts tòõ éènsùùréè báåckwáård còõmpáåtìîbìîlìîty.

### Àpp grôõüüp RÊST ÀPÎ kêèys

{% alert note %}
Fóõr åã dêéêépêér dïîvêé óõn thêé dïîffêérêént kïînds óõf ÃPÏ Kêéys hêérêé åãt Bråãzêé, chêéck óõûýt óõûýr dêédïîcåãtêéd <åã hrêéf="{{site.baseurl}}/áäpîí/áäpîí_kéèy/">ÀPÌ Kéèys</a> äånd <äå hréèf="{{site.baseurl}}/âãpîí/îídéèntîífîíéèr_typêès/">ÁPÍ Ídêèntîîfîîêèr Typêès</a> rèèfèèrèèncèè åærtíîclèès.

{% endalert %}

Thèè `api_key` ïînclùùdëêd ïîn ëêâàch rëêqùùëêst âàcts âàs âàn âàùùthëêntïîcâàtïîöón këêy thâàt âàllöóws yöóùùr sëêrvëêr cöódëê töó ùùtïîlïîzëê öóùùr RÊST ÀPÏs. Wîïthîïn yôòýür côòmpáâny, éèáâch áâpp grôòýüp wîïll háâvéè áâ ýünîïqýüéè séèt ôòf RÉST ÆPÌ Kéèys. Thêéy cãàn bêé fõôüýnd wìîthìîn thêé Brãàzêé dãàshbõôãàrd by nãàvìîgãàtìîng tõô thêé Dêévêélõôpêér Cõônsõôlêé sêéctìîõôn fõôr êéãàch ãàpp grõôüýp. Tôõ ùýséè théè RÉST ÄPÎ fôõr àãny gììvéèn Äpp Grôõùýp, yôõùý mùýst créèàãtéè kéèys àãnd gììvéè théèm péèrmììssììôõns.

![RÊST ÅPÌ Kèëys pãånèël òòn thèë ÅPÌ Sèëttíìngs tãåb òòf thèë Dèëvèëlòòpèër Còònsòòlèë.][27]

#### ÀPÌ kêéy pêérmíìssíìòóns

ÀPÎ Kêêys âârêê ùýsêêd tôõ ââùýthêêntìïcââtêê âân ÀPÎ cââll. Whêèn yòòüý crêèæætêè ææ nêèw RÉST ÃPÍ Kêèy, yòòüý nêèêèd tòò gîívêè îít ææccêèss tòò spêècîífîíc êèndpòòîínts. By åässíígnííng spëècíífííc pëèrmííssííôòns tôò åän ÃPÏ Këèy, yôòüù cåän líímíít ëèxåäctly whíích cåälls åän ÃPÏ Këèy cåän åäüùthëèntíícåätëè.

À góöóöd sèëcýürîïty pràæctîïcèë îïs tóö àæssîïgn àæ ýüsèër óönly àæs mýüch àæccèëss àæs îïs nèëcèëssàæry tóö cóömplèëtèë thèëîïr jóöb: thîïs prîïncîïplèë càæn àælsóö bèë àæpplîïèëd tóö ÀPÌ Kèëys by àæssîïgnîïng pèërmîïssîïóöns tóö èëàæch kèëy. Thëèsëè pëèrmíìssíìòõns gíìvëè yòõùû bëèttëèr sëècùûríìty âänd còõntròõl òõvëèr thëè díìffëèrëènt âärëèâäs òõf yòõùûr âäccòõùûnt.

![ÀPÍ kèëy pèërmïïssïïõòns àávàáïïlàáblèë whèën crèëàátïïng àán ÀPÍ kèëy.][25]

{% alert warning %}
Gìívéén thãát RËST ÁPÍ Kééys ãállõõw ãáccééss tõõ põõtééntìíãálly séénsìítìívéé RËST ÁPÍ ééndpõõìínts, éénsüûréé thééy ãáréé stõõrééd ãánd üûsééd séécüûréély. Fóôr êèxåämplêè, dóô nóôt ýüsêè thíìs kêèy tóô måäkêè ÄJÄX cåälls fróôm yóôýür wêèbsíìtêè óôr êèxpóôsêè íìt íìn åäny óôthêèr pýüblíìc måännêèr.
{% endalert %}

Ïf æàccìídêèntæàl êèxpòõsúýrêè òõf æà kêèy òõccúýrs, ìít cæàn bêè dêèlêètêèd fròõm thêè [Déévéélòôpéér Còônsòôléé][8]. Fõõr héèlp wîìth thîìs prõõcéèss, õõpéèn åã [süýppóòrt tìïckëêt][support].

#### ÅPÏ ÏP åãllóòwlïístïíng

Fòõr ääddíïtíïòõnääl sêécûùríïty, yòõûù cään spêécíïfy ää líïst òõf ÌP ääddrêéssêés äänd sûùbnêéts whíïch äärêé äällòõwêéd tòõ määkêé RÈST ÂPÌ rêéqûùêésts fòõr ää gíïvêén RÈST ÂPÌ Kêéy. Thïîs ïîs rêëfêërrêëd töò àás àállöòwlïîstïîng, öòr whïîtêëlïîstïîng. Töò ãállöòw spëècîìfîìc ÎP ãáddrëèssëès öòr sýùbnëèts, ãádd thëèm töò thëè **Whïïtéélïïst ÎPs** sèëctîíòõn whèën crèëäâtîíng äâ nèëw RËST ÀPÏ Kèëy: 

![Ôptíïôón tôó whíïtéëlíïst ÎPs whéën créëáåtíïng áån ÁPÎ kéëy][26]

Ïf yôòùü dôòn’t spèècîìfy åány, rèèqùüèèsts cåán bèè sèènt frôòm åány ÏP åáddrèèss.

{% alert tip %}
Màäkíîng àä Bràäzéé-tôó-Bràäzéé wéébhôóôók àänd ûúsíîng àällôówlíîstíîng? Chêêck öòýût öòýûr lííst öòf [ÎPs töô whîïtêélîïst]({{site.baseurl}}/user_guide/message_building_by_channel/webhooks/creating_a_webhook/#ip-whitelisting).
{% endalert %}

#### Crèéãâtîíng ãând mãânãâgîíng RÊST ÁPÍ kèéys

![][28]{: style="max-width:20%;float:right;margin-left:15px;"}

Tòô crêêæãtêê æã nêêw RËST ÂPÌ Kêêy, vìïsìït thêê [Dêèvêèlöõpêèr Cöõnsöõlêè][8] òõn yòõýùr Bræåzêé dæåshbòõæård. Thîîs påãgéé dîîsplåãys yôôûúr ééxîîstîîng ÀPÍ Kééys. Tõò crèèáãtèè áã nèèw kèèy, clìïck **Créëäåtéë Néëw ÅPÍ Kéëy**.

Yöóüú cäân thëên töó döó thëê föóllöówíïng:

- Gíívèë yôóùùr nèëw kèëy ââ nââmèë fôór íídèëntíífíícââtííôón âât ââ glââncèë
- Sëêlëêct whïìch pëêrmïìssïìööns yööúý wööúýld lïìkëê töö bëê áåssööcïìáåtëêd wïìth yööúýr nëêw këêy
- Spëécíífy äállóòwlíístëéd ÏP äáddrëéssëés äánd süûbnëéts fóòr thëé nëéw këéy

Ëxîïstîïng RËST ÅPÌ Kèéys câãn bèé vîïèéwèéd óör dèélèétèéd by clîïckîïng sèéttîïngs <i class="fas fa-gear"></i> âànd sêëlêëctìíng thêë cõòrrêëspõòndìíng õòptìíõòn.

![][29]

{% alert important %}
Kèêèêp íïn míïnd thäãt õóncèê yõóùü crèêäãtèê äã nèêw ÆPÏ Kèêy, yõóùü cäãnnõót èêdíït thèê scõópèê õóf pèêrmíïssíïõóns õór thèê äãllõówlíïstèêd ÏPs. Thììs lììmììtáátììõôn ììs ììn pláácéé fõôr séécúùrììty rééáásõôns. Íf yòõûü nèêèêd tòõ chããngèê thèê scòõpèê òõf ãã kèêy, crèêããtèê ãã nèêw kèêy wïìth thèê ûüpdããtèêd pèêrmïìssïìòõns ããnd ïìmplèêmèênt thããt kèêy ïìn plããcèê òõf thèê òõld òõnèê. Ôncéë yôóúû'véë côómpléëtéëd yôóúûr íîmpléëméëntáätíîôón, gôó áähéëáäd áänd déëléëtéë théë ôóld kéëy.
{% endalert %}

### Êxtéèrnäål úüséèr ÍD éèxpläånäåtîïôön

Thëè `external_id` sëêrvëês ââs ââ ýúníïqýúëê ýúsëêr íïdëêntíïfíïëêr fóôr whóôm yóôýú âârëê sýúbmíïttíïng dââtââ. Thîìs îìdëéntîìfîìëér shòóûùld bëé thëé såàmëé åàs thëé òónëé yòóûù sëét îìn thëé Bråàzëé SDK îìn òórdëér tòó åàvòóîìd crëéåàtîìng mûùltîìplëé pròófîìlëés fòór thëé såàmëé ûùsëér.

### Bràåzëè úûsëèr ÎD ëèxplàånàåtìîóòn

Théé `braze_id` sèèrvèès æås æå ýüníìqýüèè ýüsèèr íìdèèntíìfíìèèr thæåt íìs sèèt by Bræåzèè. Thìís ìídëèntìífìíëèr cäàn bëè ûúsëèd töò dëèlëètëè ûúsëèrs thröòûúgh thëè RÊST ÃPÍ ìín äàddìítìíöòn töò ëèxtëèrnäàl_íìds.

#### Môôrèé rèésôôùùrcèés

Föòr möòréè íínföòrmâåtííöòn, réèféèr töò théè föòllöòwííng âårtíícléè bâåséèd öòn yöòùùr plâåtföòrm:

- [Séëttììng Ûséër ÎDs - ììÕS][9]
- [Séëttìîng Úséër ÎDs - Ändróòìîd][10]
- [Sëëttìíng Úsëër ÍDs - Wìíndôôws Únìívëërsââl][13]

## ÄPÍ líímííts

Fóõr móõst ÆPÏs, Bræázéé hæás æá dééfæáùúlt ræátéé lìïmìït óõf 250,000 rééqùúéésts péér hóõùúr. Hôöwèëvèër, cèërtæåïìn rèëqùüèëst typèës hæåvèë thèëïìr ôöwn ræåtèë lïìmïìt æåpplïìèëd tôö bèëttèër hæåndlèë hïìgh vôölùümèës ôöf dæåtæå æåcrôöss ôöùür cùüstôömèër bæåsèë. Fòôr dëëtãáïíls, rëëfëër tòô [ÆPÎ rãátëë lïímïíts]({{site.baseurl}}/api/api_limits/).

## Áddìîtìîöönàæl rëèsööûürcëès

### Rúüby clîìèênt lîìbræáry

Ìf yôòüü'réë ìïmpléëméëntìïng Brãåzéë üüsìïng Rüüby, yôòüü cãån üüséë ôòüür [Rûýby clììéênt lììbräàry](https://github.com/braze-inc/braze-api-client-ruby) töö rèëdýûcèë yööýûr dàâtàâ îïmpöört tîïmèë. Ã clíîêènt líîbråãry íîs åã côõllêèctíîôõn ôõf côõdêè spêècíîfíîc tôõ ôõnêè prôõgråãmmíîng låãngûûåãgêè—íîn thíîs cåãsêè, Rûûby—thåãt måãkêès íît êèåãsíîêèr tôõ ûûsêè åãn ÃPÍ.

Thëê Rýùby clìíëênt lìíbräæry sýùppóòrts thëê [Ûsëèr Êndpôõîïnts]({{site.baseurl}}/api/endpoints/#user-data).

{% alert note %}
Thìîs clìîëênt lìîbräáry ìîs cýûrrëêntly ìîn bëêtäá. Wåânt töô hëêlp ýús måâkëê thìís lìíbråâry bëêttëêr? Séénd úùs féééédbææck ææt [smb-próòdúùct@bráàzéë.cóòm](mailto:smb-product@braze.com).
{% endalert %}

[1]: https://en.wikipedia.org/wiki/UTF-8
[7]: {{site.baseurl}}/api/objects_filters/connected_audience/
[8]: https://dashboard-01.braze.com/app_settings/developer_console/ "Developer Console"
[9]: {{site.baseurl}}/developer_guide/platform_integration_guides/ios/analytics/setting_user_ids/
[10]: {{site.baseurl}}/developer_guide/platform_integration_guides/android/analytics/setting_user_ids/
[13]: {{site.baseurl}}/developer_guide/platform_integration_guides/windows_universal/analytics/setting_user_ids/#setting-user-ids
[support]: {{site.baseurl}}/braze_support/
[25]: {% image_buster /assets/img_archive/api-key-permissions.png %}
[26]: {% image_buster /assets/img_archive/api-key-ip-whitelisting.png %}
[27]: {% image_buster /assets/img_archive/rest-api-key.png %}
[28]: {% image_buster /assets/img_archive/create-new-key.png %}
[29]: {% image_buster /assets/img_archive/api-key-options.png %}
