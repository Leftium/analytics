<script lang="coffeescript">

</script>

<template lang="pug">
  div.grid-wrapper
    header
      div.logo
        img(src='/img/header-logo.png' alt='logo')
        span &nbsp;Analytics
      img(src='/img/header-menu.png' alt='menu')
    aside
      div ASIDE
    main
      iframe(title='datagrid' width="100%" height="100%" frameborder="0" scrolling="no" src="https://onedrive.live.com/embed?resid=E583A51B21433AB8%213559&authkey=%21AANta_hOSePl5O8&em=2&wdInConfigurator=True")
    footer
      div FOOTER
</template>

<style>
  .grid-wrapper {
    height: 100%;
    display: grid;
    grid-template-columns: 300px 1fr;
    grid-template-rows: min-content auto min-content;
    background-color: #ffafb0;
  }
  aside {
    grid-column: 1/2;
    grid-row: 2/3;
    background-color: #004c6d;
  }
  header {
    grid-column: 1/3;
    grid-row: 1/2;
    background-color: #474747;
  }
  footer {
    grid-column: 1/3;
    grid-row: 3/4;
    background-color: #86b0cc;
  }
  main {
    grid-column: 2/3;
    grid-row: 2/3;
    background-color: #c1e7ff;
  }

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    display: flex;
    align-items: center;
  }

  header span {
    font-size: xx-large;
    font-weight: 380;
    text-transform: uppercase;
    color: white;
  }
</style>
