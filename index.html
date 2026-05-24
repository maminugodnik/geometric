<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Предварительный расчёт порошковой покраски</title>

<style>
body{
    font-family: Arial;
    max-width: 920px;
    margin: 40px auto;
}

h2{
    margin-top:30px;
}

.card{
    border:1px solid #eee;
    border-radius:10px;
    padding:15px;
    margin-top:15px;
}

label{
    display:block;
    margin-top:12px;
    font-weight:700;
}

.comment{
    font-size:12px;
    color:#666;
    margin-top:-4px;
    margin-bottom:6px;
}

input,select{
    width:100%;
    padding:10px;
    margin-top:6px;
    box-sizing:border-box;
    border:1px solid #ddd;
    border-radius:6px;
}

/* чекбоксы */
.checkline{
    display:flex;
    align-items:center;
    gap:10px;
    padding:10px;
    border:1px solid #eee;
    border-radius:8px;
    background:#fafafa;
    margin-top:8px;
}

.checkline input{
    width:18px;
    height:18px;
    accent-color:black;
}

button{
    width:100%;
    padding:14px;
    background:black;
    color:white;
    border:0;
    font-size:16px;
    margin-top:15px;
    border-radius:6px;
}

.result{
    margin-top:15px;
    font-size:16px;
    line-height:1.6;
}

.split{
    height:1px;
    background:#eee;
    margin:40px 0;
}

</style>
</head>

<body>

<h1>Предварительный расчёт порошковой покраски</h1>

<div class="card">

<label>Площадь изделия (м²)</label>
<input id="area_est">

<label>Расход краски (г/м²)</label>
<div class="comment">Норма: 150 г/м²</div>
<input id="paint_norm" value="150">

<label>Цена краски (₽/кг)</label>
<input id="paint_price_est" value="400">

<!-- ПОДГОТОВКА -->

<label class="checkline">
  <input type="checkbox" id="sand_est">
  <span>Пескоструй</span>
</label>
<input id="sand_norm" value="500">
<select id="sand_coef_est">
  <option value="1">Лёгкая (0%)</option>
  <option value="1.2">Средняя (+20%)</option>
  <option value="1.5">Сложная (+50%)</option>
  <option value="2">Очень сложная (+100%)</option>
</select>

<label class="checkline">
  <input type="checkbox" id="grind_est">
  <span>Зачистка</span>
</label>
<input id="grind_norm" value="250">
<select id="grind_coef_est">
  <option value="1">Лёгкая (0%)</option>
  <option value="1.2">Средняя (+20%)</option>
  <option value="1.5">Сложная (+50%)</option>
  <option value="2">Очень сложная (+100%)</option>
</select>

<label class="checkline">
  <input type="checkbox" id="clean_est">
  <span>Обезжиривание</span>
</label>
<input id="clean_norm" value="150">
<select id="clean_coef_est">
  <option value="1">Лёгкая (0%)</option>
  <option value="1.2">Средняя (+20%)</option>
  <option value="1.5">Сложная (+50%)</option>
  <option value="2">Очень сложная (+100%)</option>
</select>

<!-- ТЯЖЁЛЫЕ -->
<label class="checkline">
  <input type="checkbox" id="heavy_est">
  <span>Тяжёлое изделие</span>
</label>
<input id="heavy_cost_est" value="800">

<!-- ЭНЕРГИЯ -->
<label>Газ (фикс ₽/заказ)</label>
<input id="gas_norm" value="400">

<label>Электричество (₽/заказ)</label>
<input id="electric_norm" value="200">

<!-- МАРЖА -->
<label>Маржа</label>
<select id="margin">
  <option value="1">x1</option>
  <option value="1.5">x1.5</option>
  <option value="2">x2</option>
  <option value="3">x3</option>
  <option value="4">x4</option>
  <option value="5">x5</option>
  <option value="7">x7</option>
</select>

<!-- НАЛОГ -->
<label class="checkline">
  <input type="checkbox" id="tax">
  <span>Налог 13%</span>
</label>

<button onclick="calcEst()">Рассчитать</button>

<div class="result" id="result_est"></div>

</div>

<div class="split"></div>

<!-- ===================== -->
<!-- ОТДЕЛЬНЫЙ РАСХОД КРАСКИ -->
<!-- ===================== -->

<div class="card">

<h2>🎨 Расход краски (отдельный расчёт)</h2>

<label>Площадь изделия (м²)</label>
<input id="paint_area_only">

<label>Засыпано краски (кг)</label>
<input id="paint_in_only">

<label>Остаток краски (кг)</label>
<input id="paint_out_only">

<button onclick="calcPaintOnly()">Рассчитать расход</button>

<div class="result" id="result_paint_only"></div>

</div>

<script>

function getNum(id){
    return parseFloat((document.getElementById(id).value || "0").replace(",", "."));
}

/* ===================== */
function calcEst(){

    let area = getNum('area_est');

    let paint = area * (getNum('paint_norm') / 1000) * getNum('paint_price_est');

    let prep =
        (document.getElementById('sand_est').checked ? getNum('sand_norm') * getNum('sand_coef_est') : 0)
        +
        (document.getElementById('grind_est').checked ? getNum('grind_norm') * getNum('grind_coef_est') : 0)
        +
        (document.getElementById('clean_est').checked ? getNum('clean_norm') * getNum('clean_coef_est') : 0);

    let heavy = document.getElementById('heavy_est').checked ? getNum('heavy_cost_est') : 0;

    let gas = getNum('gas_norm');
    let electric = getNum('electric_norm');

    let cost = paint + prep + gas + electric + heavy;

    let margin = cost * getNum('margin');

    let tax = document.getElementById('tax').checked ? margin * 0.13 : 0;

    let finalPrice = margin + tax;

    document.getElementById('result_est').innerHTML =
        "📦 Себестоимость: " + Math.round(cost) + " ₽<br>" +
        "📈 С маржой: " + Math.round(margin) + " ₽<br>" +
        "🏛 Налог: " + Math.round(tax) + " ₽<br><br>" +
        "💰 Итог клиенту: " + Math.round(finalPrice) + " ₽";
}

/* ===================== */
function calcPaintOnly(){

    let area = getNum('paint_area_only');
    let inKg = getNum('paint_in_only');
    let outKg = getNum('paint_out_only');

    let used = Math.max(inKg - outKg, 0);

    if(area <= 0){
        document.getElementById('result_paint_only').innerHTML =
            "⚠ Укажи площадь";
        return;
    }

    let gPerM2 = (used * 1000) / area;

    document.getElementById('result_paint_only').innerHTML =
        "🎨 Израсходовано: " + used.toFixed(2) + " кг<br>" +
        "📐 Расход: " + gPerM2.toFixed(1) + " г/м²";
}

</script>

</body>
</html>
