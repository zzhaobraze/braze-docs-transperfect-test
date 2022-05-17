---
nav_title: Côöndîïtîïôönäæl Mëëssäægîïng Lôögîïc
article_title: Côõndíïtíïôõnáål Líïqúûíïd Mëêssáågíïng Lôõgíïc
page_order: 6
description: "Tåâgs åâllöów yöóûû töó íìnclûûdèè pröógråâmmíìng löógíìc íìn yöóûûr mèèssåâgíìng cåâmpåâíìgns. Thîïs réëféëréëncéë äärtîïcléë cöövéërs hööw täägs cään äänd shööüùld béë üùséëd îïn yööüùr cäämpääîïgns."

---

# Còõndìïtìïòõnäàl mèëssäàgìïng lòõgìïc (täàgs)

[Tåãgs][7] áàllòöw yòöýû tòö íînclýûdêë pròögráàmmíîng lòögíîc íîn yòöýûr mêëssáàgíîng cáàmpáàíîgns.

{% raw %}
Å tãàg múýst bèê wrãàppèêd íïn `{% %}`.
{% endraw %}

Tåãgs cåãn bèè üüsèèd fõör èèxèècüütíïng cõöndíïtíïõönåãl ståãtèèmèènts åãs wèèll åãs fõör åãdvåãncèèd üüsèè cåãsèès, líïkèè åãssíïgníïng våãríïåãblèès õör íïtèèråãtíïng thrõöüügh åã blõöck õöf cõödèè.

{% alert tip %}
Töò måàkèê yöòúür lïìfèê åà bïìt èêåàsïìèêr, Bråàzèê håàs ïìnclúüdèêd cöòlöòr-föòrmåàttïìng thåàt wïìll åàctïìvåàtèê ïìn grèêèên åànd púürplèê ïìf yöòúü'vèê cöòrrèêctly föòrmåàttèêd yöòúür Lïìqúüïìd syntåàx. Grëèëèn fõörmãáttîìng cãán hëèlp îìdëèntîìy tãágs, whîìlëè pûürplëè fõörmãáttîìng hîìghlîìghts ãárëèãás thãát cõöntãáîìn pëèrsõönãálîìzãátîìõön.
<br><br>
Îf yóöùú'réê häävìíng ää häärd tìíméê ùúsìíng cóöndìítìíóönääl méêssäägìíng, try wrìítìíng óöùút théê cóöndìítìíóönääl syntääx béêfóöréê yóöùú ìínséêrt yóöùúr cùústóöm äättrìíbùútéês äänd óöthéêr Lìíqùúìíd éêléêméênts.
<br><br>
Föòr ëêxàâmplëê, àâdd thëê föòllöòwïïng ïïntöò thëê mëêssàâgëê fïïëêld fïïrst:  
{% raw %}
```liquid
{% if X >0 %}
{% else %}
{% endif %}
```

Bëê süýrëê îít hîíghlîíghts îín grëêëên, thëên rëêplåàcëê thëê `X` wïîth yòóúûr chòóséên Lïîqúûïîd òór Còónnéêctéêd Còóntéênt úûsïîng théê blúûéê `+` íìn thèè mèèssåågèè fíìèèld cóórnèèr, åånd thèè `0` wïïth yöôûûr déèsïïréèd vààlûûéè.
<br><br>
Thëén, äädd yóôüür mëéssäägëé väärïìäätïìóôns ääs yóôüü nëéëéd thëém bëétwëéëén thëé `else` cõöndìîtìîõönäåls:
```liquid
{% if {{custom_attribute.${total_spend}}} >0 %}
Thanks for purchasing! Here's another 10% off!
{% else %}
Buy now! Would 5% off convince you?
{% endif %}
```
{% endraw %}
{% endalert %}

## Còôndîïtîïòônáâl lòôgîïc

Yõöýý cãæn ìínclýýdèë mãæny typèës õöf [îìntêéllîìgêént löögîìc wîìthîìn mêéssâãgêés][1] — õónêë êëxåãmplêë îîs åã cõóndîîtîîõónåãl ståãtêëmêënt. Sèëèë thèë fööllööwîïng èëxáæmplèë whîïch üýsèës [côòndíîtíîôònäâls][8] tóö ïìntêèrnàåtïìóönàålïìzêè àå càåmpàåïìgn:
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

### Stèëp by stèëp èëxàæmplèë

Ìn thïîs êêxäâmplêê, wêê ûüsêê täâgs wïîth "ïîf", "êêlsïîf" äând "êêlsêê" stäâtêêmêênts töó dêêlïîvêêr ïîntêêrnäâtïîöónäâlïîzêêd cöóntêênt.

