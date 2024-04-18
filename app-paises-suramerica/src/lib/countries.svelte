<script>
    export let country;
    let p;

    const countries = {
        colombia: [
            "Colombia",
            "Bogotá",
            "51,52 millones",
            "Peso Colombiano",
            "1,142 millones km2",
            "flag_co.png",
        ],
        venezuela: [
            "Venezuela",
            "Caracas",
            "28,2 millones",
            "Bolivar",
            "916.445 km2",
            "flag_ve.png",
        ],
        ecuador: [
            "Ecuador",
            "Quito",
            "17,8 millones",
            "Dolar Estadounidense",
            "256.370 millones km2",
            "flag_ec.png",
        ],
        peru: [
            "Perú",
            "Lima",
            "33,72 millones",
            "Sol",
            "1.285,215 millones km2",
            "flag_pe.png",
        ],
        brasil: [
            "Brasil",
            "Brasilia",
            "214,3 millones",
            "Real",
            "8,5 millones km2",
            "flag_br.png",
        ],
        bolivia: [
            "bolivia",
            "la Paz",
            "12,22 millosnes",
            "Real",
            "1.099 millones km²",
            "Flag_of_Bolivia.svg.png",
        ],
        argentina: [
            "argentina",
            "buenos Aire",
            "46,23 millones",
            "Real",
            "8,5 millones km2",
            "flag_Ar.png",

        ]

    };

    p = countries[country];
</script>

<div class="main">
    <div class="col1">
        <img
            src="./src/assets/{p[5]}"
            alt="bandera_colombia"
            width="300"
            height="200"
        />
    </div>
    <div class="col2">
        <div class="linea"><strong>Pais:</strong>{p[0]}</div>
        <div class="linea"><strong>Capital:</strong>{p[1]}</div>
        <div class="linea"><strong>Población:</strong>{p[2]}</div>
        <div class="linea"><strong>Moneda:</strong>{p[3]}</div>
        <div class="linea"><strong>Extensión:</strong>{p[4]}</div>
    </div>
</div>

<style>
    .main {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-gap: 5px;
        grid-auto-rows: minmax(100px, auto);
        border-radius: 10px;
        border-color: rgb(186, 190, 182);
        border-width: 2px;
        margin: left;
        width: 650px;
        box-shadow: 5px 5px 5px ;
        margin-right: 5px;
        margin-bottom: 10px;
    }

    .col1 {
        grid-column: 1;
        grid-row: 1;
        margin: 5px;
        padding: 5px;
    }

    .col2 {
        grid-column: 2;
        grid-row: 1;
        margin: 5px;
        padding: 5px;
        border-color: black;
        width: max-content;
    }

    strong {
        color: blue;
        font-weight: bolder;
    }

    .linea {
        font-size: 20px;
        margin-bottom: 18px;
    }
</style>
