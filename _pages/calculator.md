---
layout: page
title: Conversion Calculators
permalink: /calculator/
---
<style>
input[type=text], input[type=number], select {
  width: 100%;
  padding: 1px;
  margin: 4px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
</style>

## Instant Pot recipes

### Basmati Rice

|  | Harder, chewier rice | Al dente (just right) | Softer, mushier rice |
|--|----------------------|----------|----------------------|
| Rice: | <input id="inputBasmati" type="number" placeholder="grams" oninput="BasmatiHard(this.value)" onchange="BasmatiHard(this.value)"> | <input id="inputBasmati" type="number" placeholder="grams" oninput="BasmatiMed(this.value)" onchange="BasmatiMed(this.value)"> | <input id="inputBasmati" type="number" placeholder="grams" oninput="BasmatiSoft(this.value)" onchange="BasmatiSoft(this.value)"> |
| Water: | <span id="outputBasmatiHard"></span> | <span id="outputBasmatiMed"></span> | <span id="outputBasmatiSoft"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 5 minutes | 6 minutes | 6 minutes |
| Natural Pressure Release: | 10 minutes | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover}

<script>
function BasmatiHard(valNum) {
  document.getElementById("outputBasmatiHard").innerHTML = Math.round(valNum * 250 / 210) + " mL";
}
</script>

<script>
function BasmatiMed(valNum) {
  document.getElementById("outputBasmatiMed").innerHTML = Math.round(valNum * 250 / 210) + " mL";
}
</script>

<script>
function BasmatiSoft(valNum) {
  document.getElementById("outputBasmatiSoft").innerHTML = Math.round(valNum * 312.5 / 210) + " mL";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-calrose-rice/#exp)

### Calrose Rice

|  | Harder, chewier rice | Al dente (just right) | Softer, mushier rice |
|--|----------------------|----------|----------------------|
| Rice: | <input id="inputCalrose" type="number" placeholder="grams" oninput="CalroseCalcHard(this.value)" onchange="CalroseCalcHard(this.value)"> | <input id="inputCalrose" type="number" placeholder="grams" oninput="CalroseCalcMed(this.value)" onchange="CalroseCalcMed(this.value)"> | <input id="inputCalrose" type="number" placeholder="grams" oninput="CalroseCalcSoft(this.value)" onchange="CalroseCalcSoft(this.value)"> |
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
  document.getElementById("outputWaterSoft").innerHTML = Math.round(valNum * 312.5 / 235) + " mL";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-calrose-rice/#exp)
