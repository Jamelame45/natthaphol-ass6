<template>
    <div>
        <Navbar />

        <section class="about">

            <h1 class="heading"> about <span>me</span> </h1>

            <div class="row">

                <div class="info-container">

                    <h1>personal info</h1>

                    <div class="box-container">

                        <div class="box">
                            <h3> <span>name : </span>{{name}}</h3>
                            <h3> <span>age : </span>{{age}}</h3>
                            <h3> <span>email : </span>{{email}}</h3>
                            <h3> <span>address : </span>{{address}}</h3>
                        </div>

                        <div class="box">
                            <h3> <span>freelance : </span> available </h3>
                            <h3> <span>skill : </span> Full Stack Engineer </h3>
                            <h3> <span>experience : </span> 6 years </h3>
                            <h3> <span>language : </span> thai </h3>
                        </div>

                    </div>

                    <a href="/profilewithcss/files/resume.pdf" class="btn"> download CV <i class="fas fa-download"></i>
                    </a>

                </div>

                <div class="count-container">

                    <div class="box">
                        <h3>5+</h3>
                        <p>years of experience</p>
                    </div>

                    <div class="box">
                        <h3>10+</h3>
                        <p>happy clients</p>
                    </div>

                    <div class="box">
                        <h3>20+</h3>
                        <p>project completed</p>
                    </div>

                    <div class="box">
                        <h3>5+</h3>
                        <p>Certificates</p>
                    </div>

                </div>

            </div>

        </section>

        <!-- about section ends -->

        <!-- skills section starts  -->

        <section class="skills">

            <h1 class="heading"> <span>my</span> skills </h1>

            <div class="box-container">
                <div class="box">
                    <img src="images/icon-1.png">
                    <h3>html</h3>
                </div>
                <div class="box">
                    <img src="images/icon-2.png">
                    <h3>css</h3>
                </div>
                <div class="box">
                    <img src="images/icon-3.png">
                    <h3>javascript</h3>
                </div>
                <div class="box">
                    <img src="images/icon-4.png">
                    <h3>sass</h3>
                </div>
                <div class="box">
                    <img src="images/icon-5.png">
                    <h3>angular</h3>
                </div>
                <div class="box">
                    <img src="images/icon-6.png">
                    <h3>react.js</h3>
                </div>
            </div>

        </section>

        <!-- skills section ends -->

        <!-- education section starts  -->

        <section class="education">

            <h1 class="heading"> <span>my</span> experience </h1>

            <div class="box-container">

                <div class="box" v-for="e in study" :key="e.years">
                    <i class="fas fa-briefcase"></i>
                    <span>{{e.years}}</span>
                    <h3>{{e.school}}</h3>
                    <p>{{e.jobs}}</p>
                </div>

            </div>

        </section>
    </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
export default {
    components: { Navbar },
    data() {
        return {
            name: 'Natthaphol lapchai',
            age: '20',
            email: 'Natthaphol.lapc@bu.ac.th',
            address: 'Pathum Thani, Thailand 12120',
            study: [{
                years: '2015-2017',
                school: 'Phutthaisong School',
                jobs: 'student',
            }, {
                years: '2017-2020',
                school: 'Phuttthaisong School',
                jobs: 'student',
            }, {
                years: '2020-2022',
                school: 'Bangkok University',
                jobs: 'student',
            }]
        }
    }
}
</script>

<style>

</style>