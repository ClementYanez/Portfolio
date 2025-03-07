<script>

</script>

<header>
    <div>
        <ul>
            <div class="elem"></div>
            <div class="elem"></div>
            <div class="elem"></div>
            <div class="elem"></div>
            <div class="elem"></div>
        </ul>
    </div>
</header>

<style>
    div{
        position: fixed;
        top: 0;
        z-index: 999;
        width: 100%;
        height: 100px;
    }

    ul{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 0 20%;

        .elem{
            position: relative;
            height: 50px;
            width: 50px;
            background-color: white;
        }
    }
</style>