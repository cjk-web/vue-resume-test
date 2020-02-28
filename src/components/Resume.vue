<template>
    <div class="flex-grow-container">
        <div class="resume">
            <h1>{{person.name.first}} {{person.name.last}}</h1>
            <h2>{{person.job}}</h2>

            <h3 class="section-heading">Profile</h3>
            <p>{{person.profile}}</p>

            <h3 class="section-heading">Experience</h3>
            <div class="experience" v-for="job in person.experience" :key="job.id">
                <h3> {{job.position}} at {{job.company}} </h3>
                <h4>{{job.duration.start}}-{{job.duration.end}}</h4>
                <ul>
                    <li v-for="task in job.responsibilities" :key="task.id">{{task.details}}</li>
                </ul>
            </div>
            <div class="skills">
                <h3>Skills</h3>
                <ul>
                    <li v-for="skill in person.skills" :key="skill.id">{{skill.details}}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "resume",
    props: ["person"]
}
</script>

<style lang="sass" scoped>
    .flex-grow-container
        flex: 1 1 auto
    .resume
        padding: 2em 5em
        font-size: 22px
        max-width: 36em
        width: 100%
        margin: 0 auto

        h1
            border-bottom: 1px solid #000
        h2
            margin-bottom: 1em 
        .section-heading
            margin-bottom: .3em
        p
            margin-bottom: 2em
        .experience
            padding: 0 1em   
        .experience, .skills 
            margin-bottom: 2em 
            h4
                margin-bottom: .5em
            ul 
                padding: 0 2em
        .skills h3
            margin-bottom: .5em
</style>