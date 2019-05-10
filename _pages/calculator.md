---
layout: page
title: Conversion Calculators
permalink: /calculator/
---

## Instant Pot recipes

### Calrose Rice (for harder, chewier rice)


|  | Harder, chewier rice | Al dente | Softer, mushier rice |
|--|----------------------|----------|----------------------|
| Rice: | <input id="inputCalrose" type="number" style="width: 100px;" placeholder="grams" oninput="CalroseCalcHard(this.value)" onchange="CalroseCalcHard(this.value)"> | <input id="inputCalrose" type="number" style="width: 100px;" placeholder="grams" oninput="CalroseCalcMed(this.value)" onchange="CalroseCalcMed(this.value)"> | <input id="inputCalrose" type="number" style="width: 100px;" placeholder="grams" oninput="CalroseCalcSoft(this.value)" onchange="CalroseCalcSoft(this.value)"> |
| Water: | <span id="outputWaterHard"></span> mL | <span id="outputWaterMed"></span> mL | <span id="outputWaterSoft"></span> mL |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 6 minutes | 6 minutes | 6 minutes |
| Natural Pressure Release: | 9 minutes | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover}

<script>
function CalroseCalcHard(valNum) {
  document.getElementById("outputWaterHard").innerHTML=Math.round(valNum * 250 / 235);
}
</script>

<script>
function CalroseCalcMed(valNum) {
  document.getElementById("outputWaterMed").innerHTML=Math.round(valNum * 250 / 235);
}
</script>

<script>
function CalroseCalcMed(valNum) {
  document.getElementById("outputWaterMed").innerHTML=Math.round(valNum * 250 / 235);
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-calrose-rice/#exp)
