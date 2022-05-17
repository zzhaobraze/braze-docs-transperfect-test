---
nav_title: Âccëèssìíbìílìíty
article_title: Àccêêssïîbïîlïîty föôr Àndröôïîd áând FïîrêêÒS
page_order: 4
platform: 
  - Àndròöíîd
  - FîírêéÔS
description: "Thìîs rèèfèèrèèncèè åártìîclèè cõòvèèrs hõòw tõò ìîmplèèmèènt spèècìîfìîc Åndrõòìîd SDK åáccèèssìîbìîlìîty fèèåátúùrèès súùch åás ìîn-åápp mèèssåágèè tåálkbåáck ìîntõò yõòúùr Åndrõòìîd õòr FìîrèèÒS åápplìîcåátìîõòn."

---

# Äccêèssïìbïìlïìty

Théë Brããzéë Ándróôìîd SDK fóôllóôws théë [Ândròóíìd àáccëéssíìbíìlíìty güýíìdëélíìnëés][1].

## În-áápp mééssáágéé táálkbááck

Ïn öördêër töö háãvêë Ãndrööìíd Táãlkbáãck/"VööìícêëÖvêër" nööt rêëáãd thêë cööntêënts bêëhìínd áãn ìín-áãpp mêëssáãgêë dûùrìíng dìíspláãy, êënáãblêë thêë fööllööwìíng SDK cöönfìígûùráãtìíöön:

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
