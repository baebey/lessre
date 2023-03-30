<template>
    <form id="mali" class="box has-background-link-light mx-6 my-6 px-6 py-6">
        <span class="icon">
            <a @click="backHome" class="fas fa-home"></a>
        </span>
        <label class="label is-size-2 has-text-centered	">Create Account</label>
        <label class="label is-size-4 has-text-centered	">lessre ให้ความสำคัญในความปลอดภัยของข้อมูลของนักศึกษา</label>
        <!-- ชื่อจริง -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">ชื่อ</label>
            <div class="control">
                <input class="input" type="text" placeholder="ชื่อของคุณ" id="mali" v-model="fname">
            </div>
        </div>
        <!-- นามสกุล -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">นามสกุล</label>
            <div class="control">
                <input class="input" type="text" placeholder="นามสกุลของคุณ" id="mali" v-model="lname">
            </div>
        </div>
        <!-- รหัสนศ -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">รหัสนักศึกษา</label>
            <div class="control">
                <input class="input " type="number" placeholder="รหัสนักศึกษาของคุณ" id="mali" v-model="idStudent">
            </div>
        </div>
        <!-- อีเมลล์ -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">อีเมลล์</label>
            <div class="control">
                <input class="input " type="email" placeholder="email@example.com" id="mali" v-model="email">
            </div>
        </div>
        <!-- รหัสผ่าน -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">รหัสผ่าน</label>
            <div class="control">
                <input class="input " type="password" placeholder="********" v-model="password">
            </div>
        </div>
        <div class="has-text-centered">
            <button @click="signUp" class="button is-info mt-1 has-text-centered" id="mali">Sign
                Up!</button>
        </div>
    </form>
</template>

<script>
export default {
    name: 'SignUp',
    data() {
        return {
            fname: null,
            lname: null,
            idStudent: null,
            email: null,
            password: null,
            info: [],
        }
    },
    methods: {
        signUp() {
            
                
                // this.info.push(this.fname);
                // this.info.push(this.lname);
                // this.info.push(this.idStudent);
                // this.info.push(this.email);
                
                // localStorage.setItem("info", JSON.stringify(this.info));
                // this.info = localStorage.getItem("info");
                // alert(JSON.parse(this.info));
                this.$router.push({ name: "Home" })
            
        },
            backHome() {
                this.$router.push({ name: "Home" })
            },
        }
    }
    


</script>

