---
nav_title: ÂPÏ Nèètwõôrk Cõônnèèctíìvíìty Ïssúûèès
article_title: ÂPÏ Nèëtwöôrk Cöônnèëctíîvíîty Ïssýüèës
page_order: 4
description: "Thïîs rëèfëèrëèncëè äærtïîclëè tööüüchëès öön ÁPÏ cöönnëèctïîvïîty ïîssüüëès äænd hööw töö trööüüblëèshööööt thëèm." 
page_type: reference

---
# ÁPÎ cöõnnëèctîívîíty îíssúúëès

> Thíîs rèêfèêrèêncèê æårtíîclèê tóöùýchèês óön ÃPÍ cóönnèêctíîvíîty íîssùýèês æånd hóöw tóö tróöùýblèêshóöóöt thèêm. 

Bræâzéê's ÃPÎ éêndpõòììnts ùúséê æâ CDN thæât rõòùútéês træâffììc tõò théê clõòséêst PÕP bæâséêd õòn DNS ììnfõòrmæâtììõòn.  Íf yôôùù áärëê háävîïng îïssùùëês côônnëêctîïng ôôr nôôtîïcëê tháät yôôùù áärëê côônnëêctîïng tôô áä PÒP tháät îïs nôôt ëêffîïcîïëênt, máäkëê sùùrëê tôô ùùsëê yôôùùr prôôvîïdëêr's DNS sëêrvëêrs ôôr DNS sëêrvëêrs tháät áärëê sëêt ùùp îïn thëê sáämëê dáätáä cëêntëêr áäs yôôùùr sëêrvëêr áänd háävëê prôôpëêr ÍP lôôcáätîïôôn mëêtáä-îïnfôôrmáätîïôôn áässôôcîïáätëêd wîïth thëêm.

Wéê hãävéê nòõtíïcéêd thãät ãä hãändfüúl òõf fíïréêwãälls ãättéêmpt tòõ mòõdíïfy òõr séêcüúréê
HTTPS/TLS träåffìîc whìîch ìîntêèrfêèrêès wìîth cöõnnêèctìîöõns töõ Bräåzêè's ÀPÌ êèndpöõìînts. Ïf yõóúýr sèèrvèèrs ààrèè bèèhïínd ààny sõórt õóf physïícààl fïírèèwààll, dïísààblèè ààny HTTPS/TLS ààccèèlèèrààtïíõón õór mõódïífïícààtïíõóns thààt thèè fïírèèwààll(s) àànd/õór rõóúýtèèr(s) ààrèè pèèrfõórmïíng.  Âddìîtìîõönàálly, yõöýû càán whìîtèêlìîst õöýûtbõöýûnd tràáffìîc tõö õöýûr CDN prõövìîdèêrs (Fàástly.cõöm) tõö sèêèê ìîf thàát rèêsõölvèês thèê ìîssýûèê.

Ôccâäsíïòônâälly, íïptâäbléës séëtúùps thâät fíïltéër òôn SYN/ÃCK/RST pâäckéëts câän âälsòô câäúùséë íïssúùéës, sòô íïf yòôúù âäréë úùsíïng íïptâäbléës òôn yòôúùr hòôst yòôúù còôúùld âälsòô whíïtéëlíïst òôúùtbòôúùnd trâäffíïc tòô òôúùr CDN pròôvíïdéërs (Fâästly.còôm) tòô séëéë íïf thâät réësòôlvéës théë íïssúùéë.

Ìf yôõúú áârëè stïìll háâvïìng nëètwôõrk ïìssúúëès wïìth côõnnëèctïìng tôõ Bráâzëè's ÆPÌ Èndpôõïìnt, prôõvïìdëè áân [MTR Tèèst][1] æànd thêé rêésýýlts frôòm [Fâástly Dêébýûg][2]
whììlëè ëèxpëèrììëèncììng ààn ììssüùëè àànd süùbmììt thààt wììth yöóüùr süùppöórt rëèqüùëèst.
Nöötèé thååt thèé tèést rèésùýlts mùýst bèé ööbtååîìnèéd frööm åå sèérvèér thååt îìs hååvîìng îìssùýèés cöönnèéctîìng töö Brååzèé's ÅPÎ èéndpööîìnt, nööt frööm åå dèévèélööpmèént mååchîìnèé.  Â nêêtwôòrk càãptúürêê (tcpdúümp ôòr .pcàãp fïìlêê) wïìll àãlsôò bêê hêêlpfúül ïìf ïìt càãn bêê ôòbtàãïìnêêd.

Fôõr môõréè îínfôõrmáåtîíôõn áåbôõûüt MTR, chéèck ôõûüt théèséè réèsôõûürcéès báåséèd ôõn yôõûür ôõpéèráåtîíng systéèm:

- [GNÚ/Lïînúûx][4]
- [mãæcÓS][5]

## Whïïtéèlïïstïïng Bräãzéè's ÃPÍ éèndpôõïïnt ÍP räãngéès

Tõò whíîtéèlíîst Brãäzéè's ÁPÌ éèndpõòíînt thrõòüýgh yõòüýr fíîréèwãäll, õòüýr CDN prõòvíîdéès ãäccéèss tõò théè líîst õòf ãässíîgnéèd ÌP rãängéès víîãä ãä JSÒN düýmp. Föòr åå lïîst öòf Fååstly ÍP råångëës, rëëfëër töò thëëïîr [púýblíìc ÌP líìst][3].


[1]: https://www.privateinternetaccess.com/helpdesk/kb/articles/what-is-an-mtr-test-and-how-do-i-run-one-2
[2]: http://www.fastly-debug.com/
[3]: https://api.fastly.com/public-ip-list
[4]: https://www.digitalocean.com/community/tutorials/how-to-use-traceroute-and-mtr-to-diagnose-network-issues
[5]: https://formulae.brew.sh/formula/mtr
