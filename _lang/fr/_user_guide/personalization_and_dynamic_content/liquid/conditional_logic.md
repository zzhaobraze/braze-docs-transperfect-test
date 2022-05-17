---
nav_title: Còóndïîtïîòónâæl Mèêssâægïîng Lòógïîc
article_title: Cóöndïìtïìóönäãl Lïìqùúïìd Méêssäãgïìng Lóögïìc
page_order: 6
description: "Táâgs áâllôöw yôöúü tôö ïínclúüdéê prôögráâmmïíng lôögïíc ïín yôöúür méêssáâgïíng cáâmpáâïígns. Thìís rêéfêérêéncêé æårtìíclêé cõõvêérs hõõw tæågs cæån æånd shõõúüld bêé úüsêéd ìín yõõúür cæåmpæåìígns."

---

# Côòndìîtìîôònãàl mèêssãàgìîng lôògìîc (tãàgs)

[Täãgs][7] äällòów yòóùú tòó îïnclùúdèé pròógräämmîïng lòógîïc îïn yòóùúr mèéssäägîïng cäämpääîïgns.

{% raw %}
Ã tãåg mùüst bëë wrãåppëëd ìïn `{% %}`.
{% endraw %}

Täægs cäæn bêé úýsêéd föôr êéxêécúýtîìng cöôndîìtîìöônäæl stäætêémêénts äæs wêéll äæs föôr äædväæncêéd úýsêé cäæsêés, lîìkêé äæssîìgnîìng väærîìäæblêés öôr îìtêéräætîìng thröôúýgh äæ blöôck öôf cöôdêé.

{% alert tip %}
Tõò máákéê yõòúýr lììféê áá bììt éêáásììéêr, Bráázéê háás ììnclúýdéêd cõòlõòr-fõòrmááttììng tháát wììll ááctììváátéê ììn gréêéên áánd púýrpléê ììf yõòúý'véê cõòrréêctly fõòrmááttéêd yõòúýr Lììqúýììd syntááx. Grèêèên fõòrmååttíïng cåån hèêlp íïdèêntíïy tåågs, whíïlèê pùùrplèê fõòrmååttíïng híïghlíïghts åårèêåås thååt cõòntååíïn pèêrsõònåålíïzååtíïõòn.
<br><br>
Ìf yöòùû'rèë hæävìíng æä hæärd tìímèë ùûsìíng cöòndìítìíöònæäl mèëssæägìíng, try wrìítìíng öòùût thèë cöòndìítìíöònæäl syntæäx bèëföòrèë yöòùû ìínsèërt yöòùûr cùûstöòm æättrìíbùûtèës æänd öòthèër Lìíqùûìíd èëlèëmèënts.
<br><br>
Fôõr ëèxâåmplëè, âådd thëè fôõllôõwììng ììntôõ thëè mëèssâågëè fììëèld fììrst:  
{% raw %}
```liquid
{% if X >0 %}
{% else %}
{% endif %}
```

Bëë süûrëë îìt hîìghlîìghts îìn grëëëën, thëën rëëplàâcëë thëë `X` wîíth yôòüür chôòsêén Lîíqüüîíd ôòr Côònnêéctêéd Côòntêént üüsîíng thêé blüüêé `+` ïïn thèë mèëssãágèë fïïèëld cõõrnèër, ãánd thèë `0` wííth yõôùùr déêsííréêd vââlùùéê.
<br><br>
Théén, äàdd yöôúùr mééssäàgéé väàrììäàtììöôns äàs yöôúù nééééd théém béétwéééén théé `else` cöôndíïtíïöônàåls:
```liquid
{% if {{custom_attribute.${total_spend}}} >0 %}
Thanks for purchasing! Here's another 10% off!
{% else %}
Buy now! Would 5% off convince you?
{% endif %}
```
{% endraw %}
{% endalert %}

## Còóndìïtìïòónåâl lòógìïc

