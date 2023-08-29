<template>
  <NuxtLayout>
    <div>

      <section>
        <form @submit.prevent="addTodo">
          <input v-model="newTodo" name="newTodo" autocomplete="on"/>
          <button>予定を追加</button>
        </form>
      </section>

      <section>
        <ul>
          <li v-for="(todo ,index) in todos" :key="todo">
            <span class="taskliner">{{ todo }}</span>
            <button @click="deleteTodo(index)">削除</button>
          </li>
        </ul> 
      </section>

      <section class="clear">
        <button @click="clearTodo">Clear</button>
      </section>
      
    </div>
  </NuxtLayout>
</template>
<script setup>
  // cookieの保持
  const todos = useCookie(
    'todos',
    {
      default: () => []
    }
  )
  // Todoの追加
  const newTodo = ref('')
  function addTodo() {
    if(newTodo.value.length >= 1) {
      todos.value.push(newTodo.value)
    }
    newTodo.value = ''
  }
  // Todoの削除
  function deleteTodo(index) {
    todos.value.splice(index, 1)
  }
  // Todoの全クリア
  function clearTodo() {
    todos.value = []
  }
</script>
