You may want to integrate Drift with your Legal Server if you want to
provide real-time live chat assistance to your Legal Server users.
Drift adds a widget to the lower-right-hand corner of the screen.
When the user clicks it, a chat window opens up.

Integrating Legal Server with the Drift on-line chat system is
extremely easy.  This repository consists of nothing but this README
-- this is all you need to set up the integration.

To set up the integration, first register for Drift at
https://drift.com.  No credit card information is required.  Follow
the standard setup.  When it asks you if you want to integrate with
Drupal, Wordpress, or "do it yourself," choose the "do it yourself"
option.

The web site will provide you with a block of HTML that you can insert
into your site.  Copy this HTML.

Then go into your Legal Server, go to Admin -> "Processes, Forms, and
Profiles," and go to Profiles.  Edit the Main Profile for cases.

Insert an "instruction" to the bottom of the screen.  Select the
"Format as HTML" checkbox.  Then you will paste two things into the
body of the Instruction.

First, paste the HTML you copied from the Drift web site.

Second, copy and paste the following into the same Instruction:

    <div id="driftInstruction"></div>
    <script type="text/javascript">
      document.getElementById("driftInstruction").parentNode.style.display="none";
    </script>

The second part is optional; if you don't include it, the Drift
integration will still work, but there will be a yellow bar at the
bottom of the screen.  This code simply makes the yellow bar disappear.

Drift pricing is free if you just have one administrator, and $25/seat
for two administrators, and $10/seat for 5 administrators.  Drift also
has a Slack integration option.

You will need to put this same "instruction" into every page where the
user might request help.  If you put it on the "Home" page and the
"Main Profile," that will probably cover 99% of users' needs.
