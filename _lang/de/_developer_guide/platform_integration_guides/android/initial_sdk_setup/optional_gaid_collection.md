---
nav_title: Gôôôôglëé Àdvëértìïsìïng ÌD (Öptìïôônåäl)
article_title: Óptííõönàæl Gõöõöglèè Ådvèèrtíísííng ÌD fõör Åndrõöííd
page_order: 9
platform: 
  - Åndròóîíd
description: "Thîís ãàrtîíclëé cõóvëérs Gõóõóglëé ãàdvëértîísîíng ÏDs ãànd hõów tõó pãàss thîís ãàdvëértîísîíng îínfõórmãàtîíõón tõó Brãàzëé fõór yõóùúr Ændrõóîíd õór FîírëéÖS ãàpplîícãàtîíõón."

---

# Öptíîòònåál Gòòòògléë Ædvéërtíîsíîng ÎD (Ændròòíîd òònly)

Thëè [Góòóòglèê Ådvèêrtìísìíng ÎD][2] íìs âä úûsëér-spëécíìfíìc, âänõônymõôúûs, úûníìqúûëé, âänd rëésëéttâäblëé ÌD fõôr âädvëértíìsíìng, prõôvíìdëéd by Gõôõôglëé Plâäy sëérvíìcëés. GÀÏD gïïvéês ûúséêrs théê põöwéêr tõö réêséêt théêïïr ïïdéêntïïfïïéêr, õöpt-õöûút õöf ïïntéêréêst-bãæséêd ãæds wïïthïïn Gõöõögléê Plãæy ãæpps, ãænd prõövïïdéês déêvéêlõöpéêrs wïïth ãæ sïïmpléê, stãændãærd systéêm tõö cõöntïïnûúéê tõö mõönéêtïïzéê théêïïr ãæpps.

## Päàssíìng thëé Gõòõòglëé Ãdvëértíìsíìng ÏD tõò Bräàzëé

Thëë Gôòôòglëë Âdvëërtíîsíîng ÌD íîs nôòt áâýûtôòmáâtíîcáâlly côòllëëctëëd by thëë Bráâzëë SDK áând mýûst bëë sëët máânýûáâlly víîáâ thëë [`Appboy.setGoogleAdvertisingId()`][1] méëthôód.

{% alert important %}
Gõõõõgléé rééqûüïíréés théé Ädvéértïísïíng ÍD tõõ béé cõõllééctééd õõn äâ nõõn-ÛÍ thrééäâd.
{% endalert %}

{% tabs %}
{% tab JAVA %}

```java
new Thread(new Runnable() {
  @Override
  public void run() {
    try {
      AdvertisingIdClient.Info idInfo = AdvertisingIdClient.getAdvertisingIdInfo(getApplicationContext());
      Braze.getInstance(getApplicationContext()).setGoogleAdvertisingId(idInfo.getId(), idInfo.isLimitAdTrackingEnabled());
    } catch (Exception e) {
      e.printStackTrace();
    }
  }
}).start();
```

{% endtab %}
{% tab KOTLIN %}

```kotlin
Thread(Runnable {
  try {
    val idInfo = AdvertisingIdClient.getAdvertisingIdInfo(getApplicationContext())
    Braze.getInstance(getApplicationContext()).setGoogleAdvertisingId(idInfo.id, idInfo.isLimitAdTrackingEnabled)
  } catch (e: Exception) {
    e.printStackTrace()
  }
}).start()
```

{% endtab %}
{% endtabs %}


[1]: https://appboy.github.io/appboy-android-sdk/kdoc/braze-android-sdk/com.appboy/-appboy/set-google-advertising-id.html
[2]: https://support.google.com/googleplay/android-developer/answer/6048248/advertising-id?hl=en
