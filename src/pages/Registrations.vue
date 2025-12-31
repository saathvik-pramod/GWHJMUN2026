<script setup>
const display = "active" //pending, active, elapsed
</script>

<template>
    <main>
        <div v-if="display=='pending'">
            <div class="pending">
                <h1>Registrations opening on 9th January.</h1>
                Due to unforeseen circumstances, the registration date has been pushed back. Read <a href="https://docs.google.com/document/d/1HJREGolCF2uzeF8WSqsMbv8kPYXZYY-3NFDP2BHgzgk/edit?usp=sharing" target="_blank">this notice</a> for more information.
            </div>
        </div>
        <div v-if="display=='active'" class="active-btn"> 
            <h1>Registrations</h1>
            <p>Registrations will close once requisite numbers are reached, so register quickly!</p>
            <div class="registration-links">
                <a href="https://paytm.me/PYTMPS/aOsoFPP" target="_blank" class="reglink">
                    <h3>GWHJMUN-IB</h3>
                    <p>Rs. 1200/- per student</p>
                </a>
                <a href="https://paytm.me/PYTMPS/PtTmFPP" target="_blank" class="reglink">
                    <h3>GWHJMUN-ICSE</h3>
                    <p>Rs. 1200/- per student</p>
                </a>
                <a href="https://paytm.me/PYTMPS/FMDBFPP" target="_blank" class="reglink">
                    <h3>GWHJMUN-BGT</h3>
                    <p>Rs. 1200/- per student</p>
                </a>
                <a href="https://paytm.me/PYTMPS/eKbyFPP" target="_blank" class="reglink">
                    <h3>GWHJMUN-External Registration</h3>
                    <p>Rs. 1200/- per student</p>
                </a>
            </div>
            <div class="reg-note">
                <div><h2>Note:</h2></div>
                <div>1. Due to a character limit in the email entry field, simply enter as many characters as will fit. Our registrations department will make the necessary changes. </div>
                <div>2. If your section is not present in the dropdown, add it in as a clarification in the MUN experience part of the form. </div>
                <div>3. Confirmation mails are currently not being sent - rest assured that if the PayTM screen is displayed, the payment has gone through. If you have not received your allocation past January 10th, feel free to reach out.</div>
            </div>
        </div>
        <div v-if="display=='elapsed'" class="pending">
            <h1>Registrations have closed.</h1>
            <p>Thank you for the overwhelming response.</p>
            <p>Allocations are out!</p>
        </div>
    </main>
</template>

<style scoped>
main {
    padding: 10px;
}

.registration-links {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    margin-top: 20px;
}

.reglink {
    border: 2px solid #3b3b3b;
    border-radius: 15px;
    padding: 20px;
    text-decoration: none;
    color: #fff;
    font-size: 1.1em;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    background: #282828;
    width: 250px;
}

.reglink > h3 {
    font-size: 1.5em;
    margin-bottom: 10px;
}

.reglink > p {
    font-size: 1.2em;
    color: #aaa;
}

.pending {
    text-align: center;
    padding: 250px 0;
    font-size: 1.25em;
}

.pending > h1 {
    font-size: 2.5em
}

.active-btn {
    padding: 100px 0;
    text-align: center;
}

.reg-note {
    text-align: center;
    padding: 20px 10%;
}

.reg-note > div {
    padding: 5px 0;
    font-size: 1.1em;
}
</style>
