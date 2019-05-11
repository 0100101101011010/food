---
layout: page
title: Conversion Calculators
permalink: /calculator/
---
<style>
input[type=text], input[type=number], select {
  width: 100%;
  padding: 1px 2px;
  margin: 2px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
</style>

## Instant Pot recipes

### Basmati Rice

\* Use cold water and *unrinsed* rice. If rinsing your rice, weigh out the inner pot + dry rice first before rinsing and adding water.

|  | Harder, chewier rice | Al dente (just right) | Softer, mushier rice |
|--|----------------------|-----------------------|----------------------|
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

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-basmati-rice/#exp)

### Calrose Rice

\* Use cold water and *unrinsed* rice. If rinsing your rice, weigh out the inner pot + dry rice first before rinsing and adding water.

|  | Harder, chewier rice | Al dente (just right) | Softer, mushier rice |
|--|----------------------|-----------------------|----------------------|
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

### Chickpeas (or Garbanzo Beans)

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

### Eggs

\* Use cold water and cold eggs. Manually release pressure immediately and submerge eggs in a cold water bath as fast as possible.

|  | Low pressure (ideal) | High pressure |
|--|----------------------|---------------|
| Number of eggs: | <input id="inputEggNum" type="number" placeholder="eggs" oninput="EggLP()" onchange="EggLP()"> | <input id="inputEgg" type="number" placeholder="eggs" oninput="EggHP()" onchange="EggLP()"> |
| Egg doneness: | <select id="inputEggOpt" oninput="EggLP()" onchange="EggLP()"><option value="1">Runny</option><option value="2">Soft</option><option value="3">Hard</option></select> | <select id="inputEgg" oninput="EggHP()" onchange="EggHP()"><option value="1">Runny</option><option value="2">Soft</option><option value="3">Hard</option></select> |
| Water: | 250 mL | 250 mL |
| Cook Setting: | Pressure cook on LOW | Pressure cook on HIGH |
| Cook Time: | <span id="outputEggLP"></span> | <span id="outputEggHP"></span> |
| Natural Pressure Release: | 0 minutes | 0 minutes |
{: .table .table-striped .table-hover}

<script>
function EggLP() {
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
}
function EggHP() {
  var valNum = document.getElementById("inputEggNum").value;
  var valOpt = document.getElementById("inputEggOpt").value;
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

<script>
function EggHP(valNum) {
  document.getElementById("outputEggHP").innerHTML = Math.round(valNum * 1250 / 454) + " mL";
}
</script>

Recipe credit: [Sweet Peas and Saffron](https://sweetpeasandsaffron.com/instant-pot-chickpeas/)

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
