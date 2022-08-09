<script>
	import PostCard from './PostCard.svelte';
    export /**
* @type {any[]}
*/
     let posts=[];
</script>

<section class=" dark:bg-gray-800 dark:text-gray-100">       
    <div class="container max-w-6xl p-6 mx-auto space-y-6 sm:space-y-12">
      <span class="  ">
        <!-- <Featured /> -->
      </span>

      
        <div class="grid justify-center grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
          {" "}
          {#each posts as post}            
            <PostCard post={post}/>

          {/each}
          
        </div>{" "}
       

      <div class="flex justify-center">
        <button
          type="button"
          class="px-6 py-3 text-sm rounded-md hover:underline dark:bg-gray-900 dark:text-gray-400"
        >
         
        </button>
      </div>
    </div>
  </section>