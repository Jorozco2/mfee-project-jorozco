 <template>
  <div class="container mt-5">
      <div class="d-flex justify-content-between">
        <h1 class="display-6">Categories</h1>
        <button class="btn btn-outline-success" data-bs-toggle="modal" data-bs-target="#createCategoryModal">Add Category</button>
      </div>

      <hr />
      <li v-for="category in categories" :key="category._id">
        {{ category.name }}
      </li>
  </div>
  <CategoryForm/>
 </template>
<script>
import CategoryForm from './CategoryForm.vue';

export default {
  components: {
    CategoryForm
  },
  data(){
        return {
            categories: [
            {
                _id:'2',
                name: 'Category 1'
            } ,  
            {
                _id:'3',
                name: 'Category 2'
            } ,  
            {
                _id:'4',
                name: 'Category 3'
            } ,   
            {
                _id:'5',
                name: 'Category 4'
            } ,  
            ]
        }
    },
    buildCategories(){
        this.categoriies = [
            {
                _id:'1',
                name: 'All'
            },
            ...this.categoriies
        ]

        this.categoriies = this.categoriies.map((categoriies) => ({
            ...categoriies,
            active: category.name ==='All'
        })
        )
    }
};
</script>