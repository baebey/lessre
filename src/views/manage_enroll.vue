<template>
    <div class="box has-background-danger-light" style="margin: 120px;">
        <label class="label is-size-2 my-5 has-text-centered">Enrolled</label>

        <div class="field is-grouped px-6 mb-6">

            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">รหัสวิชา</label>
                <input class="input" type="number" placeholder="e.g. 06016322" style="font-family: 'Mali', cursive;">
            </div>

            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">ชื่อวิชา</label>
                <input class="input" type="text" placeholder="e.g. Web Programming" style="font-family: 'Mali', cursive;">
            </div>

            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">จำนวนหน่วยกิต</label>
                <input class="input" type="number" placeholder="e.g. 3" style="font-family: 'Mali', cursive;">
            </div>

        </div>

        <div class="field is-grouped px-6 mb-6">


            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">วันสอบกลางภาค</label>
                <input class="input" type="date" style="font-family: 'Mali', cursive;">
            </div>

            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">วันสอบปลายภาค</label>
                <input class="input" type="date" style="font-family: 'Mali', cursive;">
            </div>

        </div>

        <hr class="has-background-grey-light">

        <div class="field is-grouped px-6 mb-6">

            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">เวลาเรียน</label>
                <input class="input" type="text" placeholder="e.g. 09.00-13.00" style="font-family: 'Mali', cursive;">
            </div>

            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">ห้องเรียน</label>
                <input class="input" type="text" placeholder="e.g. L-305" style="font-family: 'Mali', cursive;">
            </div>

            <div class="control is-expanded">
                <label class="label is-pulled-left is-size-5">เทอมที่ลง</label>
                <br>
                <div class="select is-fullwidth">
                    <select style="font-family: 'Mali', cursive;">
                        <option style="font-family: 'Mali', cursive;">เลือกเทอมที่ลงเรียน</option>
                        <option style="font-family: 'Mali', cursive;">ปี 1/1</option>
                        <option style="font-family: 'Mali', cursive;">ปี 1/2</option>
                        <option style="font-family: 'Mali', cursive;">ปี 2/1</option>
                        <option style="font-family: 'Mali', cursive;">ปี 2/2</option>
                        <option style="font-family: 'Mali', cursive;">ปี 3/1</option>
                        <option style="font-family: 'Mali', cursive;">ปี 3/2</option>
                        <option style="font-family: 'Mali', cursive;">ปี 4/1</option>
                        <option style="font-family: 'Mali', cursive;">ปี 4/2</option>
                    </select>
                </div>
            </div>

        </div>

        <div class="buttons is-pulled-left ml-6">
            <button class="button is-danger is-outlined" style="font-family: 'Mali', cursive;">Delete</button>
        </div>

        <div class="buttons is-pulled-right mt-2">
            <button class="button is-success" style="font-family: 'Mali', cursive;">Submit</button>
            <button class="button is-danger" style="font-family: 'Mali', cursive;">Cancel</button>
        </div>

        <br><br>

        

    </div>
</template>

<script>
export default {
    name: 'manage_enroll',

}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Mali:wght@500&display=swap');

.box{
    font-family: 'Mali', cursive;
}

</style>