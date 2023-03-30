<template>
    <div class="box has-background-light pb-6" style="margin: 120px;">

        <label class="label is-size-2 ">Assignment</label>
        <label class="label is-size-4 ">add or update</label>

        <div class="field">
            <label class="label is-size-5 is-pulled-left has-text-primary-dark">ชื่องาน/คำอธิบาย</label>
            <div class="control">
                <input class="input is-primary" type="text" placeholder="ชื่องานหรือคำอธิบายเกี่ยวกับงาน"
                    style="font-family: 'Mali', cursive;">
            </div>
        </div>

        <div class="field">
            <label class="label is-size-5 is-pulled-left has-text-link-dark">กำหนดส่ง</label>
            <div class="control">
                <input class="input is-link" type="date" placeholder="กำลังส่ง" style="font-family: 'Mali', cursive;">
            </div>
        </div>

        <div class="field">
            <label class="label is-size-5 is-pulled-left has-text-info-dark">สถานะของงาน</label>
            <br><br>
            <div class="select is-info is-pulled-left" style="font-family: 'Mali', cursive;">
                <select style="font-family: 'Mali', cursive;">
                    <option style="font-family: 'Mali', cursive;">สถานะของงาน</option>
                    <option style="font-family: 'Mali', cursive;">ยังไม่เริ่มทำ</option>
                    <option style="font-family: 'Mali', cursive;">กำลังทำ</option>
                    <option style="font-family: 'Mali', cursive;">งานเสร็จสิ้น</option>
                </select>
            </div>
        </div>

        <br>

        <div class="buttons is-pulled-right mt-3">
            <button class="button is-success" style="font-family: 'Mali', cursive;">Submit</button>
            <button class="button is-danger" style="font-family: 'Mali', cursive;">Cancel</button>
        </div>
        <br>

    </div>
</template>

<script>
export default {
    name: 'manage_assignment',

}

</script>

<style>

.box {
    font-family: 'Mali', cursive;
}
</style>