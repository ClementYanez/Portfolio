<script>
    import Header from "../components/Header.svelte";
    import Parallax from "../components/Parallax.svelte";
    import TextOver from "../components/TextOver.svelte";
</script>
    
    
    <Header />
    
    <TextOver />

    <div class="part1">
        <Parallax/>
        <div class="fondgradient"></div>
    </div>


    
    
    <style>
        .fondgradient{
        background: rgb(212,232,247);
        background: linear-gradient(0deg, rgba(212,232,247,1) 0%, rgba(85,182,255,1) 100%);
        position: sticky;
        bottom: 0;
        height: 1000px;
        }

    </style>