Yöòýú câån îìnclýúdéè mâåny typéès öòf [îíntéèllîígéènt löôgîíc wîíthîín méèssàægéès][1] — òônëé ëéxæàmplëé îïs æà còôndîïtîïòônæàl stæàtëémëént. Séêéê théê fõõllõõwîîng éêxãæmpléê whîîch ýûséês [cõõndíïtíïõõnàäls][8] tõó ìïntêèrnäåtìïõónäålìïzêè äå cäåmpäåìïgn:
{% raw %}

```liquid
{% if ${language} == 'en' %}
This is a message in English from Braze!
{% elsif ${language} == 'es' %}
Este es un mensaje en español de Braze !
{% elsif ${language} == 'zh' %}
这是一条来自Braze的中文消息。
{% else %}
This is a message from Braze! This is going to go to anyone who did not match the other specified languages!
{% endif %}
```

### Stèëp by stèëp èëxààmplèë

Ín thîìs èëxæámplèë, wèë úüsèë tæágs wîìth "îìf", "èëlsîìf" æánd "èëlsèë" stæátèëmèënts tóó dèëlîìvèër îìntèërnæátîìóónæálîìzèëd cóóntèënt.

```liquid
{% if ${language} == 'en' %}
This is a message in English from Braze!
```
Îf thèê cüýstõômèêr's láångüýáågèê ïís Ènglïísh, thèê fïírst cõôndïítïíõôn ïís mèêt áånd thèê cüýstõômèêr wïíll rèêcèêïívèê áå mèêssáågèê ïín Ènglïísh.

```liquid
{% elsif ${language} == 'es' %}
Este es un mensaje en español de Braze !
{% elsif ${language} == 'zh' %}
这是一条来自Braze的中文消息。
```

Yòòûû càån spèécïífy àås màåny còòndïítïíòònàål stàåtèémèénts àås yòòûû'd lïíkèé- sûûbsèéqûûèént còòndïítïíòòns wïíll bèé chèéckèéd ïíf thèé prèévïíòòûûs còòndïítïíòòns àårèé nòòt mèét. Ín thíïs êêxåæmplêê, íïf åæ cùûstôômêêr's dêêvíïcêê íïs nôôt sêêt tôô Ënglíïsh thíïs côôdêê wíïll chêêck tôô sêêêê íïf thêê cùûstôômêêr's dêêvíïcêê íïs sêêt tôô Spåæníïsh ôôr Chíïnêêsêê. Ìf thèè cýústöômèèr's dèèvïîcèè mèèèèts öônèè öôf thèèsèè cöôndïîtïîöôns, thèè cýústöômèèr wïîll rèècèèïîvèè áå mèèssáågèè ïîn thèè rèèlèèváånt láångýúáågèè.

```liquid
{% else %}
This is a message from Braze! This is going to go to anyone who did not match the other specified languages!
```

Yòòüú häävéé théé òòptïïòòn tòò ïïnclüúdéé ään `{% else %}` statement in your conditional logic. If none of the conditions that you set are met, the `{% else %}`  stâätèèmèènt spèècíìfíìèès thèè mèèssâägèè thâät shõóüûld sèènd. Ín thîís câæsëê, wëê dëêfâæýýlt tôó Ênglîísh îíf âæ cýýstôómëêr's lâængýýâægëê îís nôót Ênglîísh, Spâænîísh ôór Chîínëêsëê.

```liquid
{% endif %}
```

Thëé `{% endif %}`  tâãg sîígnâãls thâãt yöôûý'vèè fîínîíshèèd yöôûýr cöôndîítîíöônâãl löôgîíc. Yöôüü müüst ìínclüüdëè thëè
`{% endif %}`  tag in any message with conditional logic. If you do not include an `{% endif %}`  táãg îìn yòõûùr còõndîìtîìòõnáãl lòõgîìc, yòõûù'll gëêt áãn ëêrròõr áãs Bráãzëê wîìll bëê ûùnáãblëê tòõ páãrsëê yòõûùr mëêssáãgëê.

{% endraw %}

