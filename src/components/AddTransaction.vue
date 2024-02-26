<template>
    <h3>Add new transaction</h3>
    <form id="form">
        <div class="form-control">
            <label for="text">Transaction</label>
            <input type="text" id="text" placeholder="Enter details">
        </div>
        <div class="form-control">
            <label for="amount">
                Cost 
                <br />
                <span class="pos"> Income + </span>
                <span class="neg"> Expense - </span>
                </label>
            <input type="text" id="amount" placeholder="Enter amount">
        </div>
        <button class="btn">Add Transaction</button>
    </form>
</template>

