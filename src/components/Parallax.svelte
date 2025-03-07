<script lang="ts">
    import fond from "$lib/illustrations/illustration_01/Illu01.jpg";
    import layer9 from "$lib/illustrations/illustration_01/layer9-1.png";
    import layer6 from "$lib/illustrations/illustration_01/layer6-1.png";
    import layer5 from "$lib/illustrations/illustration_01/Layer 5.png";
    import layer3 from "$lib/illustrations/illustration_01/Layer 3.png";
    import layer2 from "$lib/illustrations/illustration_01/Layer 2.png";
    import nuage from "$lib/illustrations/illustration_01/Nuages.png";
    import papillons1 from "$lib/illustrations/illustration_01/Papillons.png";
    import papillons2 from "$lib/illustrations/illustration_01/Papillons-2.png";

    let scroll: number;
</script>

<svelte:window bind:scrollY={scroll}/>

<!-- 
Pour gérer le scroll avec parallax :

Le calcul prend la var "scroll" qui correspond au nombre de pixel scrollé sur l'axe des Y, multiplié par,
-1 qui inverse l'accéleration de l'image pour la faire aller vers le haut au scroll, multiplié par,
0.1 qui manipule la vitesse à laquelle le défilement à lieu (0<loin<1, 1=pov, 1<proche),
il faut une valeut à ajouter pour définir le point de hauteur au scroll sur lequel à lieu l'alignement
des layers (à définir en fonction de la position de l'illustration dans la page web et donc de la variable scroll)
-->

<div class="illustration illu01">
    <img class="layer left layer2 z6" src="{layer2}" alt="Premier plan" style:transform="translate3d(0, {scroll * -1 * 0.70 + 1200}px, 0)">
    <img class="layer z6 papillons1" src="{papillons1}" alt="Papillons" style:transform="translate3d(0, {scroll * -1 * 0.60 - 50}px, 0)">
    <img class="layer left layer3 z5" src="{layer3}" alt="Roche à Gauche" style:transform="translate3d(0, {scroll * -1 * 0.45 + 100}px, 0)">
    <img class="layer right layer5 z4" src="{layer5}" alt="roche à droite" style:transform="translate3d(0, {scroll * -1 * 0.35}px, 0)">
    <img class="layer layer2 fond z3" src="{layer6}" alt="Layer principal, personnage qui dort" style:transform="translate3d(0, {scroll * -1 * 0.25}px, 0)">
    <img class="layer z3 papillons2" src="{papillons2}" alt="Papillons" style:transform="translate3d(50%, {scroll * -1 * 0.30 - 450}px, 0)">
    <img class="layer nuage z2" src="{nuage}" alt="Nuage" style:transform="translate3d(-50%, {scroll * -1 * 0.15 - 550}px, 0)">
    <img class="layer fond z1" src="{layer9}" alt="Fond d'illustration montagne" style:transform="translate3d(0, {scroll * -1 * 0.1}px, 0)">
</div>

<style>

    .illustration{
        width: 100%;
        height: 100vh;
        position: relative;
        top: 700px;
    }
    .layer{
        position: absolute;
        bottom: 0;
        
        &.layer5{
            width: 1100px;
        }
        &.layer3{
            width: 95%;
        }
        &.layer2{
            width: 100%;
        }
    }

    .papillons1{
        right: 25%;
    }
    .papillons2{
        left: 38%;
    }
    .nuage{
        left: 55%;
    }

    .fond{
        position: absolute;
        width: 100%;
        bottom: 0;
        
    }

    .right{
        right: 0;
    }
    .left{
        left: 0;
    }

    .z-1{
        z-index: -1;
    }
    .z-2{
        z-index: -2;
    }
    .z-3{
        z-index: -3;
    }
    .z-4{
        z-index: -4;
    }
    .z1{
        z-index: 1;
    }
    .z2{
        z-index: 2;
    }
    .z3{
        z-index: 3;
    }
    .z4{
        z-index: 4;
    }
    .z5{
        z-index: 5;
    }
    .z6{
        z-index: 6;
    }
    .z7{
        z-index: 7;
    }
    .z8{
        z-index: 8;
    }
</style>