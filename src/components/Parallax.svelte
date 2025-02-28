<script lang="ts">
    let scroll: number;
</script>

<svelte:window bind:scrollY={scroll}/>

<p>{scroll}</p>

<div class="container cont2">
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.5 + 300}px, 0)">je suis parallaxé</div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.3 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.8 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.2 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.5 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.7 + 300}px, 0)"></div>
</div>

<div class="container cont2">
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.5 + 300}px, 0)">je suis parallaxé</div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.3 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.8 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.2 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.5 + 300}px, 0)"></div>
    <div class="box" style:transform="translate3d(0, {scroll * -1 * 0.7 + 300}px, 0)"></div>
</div>

<style>
    .box{
        width: 100px; height: 100px;
        background-color: blue;

        margin: 20px;
    }

    .container {
        height: 100vh;
        background-color: aqua;
        display: flex;
        flex-direction: row;
        align-items: flex-end; justify-content: center;

        margin: 20px 0;
    }
</style>