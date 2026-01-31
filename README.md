<!DOCTYPE html>
<html lang="te">
<head>
<meta charset="UTF-8">
<title>Telugu Unicode to Non-Unicode Converter</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
    font-family: Arial, sans-serif;
    background:#f4f6f8;
    margin:0;
    padding:0;
}
header{
    background:#111827;
    color:white;
    padding:15px;
    text-align:center;
}
header h1{
    margin:0;
    font-size:22px;
}
header p{
    margin:5px 0 0;
    font-weight:bold;
    color:#facc15;
}

.container{
    max-width:800px;
    margin:20px auto;
    background:white;
    padding:20px;
    border-radius:10px;
    box-shadow:0 0 10px rgba(0,0,0,0.1);
}

textarea{
    width:100%;
    height:160px;
    padding:12px;
    font-size:16px;
    margin-bottom:15px;
    border-radius:8px;
    border:1px solid #ccc;
}

button{
    padding:12px 20px;
    font-size:16px;
    border:none;
    border-radius:8px;
    cursor:pointer;
    background:#2563eb;
    color:white;
}
button:hover{
    background:#1e40af;
}

.output{
    background:#f9fafb;
    font-family: "AnuScript", Arial;
}
footer{
    text-align:center;
    margin-top:20px;
    font-size:14px;
    color:#555;
}
</style>
</head>

<body>

<header>
    <h1>Telugu Unicode to Non-Unicode Converter</h1>
    <p>Developer: Shiva</p>
</header>

<div class="container">

    <h3>Unicode Telugu Text</h3>
    <textarea id="unicodeInput" placeholder="ఇక్కడ తెలుగు యూనికోడ్ టెక్స్ట్ పేస్ట్ చేయండి..."></textarea>

    <button onclick="convertText()">Convert</button>

    <h3 style="margin-top:20px;">Non-Unicode Output (AnuScript)</h3>
    <textarea id="nonUnicodeOutput" class="output" placeholder="Converted Non-Unicode text here..."></textarea>

</div>

<footer>
    © 2026 Telugu Converter | Developed by Shiva
</footer>

<script>
function convertText() {

    let text = document.getElementById("unicodeInput").value;

    // SAMPLE Telugu Unicode → Non-Unicode Mapping
    // (You can extend this table fully)
    const map = {
        "అ":"","ఆ":"","ఇ":"","ఈ":"",
        "ఉ":"","ఊ":"","ఎ":"","ఏ":"",
        "ఐ":"","ఒ":"","ఓ":"","ఔ":"",

        "క":"","ఖ":"","గ":"","ఘ":"","చ":"",
        "జ":"","ట":"","డ":"","త":"","ద":"",
        "న":"","ప":"","బ":"","మ":"","య":"",
        "ర":"","ల":"","వ":"","శ":"","స":"",
        "హ":"",

        "ా":"","ి":"","ీ":"","ు":"","ూ":"",
        "ె":"","ే":"","ై":"","ొ":"","ో":"","ౌ":"",
        "్":"","ం":"","ః":""," ":" "
    };

    let result = "";
    for (let char of text) {
        result += map[char] || char;
    }

    document.getElementById("nonUnicodeOutput").value = result;
}
</script>

</body>
</html>
