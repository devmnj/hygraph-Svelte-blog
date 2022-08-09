<script>
import Nav from "../components/nav.svelte";

    import "../app.css";
  </script>
  
  <div class="bg-gray-800">
    <Nav />
    <div class=" dark:text-white dark:bg-gray-800 items-center overflow-auto h-screen">
      <slot/>
    </div>
  </div>
 