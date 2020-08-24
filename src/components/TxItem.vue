<template>
    <tr>
        <td>{{ transaction.age }}</td>
        <td><a :href="transaction.link">{{ transaction.hash }}</a></td>
        <td>{{ transaction.fee }}</td>
        <td>{{ transaction.in }}/{{ transaction.out }}</td>
        <td>{{ transaction.size }}</td>
    </tr>
</template>

<script>
export default {
    name: 'TxItem',
    props: ["transaction"]
}
</script>
