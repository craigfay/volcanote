
<script>
  import Menu from "$components/Menu.svelte";
  import NavBar from "$components/NavBar.svelte";

  let isOpen = false;
  let toggleMenu = () => isOpen = !isOpen;
  let closeMenu = () => isOpen = false;
</script>


<div class="max-h-screen flex flex-col fixed">
  <Menu {isOpen} closeBehavior={closeMenu}/>
  <NavBar {isOpen} {toggleMenu}/>
  <div class="overflow-y-scroll overflow-x-hidden"><slot /></div>
</div>
