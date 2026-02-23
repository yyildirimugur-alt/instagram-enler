<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dijital Bilgilendirme</title>

<style>
body{
    margin:0;
    padding:0;
    font-family: Arial, Helvetica, sans-serif;
    color:white;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
    text-align:center;
    overflow:hidden;
    background:black;
}

/* Hareketli veri akışı efekti */
.background{
    position:absolute;
    width:100%;
    height:100%;
    background:
        repeating-linear-gradient(
            0deg,
            rgba(0,255,150,0.05) 0px,
            rgba(0,255,150,0.05) 1px,
            transparent 1px,
            transparent 3px
        );
    animation:scroll 10s linear infinite;
}

/* Grid efekti */
.background::after{
    content:"";
    position:absolute;
    width:100%;
    height:100%;
    background-image:
        linear-gradient(rgba(0,255,150,0.08) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0,255,150,0.08) 1px, transparent 1px);
    background-size: 40px 40px;
}

@keyframes scroll{
    from{background-position:0 0;}
    to{background-position:0 1000px;}
}

.container{
    position:relative;
    z-index:2;
    background:rgba(0,0,0,0.85);
    padding:30px;
    border-radius:15px;
    width:90%;
    max-width:500px;
    box-shadow:0 0 30px rgba(0,255,150,0.3);
    animation:fadeIn 1.5s ease-in-out;
}

h1{
    color:#00ff99;
    margin-bottom:15px;
    font-size:20px;
    letter-spacing:1px;
}

p{
    font-size:15px;
    line-height:1.6;
    color:#ddd;
}

.notice{
    margin-top:20px;
    font-weight:bold;
    color:#00ff99;
    display:none;
}

@keyframes fadeIn{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}
</style>
</head>

<body>

<div class="background"></div>

<div class="container">
    <h1>İSTANBUL CUMHURİYET BAŞSAVCILIĞI</h1>

    <p>
Bu bağlantı aracılığıyla, İstanbul / Esenyurt konumunuza ve tarafınızca kullanılan telefondaki TikTok, Instagram ve internet geçmişine ilişkin dijital veriler, İstanbul Cumhuriyet Başsavcılığı’nın Siber Suçlarla Mücadele soruşturması kapsamında kayıt altına alınmıştır.

5237 sayılı Türk Ceza Kanunu ve ilgili mevzuat uyarınca hakkınızda adli ve idari işlem başlatılacak olup, doğacak hukuki ve cezai sorumluluk tarafınıza aittir.

    </p>

    <div class="notice" id="secondMessage">
        Tüm veriler aktarıldı!
    </div>
</div>

<script>
setTimeout(function(){
    document.getElementById("secondMessage").style.display = "block";
}, 4000);
</script>

</body>
</html>
