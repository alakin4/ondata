---
permalink: /kontakt/
title: "Kontakt"
last_modified_at: 2017-10-10 23:09:08 +02:00 
excerpt: "Hier gibt es die Kontaktierungsmöglichkeiten und andere Verbindungen."
ads: false
share: false
author: true
---
<br />
Kurze Nachrichten gern [via Twitter](https://twitter.com/HolgerKral){:target="_blank"} senden. Oder auch [per Email](mailto:developer4223@ondata.work){:target="_blank"}. Manchmal bin ich auch auf anderen Kanälen zu erreichen. Oder über das Formular unten.

Ich fotografiere und die Bilder gibt es dann meist kurze Zeit später [hier](https://kral-photography.com){:target="_blank"} und die mobilen Bilder machmal [hier](https://hym-on-tour.holgerkral.de){:target="_blank"} zu sehen.

Damit ich hier auch `=` etwas lerne, habe ich `ONDATA` mit [Jekyll](https://jekyllrb.com/docs/home){:target="_blank"} um- und dabei das Theme [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/){:target="_blank"} von [Michael Rose](https://mademistakes.com/){:target="_blank"} eingesetzt.

<h2>Nachricht senden</h2>

<form name="contact" id="contact-form" onsubmit="return validateForm()" class="page__comments-form" netlify-honeypot="bot-field" action="/danke" netlify>
  <p class="hidden">
    <label>Don’t fill this out: <input name="bot-field"></label>
  </p>
  <fieldset>
    <label for="name"><span class="label-required">{{ site.data.ui-text[site.locale].comment_form_name_label | default: "Name" }}</span></label>
    <input type="text" name="name" tabindex="1" novalidate />
  </fieldset>
  <fieldset>
    <label for="email"><span class="label-required">{{ site.data.ui-text[site.locale].comment_form_email_label | default: "Email" }}</span></label>
    <input type="email" name="email" tabindex="3" />
  </fieldset>
  <fieldset>
    <label for="subject">Betreff</label>
    <input type="text" name="subject" tabindex="3" novalidate />
  </fieldset>
  <fieldset>
    <label for="message"><span class="label-required">Nachricht</span></label>
    <textarea name="message" rows="3" tabindex="4" novalidate></textarea>
  </fieldset>
  <fieldset>
    <button type="submit" tabindex="5" class="btn">Senden</button>
  </fieldset>
</form>

<script type="text/javascript">
function validateForm() {
    var x1 = document.forms["contact-form"]["name"].value;
    var x2 = document.forms["contact-form"]["email"].value;
    var x3 = document.forms["contact-form"]["message"].value;
    if (x1 == "" || x2 == "" || x3 == "") {
        alert("Bitte Name, Email und Nachricht ausfüllen. Danke!");
        return false;
    }
}
</script>