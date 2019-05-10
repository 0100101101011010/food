---
layout: page
title: Conversion Calculators
permalink: /calculator/
---
<style>
input[type=text], input[type=number], select {
  width: 100%;
  padding: 2px 2px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
</style>

## Instant Pot recipes

### Calrose Rice

|  | Harder, chewier rice | Al dente | Softer, mushier rice |
|--|----------------------|----------|----------------------|
| Rice: | <input id="inputCalrose" type="number" style="width: 100px;" placeholder="grams" oninput="CalroseCalcHard(this.value)" onchange="CalroseCalcHard(this.value)"> | <input id="inputCalrose" type="number" style="width: 100px;" placeholder="grams" oninput="CalroseCalcMed(this.value)" onchange="CalroseCalcMed(this.value)"> | <input id="inputCalrose" type="number" style="width: 100px;" placeholder="grams" oninput="CalroseCalcSoft(this.value)" onchange="CalroseCalcSoft(this.value)"> |
| Water: | <span id="outputWaterHard"></span> | <span id="outputWaterMed"></span> | <span id="outputWaterSoft"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 6 minutes | 6 minutes | 6 minutes |
| Natural Pressure Release: | 9 minutes | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover}

<script>
function CalroseCalcHard(valNum) {
  document.getElementById("outputWaterHard").innerHTML = Math.round(valNum * 250 / 235) + " mL";
}
</script>

<script>
function CalroseCalcMed(valNum) {
  document.getElementById("outputWaterMed").innerHTML = Math.round(valNum * 295 / 235) + " mL";
}
</script>

<script>
function CalroseCalcSoft(valNum) {
  document.getElementById("outputWaterSoft").innerHTML = Math.round(valNum * 313 / 235) + " mL";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-calrose-rice/#exp)
