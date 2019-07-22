---
layout: page
author: Kelly Zhang
title: Conversion Calculators
permalink: /calculator/
excerpt: "A cooking conversion calculator to give you ratios and cooking times for common foods."
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

* Table of Contents
{:toc}

## Instant Pot

Note: It may be helpful to weigh your inner pot by itself and keep the number handy, for instance if you forget to weigh something before you put it in the pot, you can use subtraction to work backwards and figure it out. For reference, the inner pot of my Instant Pot Viva 6 Qt (pretty much similar to IP Duo) is **843 g**.

\* Use cold tap water for all recipes unless otherwise stated.

### Basmati Rice

\* If rinsing your rice, weigh out the inner pot + dry rice first before rinsing and adding water, as the water absorbed by the rice should be counted as part of the water volumes below.

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

\* If rinsing your rice, weigh out the inner pot + dry rice first before rinsing and adding water, as the water absorbed by the rice should be counted as part of the water volumes below.

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
  document.getElementById("outputChickpeaUnsoaked").innerHTML = Math.round(valNum * 1250 / 454) + " mL";
  document.getElementById("outputChickpeaUnsoaked1").innerHTML = Math.round(valNum * 6 / 454) + " g";
  document.getElementById("outputChickpeaSoaked").innerHTML = Math.round(valNum * 1000 / 454) + " mL";
  document.getElementById("outputChickpeaSoaked1").innerHTML = Math.round(valNum * 6 / 454) + " g";
}
</script>

