# <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>Garena Top Up</title>
    <style>
        body { margin: 0; background: #1a1a1a; color: white; font-family: sans-serif; display: flex; justify-content: center; padding: 20px; }
        .box { background: rgba(255,255,255,0.1); padding: 20px; border-radius: 15px; width: 100%; max-width: 400px; }
        input { width: 100%; padding: 12px; margin: 10px 0; border-radius: 8px; border: none; box-sizing: border-box; }
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin: 15px 0; }
        .btn-dia { background: #333; padding: 15px; text-align: center; border-radius: 8px; cursor: pointer; border: 1px solid #555; }
        .btn-pay { background: #d32f2f; width: 100%; padding: 15px; border: none; border-radius: 8px; color: white; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>

<div class="box">
    <h2>مركز الشحن</h2>
    <input type="text" id="uid" placeholder="ID اللاعب">
    <div class="grid">
        <div class="btn-dia" onclick="select(530)">530 💎</div>
        <div class="btn-dia" onclick="select(1080)">1080 💎</div>
        <div class="btn-dia" onclick="select(2200)">2200 💎</div>
        <div class="btn-dia" onclick="select(5600)">5600 💎</div>
    </div>
    <button class="btn-pay" onclick="pay()">شراء الآن</button>
</div>

<script>
    let amount = 0;
    function select(val) {
        amount = val;
        alert("تم اختيار: " + val + " جوهرة");
    }
    function pay() {
        let uid = document.getElementById('uid').value;
        if(uid === "" || amount === 0) {
            alert("يرجى إدخال ID واختيار الكمية");
        } else {
            alert("جارٍ التحقق من الحساب...");
        }
    }
</script>

</body>
</html>
