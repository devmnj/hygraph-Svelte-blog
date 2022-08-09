<script>
 export let post= {}
 $:{
 console.log(post);}
</script>
<!-- {JSON.stringify(post)} -->
<div class="container bg-gray-700">
<a
        href={`/post/${post.slug}`}
        rel="noopener noreferrer"
        class="max-w-sm mx-auto group hover:no-underline focus:no-underline dark:bg-gray-900"
      >
        <img
          role="presentation"
          class="object-cover w-full rounded h-44 dark:bg-gray-500"
          src={post.image.url} alt="posy"
        />
        <div class ="flex justify-between ">
          <span class="mt-3 mx-3 text-gray-600">{post.publishedAt}</span>
<!--          <span class="mt-3 mx-3 text-gray-600">   Reactj       </span>-->
        </div>

        <div class ="px-6 py-2 space-y-2 ">
            <h3 class ="text-2xl font-semibold group-hover:underline group-focus:underline">
              { post.title || "In usu laoreet repudiare legendos"}
            </h3>        
            <p class="align-baseline">{ post.summary}</p>
          </div>
       
      </a>
    </div>

    <style>
      .container{
        width: 400px;
        height: 400px;
      }
      
      </style>