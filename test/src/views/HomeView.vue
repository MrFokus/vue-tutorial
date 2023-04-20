<template>
  <div class="main-container container">
    <SelectButton @select="select"/>
    <div class="container-cards">
      <Card v-for="(item, index) in listCard" :key="index" class="card-item" :title="item.title" :creater="item.creater"
        :date="item.date" />
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue';
import SelectButton from '@/components/SelectButton.vue';
export default {
  name: 'HomeView',
  components: {
    Card,
    SelectButton
  },
  data() {
    return {
      listCard: [
        {
          title: 'Название карточки',
          creater: 'Кобзев Андрей',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки с названием, которое занимает две строки, а может занимать более двух, но не более трёх',
          creater: 'Кобзев Андрей',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
        {
          title: 'Название карточки',
          creater: 'Дмитриев Степан',
          date: 'Последние изменения 2 дня назад'
        },
      ]
    }
  },
  methods:{
    select(el){
      console.log(el, 'vvv')
    }
  }
}
</script>

<style lang="scss" scoped>
.main-container {

  margin-top: 30px;
  flex-wrap: wrap;
}

.container-cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  width: 100%;
  gap: 24px;
  margin-top: 34px;
}

.card-item {
  width: 100%;
  height: 200px;
}
</style>
