## NextJs

#### Assets
Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

The public directory is also useful for robots.txt, Google Site Verification, and any other static assets. Check out the documentation for Static File Serving to learn more.

```
<img src="/images/profile.jpg" alt="Your Name" />
```
```
import Image from 'next/image'

const YourComponent = () => (
  <Image
    src="/images/profile.jpg" // Route of the image file
    height={144} // Desired size with correct aspect ratio
    width={144} // Desired size with correct aspect ratio
    alt="Your Name"
  />
)
```
#### Metadata
What if we wanted to modify the metadata of the page, such as the <title> HTML tag?

<title> is part of the <head> HTML tag, so let's dive into how we can modify the <head> tag in a Next.js page.

Open pages/index.js in your editor and find the following lines
  
```
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```
Notice that <Head> is used instead of the lowercase <head>. <Head> is a React Component that is built into Next.js. It allows you to modify the <head> of a page.

You can import the Head component from the next/head module.

Adding Head to first-post.js
We haven't added a <title> to our /posts/first-post route. Let's add one.

Open the pages/posts/first-post.js file and add an import for Head from next/head at the beginning of the file:
```
import Head from 'next/head'
```
Then, update the exported FirstPost component to include the Head component. For now, we‘ll add just the title tag:
```
export default function FirstPost() {
  return (
    <>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </>
  )
}
```
Try accessing http://localhost:3000/posts/first-post. The browser tab should now say “First Post”. By using your browser’s developer tools, you should see that the title tag is added to <head>.

#### CSS Styling
As you can see, our index page (http://localhost:3000) already has some styles. If you take a look at pages/index.js, you should see code like this:
```
<style jsx>{`
  …
`}</style>
```
This page is using a library called styled-jsx. It’s a “CSS-in-JS” library — it lets you write CSS within a React component, and the CSS styles will be scoped (other components won’t be affected).

Next.js has built-in support for styled-jsx, but you can also use other popular CSS-in-JS libraries such as styled-components or emotion.

Writing and Importing CSS
Next.js has built-in support for CSS and Sass which allows you to import .css and .scss files.

Using popular CSS libraries like Tailwind CSS is also supported.

In this lesson, we’ll talk about how to write and import CSS files in Next.js. We’ll also talk about Next.js’s built-in support for CSS Modules and Sass. Let’s dive in!
