<template>
<div id="app">
    <div>
        <h1 class="text-center" style="color: #cc6699"><b>View Title</b></h1>
        <!-- start slide carousel insearch-->
        <div>
            <div id="carouselExampleCaptions" class="carousel slide mj" data-ride="carousel">
                <ol class="carousel-indicators">
                    <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
                    <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
                    <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
                </ol>
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img src="./assets/img/4.jpg" height="500px" class="d-block w-100" />
                        <div class="carousel-caption d-none d-md-block">
                            <h5>First slide</h5>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <img src="./assets/img/5.jpg" height="500px" class="d-block w-100" />
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Second slide</h5>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <img src="./assets/img/6.jpg" height="500px" class="d-block w-100" />
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Third slide</h5>
                        </div>
                    </div>
                </div>
                <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="sr-only">Previous</span>
                </a>
                <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="sr-only">Next</span>
                </a>
            </div>
            <br />
        </div>
        <!-- end slide carousel-->

        <!-- รูป + ลงคพแนน -->
        <div class="container border-1 shadow">
            <h1 class="text-center" style="color: #cc6699"><b>Vote pictures</b></h1>
            <br />
            <div class="row">
                <div class="col-md-7 mb-3">
                    <img class="bd" src="./assets/img/top.jpg" width="400px" />
                    <h4>no.1</h4>
                </div>
                <br />
                <div class="col-md">
                    <counter @cc="sum1" />
                    <p class="fn">count: {{ total1 }}</p>
                </div>
            </div>

            <hr />

            <div class="row">
                <div class="col-md-7 mb-3">
                    <img class="bd" src="./assets/img/1.jpg" width="400px" />
                    <h4>no.2</h4>
                </div>
                <div class="col-md">
                    <counter @cc="sum2" />
                    <p class="fn">count: {{ total2 }}</p>
                </div>
            </div>

            <hr />

            <div class="row">
                <div class="col-md-7 mb-3">
                    <img class="bd" src="./assets/img/2.jpg" width="400px" />
                    <h4>no.3</h4>
                </div>
                <div class="col-md">
                    <counter @cc="sum3" />
                    <p class="fn">count: {{ total3 }}</p>
                </div>
            </div>
        </div>

        <br />
        <!-- รูป + ลงคพแนน -->
    </div>
</div>
</template>

<script>
import counter from "@/components/counter.vue";

export default {
    name: "App",
    components: {
        counter,
    },

    data: function () {
        return {
            total1: 0,
            total2: 0,
            total3: 0,
        };
    },

    methods: {
        sum1(counterVavue1) {
            this.total1 = counterVavue1;
        },
        sum2(counterVavue2) {
            this.total2 = counterVavue2;
        },
        sum3(counterVavue3) {
            this.total3 = counterVavue3;
        },
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

.bg-img1 {
    background-color: gray;
}

.bd {
    border: 3px solid black;
}

.bg-comment {
    background-color: lightcyan;
}

.fn {
    font-size: 20px;
    color: rgb(75, 50, 168);
    margin-top: 10px;
}

.mj {
    margin-bottom: 200px;
}

h4 {
    font-size: 20px;
    color: rgb(75, 50, 168);
    margin-top: 10px;
}
</style>