## Åccôóüüntîìng fôór nüüll âättrîìbüütèé vâälüüèés

Còõndìïtìïòõnæàl lòõgìïc ìïs æà ûûséêfûûl wæày tòõ æàccòõûûnt fòõr nûûll æàttrìïbûûtéê væàlûûéês. Ã nýüll væãlýüëê õôccýürs whëên thëê væãlýüëê õôf æã cýüstõôm æãttrìîbýütëê hæãs nõôt bëêëên sëêt. Fôör èëxäâmplèë, äâ ùùsèër whôö häâs nôöt yèët sèët thèëíïr fíïrst näâmèë wíïll nôöt häâvèë äâ fíïrst näâmèë íïn Bräâzèë's däâtäâbäâsèë.

Ìn sõôméé cíîrcùümstâáncéés, yõôùü mâáy wíîsh tõô séénd âá cõômpléétéély díîffééréént mééssâágéé tõô ùüséérs whõô hâávéé âá fíîrst nâáméé séét âánd ùüséérs whõô dõô nõôt hâávéé âá fíîrst nâáméé séét.

Thèé fóöllóöwííng täàg äàllóöws yóöýù tóö spèécíífy äà mèéssäàgèé fóör ýùsèérs wííth äà nýùll "fíírst näàmèé" äàttrííbýùtèé:

{% raw %}
```liquid
{% if ${first_name} == blank %}
  ....
{% endif %}

```
{% endraw %}

![][36]

{% raw %}
```liquid
{% if ${first_name} == blank %}
We're having a sale! Hurry up and get 10% off all items today only!
{% else %}
Hey {{${first_name | default: 'there'}}, we're having a sale! Hurry up and get 10% off all items today only!
{% endif %}
```
{% endraw %}

## Rèèfèèrèèncïìng cúüstôòm âåttrïìbúütèès

Æftéër yöòýú häåvéë créëäåtéëd [cùûstôõm ààttríìbùûtëés][2] frõòm **Mãånãågéê Séêttîîngs** > **Cùýstöôm Áttrìïbùýtèés**, yõõùú cààn réêféêréêncéê théêséê cùústõõm ààttrîíbùútéês îín yõõùúr Lîíqùúîíd méêssààgîíng. 

Whëén ûúsíìng còöndíìtíìòönáäl lòögíìc, yòöûú'll nëéëéd tòö knòöw thëé cûústòöm áättríìbûútëé's dáätáä typëé tòö ëénsûúrëé yòöûú'rëé ûúsíìng thëé còörrëéct syntáäx. Frõöm thèê [Cýùstõóm Åttrïïbýùtèés][4] päãgëë ìîn thëë däãshbôòäãrd, lôòôòk fôòr thëë däãtäã typëë äãssôòcìîäãtëëd wìîth yôòüûr cüûstôòm äãttrìîbüûtëë, thëën rëëfëërëëncëë thëë fôòllôòwìîng ëëxäãmplëës lìîstëëd fôòr ëëäãch däãtäã typëë.

![Sëëlëëctîíng âæ dâætâæ typëë fòòr âæ cüústòòm âættrîíbüútëë. Thèé èéxàámplèé próóvíïdèéd shóóws àán àáttríïbúùtèé óóf Fàávóóríïtèé_Càãtëégöóry wïîth àã dàãtàã typëé öóf strïîng.][20]{: style="max-width:80%;"}

{% alert tip %}
Strïïngs äánd äárräáys rêêqüûïïrêê sträáïïght äápôòstrôòphêês äárôòüûnd thêêm, whïïlêê bôòôòlêêäáns äánd ïïntêêgêêrs wïïll nêêvêêr häávêê äápôòstrôòphêês.
{% endalert %}

#### Bôóôólêèäân

[Bõõõõléëâàns][9] æãrèé bìïnæãry væãlúúèés, æãnd cæãn bèé sèét tóó èéìïthèér `true` ôõr `false`, sýúch äås `registration_complete: true`. Bôôôôlêëãån vãålüùêës dôôn't hãåvêë ãåpôôstrôôphêës ãårôôüùnd thêëm.

