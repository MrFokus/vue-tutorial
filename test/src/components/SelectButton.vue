<template>
    <div class="btn" @click="showList">
        <img src="@/assets/img/filter.svg" />
        <p>Фильтры</p>

        <ul v-if="statusShow">
            <li v-for="(item, index) in list" :key="index" @click="select($event, item)">{{ item }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            list: [
                'По умолчанию', 'Сначала новые', 'Сначала старые'
            ],
            statusShow: false
        }
    },
    methods: {
        showList() {
            this.statusShow = !this.statusShow
        },
        select(event, el){
            event.stopPropagation()
            this.$emit('select', el)
        }
    }
}
</script>

<style lang="scss" scoped>
.btn {
    position: relative;
    padding: 8px 16px;
    background: #FFFFFF;
    border: 1px solid #EAECF0;
    border-radius: 8px;

    img {
        margin-right: 8px;
    }
}

ul {
    position: absolute;
    top: 100%;
    left: 0;
    width: 320px;
    flex-direction: column;
    padding: 6px;
    background: #FFFFFF;

    box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.08);
    border-radius: 8px;
    gap:8px;
}
</style>