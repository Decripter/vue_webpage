<template>
    
    <div class="tile is-parent">
        <article class="tile is-child box" :class="[themeIsDark[0] ? '' : 'has-background-dark']" >
            <p class="title" :class="[themeIsDark[0] ? '' : 'has-text-white']">{{ themeIsDark[0] }}</p>
            <p class="subtitle" :class="[themeIsDark[0] ? '' : 'has-text-white']">{{ content }}</p>
        </article>
        
    </div>
</template>

<script>
export default {
name: 'boxContent', 
props:['themeIsDark', 'title', 'content']
}
</script>

<style>

</style>