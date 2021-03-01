<script lang="coffeescript">
  view = 'detailed'

</script>

<template lang="pug">
  div.grid-wrapper
    header
      div.logo
        img(src='/img/header-logo.png' alt='logo')
        span &nbsp;Analytics
      img(src='/img/header-menu.png' alt='menu')
    aside
      div
        button Import
        span Last imported 3 days ago.
      button Lifetime: Aug 1, 2019 - Feb 28, 2021 &#9660;
      fieldset
        legend View
        div: label
          input(type='radio' bind:group='{view}' value='simple')
          span &nbsp;Simple
        div: label
          input(type='radio' bind:group='{view}' value='detailed')
          span &nbsp;Detailed
        div: label
          input(type='radio' bind:group='{view}' value='custom')
          span &nbsp;Custom
      fieldset
        legend Sort
        div: select
          option Offer
          option Lander
          option Name
        div: select
          option Offer
          option(selected) Lander
          option Name
        div: select
          option Offer
          option Lander
          option(selected) Name
        button Default Sort
      fieldset
        legend Filters
        label Must contain:
        input.instant-search(type=text)
        button Reset All Filters
      fieldset
        legend Selected
        div: button Relative Growth Chart
        div: button Unselect All
      div.timezone-currency
        span
          label Timezone&nbsp;
          select
            option PST
        span
          label Currency&nbsp;
          select
            option USD


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
    background-color: #fefefe;
  }
  header {
    grid-column: 1/3;
    grid-row: 1/2;
    background-color: #474747;
  }
  footer {
    display: none;
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

  aside {
    padding: 0.2em;
  }

  header span {
    font-size: xx-large;
    font-weight: 380;
    text-transform: uppercase;
    color: white;
  }

  aside button,
  aside fieldset select,
  aside input.instant-search {
    width: 100%;
  }

  .timezone-currency {
    margin: 0.4em;
    display: flex;
    justify-content: space-around;
  }
</style>
