<template>
  <v-card height="200px">
    <div class="headline text-xs-center pa-5">
      </div>
    <v-bottom-nav  :value="true" :active.sync="e1" color="transparent">
      <v-btn flat color="teal" value="实验">
        <span>实验</span>
        <v-icon>edit</v-icon>
      </v-btn>
      <v-btn flat color="teal" value="项目">
        <span>项目</span>
        <v-icon>folder</v-icon>
      </v-btn>
      <v-btn flat color="teal" value="审批">
        <span>审批</span>
        <v-icon>comment</v-icon>
      </v-btn>
       <v-btn flat color="teal" value="我的">
        <span>我的</span>
        <v-icon>account_circle</v-icon>
      </v-btn>
    </v-bottom-nav>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      e1: "实验"
    };
  }
};
</script>