# For-Thae-Lay
<meta name='viewport' content='width=device-width, initial-scale=1'/><meta name='viewport' content='width=device-width, initial-scale=1'/><!DOCTYPE html>
<html lang="my">
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="style.css">
    <title>Surprise For You</title>
</head>
<body>
    <div id="container">
        <img id="image" src="https://png.pngtree.com/png-vector/20241105/ourmid/pngtree-depressed-sad-face-emoji-expression-symbol-png-image_14213847.png" alt="Cat" width="300">
        <h2 id="text">မောင့်ကိုချစ်လား😭? 💔</h2>
        
        <div class="buttons">
            <button id="yesBtn" onclick="nextStep()">YES 😢</button>
            <button id="noBtn" onmouseover="moveNoButton()">NO</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
<style>body { display: flex; justify-content: center; align-items: center; height: 100vh; background-color: #ffe6e6; font-family: sans-serif; }
#container { text-align: center; }
#noBtn { position: absolute; padding: 10px 20px; }
#yesBtn { padding: 10px 20px; background-color: #4CAF50; color: white; border: none; cursor: pointer; }
.buttons { margin-top: 20px; }
</style><script>let step = 0;
const texts = [
    "မောင်မနေနိုင်ဘူးကော်😢", 
    "မောင်သဲလေးက်ုချစ်တယ်💞", 
    " တခြားနည်းလမ်းရှိမှာပါနော်☹️"
];
const images = ["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTelhK576GWx2oIfnvxZkHAQt08PP4WmSCUqHmS-L0Kcg&s=10", "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgQh6ZmpU_lLz0ZwXcdQUtaKDeGl4QQ60oHIJYNhf0OdohFIm7-JT5O6B8njTx5ltxho2Xag1UFKRu9lGybZAjp6tsYdeLW-_hNfxHT71Q0GPKt6b3e1KANtlmu8C7voRst2a1FPMuje2w/s1600/love-you.png", "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRG6Zo34aXeXcSakPEzX_ghBP0krbBIu4CgEQtFt84dOw&s=10"];

function moveNoButton() {
    const btn = document.getElementById('noBtn');
    btn.style.left = Math.random() * 80 + "%";
    btn.style.top = Math.random() * 80 + "%";
}

function nextStep() {
    if (step < texts.length) {
        document.getElementById('text').innerText = texts[step];
        document.getElementById('image').src = images[step];
        step++;
    } else {
        alert("Yay! ပြန်အဆင်ပြေပြီ! ❤️");
    }
}
</script>
