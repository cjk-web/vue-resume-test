<template>
    <div class="sidebar">
        <h1>Skills</h1>

        <div class="skill-group" v-for="skillGroup in skills" :key="skillGroup.id">
            <h2>{{skillGroup.category}}</h2>
            <div class="skill-tags">
                <span v-for="skill in skillGroup.skills" :key="skill.id">{{skill.title}}</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Skills",
    props: ["skills"]
}
</script>

<style lang="sass" scoped>
    .sidebar 
        width: 15%
        background: #2d4059
        color: #fff
        padding: 2em
        display: flex
        flex-direction: column
        h1, h2
            margin-bottom: .5em
        .skill-group 
            margin-bottom: 2em
            .skill-tags
                display: flex
                flex-wrap: wrap
                span
                    font-weight: bold
                    background: rgba(0, 0, 0, .3)
                    padding: .5em
                    margin: .1em
        
</style>