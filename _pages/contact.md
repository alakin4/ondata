---
permalink: /kontakt/
title: "Kontakt"
last_modified_at: 2017-05-06 00:47:00 +02:00 
excerpt: "Hier gibt es die Kontaktierungsmöglichkeiten und andere Verbindungen."
ads: false
share: false
author: true
---
<br />
Kurze Nachrichten gern [via Twitter](https://twitter.com/HolgerKral){:target="_blank"} senden. Oder auch [per Email](mailto:developer4223@gmail.com){:target="_blank"}. Manchmal bin ich auch auf anderen Kanälen zu erreichen. Oder über das Formular unten.

Ich fotografiere und die Bilder gibt es dann meist kurze Zeit später [hier](https://kral-photography.com){:target="_blank"} und die mobilen Bilder machmal [hier](https://hym-on-tour.holgerkral.de){:target="_blank"} zu sehen.

Damit ich hier auch `=` etwas lerne, habe ich `ONDATA` mit [Jekyll](https://jekyllrb.com/docs/home){:target="_blank"} um- und dabei das Theme [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/){:target="_blank"} von [Michael Rose](https://mademistakes.com/){:target="_blank"} eingesetzt.


<form name="contact" netlify-honeypot="bot-field" action="/pages/thankyou.html" netlify>
  <p class="hidden">
    <label>Don’t fill this out: <input name="bot-field"></label>
  </p>
  <fieldset>
    <label for="name"><span class="label-required">{{ site.data.ui-text[site.locale].comment_form_name_label | default: "Name" }}</span></label>
    <input type="text" name="name" tabindex="1" />
  </fieldset>
  <fieldset>
    <label for="email"><span class="label-required">{{ site.data.ui-text[site.locale].comment_form_email_label | default: "Email" }}</span></label>
    <input type="email" name="email" tabindex="3" />
  </fieldset>
  <fieldset>
    <label for="subject">Betreff</label>
    <input type="text" name="subject" tabindex="3"/>
  </fieldset>
  <fieldset>
    <label for="message">Nachricht</label>
    <textarea name="message" rows="3" tabindex="4" class="label-required"></textarea>
  </fieldset>
  <fieldset>
    <button type="submit" tabindex="5" class="btn">Senden</button>
  </fieldset>
</form>