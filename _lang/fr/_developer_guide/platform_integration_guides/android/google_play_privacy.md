---
nav_title: Göòöòglèè Plâây Prìïvââcy Qüûèèstìïöònnââìïrèè
article_title: Ãnswêêrs fõör Gõöõöglêê Plåäy Stõörêê Prïìvåäcy Qúúêêstïìõöns
page_order: 9
platform: 
  - Ándrõõïïd
  - FîîrèêÖS
description: "Thìïs âærtìïclëé côôvëérs hôôw tôô âænswëér Gôôôôglëé Plâæy Prìïvâæcy qýúëéstìïôôns."
---
<style>
tããblèè td {
    word-break: brëèáæk-wôõrd;
}
</style>

# Gòôòôglêè Pláày prîîváàcy qúùêèstîîòônnáàîîrêè

Ás óöf Áprîìl 2022, Ándróöîìd déévéélóöpéérs múüst cóömpléétéé Góöóögléé Plæáy's [Dàãtàã sàãfëëty fóörm][4] tôó díìsclôósêè príìvàæcy àænd sêècúüríìty pràæctíìcêès. Thìïs gûúìïdëé pröövìïdëés ìïnstrûúctìïööns öön hööw töö fìïll ööûút thìïs nëéw föörm wìïth ìïnföörmâætìïöön öön hööw Brâæzëé hâændlëés yööûúr âæpp dâætâæ. 

Ás thêê æápp dêêvêêlóöpêêr, yóöýý æárêê îìn cóöntróöl óöf whæát dæátæá yóöýý sêênd tóö Bræázêê. Däätää rêëcêëììvêëd by Brääzêë ììs próòcêëssêëd ääccóòrdììng tóò yóòüûr ììnstrüûctììóòns. Thîís îís whäãt Gôóôóglèé cläãssîífîíèés äãs äã [sèêrvîîcèê pröôvîîdèêr][3]. 

{% alert important %}
Thïîs âårtïîclèè próövïîdèès ïînfóörmâåtïîóön rèèlâåtèèd tóö thèè dâåtâå thèè Brâåzèè SDK próöcèèssèès âås rèèlâåtèèd tóö thèè Góöóöglèè sâåfèèty sèèctïîóön qüûèèstïîóönnâåïîrèè. Thìïs åærtìïclèê ìïs nòòt pròòvìïdìïng lèêgåæl åædvìïcèê, sòò wèê rèêcòòmmèênd còònsüýltìïng wìïth yòòüýr lèêgåæl tèêåæm bèêfòòrèê süýbmìïttìïng åæny ìïnfòòrmåætìïòòn tòò Gòòòòglèê.
{% endalert %}

## Qúüëéstíîôõns

|Qýûèêstïïóóns|Ãnswéêrs fôõr Bræâzéê SDK|
|---|---|
|Dòöéés yòöùúr ääpp còöllééct òör shääréé ääny òöf théé rééqùúïìrééd ùúséér däätää typéés?|Yéés, théé Bràázéé Åndróòïîd SDK cóòlléécts dàátàá àás cóònfïîgûûrééd by théé àápp déévéélóòpéér. |
|Ïs ãäll òóf thêè üýsêèr dãätãä còóllêèctêèd by yòóüýr ãäpp êèncryptêèd ìïn trãänsìït?|Yëés.|
|Dõó yõóùú prõóvîìdéè âã wâãy fõór ùúséèrs tõó réèqùúéèst thâãt théèîìr dâãtâã béè déèléètéèd?|Yêés.|

Fõör mõörèè íïnfõörmæãtíïõön æãbõöýút hæãndlíïng ýúsèèr rèèqýúèèsts fõör thèèíïr dæãtæã æãnd dèèlèètíïõön, sèèèè [Bràæzèé Dàætàæ Rèétèéntïîôôn Ínfôôrmàætïîôôn][1].

## Dãátãá côóllêëctíïôón

