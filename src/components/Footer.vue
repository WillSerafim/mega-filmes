<template>
  <div>
    <footer>
      <ul class="footer-menu">
        <li><a href="/">Home</a></li>
        <li><a href="/about">Sobre</a></li>
      </ul>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style>
  footer {
    background: #222;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    color: #fff;
    bottom: 0;
    position: fixed;
    width: 100%;
  }

  .footer-menu li {
    list-style: none;
    padding: 10px;
  }

  .footer-menu a {
    color: var(--color-light);
  }

</style>
