<template>
  <section class="section">
    <div class="container">
      <div class="columns">
        <div class="column mr-5 px-0 py-0 box">
          <nav class="panel is-danger">
            <p class="panel-heading">
              Каталог
            </p>
            <ul>
              <li v-for="category in categories" :key="category._id">
                <a class="panel-block is-active">
                  <span class="panel-icon">
                    <fa icon="shopping-bag" aria-hidden="true" />
                  </span>
                  {{ category.name }}
                </a>
              </li>
            </ul>
            <a class="panel-block is-active">
              <span class="panel-icon">
                <fa icon="shopping-bag" aria-hidden="true" />
              </span>
              Активный блок
            </a>
            <a class="panel-block">
              <span class="panel-icon">
                <fa icon="tshirt" aria-hidden="true" />
              </span>
              пасивный блок
            </a>
          </nav>
        </div>

        <div class="column is-9 box">
          <p class="title">
            Content
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import categoriesQuery from '~/apollo/queries/category/categories.graphql'
export default {
  name: 'ASidebarContent',
  data () {
    return {
      categories: '',
      query: ''
    }
  },
  apollo: {
    categories: {
      prefetch: true,
      query: categoriesQuery
    }
  },
  computed: {
    filteredList () {
      return this.categories.filter((category) => {
        return category.name.toLowerCase().includes(this.query.toLowerCase())
      })
    }
  }
}
</script>

<style lang="scss" scoped>
.panel-block {
  padding: 12px;
}
</style>
