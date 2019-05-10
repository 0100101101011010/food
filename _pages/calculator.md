---
layout: page
title: Conversion Calculators
permalink: /calculator/
---

## Instant Pot recipes

### Calrose Rice (for harder, chewier rice)

  Rice: <input id="inputFeet" type="number" maxlength="5" size="5" placeholder="grams" oninput="LengthConverter(this.value)" onchange="CalroseRice(this.value)">

  Water: <span id="outputMeters"></span> mL

<script>
function CalroseRice(valNum) {
  document.getElementById("outputMeters").innerHTML=Math.round(valNum * 250 / 235);
}
</script>

Pour rice, followed by water, into the Instant Pot. Pressure cook on HIGH for 6 minutes; natural pressure release for 9 minutes; manual release the rest of the pressure. Fluff with fork and serve.

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-calrose-rice/#exp)
