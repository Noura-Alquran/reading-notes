# Readings: React 3 Summary :
### Assets
* Static assets like images can be under the 'public' directory.
* Next.js can handle Images with the 'next/image' which simplify for resizing & optimizing images.

- **Example**:
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
* With this you can set the height, width and alt all within a component.
### Metadata

* import Head from 'next/head'
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
* This is an easy way to put all the 'Head' information in a function called FirstPost.
### CSS
* You can write css within a React component.

* **Example**:
```
<style jsx>{`
  …
`}</style>
```
* Next.js has built-in support for CSS and Sass which allows you to import .css and .scss files.
* classnames is a simple library that lets you toggle class names easily. You can install it using npm install classnames or yarn add classnames.
* Next.js allows to import Sass using both the .scss and .sass extensions. You can use component-level Sass via CSS Modules and the .module.scss or .module.sass extension.
* To install sass:
```
npm install sass
```
