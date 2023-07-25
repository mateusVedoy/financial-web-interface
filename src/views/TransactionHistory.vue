<template>
    <TransactionHistoryBoardComponent :transactionHistoryValues="histories"/>
</template>
<script>
import TransactionHistoryBoardComponent from '@/components/TransactionHistoryBoard.vue'
export default {
    name: 'TransactionHistoryView',
    components: {
        TransactionHistoryBoardComponent
    },
    data() {
        let histories = [];
    },
    methods: {
        async getTransactionHistories() {
            this.histories = [{
			"id": 1,
			"type": "input",
			"amount": 1200.0,
			"date": "2023-04-09",
			"hour": "12:55:00"
            },
            {
                "id": 2,
                "type": "input",
                "amount": 1200.0,
                "date": "2023-04-09",
                "hour": "12:55:00"
            },
            {
                "id": 3,
                "type": "output",
                "amount": 2000.0,
                "date": "2023-04-09",
                "hour": "12:55:00"
            }];
        }
    },
    async beforeMount() {
        await this.getTransactionHistories();
    }
}
</script>