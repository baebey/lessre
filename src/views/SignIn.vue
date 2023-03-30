<template>
    <form id="mali" class="box has-background-link-light mx-6 my-6 px-6 py-6">
        <span class="icon">
            <a @click="backHome" class="fas fa-home"></a>
        </span>
        <label class="label is-size-2 has-text-centered">Sign In</label>
        <label class="label is-size-4 has-text-centered">Welcome to lessre!</label>
        <!-- รหัสนศ -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">รหัสนักศึกษา</label>
            <div class="control">
                <input class="input" type="number" placeholder="รหัสนักศึกษาของคุณ" id="mali">
            </div>
        </div>
        <!-- อีเมลล์ -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">อีเมลล์</label>
            <div class="control">
                <input class="input" type="email" placeholder="email@example.com" id="mali">
            </div>
        </div>
        <!-- รหัสผ่าน -->
        <div class="field">
            <label class="label is-size-6 is-pulled-left">รหัสผ่าน</label>
            <div class="control">
                <input class="input" type="password" placeholder="********">
            </div>
        </div>
        <div class="has-text-centered">
            <button @click="signIn" class="button is-info mt-1" id="mali">Sign In!</button>
        </div>
        
    </form>
</template>

<script>
export default {
    name: 'SignIn',
    methods: {
        signIn() {
            alert("Sign in!")
            this.$router.push({ name: "Home" })
            
        },
        backHome() {
            this.$router.push({ name: "Home" })
        },
    }
   
}

</script>
