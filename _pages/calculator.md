---
layout: page
title: Conversion Calculators
permalink: /calculator/
---
<style>
input[type=text], input[type=number], select {
  width: 100%;
  padding: 1px 2px;
  <!-- margin: 2px 0; -->
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
</style>

## Instant Pot recipes

### Basmati Rice

\* Use cold water and *unrinsed* rice. If rinsing your rice, weigh out the inner pot + dry rice first before rinsing and adding water.

| <sup>Amount of rice:</sup> <input id="inputBasmati" type="number" placeholder="grams" oninput="BasmatiCalc(this.value)" onchange="BasmatiCalc(this.value)"> | Harder, chewier rice | Al dente (just right) | Softer, mushier rice |
|--|----------------------|-----------------------|----------------------|
| Water: | <span id="outputBasmatiHard"></span> | <span id="outputBasmatiMed"></span> | <span id="outputBasmatiSoft"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 5 minutes | 6 minutes | 6 minutes |
| Natural Pressure Release: | 10 minutes | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover .table-bordered}

<script>
function BasmatiCalc(valNum) {
  document.getElementById("outputBasmatiHard").innerHTML = Math.round(valNum * 250 / 210) + " mL";
  document.getElementById("outputBasmatiMed").innerHTML = Math.round(valNum * 250 / 210) + " mL";
  document.getElementById("outputBasmatiSoft").innerHTML = Math.round(valNum * 312.5 / 210) + " mL";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-basmati-rice/#exp)

### Calrose Rice

\* Use cold water and *unrinsed* rice. If rinsing your rice, weigh out the inner pot + dry rice first before rinsing and adding water.

| <sup>Amount of rice:</sup> <input id="inputCalrose" type="number" placeholder="grams" oninput="CalroseCalc(this.value)" onchange="CalroseCalc(this.value)"> | Harder, chewier rice | Al dente (just right) | Softer, mushier rice |
|--|----------------------|-----------------------|----------------------|
| Water: | <span id="outputWaterHard"></span> | <span id="outputWaterMed"></span> | <span id="outputWaterSoft"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 6 minutes | 6 minutes | 6 minutes |
| Natural Pressure Release: | 9 minutes | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover}

<script>
function CalroseCalc(valNum) {
  document.getElementById("outputWaterHard").innerHTML = Math.round(valNum * 250 / 235) + " mL";
  document.getElementById("outputWaterMed").innerHTML = Math.round(valNum * 295 / 235) + " mL";
  document.getElementById("outputWaterSoft").innerHTML = Math.round(valNum * 312.5 / 235) + " mL";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-calrose-rice/#exp)

### Chickpeas (or Garbanzo Beans), Dry

\* Baking soda optional—produces more tender chickpeas (useful for hummus).

| <sup>Amount of chickpeas:</sup> <input id="inputChickpea" type="number" placeholder="grams" oninput="ChickpeaCalc(this.value)" onchange="ChickpeaCalc(this.value)"> | Unsoaked | Soaked 8+ hours |
|--|----------|-----------------|
| Water: | <span id="outputChickpeaUnsoaked"></span> | <span id="outputChickpeaSoaked"></span> |
| Baking Soda: | <span id="outputChickpeaUnsoaked1"></span> | <span id="outputChickpeaSoaked1"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 40 minutes | 10 minutes |
| Natural Pressure Release: | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover}

<script>
function ChickpeaCalc(valNum) {
  document.getElementById("outputChickpeaUnsoaked").innerHTML = Math.round(valNum * 1500 / 454) + " mL";
  document.getElementById("outputChickpeaUnsoaked1").innerHTML = Math.round(valNum * 6 / 454) + " g";
  document.getElementById("outputChickpeaSoaked").innerHTML = Math.round(valNum * 1250 / 454) + " mL";
  document.getElementById("outputChickpeaSoaked1").innerHTML = Math.round(valNum * 6 / 454) + " g";
}
</script>

