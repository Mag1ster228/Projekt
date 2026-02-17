<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sieci Komputerowe</title>

<style>
body {font-family: Arial; margin:0; background:#f0f0f0;}
header, footer {background:#003366; color:white; text-align:center; padding:10px;}
nav {background:#0055aa; text-align:center; padding:10px;}
nav a {color:white; margin:10px; text-decoration:none;}
section {background:white; margin:15px; padding:15px;}
table {width:100%; border-collapse:collapse;}
table, th, td {border:1px solid black;}
th, td {padding:8px;}
button {margin-top:10px; padding:5px;}
@media(max-width:600px){ nav a{display:block; margin:5px;} }
</style>
</head>

<body>

<header>
<h1>Montaż i Konfiguracja Sieci</h1>
</header>

<nav>
<a href="#normy">Normy</a>
<a href="#topologie">Topologie</a>
<a href="#modele">Modele</a>
<a href="#koszt">Kosztorys</a>
</nav>

<main>

<section id="normy">
<h2>Normy</h2>
<table>
<tr><th>Norma</th><th>Opis</th></tr>
<tr><td>ISO/IEC 11801</td><td>Okablowanie strukturalne</td></tr>
<tr><td>TIA/EIA-568</td><td>Standard USA</td></tr>
</table>
</section>

<section id="topologie">
<h2>Topologie</h2>
<ul>
<li>Gwiazda</li>
<li>Magistrala</li>
<li>Pierścień</li>
</ul>
<iframe width="300" height="200"
src="https://www.youtube.com/embed/3QhU9jd03a0"
title="Topologie"></iframe>
</section>

<section id="modele">
<h2>Model OSI</h2>
<ol>
<li>Fizyczna</li>
<li>Łącza danych</li>
<li>Sieciowa</li>
<li>Transportowa</li>
<li>Aplikacji</li>
</ol>
</section>

<section id="koszt">
<h2>Kalkulator kosztów</h2>
<form id="form">
Ilość metrów:<br>
<input type="number" id="m" required><br>
Cena za metr:<br>
<input type="number" id="c" required><br>
<button type="submit">Oblicz</button>
</form>
<p id="wynik"></p>
</section>

</main>

<footer>
<p>Projekt edukacyjny 2026</p>
</footer>

<script>
document.getElementById("form").addEventListener("submit", function(e){
e.preventDefault();
let m = document.getElementById("m").value;
let c = document.getElementById("c").value;
document.getElementById("wynik").innerText =
"Koszt: " + (m*c) + " zł";
});
</script>

</body>
</html>
