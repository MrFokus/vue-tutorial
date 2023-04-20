<template>
    <div class="card">
        <h3>{{ title }}</h3>
        <div>
            <p>Создал: {{ creater }}</p>
            <p>{{ date }}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
        },
        creater: {
            type: String
        },
        date: {
            type: String
        }
    }
}
</script>

<style lang="scss" scoped>
.card {
    flex-direction: column;
    justify-content: space-between;
    background: #FFFFFF;
    border: 1px solid #EAECF0;
    box-shadow: 0px 1px 3px rgba(16, 24, 40, 0.1), 0px 1px 2px rgba(16, 24, 40, 0.06);
    border-radius: 12px;
    padding: 24px;

    div {
        flex-direction: column;
    }

    h3 {
        font-size: 16px;
        line-height: 28px;
    }

    h3,
    p {
        text-align: left;
    }

    p:first-child {
        margin-bottom: 8px;
    }
}</style>