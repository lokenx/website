---
layout: default
title: Contact
permalink: /contact/
---

<div id="contact">
  <h1 class="pageTitle">Contact Me</h1>
  <div class="contactContent">
    <p class="intro">Need to get a hold of me for something?</p>
    <p>Use the form to the right with any questions, comments, or requests you may have for me.</p>
    <p>Your email will not be used for anything but responding to you, I hate spam just as much as you!</p>
  </div>
  <form action="http://formspree.io/mikhail@delport.ca" method="post">
    <label for="name">Name</label>    
    <input type="text" id="name" name="name" class="full-width"><br>
    <label for="email">Email Address</label>
    <input type="email" id="email" name="_replyto" class="full-width"><br>
    <label for="message">Message</label>
    <textarea name="message" id="message" cols="30" rows="10" class="full-width"></textarea><br>
    <input type="hidden" name="_next" value="/thankyou" />
    <input type="submit" value="Send" class="button">
  </form>
</div>