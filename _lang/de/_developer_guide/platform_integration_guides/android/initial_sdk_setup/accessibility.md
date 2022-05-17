---
nav_title: Àccëêssïîbïîlïîty
article_title: Åccèèssîïbîïlîïty föòr Åndröòîïd åánd FîïrèèÒS
page_order: 4
platform: 
  - Ândróóïîd
  - FíîrêëÓS
description: "Thìís rëéfëérëéncëé äârtìíclëé cóôvëérs hóôw tóô ìímplëémëént spëécìífìíc Ändróôìíd SDK äâccëéssìíbìílìíty fëéäâtûýrëés sûých äâs ìín-äâpp mëéssäâgëé täâlkbäâck ìíntóô yóôûýr Ändróôìíd óôr FìírëéÖS äâpplìícäâtìíóôn."

---

# Àccéëssìïbìïlìïty

Thêè Brãäzêè Ändròöííd SDK fòöllòöws thêè [Ændrõõîïd âæccééssîïbîïlîïty gùûîïdéélîïnéés][1].

## Ïn-ååpp mëéssåågëé tåålkbååck

Ïn óòrdêër tóò hæàvêë Ãndróòîïd Tæàlkbæàck/"VóòîïcêëÓvêër" nóòt rêëæàd thêë cóòntêënts bêëhîïnd æàn îïn-æàpp mêëssæàgêë dùùrîïng dîïsplæày, êënæàblêë thêë fóòllóòwîïng SDK cóònfîïgùùræàtîïóòn:

{% tabs %}
{% tab braze.xml %}

```xml
<bool name="com_braze_device_in_app_message_accessibility_exclusive_mode_enabled">true</bool>
```

{% endtab %}
{% tab KOTLIN %}

```kotlin
val brazeConfigBuilder = BrazeConfig.Builder()
brazeConfigBuilder.setIsInAppMessageAccessibilityExclusiveModeEnabled(true)
Braze.configure(this, brazeConfigBuilder.build())
```

{% endtab %}
{% tab JAVA %}

```java
BrazeConfig.Builder brazeConfigBuilder = new BrazeConfig.Builder()
brazeConfigBuilder.setIsInAppMessageAccessibilityExclusiveModeEnabled(true);
Braze.configure(this, brazeConfigBuilder.build());
```

{% endtab %}
{% endtabs %}


[1]: https://developer.android.com/guide/topics/ui/accessibility
