<template>
  <h1>Nuxt 3 ToDoアプリ</h1>
  <div class="contents">
    <slot />
  </div>
</template>

<style>
  body {
    font-family: "Meiryo","Hiragino Kaku Gothic ProN","MS PGothic",sans-serif;
    margin: 0;
    color: #333;
  }
  h1 {
    margin-top: 0;
    background-color: #4b545c;
    color: #fff;
    padding: 0.7rem 1rem;
  }
  .contents {
    padding: 1rem;
  }
  button {
    padding: 0.7rem 1rem;
    border: none;
    border-radius: 7px;
    font-weight: bold;
    font-family: inherit;
    cursor: pointer;
    font-size: 16px;
    font-weight: 600;
  }
  .clear button {
    background-color: #4cdd99;
    color: white;
  }
  .clear button:hover {
    /* background-color: #4cdd99; */
    opacity: 0.5;
  }
  form {
    display: grid;
    grid-template-columns: auto 25%;
    gap: 10px;
  }
  input {
    padding: 0.7rem;
    border: 1px solid #dddddd;
    border-radius: 7px;
    font-size: inherit;
    color: inherit;
  }
  form > button {
    background-color: #2b75e3;
    color: #fff;
  }
  form > button:hover {
    /* background-color: #2b75e3; */
    opacity: 0.5;
  }
  ul {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 2rem;
    padding: 0;
  }
  ul li {
    display: grid;
    grid-template-columns: auto 25%;
    align-items: center;
    gap: 10px;
  }
  ul li button {
    background-color: #dd3e8b;
    color: #fff;
  }
  ul li button:hover {
    /* background-color: #dd3e8b; */
    opacity: 0.5;
  }
  .contents > button {
    display: block;
    width: 100%;
    margin-top: 2rem;
    background-color: #e6e6e6;
  }
  .taskliner {
    padding: 0.7rem 1rem;
    border-radius: 7px;
    font-size: 16px;
    font-weight: 600;
    background-color: #f4e986;
  }
</style>