<script>
    import Timer from './components/Timer.svelte'
    import HowTo from './components/HowTo.svelte'
    
    let audio

    const timerEnds = (e) => {
        audio.play()
    }
</script>

<style>
    h1, h3 {
        text-align: center;
    }
</style>


<h1>Handwashing App</h1>

<Timer on:end={timerEnds} />

<HowTo />

<h3>
    <a href="http://www.who.int/gpsc/clean_hands_protection/en">Picture source</a>
</h3>
<h3>
    <a href="http://freesound.org/people/metrostock99/sounds/345086/">Sound source</a>
</h3>

<audio bind:this={audio}>
    <source src="/build/sound.wav" />
</audio>