Recipe credit: [Sweet Peas and Saffron](https://sweetpeasandsaffron.com/instant-pot-chickpeas/)

### Eggs

\* Use cold eggs. Manually release pressure immediately and submerge eggs in a cold water bath as fast as possible.

| <sup>Number of eggs and preferred doneness:</sup> <input id="inputEggNum" type="number" placeholder="eggs" oninput="EggCalc()" onchange="EggCalc()"> <select id="inputEggOpt" oninput="EggCalc()" onchange="EggCalc()"><option value="1">Runny</option><option value="2">Soft</option><option value="3">Hard</option></select> | Low pressure (ideal) | High pressure |
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
      document.getElementById("outputEggLP").innerHTML = "2 minutes"
    } else if (valNum >= 8) {
      document.getElementById("outputEggLP").innerHTML = "not tested with 8 or more eggs"
    } else {
      document.getElementById("outputEggLP").innerHTML = ""
    }
  } else if (valOpt == 2) {
    if (valNum == 1 || valNum == 2 || valNum == 3) {
      document.getElementById("outputEggLP").innerHTML = "6 minutes"
    } else if (valNum == 4 || valNum == 5) {
      document.getElementById("outputEggLP").innerHTML = "5 minutes"
    } else if (valNum == 6 || valNum == 7) {
      document.getElementById("outputEggLP").innerHTML = "3 minutes"
    } else if (valNum >= 8) {
      document.getElementById("outputEggLP").innerHTML = "not tested with 8 or more eggs"
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
      document.getElementById("outputEggLP").innerHTML = "not tested with 8 or more eggs"
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
      document.getElementById("outputEggHP").innerHTML = "not tested with 6 or more eggs"
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
      document.getElementById("outputEggHP").innerHTML = "not tested with 8 or more eggs"
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
      document.getElementById("outputEggHP").innerHTML = "not tested with 8 or more eggs"
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

### Soy Milk

\* The "amount of soybeans" (input) uses dried, unsoaked, unrinsed beans. The "total mass of soybeans + water" (output) indicates the weight of the soybeans *after* soaking, in addition to the water you should add. Place the inner pot on the scale, tare the scale, add all the soybeans, then pour in water until it reaches the number indicated in the table.

| <sup>Amount of soybeans:</sup> <input id="inputSoyMilkCalc" type="number" placeholder="grams" oninput="SoyMilkCalc(this.value)" onchange="SoyMilkCalc(this.value)"> | Thin (for drinking) | Concentrated (for cooking) |
|--|----------------------|-----------------------|----------------------|
| Total mass of soybeans + water: | <span id="outputSoyMilkThin"></span> | <span id="outputSoyMilkThick"></span> |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 5 minutes | 5 minutes |
| Natural Pressure Release: | 25 minutes | 25 minutes |
{: .table .table-striped .table-hover}

<script>
function SoyMilkCalc(valNum) {
  document.getElementById("outputSoyMilkThin").innerHTML = Math.round(valNum * 11) + " mL";
  document.getElementById("outputSoyMilkThick").innerHTML = Math.round(valNum * 7) + " mL";
}
</script>

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-soy-milk/)

### Steel Cut Oats

\* You can pour in the oats and water the night before and set a delay timer; the overnight soaking won't affect the texture of the oats very much, but you can reduce the cook time by 1 minute if you want.

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

### Steamed Vegetables

\* Times are for cooking on the trivet or steamer rack. This is preferable to steaming directly in the liquid because it retains more nutrients and cooks all vegetables evenly. Note that you may also use the *Steam* function if your Instant Pot has it ([using a trivet is essential if you are using Steam](https://www.reddit.com/r/instantpot/comments/8cyfhk/what_is_the_functional_difference_between_the/)).

Amount of veggies: <input id="inputVeggies" type="number" placeholder="grams" oninput="VeggieCalc(this.value)" onchange="VeggieCalc(this.value)">

#### Broccoli or Cauliflower

|  | Crunchy | Tender |
|--------|--------|--------|
| Water: | 125 mL | 125 mL |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | <span id="outputBroccoliHard"></span> | <span id="outputBroccoliSoft"></span> |
| Natural Pressure Release: | 0 minutes | 0 minutes |
{: .table .table-striped .table-hover}

Recipe credit: [Pressure Cook Recipes (Broccoli)](https://www.pressurecookrecipes.com/instant-pot-broccoli/) and [Pressure Cook Recipes (Cauliflower)](https://www.pressurecookrecipes.com/instant-pot-cauliflower/)

#### Brussels Sprouts

|  | Crunchy | Tender |
|--------|--------|--------|
| Water: | 250 mL | 250 mL |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | <span id="outputBrusselsHard"></span> | <span id="outputBrusselsSoft"></span> |
| Natural Pressure Release: | 0 minutes | 0 minutes |
{: .table .table-striped .table-hover}

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-brussels-sprouts/)

#### Potato

|  | Small | Medium | Large |
|--------|--------|--------|--------|
| Water: | 250 mL | 250 mL | 250 mL |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 8 minutes | 12 minutes | 20 minutes |
| Natural Pressure Release: | 10 minutes | 10 minutes | 10 minutes |
{: .table .table-striped .table-hover}

Recipe credit: [/u/Paths98](https://www.reddit.com/r/instantpot/comments/biomro/i_just_discovered_perfect_ip_veggies/em2j7y0/)

#### Spaghetti Squash

\* Slice in half cross-wise or length-wise before pressure cooking.

|  | Firm (al dente) | Soft (well done) |
|--------|--------|--------|
| Water: | 250 mL | 250 mL |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 7 minutes | 7 minutes |
| Natural Pressure Release: | 0 minutes | 5 minutes |
{: .table .table-striped .table-hover}

Recipe credit: [Instant Pot Eats](https://instantpoteats.com/instant-pot-101-how-to-cook-vegetables/)

#### Sweet Potato

\* Sweet potato cooking times are more size-dependent than weight-dependent. Pierce skins in several places with a fork or toothpick before pressure cooking. You can slice larger sweet potatoes in half to effectively reduce their circumference and reduce cooking time.

| Circumference: | 6 inch | 8 inch | 10 inch | 12 inch |
|--|--|--|--|--|
| Water: | 250 mL | 250 mL | 250 mL  | 250 mL |
| Cook Setting: | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH | Pressure cook on HIGH |
| Cook Time: | 15–20 minutes | 25–30 minutes | 35–40 minutes | 45–50 minutes |
| Natural Pressure Release: | 10–11 minutes | 10–11 minutes | 10–11 minutes | 10–11 minutes |
{: .table .table-striped .table-hover}

Recipe credit: [Pressure Cook Recipes](https://www.pressurecookrecipes.com/instant-pot-sweet-potato/)

<script>
function VeggieCalc(valNum) {

  if (valNum <= 0) {
    document.getElementById("outputBroccoliHard").innerHTML = "";
    document.getElementById("outputBroccoliSoft").innerHTML = "";
    document.getElementById("outputBrusselsHard").innerHTML = "";
    document.getElementById("outputBrusselsSoft").innerHTML = "";
  }

  if ((valNum - 500)/-350 < 0) {
    document.getElementById("outputBroccoliHard").innerHTML = "not recommended";
  } else if ((valNum - 500)/-350 > 0) {
    document.getElementById("outputBroccoliHard").innerHTML = Math.round((valNum - 500) / -350) + " minutes";
  } else {
    document.getElementById("outputBroccoliHard").innerHTML = "";
  }

  if ((valNum - 900)/-380 < 0) {
    document.getElementById("outputBroccoliSoft").innerHTML = "not recommended";
  } else if ((valNum - 900)/-380 > 0) {
    document.getElementById("outputBroccoliSoft").innerHTML = Math.round((valNum - 900) / -380) + " minutes";
  } else {
    document.getElementById("outputBroccoliSoft").innerHTML = "";
  }

  if ( -(Math.log10(valNum)) + 4.5 <= 0.5) {
    document.getElementById("outputBrusselsHard").innerHTML = "not recommended";
  } else if ( -(Math.log10(valNum)) + 4.5 > 0.5) {
    document.getElementById("outputBrusselsHard").innerHTML = Math.round(( -(Math.log10(valNum)) + 4.5)) + " minutes";
  } else {
    document.getElementById("outputBrusselsHard").innerHTML = "";
  }

  if ( -(Math.log10(valNum)) + 5.5 <= 0.5) {
    document.getElementById("outputBrusselsSoft").innerHTML = "not recommended";
  } else if ( -(Math.log10(valNum)) + 5.5 > 0.5) {
    document.getElementById("outputBrusselsSoft").innerHTML = Math.round(( -(Math.log10(valNum)) + 5.5)) + " minutes";
  } else {
    document.getElementById("outputBrusselsSoft").innerHTML = "";
  }

}
</script>

## Slow Cooking

https://blogs.extension.iastate.edu/answerline/2014/02/06/slow-cookers-times-temperatures-and-techniques/

## Roasting Vegetables

Toss all veggies in 1–2 tbsp of oil (just to get everything barely covered)

### Crucifers (Broccoli, Brussels Sprouts, Cabbage, Cauliflower)

> 15–25 min @ 400 °F (flip after 15 min)

Recipe credit: [samnan2 from Allrecipes](https://www.allrecipes.com/recipe/240800/roasted-cabbage/), [The Kitchn](https://www.thekitchn.com/how-to-roast-any-vegetable-101221)

### Garlic

> 40–60 min @ 400 °F wrapped in foil (until center clove is completely soft throughout)

Recipe credit: [The Kitchn](https://www.thekitchn.com/how-to-roast-garlic-in-the-oven-5341)

### Root Veggies (Beets, Carrots, Potatoes, Sweet Potatoes) and Onions

> For sticks or fries: 15–25 min @ 425 °F (flip or shake around after 10 min)
> For wedges: 30–45 min @ 425 °F (after 30, check every 5 min)

Recipe credit: [The Kitchn](https://www.thekitchn.com/how-to-roast-any-vegetable-101221)

### Soft Veggies (Bell Pepper, Summer Squash, Tomatoes, Zucchini)

10–20 min

Recipe credit: [The Kitchn](https://www.thekitchn.com/how-to-roast-any-vegetable-101221)

### Thin Veggies (Asparagus, Green Beans)

> 10–20 min

Recipe credit: [The Kitchn](https://www.thekitchn.com/how-to-roast-any-vegetable-101221)

### Winter Squash (Butternut Squash, Acorn Squash)

> 20–60 min (after 20, check every 10 min)

Recipe credit: [The Kitchn](https://www.thekitchn.com/how-to-roast-any-vegetable-101221)

### Rule of Thumb for Roasting a New Vegetable
