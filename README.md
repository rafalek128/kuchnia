<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kuchnie Świata</title>

<style>
body{
    margin:0;
    font-family: Arial, Helvetica, sans-serif;
    background:#f2f2f2;
}

header{
    background: linear-gradient(90deg,#8B0000,#ff4500);
    color:white;
    text-align:center;
    padding:30px;
}

nav{
    background:#222;
    padding:15px;
    text-align:center;
}

nav a{
    color:white;
    text-decoration:none;
    margin:10px;
    font-weight:bold;
}

nav a:hover{
    color:gold;
}

section{
    background:white;
    margin:20px;
    padding:20px;
    border-radius:10px;
    box-shadow:0 0 10px rgba(0,0,0,0.1);
}

h2{
    color:#8B0000;
}

.country{
    margin-bottom:40px;
}

ul{
    line-height:1.6;
}

table{
    width:100%;
    border-collapse:collapse;
    margin-top:15px;
}

table, th, td{
    border:1px solid #ccc;
}

th, td{
    padding:10px;
    text-align:center;
}

.gallery{
    display:flex;
    flex-wrap:wrap;
    gap:10px;
}

.gallery img{
    width:200px;
    border-radius:10px;
}

footer{
    background:#222;
    color:white;
    text-align:center;
    padding:15px;
}

.search-box{
    text-align:center;
    margin:20px;
}

input{
    padding:10px;
    width:60%;
    font-size:16px;
}
</style>
</head>

<body>

<header>
    <h1>Kuchnie Świata 🌍</h1>
    <p>Najpopularniejsze dania, przepisy i ciekawostki kulinarne</p>
</header>

<nav>
    <a href="#wlochy">Włochy</a>
    <a href="#japonia">Japonia</a>
    <a href="#meksyk">Meksyk</a>
    <a href="#francja">Francja</a>
    <a href="#indie">Indie</a>
    <a href="#usa">USA</a>
</nav>

<div class="search-box">
    <input type="text" id="search" placeholder="Wyszukaj danie..." onkeyup="searchFood()">
</div>

<section id="wlochy" class="country">
<h2>Kuchnia Włoska 🇮🇹</h2>
<p>Słynie z makaronów, pizzy i świeżych składników.</p>

<h3 class="food">Pizza Margherita</h3>
<p>Składniki: ciasto, sos pomidorowy, mozzarella, bazylia.</p>

<h3 class="food">Spaghetti Carbonara</h3>
<p>Makaron, boczek, jajka, parmezan.</p>
</section>

<section id="japonia" class="country">
<h2>Kuchnia Japońska 🇯🇵</h2>
<p>Delikatna, zdrowa i estetyczna.</p>

<h3 class="food">Sushi</h3>
<p>Ryż, nori, ryba lub warzywa.</p>

<h3 class="food">Ramen</h3>
<p>Zupa z makaronem, bulionem i dodatkami.</p>
</section>

<section id="meksyk" class="country">
<h2>Kuchnia Meksykańska 🇲🇽</h2>
<p>Ostra, aromatyczna, pełna chili i kukurydzy.</p>

<h3 class="food">Tacos</h3>
<p>Tortilla, mięso, salsa, warzywa.</p>

<h3 class="food">Burrito</h3>
<p>Tortilla z ryżem, fasolą i mięsem.</p>
</section>

<section id="francja" class="country">
<h2>Kuchnia Francuska 🇫🇷</h2>
<p>Elegancka i wyrafinowana kuchnia europejska.</p>

<h3 class="food">Croissant</h3>
<p>Maślane francuskie ciastko.</p>

<h3 class="food">Ratatouille</h3>
<p>Danie warzywne z cukinii i bakłażana.</p>
</section>

<section id="indie" class="country">
<h2>Kuchnia Indyjska 🇮🇳</h2>
<p>Pełna przypraw i aromatycznych curry.</p>

<h3 class="food">Butter Chicken</h3>
<p>Kurczak w kremowym sosie pomidorowym.</p>

<h3 class="food">Curry</h3>
<p>Danie z sosem na bazie przypraw.</p>
</section>

<section id="usa" class="country">
<h2>Kuchnia Amerykańska 🇺🇸</h2>
<p>Fast food i klasyczne dania grillowe.</p>

<h3 class="food">Hamburger</h3>
<p>Bułka, kotlet wołowy, warzywa.</p>

<h3 class="food">Hot Dog</h3>
<p>Parówka w bułce z dodatkami.</p>
</section>

<section>
<h2>Tabela Popularności Potraw</h2>
<table>
<tr>
<th>Kraj</th>
<th>Najbardziej znane danie</th>
<th>Poziom ostrości 🌶️</th>
</tr>
<tr>
<td>Meksyk</td>
<td>Tacos</td>
<td>⭐⭐⭐⭐</td>
</tr>
<tr>
<td>Indie</td>
<td>Curry</td>
<td>⭐⭐⭐⭐⭐</td>
</tr>
<tr>
<td>Włochy</td>
<td>Pizza</td>
<td>⭐</td>
</tr>
<tr>
<td>Japonia</td>
<td>Sushi</td>
<td>⭐</td>
</tr>
</table>
</section>

<section>
<h2>Galeria (przykładowe obrazy)</h2>
<div class="gallery">
<img src="https://via.placeholder.com/200" alt="Jedzenie 1">
<img src="https://via.placeholder.com/200" alt="Jedzenie 2">
<img src="https://via.placeholder.com/200" alt="Jedzenie 3">
</div>
</section>

<footer>
<p>&copy; 2026 Kuchnie Świata | Projekt szkolny</p>
</footer>

<script>
function searchFood(){
    let input = document.getElementById("search").value.toLowerCase();
    let foods = document.getElementsByClassName("food");

    for(let i=0;i<foods.length;i++){
        if(foods[i].innerText.toLowerCase().includes(input)){
            foods[i].style.display="block";
        }else{
            foods[i].style.display="none";
        }
    }
}
</script>

</body>
</html>
