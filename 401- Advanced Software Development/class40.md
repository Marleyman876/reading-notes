# [NEXT Dynamic Routes](https://nextjs.org/learn/basics/dynamic-routes/page-path-external-data)

Here is some essential information you should know about dynamic routes.

Fetch External API or Query Database
Like getStaticProps, getStaticPaths can fetch data from any data source. In our example, getAllPostIds (which is used by getStaticPaths) may fetch from an external API endpoint:

export async function getAllPostIds() {
// Instead of the file system,
// fetch post data from an external API endpoint
const res = await fetch('..')
const posts = await res.json()
return posts.map(post => {
return {
params: {
id: post.id
}
}
})
}
Development v.s. Production
In development (npm run dev or yarn dev), getStaticPaths runs on every request.
In production, getStaticPaths runs at build time.
Fallback
Recall that we returned fallback: false from getStaticPaths. What does this mean?

If fallback is false, then any paths not returned by getStaticPaths will result in a 404 page.

If fallback is true, then the behavior of getStaticProps changes:

The paths returned from getStaticPaths will be rendered to HTML at build time.
The paths that have not been generated at build time will not result in a 404 page. Instead, Next.js will serve a “fallback” version of the page on the first request to such a path.
In the background, Next.js will statically generate the requested path. Subsequent requests to the same path will serve the generated page, just like other pages pre-rendered at build time.
If fallback is blocking, then new paths will be server-side rendered with getStaticProps, and cached for future requests so it only happens once per path.

This is beyond the scope of our lessons, but you can learn more about fallback: true and fallback: 'blocking' in the fallback documentation.

Catch-all Routes
Dynamic routes can be extended to catch all paths by adding three dots (...) inside the brackets. For example:

pages/posts/[...id].js matches /posts/a, but also /posts/a/b, /posts/a/b/c and so on.
If you do this, in getStaticPaths, you must return an array as the value of the id key like so:

return [
{
params: {
// Statically Generates /posts/a/b/c
id: ['a', 'b', 'c']
}
}
//...
]
And params.id will be an array in getStaticProps:

export async function getStaticProps({ params }) {
// params.id will be like ['a', 'b', 'c']
}
Take a look at the catch all routes documentation to learn more.

Router
If you want to access the Next.js router, you can do so by importing the useRouter hook from next/router.

404 Pages
To create a custom 404 page, create pages/404.js. This file is statically generated at build time.

// pages/404.js
export default function Custom404() {
return <h1>404 - Page Not Found</h1>
}
Take a look at our Error Pages documentation to learn more.

More Examples
We have created several examples to illustrate getStaticProps and getStaticPaths — take a look at their source code to learn more:

Blog Starter using markdown files (Demo)
WordPress Example (Demo)
DatoCMS Example (Demo)
TakeShape Example (Demo)
Sanity Example (Demo)
