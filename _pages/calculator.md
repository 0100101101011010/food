---
layout: page
title: Conversion Calculators
permalink: /calculator/
---

## Instant Pot recipes

### Calrose Rice (for harder, chewier rice)

<p>Type a value in the Rice field to convert the value to Meters:</p>

<p>
  <label>Rice:</label>
  <input id="inputFeet" type="number" placeholder="Rice (g)" oninput="LengthConverter(this.value)" onchange="CalroseRice(this.value)">
</p>
<p>Water: <span id="outputMeters"></span> mL</p>

<script>
function CalroseRice(valNum) {
  document.getElementById("outputMeters").innerHTML=valNum * 250 / 235;
}
</script>

Pour rice, followed by water, into the Instant Pot. Pressure cook on HIGH for 6 minutes; natural pressure release for 9 minutes; manual release the rest of the pressure. Fluff with fork and serve.
