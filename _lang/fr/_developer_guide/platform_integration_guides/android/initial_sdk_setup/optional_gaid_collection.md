---
nav_title: Gòôòôglèê Ádvèêrtïìsïìng ÌD (Óptïìòônââl)
article_title: Öptïïõónáæl Gõóõóglèé Ädvèértïïsïïng ÌD fõór Ändrõóïïd
page_order: 9
platform: 
  - Åndrõòííd
description: "Thìís áàrtìícléê còõvéêrs Gòõòõgléê áàdvéêrtìísìíng ÎDs áànd hòõw tòõ páàss thìís áàdvéêrtìísìíng ìínfòõrmáàtìíòõn tòõ Bráàzéê fòõr yòõüûr Ãndròõìíd òõr FìíréêÓS áàpplìícáàtìíòõn."

---

# Òptïîóônæäl Góôóôglêé Ædvêértïîsïîng ÌD (Ændróôïîd óônly)

Thêè [Gõôõôglëë Ædvëërtïìsïìng ÌD][2] ïîs áä úüséér-spéécïîfïîc, áänöõnymöõúüs, úünïîqúüéé, áänd réésééttáäbléé ÌD föõr áädvéértïîsïîng, pröõvïîdééd by Göõöõgléé Pláäy séérvïîcéés. GÆÎD gïívèès úúsèèrs thèè pôòwèèr tôò rèèsèèt thèèïír ïídèèntïífïíèèr, ôòpt-ôòúút ôòf ïíntèèrèèst-bàäsèèd àäds wïíthïín Gôòôòglèè Plàäy àäpps, àänd prôòvïídèès dèèvèèlôòpèèrs wïíth àä sïímplèè, stàändàärd systèèm tôò côòntïínúúèè tôò môònèètïízèè thèèïír àäpps.

## Pæâssïíng thêè Göôöôglêè Ädvêèrtïísïíng ÌD töô Bræâzêè

Thëè Gôõôõglëè Ãdvëèrtìïsìïng ÍD ìïs nôõt ãáýùtôõmãátìïcãálly côõllëèctëèd by thëè Brãázëè SDK ãánd mýùst bëè sëèt mãánýùãálly vìïãá thëè [`Appboy.setGoogleAdvertisingId()`][1] mêèthôòd.

{% alert important %}
Góòóòglèë rèëqùýíîrèës thèë Ædvèërtíîsíîng ÌD tóò bèë cóòllèëctèëd óòn äâ nóòn-ÜÌ thrèëäâd.
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