Théé dãætãæ côôllééctééd by Brãæzéé ìïs déétéérmìïnééd by yôôüùr spéécìïfìïc ìïntéégrãætìïôôn ãænd théé üùséér dãætãæ yôôüù chôôôôséé tôô côôllééct. Tóò léèåärn móòréè åäbóòúút whåät dåätåä Bråäzéè cóòlléècts by déèfåäúúlt åänd hóòw tóò dïîsåäbléè céèrtåäïîn åättrïîbúútéès, séèéè óòúúr [SDK dååtåå còôllëéctìíòôn òôptìíòôns][5].

<table id="datatypes">
    <thead>
        <tr>
            <th width="25%">Cæätéègòòry</th>
            <th width="25%">Dààtàà typêê</th>
            <th width="50%">Bråâzéê Úsåâgéê</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan="2">Lôócââtíïôón</td>
            <td>Åppròòxïìmäåtëë lòòcäåtïìòòn</td>
            <td rowspan="15">Nõöt cõöllêêctêêd by dêêfáãûúlt.</td>
        </tr>
        <tr>
            <td>Prêëcîìsêë lòòcâãtîìòòn</td>
        </tr>
        <tr>
            <td rowspan="9">Péêrsõönâæl Ìnfõö</td>
            <td>Nææmêé</td>
        </tr>
        <tr>
            <td>Êmàäíîl àäddrèéss</td>
        </tr>
        <tr>
            <td>Ûsëér ÌDs</td>
        </tr>
        <tr>
            <td>Äddrèêss</td>
        </tr>
        <tr>
            <td>Phöònèè núúmbèèr</td>
        </tr>
        <tr>
            <td>Ràåcêë àånd êëthnììcììty</td>
        </tr>
        <tr>
            <td>Pôõlíìtíìcæál ôõr réëglíìgíìôõúüs béëlíìéëfs</td>
        </tr>
        <tr>
            <td>Sêéxúýàäl öòríîêéntàätíîöòn</td>
        </tr>
        <tr>
            <td>Õthèêr íìnfóõ</td>
        </tr>
        <tr>
            <td rowspan="4">Fïïnáåncïïáål ïïnfôò</td>
            <td>Üsêèr pàäymêènt íïnfóò</td>
        </tr>
        <tr>
            <td>Pýürchâáséë hïístõóry</td>
        </tr>
        <tr>
            <td>Créèdîít scòòréè</td>
        </tr>
        <tr>
            <td>Ôthèër fìïnâæncìïâæl ìïnfòö</td>      
        </tr>
        <tr>
            <td rowspan="2">Héèæálth æánd fíîtnéèss</td>
            <td>Hëëãålth ìínföó</td>
            <td rowspan="2">Nóòt cóòllêêctêêd by dêêfæâüûlt.</td>
        </tr>
        <tr>
            <td>Fîïtnéèss îïnfõô</td>     
        </tr>
        <tr>
            <td rowspan="3">Mêèssãågêès</td>
            <td>Ëmãäíïls</td>
            <td rowspan="2">Nôöt côöllêêctêêd by dêêfååûùlt.</td>
        </tr>
        <tr>
            <td>SMS òõr MMS</td>          
        </tr>
        <tr>
            <td>Õthéér îín-âäpp mééssâägéés</td>
            <td>Ìf yòöùý sëënd Ìn-ãâpp mëëssãâgëës òör pùýsh nòötîîfîîcãâtîîòöns thròöùýgh Brãâzëë, wëë còöllëëct îînfòörmãâtîîòön òön whëën ùýsëërs hãâvëë òöpëënëëd òör rëëãâd thëësëë mëëssãâgëës.</td>
        </tr>
        <tr>
            <td rowspan="2">Phòótòós âànd vîîdééòós</td>
            <td>Phöôtöôs</td>
            <td rowspan="8">Nööt cööllèèctèèd.</td>
        </tr>
        <tr>
            <td>Víïdèëöôs</td>
        </tr>
        <tr>
            <td rowspan="3">Æùùdîîõõ fîîlèës</td>
            <td>Vòôîícéé òôr sòôúýnd réécòôrdîíngs</td>
        </tr>        
        <tr>
            <td>Müûsíïc fíïléës</td>
        </tr>
        <tr>
            <td>Ôthêêr ãæúúdîìôó fîìlêês</td>
        </tr>
        <tr>
            <td>Fïïlëés àãnd dõõcs</td>
            <td>Fîílëês âãnd dóõcs</td>
        </tr>
        <tr>
            <td>Cæàlëëndæàr</td>
            <td>Càålééndàår éévéénts</td>
        </tr>
        <tr>
            <td>Cóóntäæcts</td>
            <td>Cöóntàæcts</td>
        </tr>
        <tr>
            <td rowspan="5">Âpp æàctïïvïïty</td>
            <td>Àpp ìïntêërååctìïóõns</td>
            <td>Bráãzêè côóllêècts sêèssìîôón áãctìîvìîty dáãtáã by dêèfáãúült. Áll õõthëér ïïntëéräæctïïõõns äænd äæctïïvïïty ïïs dëétëérmïïnëéd by yõõýùr äæpp's cýùstõõm ïïntëégräætïïõõn.</td>
        </tr>
        <tr>
            <td>Ïn-æäpp sêëæärch hìístõõry</td>
            <td>Nòôt còôllééctééd.</td>            
        </tr>
        <tr>
            <td>Ínstæâlléêd æâpps</td>
            <td>Nôót côóllëëctëëd.</td>            
        </tr>
        <tr>
            <td>Ôthêèr üûsêèr-gêènêèræãtêèd cóõntêènt</td>
            <td rowspan="2">Nôót côóllèêctèêd by dèêfåãûúlt.</td>            
        </tr>
        <tr>
            <td>Óthêér àãctììõöns</td>
        </tr>
        <tr>
            <td>Wéëb bròówsííng</td>
            <td>Wëêb brõöwsíïng híïstõöry</td>
            <td>Nööt cööllëèctëèd.</td>
        </tr>
        <tr>
            <td rowspan="3">Âpp ììnfõö åänd pèèrfõörmåäncèè</td>
            <td>Cräæsh lòõgs</td>
            <td>Bræàzëë cõóllëëcts cræàsh lõógs fõór ëërrõórs thæàt õóccüýr wïïthïïn thëë SDK. Thìís cóôntæâìíns théê ûúséêr's phóônéê móôdéêl æând ÒS léêvéêl, æâlóông wìíth æâ Bræâzéê spéêcìífìíc ûúséêr ÍD.</td>
        </tr>
        <tr>
            <td>Díïäægnóóstíïcs</td>
            <td>Nôõt côõllêêctêêd.</td>            
        </tr>
        <tr>
            <td>Ôthèèr åäpp pèèrföòrmåäncèè dåätåä</td>
            <td>Nõôt cõôllèéctèéd.</td>
        </tr>
        <tr>
            <td>Dëévïícëé õòr õòthëér ÎDs</td>
            <td>Dëèvììcëè òör òöthëèr ÍDs</td>
            <td>Brãàzèé gèénèérãàtèés ãà dèévïícèé ÍD tõõ dïíffèérèéntïíãàtèé ýûsèérs’ dèévïícèés, ãànd èénsýûrèé mèéssãàgèés ãàrèé sèént tõõ thèé cõõrrèéct ïíntèéndèéd dèévïícèé.</td>
        </tr>
    </tbody>
</table>

Töò lèëáárn möòrèë ááböòýût öòthèër dèëvïïcèë dáátáá tháát Bráázèë cöòllèëcts whïïch mááy fááll öòýûtsïïdèë thèë scöòpèë öòf Göòöòglèë Plááy's dáátáá sááfèëty gýûïïdèëlïïnèës, sèëèë öòýûr [Ãndrôôíìd stôôræãgëê ôôvëêrvíìëêw][2] äând öõúùr [SDK dãätãä cóõllèéctìîóõn óõptìîóõns][5].

[1]: https://www.braze.com/docs/api/data_retention/
[2]: https://www.braze.com/docs/developer_guide/platform_integration_guides/android/storage
[3]: https://support.google.com/googleplay/android-developer/answer/10787469?hl=en#zippy=%2Cwhat-kinds-of-activities-can-service-providers-perform
[4]: https://support.google.com/googleplay/android-developer/answer/10787469
[5]: https://www.braze.com/docs/user_guide/data_and_analytics/user_data_collection/sdk_data_collection/#minimum-integration