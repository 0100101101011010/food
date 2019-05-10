---
layout: page
title: Conversion Calculators
permalink: /calculator/
---

## Instant Pot recipes

### Calrose Rice (for harder, chewier rice)

<script>
function CalroseCalcHard(valNum) {
  document.getElementById("outputWater").innerHTML=Math.round(valNum * 250 / 235);
}
</script>



Rice: <input id="inputCalrose" type="number" style="width: 100px;" placeholder="grams" oninput="CalroseCalcHard(this.value)" onchange="CalroseCalcHard(this.value)">

Water: <span id="outputWater"></span> mL

Pour rice, followed by water, into the Instant Pot. Pressure cook on HIGH for 6 minutes; natural pressure release for 9 minutes; manual release the rest of the pressure. Fluff with fork and serve.

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-calrose-rice/#exp)