Recipe credit: [Sweet Peas and Saffron](https://sweetpeasandsaffron.com/instant-pot-chickpeas/)

### Eggs

\* Use cold water and cold eggs. Manually release pressure immediately and submerge eggs in a cold water bath as fast as possible.

| <sup>Number of eggs and preferred doneness:</sup> <span style="width:50%;"><input id="inputEggNum" type="number" placeholder="eggs" oninput="EggCalc()" onchange="EggCalc()"></span> <span style="width:50%;"><select id="inputEggOpt" oninput="EggCalc()" onchange="EggCalc()"><option value="1">Runny</option><option value="2">Soft</option><option value="3">Hard</option></select></span> | Low pressure (ideal) | High pressure |
|--------|--------|--------|
| Water: | 250 mL | 250 mL |
| Cook Setting: | Pressure cook on LOW | Pressure cook on HIGH |
| Cook Time: | <span id="outputEggLP"></span> | <span id="outputEggHP"></span> |
| Natural Pressure Release: | 0 minutes | 0 minutes |
{: .table .table-striped .table-hover}

<script>
function EggCalc() {
  var valNum = document.getElementById("inputEggNum").value;
  var valOpt = document.getElementById("inputEggOpt").value;
  if (valOpt == 1) {
    if (valNum == 1 || valNum == 2 || valNum == 3) {
      document.getElementById("outputEggLP").innerHTML = "5 minutes"
    } else if (valNum == 4 || valNum == 5) {
      document.getElementById("outputEggLP").innerHTML = "4 minutes"
    } else if (valNum == 6 || valNum == 7) {
      document.getElementById("outputEggLP").innerHTML = "3 minutes"
    } else if (valNum >= 8) {
      document.getElementById("outputEggLP").innerHTML = "2 minutes (have not tested with 8 or more eggs)"
    } else {
      document.getElementById("outputEggLP").innerHTML = ""
    }
  } else if (valOpt == 2) {
    if (valNum == 1 || valNum == 2 || valNum == 3) {
      document.getElementById("outputEggLP").innerHTML = "6 minutes"
    } else if (valNum == 4 || valNum == 5) {
      document.getElementById("outputEggLP").innerHTML = "5 minutes"
    } else if (valNum == 6 || valNum == 7) {
      document.getElementById("outputEggLP").innerHTML = "4 minutes"
    } else if (valNum >= 8) {
      document.getElementById("outputEggLP").innerHTML = "3 minutes (have not tested with 8 or more eggs)"
    } else {
      document.getElementById("outputEggLP").innerHTML = ""
    }
  } else if (valOpt == 3) {
    if (valNum == 1 || valNum == 2) {
      document.getElementById("outputEggLP").innerHTML = "13 minutes"
    } else if (valNum == 3) {
      document.getElementById("outputEggLP").innerHTML = "12 minutes"
    } else if (valNum == 4) {
      document.getElementById("outputEggLP").innerHTML = "11 minutes"
    } else if (valNum == 5) {
      document.getElementById("outputEggLP").innerHTML = "10 minutes"
    } else if (valNum == 6) {
      document.getElementById("outputEggLP").innerHTML = "9 minutes"
    } else if (valNum == 7) {
      document.getElementById("outputEggLP").innerHTML = "8 minutes"
    } else if (valNum >= 8) {
      document.getElementById("outputEggLP").innerHTML = "7 minutes (have not tested with 8 or more eggs)"
    } else {
      document.getElementById("outputEggLP").innerHTML = ""
    }
  } else {
    document.getElementById("outputEggLP").innerHTML = ""
  }

  if (valOpt == 1) {
    if (valNum == 1 || valNum == 2 || valNum == 3) {
      document.getElementById("outputEggHP").innerHTML = "3 minutes"
    } else if (valNum == 4 || valNum == 5) {
      document.getElementById("outputEggHP").innerHTML = "2 minutes"
    } else if (valNum >= 6) {
      document.getElementById("outputEggHP").innerHTML = "1 minute (have not tested with 6 or more eggs)"
    } else {
      document.getElementById("outputEggHP").innerHTML = ""
    }
  } else if (valOpt == 2) {
    if (valNum == 1 || valNum == 2 || valNum == 3) {
      document.getElementById("outputEggHP").innerHTML = "4 minutes"
    } else if (valNum == 4 || valNum == 5) {
      document.getElementById("outputEggHP").innerHTML = "3 minutes"
    } else if (valNum == 6 || valNum == 7) {
      document.getElementById("outputEggHP").innerHTML = "3 minutes"
    } else if (valNum >= 8) {
      document.getElementById("outputEggHP").innerHTML = "2 minutes (have not tested with 8 or more eggs)"
    } else {
      document.getElementById("outputEggHP").innerHTML = ""
    }
  } else if (valOpt == 3) {
    if (valNum == 1 || valNum == 2) {
      document.getElementById("outputEggHP").innerHTML = "8 minutes"
    } else if (valNum == 3) {
      document.getElementById("outputEggHP").innerHTML = "7 minutes"
    } else if (valNum == 4) {
      document.getElementById("outputEggHP").innerHTML = "7 minutes"
    } else if (valNum == 5) {
      document.getElementById("outputEggHP").innerHTML = "6 minutes"
    } else if (valNum == 6) {
      document.getElementById("outputEggHP").innerHTML = "6 minutes"
    } else if (valNum == 7) {
      document.getElementById("outputEggHP").innerHTML = "5 minutes"
    } else if (valNum >= 8) {
      document.getElementById("outputEggHP").innerHTML = "5 minutes (have not tested with 8 or more eggs)"
    } else {
      document.getElementById("outputEggHP").innerHTML = ""
    }
  } else {
    document.getElementById("outputEggHP").innerHTML = ""
  }
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/pressure-cooker-soft-hard-boiled-eggs/)

|  | Egg Loaf (for salads, sandwiches, etc) |
|--|----------------------------------------|
| Number of eggs: | <input id="inputEggLoaf" type="number" placeholder="eggs" oninput="EggLoafCalc(this.value)" onchange="EggLoafCalc(this.value)"> |
| Water: | 250 mL |
| Cook Setting: | Pressure cook on HIGH |
| Cook Time: | <span id="outputEggLoaf"></span> |
| Natural Pressure Release: | 10 min |
{: .table .table-striped .table-hover}

<script>
function EggLoafCalc(valNum) {
  document.getElementById("outputEggLoaf").innerHTML = Math.round(1 + 5 * Math.log10(valNum)) + " minutes";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-kathy-egg-loaf/)

### Steel Cut Oats

\* Use cold water. You can pour in the oats and water the night before and set a delay timer; the overnight soaking won't affect the texture of the oats very much, but you can reduce the cook time by 1 minute if you want.

| <sup>Amount of oats:</sup> <input id="inputSCOat" type="number" placeholder="grams" oninput="SCOatCalc(this.value)" onchange="SCOatCalc(this.value)"> | Thick, chewy | Just right | Moist, creamy |
|--|----------------------|-----------------------|----------------------|
| Water: | <span id="outputSCOatHard"></span> | <span id="outputSCOatMed"></span> | <span id="outputSCOatSoft"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 10 minutes | 10 minutes | 20 minutes |
| Natural Pressure Release: | full length | full length | full length |
{: .table .table-striped .table-hover}

<script>
function SCOatCalc(valNum) {
  document.getElementById("outputSCOatHard").innerHTML = Math.round(valNum * 250 / 80) + " mL";
  document.getElementById("outputSCOatMed").innerHTML = Math.round(valNum * 312.5 / 80) + " mL";
  document.getElementById("outputSCOatSoft").innerHTML = Math.round(valNum * 312.5 / 80) + " mL";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-steel-cut-oats/)

### Steamed Veggies

\* Baking soda optional—produces more tender chickpeas (useful for hummus).

|  | Unsoaked | Soaked 8+ hours |
|--|----------|-----------------|
| Dry chickpeas: | <input id="inputChickpea" type="number" placeholder="grams" oninput="ChickpeaUnsoaked(this.value)" onchange="ChickpeaUnsoaked(this.value)"> | <input id="inputChickpea" type="number" placeholder="grams" oninput="ChickpeaSoaked(this.value)" onchange="ChickpeaSoaked(this.value)"> |
| Water: | <span id="outputChickpeaUnsoaked"></span> | <span id="outputChickpeaSoaked"></span> |
| Baking Soda: | <span id="outputChickpeaUnsoaked1"></span> | <span id="outputChickpeaSoaked1"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 40 minutes | 10 minutes |
| Natural Pressure Release: | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover}

<script>
function ChickpeaUnsoaked(valNum) {
  document.getElementById("outputChickpeaUnsoaked").innerHTML = Math.round(valNum * 1500 / 454) + " mL";
  document.getElementById("outputChickpeaUnsoaked1").innerHTML = Math.round(valNum * 6 / 454) + " g";
}
</script>

<script>
function ChickpeaSoaked(valNum) {
  document.getElementById("outputChickpeaSoaked").innerHTML = Math.round(valNum * 1250 / 454) + " mL";
  document.getElementById("outputChickpeaSoaked1").innerHTML = Math.round(valNum * 6 / 454) + " g";
}
</script>

Recipe credit: [Sweet Peas and Saffron](https://sweetpeasandsaffron.com/instant-pot-chickpeas/)
