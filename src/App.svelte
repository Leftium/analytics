<script lang="coffeescript">
  export name = null

  ## Counter sample based on https://svelte.dev/tutorial/reactive-statements
  count = 0
 
  ## Mark Svelte reactive CoffeeScript statements by escaping out to JavaScript.
  ## (Normally CoffeeScript syntax is incompatible with Svelte Reactive statements.)

  `$: {`  ## Start Svelte reactive block.
  if count >= 10
    alert 'count is dangerously high!'
    count = 9
  `}`     ## End reactive block.

  handleClick = () ->
    count += 1
</script>

<template lang="pug">
  div.grid-wrapper
    header
      div HEADER
    aside
      div ASIDE
    main
      h1 Hello {name}!
      p.
        Visit the #[a(href='https://svelte.dev/tutorial') Svelte tutorial]
        to learn how to build Svelte apps.

      // How reactive buttons are done in Svelte + Pug.
      // Note CoffeeScript cannot be used here.
      button(on:click='{handleClick}') Clicked {count} {count === 1 ? 'time' : 'times'}
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
    background-color: #4c7c9b;
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
</style>