```liquid
{% if ${language} == 'en' %}
This is a message in English from Braze!
```
Îf thêê cýùstôõmêêr's lâængýùâægêê îìs Ènglîìsh, thêê fîìrst côõndîìtîìôõn îìs mêêt âænd thêê cýùstôõmêêr wîìll rêêcêêîìvêê âæ mêêssâægêê îìn Ènglîìsh.

```liquid
{% elsif ${language} == 'es' %}
Este es un mensaje en español de Braze !
{% elsif ${language} == 'zh' %}
这是一条来自Braze的中文消息。
```

Yöòýü cáän spèècïïfy áäs máäny cöòndïïtïïöònáäl stáätèèmèènts áäs yöòýü'd lïïkèè- sýübsèèqýüèènt cöòndïïtïïöòns wïïll bèè chèèckèèd ïïf thèè prèèvïïöòýüs cöòndïïtïïöòns áärèè nöòt mèèt. Ïn thîís èêxæámplèê, îíf æá cúústôòmèêr's dèêvîícèê îís nôòt sèêt tôò Ênglîísh thîís côòdèê wîíll chèêck tôò sèêèê îíf thèê cúústôòmèêr's dèêvîícèê îís sèêt tôò Spæánîísh ôòr Chîínèêsèê. Ìf thêè cüüstöómêèr's dêèvíïcêè mêèêèts öónêè öóf thêèsêè cöóndíïtíïöóns, thêè cüüstöómêèr wíïll rêècêèíïvêè ââ mêèssââgêè íïn thêè rêèlêèvâânt lâângüüââgêè.

```liquid
{% else %}
This is a message from Braze! This is going to go to anyone who did not match the other specified languages!
```

Yòõüý hãävëê thëê òõptïìòõn tòõ ïìnclüýdëê ãän `{% else %}` statement in your conditional logic. If none of the conditions that you set are met, the `{% else %}`  stäätééméént spéécïìfïìéés théé mééssäägéé thäät shôõùùld séénd. Ìn thììs cæàsëè, wëè dëèfæàüült tòò Ênglììsh ììf æà cüüstòòmëèr's læàngüüæàgëè ììs nòòt Ênglììsh, Spæànììsh òòr Chììnëèsëè.

```liquid
{% endif %}
```

Thêè `{% endif %}`  täág sïîgnäáls thäát yôóûú'vëë fïînïîshëëd yôóûúr côóndïîtïîôónäál lôógïîc. Yóöýù mýùst ïìnclýùdêë thêë
`{% endif %}`  tag in any message with conditional logic. If you do not include an `{% endif %}`  tââg ìîn yôöýýr côöndìîtìîôönââl lôögìîc, yôöýý'll géèt âân éèrrôör ââs Brââzéè wìîll béè ýýnââbléè tôö pâârséè yôöýýr méèssââgéè.

{% endraw %}

## Ãccóôüúntíìng fóôr nüúll äàttríìbüútëé väàlüúëés

Cóôndìítìíóônâäl lóôgìíc ìís âä úüsèëfúül wâäy tóô âäccóôúünt fóôr núüll âättrìíbúütèë vâälúüèës. Â nýùll vâålýùèê òõccýùrs whèên thèê vâålýùèê òõf âå cýùstòõm âåttrïîbýùtèê hâås nòõt bèêèên sèêt. Föôr éèxææmpléè, ææ ûúséèr whöô hææs nöôt yéèt séèt théèîïr fîïrst nææméè wîïll nöôt hæævéè ææ fîïrst nææméè îïn Brææzéè's dæætææbææséè.

În sõöméê cìírcüýmstæåncéês, yõöüý mæåy wìísh tõö séênd æå cõömpléêtéêly dìífféêréênt méêssæågéê tõö üýséêrs whõö hæåvéê æå fìírst næåméê séêt æånd üýséêrs whõö dõö nõöt hæåvéê æå fìírst næåméê séêt.

Thëê föòllöòwîïng tàâg àâllöòws yöòûü töò spëêcîïfy àâ mëêssàâgëê föòr ûüsëêrs wîïth àâ nûüll "fîïrst nàâmëê" àâttrîïbûütëê:

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

## Rêêfêêrêêncïíng cûûstóòm äãttrïíbûûtêês

Ãftêër yõöýý hââvêë crêëââtêëd [cúûstòôm åãttrîîbúûtèës][2] fròöm **Mäànäàgëë Sëëttîìngs** > **Cûústóöm Àttrîîbûútéés**, yôõüü cãæn rëêfëêrëêncëê thëêsëê cüüstôõm ãættríîbüütëês íîn yôõüür Líîqüüíîd mëêssãægíîng. 

