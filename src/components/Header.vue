<template>
  <div>
    <header>
      <div class="header-brand">
        Mega filmes HD  2.0
      </div>
      <ul class="header-menu">
        <li><a href="/">Home</a></li>
        <li><a href="/about">Sobre</a></li>
      </ul>
    </header>
  </div>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style>
  :root {
    --color-light: #fff;
  }

  header {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    height: 70px;
    background-color: #222;
    padding: 10px;
  }

  .header-brand {
    display: flex;
    color: var(--color-light);
  }

  .header-menu {
    list-style: none;
    display: flex;

  }

  .header-menu li {
    display: inline;
  }

  .header-menu li a{
    color: var(--color-light);
    text-decoration: none;
    padding-left: 10px;
  }
</style>>
