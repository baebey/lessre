<template>
    <Header></Header>
    <div class="container is-fluid mt-3" id="mali">
        <div class="notification has-background-white">
            <label class="label is-size-2 has-text-centered">My Assignment</label>
            <button @click="showModal" class="button is-info mr-5 is-pulled-right" id="mali">Add
                Assignment</button>


            <br><br><br>

            <div class="tile is-ancestor" style="margin-top: -30px;">
                <div class="tile is-vertical is-8">
                    <div class="tile">

                        <div class="tile is-parent is-vertical ml-4">
                            <article class="tile is-child notification has-background-white">
                                <p class="title is-size-4 has-text-black-bis ml-2">ยังไม่เริ่ม
                                    <span class="icon">

                                        <i class="fa-solid fa-question fa-shake"></i>

                                    </span>
                                </p>

                                <div class="box has-background-danger-light" v-for="nst in NotStarted" :key="nst.number">
                                    <label class="label is-size-5 ">{{ nst.asm_name }}</label>
                                    <label class="label is-size-6 has-text-grey">กำหนดส่ง : {{ nst.deadline }}</label>

                                    <span class="icon mt-1">

                                        <a @click="showEditModal" class="fa-regular fa-pen-to-square"></a>

                                    </span>

                                    <progress class="progress is-small is-danger mt-3" value="10" max="100"></progress>
                                </div>


                            </article>

                        </div>
                        <div class="tile is-parent">
                            <article class="tile is-child notification has-background-white">
                                <p class="title is-size-4 has-text-black-bis ml-2">กำลังทำ

                                    <span class="icon">

                                        <i class="fas fa-spinner fa-pulse"></i>

                                    </span>
                                </p>

                                <div class="box has-background-warning-light" v-for="wip in Doing" :key="wip.number">
                                    <label class="label is-size-5 ">{{ wip.asm_name }}</label>
                                    <label class="label is-size-6 has-text-grey">กำหนดส่ง : {{ wip.deadline }}</label>
                                    <span class="icon mt-1">
                                        <a @click="showEditModal" class="fa-regular fa-pen-to-square"></a>
                                    </span>
                                    <progress class="progress is-small is-warning mt-3" max="100"></progress>
                                </div>
                            </article>
                        </div>
                    </div>

                </div>
                <!-- งานเสร็จ -->
                <div class="tile is-parent">
                    <article class="tile is-child notification has-background-white">

                        <p class="title is-size-4 has-text-black-bis ml-2">งานเสร็จสิ้น
                            <span class="icon">


                                <i class="fa-solid fa-check fa-bounce"></i>

                            </span>
                        </p>

                        <div class="box has-background-success-light" v-for="fns in Finished" :key="fns.number">
                            <label class="label is-size-5 ">{{ fns.asm_name }}</label>
                            <label class="label is-size-6 has-text-grey">กำหนดส่ง : {{ fns.deadline }}</label>

                            <span class="icon mt-1">

                                <i class="fa-solid fa-crown"></i>

                            </span>

                            <progress class="progress is-small is-success mt-3" value="100" max="100"></progress>
                        </div>

                    </article>
                </div>
            </div>






        </div>
    </div>

    <!-- footer -->
    <Footer></Footer>

    <!-- modal add -->
    <div id="mali" class="modal has-background-white" :class="{ 'is-active': showModalFlag }">
        <div class="modal-background"></div>
        <div class="modal-card">
            <header class="modal-card-head ">
                <p class="modal-card-title is-size-3 ml-1 py-3" id="mali" ><strong>Add Assignment</strong></p>
                <button class="delete" aria-label="close" @click="cancelModal"></button>
            </header>
            <section class="modal-card-body">
                
                    <div class="field">
                        <label class="label is-size-5 is-pulled-left has-text-primary-dark">ชื่องาน/คำอธิบาย</label>
                        <div class="control">
                            <input class="input is-primary" type="text" placeholder="ชื่องานหรือคำอธิบายเกี่ยวกับงาน"
                                id="mali">
                        </div>
                    </div>

                    <div class="field">
                        <label class="label is-size-5 is-pulled-left has-text-link-dark">กำหนดส่ง</label>
                        <div class="control">
                            <input class="input is-link" type="date" placeholder="กำลังส่ง"
                                id="mali">
                        </div>
                    </div>

                    <div class="field">
                        <label class="label is-size-5 is-pulled-left has-text-info-dark">สถานะของงาน</label>
                        <br><br>
                        <div class="select is-info is-pulled-left" id="mali">
                            <select id="mali">
                                <option>สถานะของงาน</option>
                                <option>ยังไม่เริ่มทำ</option>
                                <option>กำลังทำ</option>
                                <option>งานเสร็จสิ้น</option>
                            </select>
                        </div>
                    </div>

            </section>
            <footer class="modal-card-foot">
                <button @click="okModal" class="button is-success" id="mali">Submit</button>
                <button @click="cancelModal" class="button is-danger" id="mali">Cancel</button>
                
            </footer>
        </div>
    </div>

    <!-- modal edit -->
    <div id="mali" class="modal has-background-white" :class="{ 'is-active': showEditModalFlag }">
        <div class="modal-background"></div>
        <div class="modal-card">
            <header class="modal-card-head ">
                <p class="modal-card-title is-size-3 ml-1 py-3" id="mali" ><strong>Edit Assignment</strong></p>
                <button class="delete" aria-label="close" @click="cancelModal"></button>
            </header>
            <section class="modal-card-body">
                
                    <div class="field">
                        <label class="label is-size-5 is-pulled-left has-text-primary-dark">ชื่องาน/คำอธิบาย</label>
                        <div class="control">
                            <input class="input is-primary" type="text" placeholder="ชื่องานหรือคำอธิบายเกี่ยวกับงาน"
                                id="mali">
                        </div>
                    </div>

                    <div class="field">
                        <label class="label is-size-5 is-pulled-left has-text-link-dark">กำหนดส่ง</label>
                        <div class="control">
                            <input class="input is-link" type="date" placeholder="กำลังส่ง"
                                id="mali">
                        </div>
                    </div>

                    <div class="field">
                        <label class="label is-size-5 is-pulled-left has-text-info-dark">สถานะของงาน</label>
                        <br><br>
                        <div class="select is-info is-pulled-left" id="mali">
                            <select id="mali">
                                <option>สถานะของงาน</option>
                                <option>ยังไม่เริ่มทำ</option>
                                <option>กำลังทำ</option>
                                <option>งานเสร็จสิ้น</option>
                            </select>
                        </div>
                    </div>

            </section>
            <footer class="modal-card-foot">
                <button @click="okModal" class="button is-success" id="mali">Submit</button>
                <button @click="cancelModal" class="button is-danger" id="mali">Cancel</button>
                
            </footer>
        </div>
    </div>
</template>

<script>
import Header from '../components/Header.vue'
import Footer from '../components/Footer.vue'
import Assignments from '../assets/json/jsonAssignment.json'
export default {
    name: 'AssignmentPage',
    el: "#modalAssignment",
    components: {
        Header,
        Footer
    },
    data() {
        return {
            data: Assignments,
            showModalFlag: false,
            showEditModalFlag: false,
            okPressed: false,


        }


    },
    methods: {
        showModal() {
            this.okPressed = false;
            this.showModalFlag = true;
        },
        showEditModal() {
            this.okPressed = false;
            this.showEditModalFlag = true;
        },
        okModal() {
            this.okPressed = true;
            this.showModalFlag = false;
            this.showEditModalFlag = false;
        },
        cancelModal() {
            this.okPressed = false;
            this.showModalFlag = false;
            this.showEditModalFlag = false;
        }
    },
    computed: {
        NotStarted: function () {
            return this.data.filter(data => data.asm_status === 'ยังไม่เริ่มทำ')
        },
        Doing: function () {
            return this.data.filter(data => data.asm_status === 'กำลังทำ')
        },
        Finished: function () {
            return this.data.filter(data => data.asm_status === 'เสร็จแล้ว')
        }
    }
}

</script>

<style>

</style>