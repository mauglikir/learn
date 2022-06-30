<template>
    <div @click="checkClick" ref="invoiceWrap" class="invoice-wrap flex flex-column">
        <form @submit.prevent="submitForm" class="invoice-content">
            <h1>New Invoice</h1>

            <!-- Bill Form -->
            <div class="bill-form flex flex-column">
                <h4>Bill Form</h4>
                <div class="input flex flex-column">
                    <label for="billerStreetAddress">Street Address</label>
                    <input v-model="billerStreetAddress" required type="text" id="billerStreetAddress">
                </div>
                <div class="location-details flex">
                    <div class="input flex flex-column">
                        <label for="billerCity">City</label>
                        <input v-model="billerCity" required type="text" id="billerCity">
                    </div>
                    <div class="input flex flex-column">
                        <label for="billerZipCode">Zip Code</label>
                        <input v-model="billerZipCode" required type="text" id="billerZipCode">
                    </div>
                    <div class="input flex flex-column">
                        <label for="billerCoutry">Coutry</label>
                        <input v-model="billerCoutry" required type="text" id="billerCoutry">
                    </div>
                </div>
            </div>
            <!-- End Bill Form -->
            <!-- Bill To -->
            <div class="biil-to flex flex-column">
                <h4>Bill To</h4>
                <div class="input flex flex-column">
                    <label for="clientName">Client`s Name</label>
                    <input v-model="clientName" required type="text" id="clientName">
                </div>
                <div class="input flex flex-column">
                    <label for="clientEmail">Client`s Email</label>
                    <input v-model="clientEmail" required type="text" id="clientEmail">
                </div>
                <div class="input flex flex-column">
                    <label for="clientStreetAddress">Street Address</label>
                    <input v-model="clientStreetAddress" required type="text" id="clientStreetAddress">
                </div>
                <div class="location-details flex">
                    <div class="input flex flex-column">
                        <label for="clientCity">City</label>
                        <input v-model="clientCity" required type="text" id="clientCity">
                    </div>
                    <div class="input flex flex-column">
                        <label for="clientZipCode">Zip Code</label>
                        <input v-model="clientZipCode" required type="text" id="clientZipCode">
                    </div>
                    <div class="input flex flex-column">
                        <label for="clientCountry">Coutry</label>
                        <input v-model="clientCountry" required type="text" id="clientCountry">
                    </div>
                </div>
            </div>
            <!-- End Bill To -->
 

        </form>
    </div>
</template>

<script>
export default {
    name:"invoiceModal",
    data() {
        return {
            billerStreetAddress: null,
            billerCity: null,
            billerZipCode: null,
            billerCoutry: null,
            clientName: null,
            clientEmail: null,
            clientStreetAddress: null,
            clientCity:null,
            clientZipCode: null,
            clientCountry: null,
            invoiceDateUnix: null,
            invoiceData: null,
            paymentTerms: null,
            paymentDueDateUnix: null,
            paymentDueDate: null,
            productDescription: null,
            productDueDate: null,
            invoicePending: null,
            invoiceDraft: null,
            invoiceItemList: [],
            invoiceTotal:0,
        }
    },

}
</script>

<style>

</style>