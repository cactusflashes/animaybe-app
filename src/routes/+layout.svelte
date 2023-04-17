<script>
  import { fade } from 'svelte/transition'
  import { fly } from 'svelte/transition'
  import { cubicIn, cubicOut } from 'svelte/easing'


  export let data
</script>

<style>
  @import '/Users/jas2598/Desktop/sunday /my-app/src/app.css';

  @import url('https://fonts.googleapis.com/css2?family=Crimson+Text:ital,wght@0,400;0,600;0,700;1,400;1,600;1,700&family=Plus+Jakarta+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300&family=Poppins:ital,wght@0,100;0,200;0,400;0,500;0,700;1,300&display=swap');
</style>


{#key data.pathname}
  <div
      in:fly={{ x: -30, duration: 500, delay: 500 }} 
      out:fly={{ x: -30, duration: 500 }}>
    <slot />
  </div>
{/key}