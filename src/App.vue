<template>
    <div class="app">
      <my-dialog :show="dialogVisible">
      <post-form></post-form>
      </my-dialog>
      <header class="header">
        <a href="#"><img src="@/components/UI/logo.svg" alt="Логотип сайта" class="logo"></a>
        <button class="enter--button" @click="showDialog">Вход</button>
      </header>
      <body class="body">
        <h1>Мои заметки</h1>
        <p>Не забывай о важном, храни его в облаке.</p>
      </body>
    </div>
</template>

<script>
import PostForm from '@/components/PostForm';
export default {
  components: {
    PostForm
  },
  data() {
    return {
      dialogVisible: false,
    }
  },
  methods: {
    showDialog() {
      this.dialogVisible = true;
    }
  }
}


</script>

<style>
*{
  background-color: #0A1F38;
}
.body {
  background-image: url('@/components/UI/Group.svg');
  background-repeat: no-repeat;
  position: fixed;
  top: 100px;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 2;
}
.header {
  display: flex;
  justify-content: space-between;
  z-index: 1;
}
.enter--button{
  background-color: #B1C909;
  font-size: 20px;
  border-radius: 32px;
  border: 0;
  width: 144px;
  height: 56px;
  }
  .enter--button::before{
    content: "";
    display: inline-block;
    background:no-repeat url("@/components/UI/Vector.svg");
    width: 32px;
    height: 32px;
  }
  .enter--button:hover {
    background-color: #B1C909;
  }
</style>