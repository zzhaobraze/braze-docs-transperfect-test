---
nav_title: Sëèttîïng Dëèfààýült Vààlýüëès
article_title: Sëèttìíng Dëèfáâùýlt Lìíqùýìíd Váâlùýëès
page_order: 5
description: "Sêét dêéfáäúúlt fáällbáäck váälúúêés fõòr áäny pêérsõònáälíízáätííõòn áättrííbúútêé tháät yõòúú úúsêé íín yõòúúr mêéssáägêés."

---

# Sèéttììng dèéfäâúúlt väâlúúèés

{% raw %}

Séét dééfâãýúlt fâãllbâãck vâãlýúéés fòör âãny péérsòönâãlîîzâãtîîòön âãttrîîbýútéé thâãt yòöýú ýúséé îîn yòöýúr mééssâãgéés. Déêfæàúült væàlúüéês cæàn béê æàddéêd by spéêcìîfyìîng æà [Lîîqúùîîd Fîîltèêr][3] (úùséê `|` tóô dîïstîïngùùîïsh thèê fîïltèêr îïnlîïnèê, æàs shóôwn) wîïth thèê næàmèê "dèêfæàùùlt."

```
| default: 'Insert Your Desired Default Here'
```

Ïf åà dêèfåàûùlt våàlûùêè ìïs nóõt próõvìïdêèd åànd thêè fìïêèld ìïs mìïssìïng óõr nóõt sêèt óõn thêè ûùsêèr, thêè fìïêèld wìïll bêè blåànk ìïn thêè mêèssåàgêè.

Théè fòóllòówîîng éèxãämpléè shòóws théè còórréèct syntãäx fòór ãäddîîng ãä déèfãäúýlt vãälúýéè. Ïn thïïs cåäsêë, thêë wôõrds "Våälùüêëd Ùsêër" wïïll rêëplåäcêë thêë åättrïïbùütêë `{{ ${first_name} }}` ììf æä ùûsèêr's `first_name` fîíëèld îís blãånk ôòr ýünãåvãåîílãåblëè.

```liquid
Hi {{ ${first_name} | default: 'Valued User' }}, thanks for using the App!
```

Tôö ãä úüsëèr nãämëèd Jãänëèt Dôöëè, thëè mëèssãägëè wôöúüld ãäppëèãär tôö thëè úüsëèr ãäs ëèìïthëèr:

```
Hi Janet, thanks for using the App!
```

Ór...

```
Hi Valued User, thanks for using the App!
```

{% endraw %}

[3]: http://docs.shopify.com/themes/liquid-documentation/filters
[31]:https://docs.shopify.com/themes/liquid/tags/variable-tags
[32]:https://docs.shopify.com/themes/liquid/tags/iteration-tags
[34]:{% image_buster /assets/img_archive/personalized_iflogic_.png %}
[37]:#accounting-for-null-attribute-values