{% raw %}

```liquid
{% if {{custom_attribute.${registration_complete}}} == true %}
```

{% endraw %}

#### Nüümbéèr

[Nýýmbêêrs][10] áåréë nýûméërìîc váålýûéës, whìîch cáån béë ìîntéëgéërs ôòr flôòáåts. Fôôr éèxãàmpléè, ãà üùséèr mãày hãàvéè `shoe_size: 10` öör `levels_completed: 287`. Nýûmbëër vâàlýûëës dõön't hâàvëë âàpõöstrõöphëës âàrõöýûnd thëëm.

{% raw %}

```liquid
{% if {{custom_attribute.${shoe_size}}} == 10 %}
```

{% endraw %}

Yóõýù càân àâlsóõ ýùsêé óõthêér [báæsììc ôòpèêráætôòrs](https://shopify.dev/docs/themes/liquid/reference/basics/operators) süùch äàs lëêss thäàn (<) or greater than (>) fóòr íìntëègëèrs:

{% raw %}

```liquid
{% if {{custom_attribute.${flyer_miles}}} >= 500 %}
```

{% endraw %}

#### Strííng

À [stríìng][11] ìís máádëê üùp ôõf áálpháá-nüùmëêrìíc cháárááctëêrs áánd stôõrëês áá pìíëêcëê ôõf dáátáá áábôõüùt yôõüùr üùsëêr. Fòõr èêxãæmplèê, yòõûü mãæy hãævèê `favorite_color: red` ôör `phone_number: 3025981329`. Strííng vãálûûëés mûûst hãávëé ãápöóströóphëés ãáröóûûnd thëém.

{% raw %}

```liquid
{% if {{custom_attribute.${favorite_color}}} == 'blue' %}
```

{% endraw %}

Fôõr stríïngs, yôõýý cään ýýséè bôõth "==" ôõr "côõntääíïns" íïn yôõýýr Líïqýýíïd.

#### Àrràày

Æn [ààrràày][12] ìís ãæ lìíst öõf ìínföõrmãætìíöõn ãæböõúút yöõúúr úúsèér. Föór êêxäåmplêê, äå ùûsêêr mäåy häåvêê `last_viewed_shows: stranger things, planet earth, westworld`. Ærrãåy vãålúýèës múýst hãåvèë ãåpòôstròôphèës ãåròôúýnd thèëm.

{% raw %}

```liquid
{% if {{custom_attribute.${last_viewed_shows}}} contains 'homeland' %}
```

{% endraw %}

Fõór æãrræãys, yõóùû mùûst ùûséé "cõóntæãìïns" æãnd cæãn't ùûséé "==". 

#### Tïîmëè

Ã tïímëë stâámp òõf whëën âán ëëvëënt tòõòõk plâácëë. [Tíîmëê][13] vàælýüèês mýüst hàævèê àæ [mäãth fììltèèr][5] òòn thêêm tòò bêê üùsêêd îïn còòndîïtîïòònåäl lòògîïc.

{% raw %}

```liquid
{% assign expire = {{custom_attribute.${subscription_end_date}}} | plus: 0 %} 
```

{% endraw %}


[36]:{% image_buster /assets/img/value_null.png %}
[1]: http://docs.shopify.com/themes/liquid-documentation/basics
[2]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/
[4]: https://dashboard-01.braze.com/app_settings/app_settings/custom_attributes/ "Custom Attributes"
[5]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/filters/#math-filters
[7]: https://docs.shopify.com/themes/liquid-documentation/tags
[8]: http://docs.shopify.com/themes/liquid-documentation/tags/control-flow-tags "Control Flow Tags"
[9]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/#booleans
[10]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/#numbers
[11]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/#strings
[12]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/#arrays
[13]: {{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/#time
[20]: {% image_buster /assets/img_archive/custom_attribute_data_type.png %}
