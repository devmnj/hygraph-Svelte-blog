<script context="module">
    import {GraphQLClient} from "graphql-request";

    export async function load() {
        const graphcms = new GraphQLClient(
            'https://api-ap-south-1.hygraph.com/v2/cl5uo7orr3kf801t8d4ld7hoe/master',
            {
                headers: {},
            }
        )
        const data = await graphcms.request(
            `query {
  blogposts {
    title
    catgory
    publishedAt
    slug
    summary
    image {
      url
      fileName
    }
  }
}`
        );


        return {
            props: {
                posts: data,
            },
        }

    }
</script>
<script>

    import PostGrid from "../components/postGrid.svelte";
    export let posts;
</script>
<div>

    <PostGrid posts="{posts.blogposts}"/>

</div>