Whéén úýsîìng cöóndîìtîìöónâäl löógîìc, yöóúý'll nééééd töó knöów théé cúýstöóm âättrîìbúýtéé's dâätâä typéé töó éénsúýréé yöóúý'réé úýsîìng théé cöórrééct syntâäx. Fròôm thèê [Cýústóöm Ättrííbýútéês][4] pâågéê ììn théê dâåshbööâård, löööök föör théê dâåtâå typéê âåssööcììâåtéêd wììth yööùür cùüstööm âåttrììbùütéê, théên réêféêréêncéê théê fööllööwììng éêxâåmpléês lììstéêd föör éêâåch dâåtâå typéê.

![Sèélèéctîìng ââ dââtââ typèé fóòr ââ cùûstóòm ââttrîìbùûtèé. Thëè ëèxååmplëè pròövíîdëèd shòöws åån ååttríîbúütëè òöf Fååvòöríîtëè_Cäãtêêgòõry wìíth äã däãtäã typêê òõf strìíng.][20]{: style="max-width:80%;"}

{% alert tip %}
Strîïngs àând àârràâys rèéqúùîïrèé stràâîïght àâpõôstrõôphèés àârõôúùnd thèém, whîïlèé bõôõôlèéàâns àând îïntèégèérs wîïll nèévèér hàâvèé àâpõôstrõôphèés.
{% endalert %}

#### Bóöóölëêåån

[Bôöôölèêâæns][9] ãærëë bïînãæry vãælýýëës, ãænd cãæn bëë sëët tóö ëëïîthëër `true` òör `false`, sûúch ææs `registration_complete: true`. Bòóòólëêãån vãålüýëês dòón't hãåvëê ãåpòóstròóphëês ãåròóüýnd thëêm.

{% raw %}

```liquid
{% if {{custom_attribute.${registration_complete}}} == true %}
```

{% endraw %}

#### Nüümbèër

[Nýûmbêérs][10] áåréê nýüméêrïîc váålýüéês, whïîch cáån béê ïîntéêgéêrs óôr flóôáåts. Föõr èêxãàmplèê, ãà üýsèêr mãày hãàvèê `shoe_size: 10` òôr `levels_completed: 287`. Núùmbëër vããlúùëës dõõn't hããvëë ããpõõstrõõphëës ããrõõúùnd thëëm.

{% raw %}

```liquid
{% if {{custom_attribute.${shoe_size}}} == 10 %}
```

{% endraw %}

Yòõýù cæãn æãlsòõ ýùséê òõthéêr [bäásììc ôòpèèräátôòrs](https://shopify.dev/docs/themes/liquid/reference/basics/operators) süüch ãâs lèèss thãân (<) or greater than (>) fóör ïìntëêgëêrs:

{% raw %}

```liquid
{% if {{custom_attribute.${flyer_miles}}} >= 500 %}
```

{% endraw %}

#### Strììng

Ä [stríìng][11] îìs màådëë ýûp öôf àålphàå-nýûmëërîìc chàåràåctëërs àånd stöôrëës àå pîìëëcëë öôf dàåtàå àåböôýût yöôýûr ýûsëër. Fóõr èëxàæmplèë, yóõúý màæy hàævèë `favorite_color: red` õór `phone_number: 3025981329`. Strîìng væälüûëés müûst hæävëé æäpöòströòphëés æäröòüûnd thëém.

{% raw %}

```liquid
{% if {{custom_attribute.${favorite_color}}} == 'blue' %}
```

{% endraw %}

Fõör strìîngs, yõöýù câân ýùsêë bõöth "==" õör "cõöntââìîns" ìîn yõöýùr Lìîqýùìîd.

#### Ârrããy

Ãn [æærrææy][12] íìs äá líìst òòf íìnfòòrmäátíìòòn äábòòüüt yòòüür üüsëér. Fõör ëëxáàmplëë, áà ùúsëër máày háàvëë `last_viewed_shows: stranger things, planet earth, westworld`. Ãrrâây vââlüùëés müùst hââvëé ââpöòströòphëés ââröòüùnd thëém.

{% raw %}

```liquid
{% if {{custom_attribute.${last_viewed_shows}}} contains 'homeland' %}
```

{% endraw %}

Fòör áárrááys, yòöûý mûýst ûýsëë "còöntááïìns" áánd cáán't ûýsëë "==". 

#### Tìîméé

Á tíïméê stâämp ôôf whéên âän éêvéênt tôôôôk plâäcéê. [Tíîmêé][13] váälüüëês müüst háävëê áä [màäth fîìltèèr][5] öôn thêém töô bêé ùûsêéd îïn cöôndîïtîïöônåál löôgîïc.

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
