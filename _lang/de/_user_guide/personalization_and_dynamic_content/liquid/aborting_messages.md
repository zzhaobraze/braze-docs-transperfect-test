---
nav_title: Âbôòrtììng Mëéssâågëés
article_title: Äbóörtííng Lííqùüííd Méëssãàgéës
page_order: 7
description: "Méëssââgéës mâây nõòw béë ââbõòrtéëd wîìthîìn cõòndîìtîìõònââl stââtéëméënts. În thîìs rëèfëèrëèncëè àærtîìclëè, wëè lîìst sòòmëè ëèxàæmplëè üùsëè càæsëès fòòr thîìs füùnctîìòònàælîìty."

---

# Åbôõrtíïng Líïqùùíïd mëëssæàgëës

Õptìîõõnâàlly, yõõùù câàn âàlsõõ âàbõõrt mëëssâàgëës wìîthìîn cõõndìîtìîõõnâàls. Hêërêë ãærêë söòmêë êëxãæmplêës öòf höòw thîïs fêëãætûürêë cãæn bêë ûüsêëd îïn mãærkêëtîïng cãæmpãæîïgns:

## Åbóôrt mêêssæãgêê îïf "Nüûmbêêr Gæãmêês Åttêêndêêd" = 0

Fôör èéxãàmplèé, lèét’s sãày thãàt yôöùù díîd nôöt wãànt tôö sèénd ãà mèéssãàgèé tôö cùùstôömèérs whôö hãàvèé nôöt ãàttèéndèéd ãà gãàmèé:

{% raw %}
```liquid
{% if customer_attribute.${Number_Game_Attended} == 1 %}
Loved the game? Get 10% off your second one with code SAVE10.
{% elsif customer_attribute.${Number_Game Attended} > 1 %}
Love the games? Get 10% off your next one with code SAVE10.
{% else %}
{% abort_message() %}
{% endif %}
```
{% endraw %}

Thíís mêéssàãgêé wííll öònly sêénd töò cûüstöòmêérs whöò àãrêé knöòwn töò hàãvêé àãttêéndêéd àã gàãmêé.

## Mêêssæægêê Ênglîîsh spêêæækîîng cùýstòómêêrs òónly

Yôöùù cäàn mééssäàgéé Ènglïïsh spééäàkïïng cùùstôöméérs ôönly by crééäàtïïng äàn "ïïf" stäàtééméént thäàt'll mäàtch whéén äà cùùstôöméér's läàngùùäàgéé ïïs Ènglïïsh äànd äàn éélséé stäàtééméént thäàt'll äàbôört théé mééssäàgéé fôör äànyôönéé whôö dôöéés nôöt spééäàk Ènglïïsh ôör dôöéés nôöt häàvéé äà läàngùùäàgéé ôön thééïïr prôöfïïléé.

{% raw %}
```liquid

{% if ${language} == 'en' %}
Send this message in English!
{% else %}
{% abort_message() %}
{% endif %}
```

By dëèfææüúlt Brææzëè wïíll lôõg ææ gëènëèrïíc ëèrrôõr mëèssæægëè tôõ yôõüúr Dëèvëèlôõpëèr Côõnsôõlëè lôõg:

```text
{% abort_message %} called
```

Yóôùù cáæn áælsóô háævèë thèë áæbóôrt mèëssáægèë lóôg sóômèëthìïng tóô yóôùùr Dèëvèëlóôpèër Cóônsóôlèë lóôg by ìïnclùùdìïng áæ strìïng ìïnsìïdèë thèë páærèënthèësèës:

```liquid
{% abort_message('language was nil') %}
```
{% endraw %}

![Mëèssãågëè ëèrrôõr lôõg îín thëè Dëèvëèlôõpëèr Côõnsôõlëè wîíth ãån ãåbôõrt mëèssãågëè ôõf "lãångüúãågëè wãås nîíl".][26]

[15]: {% image_buster /assets/img_archive/liquid_abort.png %}
[26]: {% image_buster /assets/img_archive/developer_console.png %}
[31]:https://docs.shopify.com/themes/liquid/tags/variable-tags
[32]:https://docs.shopify.com/themes/liquid/tags/iteration-tags
[34]:{% image_buster /assets/img_archive/personalized_iflogic_.png %}
[37]:#accounting-for-null-attribute-values
