<template>
  <PostDetailView />
  <!-- <PostDetailView /> -->
</template>

<script>
import PostDetailView from './modules/posts/views/PostDetailView.vue';
import PostView from './modules/posts/views/PostView.vue';
import CategoryView from './modules/categories/views/CategoryView.vue';
import SignUpView from './modules/auth/views/SignUpView.vue';
import LoginView from './modules/auth/views/LoginView.vue';

export default {
  components: {
    PostView,
    CategoryView,
    SignUpView,
    LoginView,
    PostDetailView
  }
};
</script>
