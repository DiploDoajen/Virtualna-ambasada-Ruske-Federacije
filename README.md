# Virtualna-ambasada-Ruske-Federacije
<!-- KOMPLETAN HTML SA SVIM OPISIMA INSTITUCIJA -->
<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<title>Virtuelna ambasada Ruske Federacije u Republici Srbiji</title>
<style>
body {font-family: 'Segoe UI', Arial, sans-serif; margin:0; background:#f4f6f8; color:#1a1a1a;}
header {background:#1f3a5f; color:#fff; padding:20px; text-align:center;}
main {display:flex;}
nav {width:300px; background:#ffffff; border-right:1px solid #ddd; padding:20px; height:100vh; overflow-y:auto;}
nav h3 {color:#1f3a5f;}
nav ul {list-style:none; padding-left:0;}
nav li {margin:10px 0; cursor:pointer;}
nav li:hover {text-decoration:underline;}
section {flex:1; padding:30px; overflow-y:auto;}
section h2 {color:#1f3a5f;}
.card {background:#fff; padding:20px; margin-bottom:20px; border-radius:6px; box-shadow:0 2px 6px rgba(0,0,0,0.08);} 
</style>
</head>
<body>
<header>
<img src="https://upload.wikimedia.org/wikipedia/en/f/f3/Flag_of_Russia.svg" alt="Zastava Ruske Federacije" style="height:60px; margin-bottom:10px;">
<h1>Virtuelna ambasada Ruske Federacije u Republici Srbiji</h1>
<p>Zvanična struktura i unutrašnja organizacija diplomatske misije</p>
</header>
<main>
<nav>
<h3>Prostorije ambasade</h3>
<ul>
<li onclick="show('amb')">Kabinet ambasadora</li>
<li onclick="show('dip')">Diplomatska kancelarija</li>
<li onclick="show('pol')">Političko odeljenje</li>
<li onclick="show('eko')">Ekonomsko odeljenje</li>
<li onclick="show('konz')">Konzularno odeljenje</li>
<li onclick="show('odbr')">Izaslanik odbrane</li>
<li onclick="show('kul')">Kultura i saradnja</li>
<li onclick="show('adm')">Administrativno-tehnička služba</li>
</ul>
</nav>
<section id="content">
<div class="card">
<h2>Dobrodošli</h2>
<p>Ova virtuelna simulacija prikazuje unutrašnju organizaciju Ambasade Ruske Federacije u Republici Srbiji, sa detaljnim opisom nadležnosti svakog odeljenja i institucije u sastavu diplomatske misije.</p>
</div>
</section>
</main>
<script>
const data = {
amb: `<div class='card'><h2>Kabinet ambasadora</h2><p><strong>Šef misije:</strong> Nj. E. gospodin Aleksandar Bocan-Harčenko, Izvanredni i Opunomoćeni Ambasador Ruske Federacije u Republici Srbiji.</p><p>Ukazom Predsednika Ruske Federacije od 10. juna 2019. godine br. 256, Aleksandar Bocan-Harčenko imenovan je za Izvanrednog i Opunomoćenog Ambasadora Ruske Federacije u Republici Srbiji.</p></div>`,
dip: `<div class='card'><h2>Diplomatska kancelarija</h2><p>Diplomatska kancelarija obuhvata diplomatsko osoblje koje pomaže ambasadoru u obavljanju političkih, protokolarnih i analitičkih zadataka. Nadležnosti uključuju pripremu izveštaja, analizu političke situacije u Republici Srbiji, održavanje kontakata sa državnim institucijama i pripremu bilateralnih sastanaka i poseta.</p></div>`,
pol: `<div class='card'><h2>Političko odeljenje</h2><p>Političko odeljenje prati unutrašnju i spoljnu politiku Republike Srbije, regionalna i međunarodna politička kretanja. Izrađuje analitičke i informativne izveštaje za Ministarstvo spoljnih poslova Ruske Federacije i učestvuje u pripremi političkih konsultacija i zvaničnih poseta.</p></div>`,
eko: `<div class='card'><h2>Trgovinsko predstavništvo Ruske Federacije</h2><p><strong>Adresa:</strong> Katićeva 8–10, 11000 Beograd</p><p><strong>Trgovinski predstavnik:</strong> gđa Irina Negrbetskaia.</p><p><strong>Zamenici:</strong> Aleksandr Vosmirko, Aleksandr Svigach, Aleksandr Beliaev, Vitalii Stanevka.</p><p>Trgovinsko predstavništvo predstavlja trgovinsko-ekonomske interese Ruske Federacije u Republici Srbiji i deluje u skladu sa bilateralnim međuvladinim sporazumima.</p></div>`,
konz: `<div class='card'><h2>Konzularno odeljenje</h2><p><strong>Adresa:</strong> Deligradska 32, 11000 Beograd</p><p><strong>Šef konzularnog odeljenja:</strong> Savetnik Aleksandra Simonova.</p><p>Konzularno odeljenje obavlja poslove zaštite prava i interesa državljana Ruske Federacije u Republici Srbiji, uključujući izdavanje viza i putnih isprava, overu dokumenata i pružanje konzularne pomoći u skladu sa međunarodnim konvencijama.</p></div>`,
odbr: `<div class='card'><h2>Aparat Izaslanika odbrane</h2><p><strong>Adresa:</strong> Deligradska 32, 11000 Beograd</p><p><strong>Izaslanik odbrane:</strong> general-major Gennady Mozhaev.</p><p><strong>Vojni i vazduhoplovni ataše:</strong> pukovnik Dmitry Mokrov.</p><p><strong>Zamenici vojnog atašea:</strong> pukovnik Alexander Tikhonov (prvi pomoćnik), pukovnik Evgenii Poliakov (pomoćnik), major Denis Kuchenev (pomoćnik).</p><p>Aparat Izaslanika odbrane je zvanično predstavništvo Ministarstva odbrane Ruske Federacije i predstavlja vojno-političke, vojne, vojno-tehničke i odbrambeno-ekonomske interese Ruske Federacije u Republici Srbiji.</p></div>`,
kul: `<div class='card'><h2>Ruski centar za nauku i kulturu u Beogradu</h2><p><strong>Adresa:</strong> Kraljice Natalije 33, 11000 Beograd</p><p><strong>Direktor:</strong> Jevgenij Baranov.</p><p>Ruski centar za nauku i kulturu u Beogradu (Ruski dom) otvoren je 9. aprila 1933. godine i najstariji je Ruski dom u sistemu Rossotrudničestva. Centar realizuje programe kulturne, obrazovne i naučne saradnje.</p></div>`,
adm: `<div class='card'><h2>Administrativno-tehnička služba</h2><p>Administrativno-tehnička služba obezbeđuje logističku, finansijsku i tehničku podršku radu ambasade. Zadužena je za održavanje objekta, bezbednost, administraciju i nesmetano funkcionisanje diplomatske misije.</p></div>`
};
function show(key){ document.getElementById('content').innerHTML = data[key]; }
</script>
</body>
</html>

