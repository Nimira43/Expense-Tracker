<template>
    <h3>Add new transaction</h3>
    <form id="form" @submit.prevent="onSubmit">
        <div class="form-control">
            <label for="text">Transaction</label>
            <input type="text" id="text" v-model="text" placeholder="Enter details">
        </div>
        <div class="form-control">
            <label for="amount">
                Cost 
                <br />
                <span class="pos"> Income + </span>
                <span class="neg"> Expense - </span>
                </label>
            <input type="text" id="amount" v-model="amount" placeholder="Enter amount">
        </div>
        <button class="btn">Add Transaction</button>
    </form>
</template>

<script setup>
    import { ref } from 'vue'
    import { useToast } from 'vue-toastification'

    const text = ref('')
    const amount = ref('')
    const toast = useToast()

    const onSubmit = () => {
        if (!text.value || !amount.value) {
            toast.error('Require Transaction and Cost ')
        }
        console.log(text.value, amount.value)    
    }
</script>

