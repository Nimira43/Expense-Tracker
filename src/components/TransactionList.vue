<template>
    <h3>History</h3>
    <ul id="list" class="list">
        <li 
            v-for="transaction in transactions"
            :key="transaction.id"
            :class="transaction.amount < 0 ? 'minus' : 'plus '"
        >
            {{ transaction.text }}<span>£{{ transaction.amount }}
            </span>
            <button class="delete-btn">x</button>
        </li>
    </ul>
</template>

<script>
    export default {
        setup() {
            const transactions = [
                { id: 1, text: 'Bus', amount: -32.00 },
                { id: 2, text: 'Wages', amount: 1532.00 },
                { id: 3, text: 'Pet Plan', amount: -10.00 },
                { id: 4, text: 'Udemy', amount: -69.90 },
            ]
            return {
                transactions,
            }
        }
    }
</script>