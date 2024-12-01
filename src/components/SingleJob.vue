<template>
    <div class="job-details">
        <h2 class="job-title">{{job.job_title}}</h2>
        <p class="job description"><b>Description:</b> {{job.description}}</p>
        <p class="job location"><b>Location:</b>  {{job.location}}</p>
        <p class="job department"><b>Department:</b> {{job.department}}</p>
        <p class="job salary"><b>Salary:</b> {{job.salary}}</p>
        <p class="job role"><b>Role:</b> {{job.role}}</p>
    </div>
</template>

<script>
    export default{
        name: 'SingleJob',
        props:{
            job: Object
        }
    }
</script>

<style scoped>
    h4{
        margin: 2px;
    }
    div{
        color: black;
        padding: 1em;
    }
    .job-details{
        border: 2px solid #000;
        color: black;
        background-color: silver;
    }
    .job-title{
        text-align: center;
        text-transform: uppercase;
        margin-bottom: 1rem;
        font-size: 1.1rem;
        font-weight: bold;
    }
    .job{
        line-height: 1.5rem;
    font-size: 15px;
    text-align: justify;
    }
    .description{
        color: black;
    }
    
</style>