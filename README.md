<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chartjs-adapter-date-fns/dist/chartjs-adapter-date-fns.bundle.min.js">

    </script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@1.0.2/css/bulma.min.css">
    <link rel="stylesheet" href="stylebulma.css">
</head>

<body>
    <nav class="box " style="background-color: #87B1C6;">
        <img class="image
        " src="Affiche_CCampan_QMoenner_CThomas.jpg" alt="Map sur les disparités d'éducation par rapport au genre.">
        <figure class="image is-48x48">
            <img class="" src="Group 1.png" alt="">
        </figure>

    </nav>


    <div class="card" style="width: 70% ; margin: auto;height: auto;">
        <div class="card-header" style="background-color: #F3C2C2;">
            <p class="card-header-title" style="color: aliceblue; ">
                contexte
            </p>
        </div>
    
        <div class="content" style="margin-left: 5%; ; margin-right: 5%; margin-top: 5%; padding-bottom: 5%;">
        <p>Au fil de ces dernières années, l'accès à l'éducation des filles n'a cessé d'évoluer.
            L'inégalité des genres dans l'éducation reste une problématique majeure dans de nombreuses régions du
            monde, malgré des avancées significatives au cours des dernières décennies.
            Cette inégalité reflète une combinaison de barrières sociales, économiques, culturelles et structurelles
            qui limitent l'accès des filles et des femmes à une éducation de qualité.</p>
        </div>
    </div>



    <h1 class="title is-2">Chiffres clés</h1>

    <div class="fixed-grid has-4-cols">
        <div class="grid">
            <div class="cell cell is-col-span-2 is-row-span-2" id="cell_camembert">
                    <p class="title is-4 has-text-centered has-text-white" id="titre_camembert">Ecart de genre dans les études supérieures en Afghanistan</p>
                    <canvas id="chartcam"></canvas>
            </div>

            <div class="cell is-col-span-2">
                <span class="test">
                    <p class="title is-1 has-text-centered has-text-white" id="chiffres">9 millions</p><span class="survol"><p class="title is-4 has-text-centered has-text-white">de filles en âge de fréquenter
                        le cycle primaire n’entreront jamais dans une salle de classe</p>
                    </span>
                </span>  
            </div>

            <div class="cell">
                <span class="test">
                    <p class="title is-1 has-text-centered has-text-white " id="chiffres1">63%</p><span class="survol"><p class="title is-4 has-text-centered has-text-white">des adultes analphabètes dans le monde
                        sont des femmes</p>
                    </span>
                </span>  
                
            </div>

            <div class="cell">
                <span class="test">
                    <p class="title is-1 has-text-centered has-text-white"  id="chiffres1">59%</p><span class="survol"><p class="title is-4 has-text-centered has-text-white">des enfants arrêtent leurs études avant
                        le lycée dans les pays à revenu faible</p>
                    </span>
                </span>  
            </div>
        </div>
    </div>

    <h1 class="title is-2" id="texte1">Mais encore</h1>


    <div class="card" style="width: 70% ; margin: auto; margin-bottom: 3%; height: auto;">
        <div class="card-header" style="background-color: #F3C2C2;">
            <p class="card-header-title" style="color: aliceblue;">
                Dominance de sexe dans les études supérieures par pays
            </p>
        </div>
    
        <div class="card-content">
            <div class="columns is-variable is-8 is-flex-wrap-wrap-mobile is-flex-wrap-wrap-tablet is-flex-wrap-wrap-desktop">
                <!-- Texte -->
                <div class="column is-half">
                    <p class="map " style="margin-top: 10%; padding: 10%;">
                        Cette map montre que l’éducation pour les hommes est plus favorisée que pour les femmes et
                        qu’il n’y a pas beaucoup de pays dont la parité est égale.
    
                        Pour comprendre ce graphique, les pays en bleu sont ceux qui favorisent les hommes, les pays rose sont
                        ceux qui favorisent les femmes et les pays orange ceux qui ont une parité homme-femme.
                    </p>
                </div>
                <!-- Graphique -->
                <div class="column is-half center is-flex is-justify-content-center">
                    <object type="text/html" data="Map_cam.html" style="width: 80%; height:auto; margin: 5%;" ></object>
                </div>
            </div>
        </div>
    </div>


    
    <div class="card" style="width: 70% ; margin: auto; height: auto;" >

        <div class="card-header" style="background-color: #87B1C6;">
            <p class="card-header-title has-text-white">
                Evolution dans le temps de la répartition des sexes selon le niveau d'étude
            </p>
        </div>
        
        <div class="card-content">
            <div class="column is-flex is-justify-content-center">
                    <object class="image is-fullwidth" type="text/html" data="graph.html"  style= " width: 80%; height: 680px; " ></object>
            </div>
        </div>
    </div>




    <p id="source">Source : https://ourworldindata.org/global-education</p>
    <p id="credit">Crédits - Camille Thomas    Quentin Moenner    Cyléa Campan</p>



</body>
<script>

    //camembert

    let ctxcam = document.getElementById('chartcam');

    new Chart(ctxcam, {
        type: 'pie',
        data: {
            labels: ["femme", "homme"],
            datasets: [{
                data: [27, 73],
                backgroundColor: ['#FC9797', '#4A9DC7',],
                borderWidth: 0,
                hoverBackgroundColor: ['#D86060', '#005B88',],
            }]
        },

        options: {
            plugins: {
                legend: {
                    display: true,
                    labels: {
                        color: ['#ffffff'],
                        font: {
                            size: 20
                        }
                    }
                }
            }
        },

    });



</script>
</html>
