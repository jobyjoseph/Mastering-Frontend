Getting Started with Nextjs - https://nextjs.org/learn/basics/getting-started

```javascript
// We just need 3 packages to start
npm install --save react react-dom next
```

Navigate Between Pages - https://nextjs.org/learn/basics/navigate-between-pages

```javascript
import Link from 'next/link';

//...

//Inside component JSX
<Link href="/about">
  <a>About Page</a>
</Link>
```

Using Shared Components - https://nextjs.org/learn/basics/using-shared-components

```javascript
// Layout JSX
const Layout = props => (
  <div style={layoutStyle}>
    <Header />
    {props.children}
  </div>
);

//...

// Using Layout
export default function Index() {
  return (
    <Layout>
      <p>Hello Next.js</p>
    </Layout>
  );
}
```

Create Dynamic Pages - https://nextjs.org/learn/basics/create-dynamic-pages

```javascript
// Read query string
import { useRouter } from 'next/router';

//...

// Inside component
const router = useRouter();

//...

// Inside Component JSX
<h1>{router.query.title}</h1>
```

Clean urls with Dynamic Routing - https://nextjs.org/learn/basics/clean-urls-with-dynamic-routing

```javascript
// Reading params from url. Inside pages/p/[id].js
import { useRouter } from 'next/router';

//...

// Inside component
const router = useRouter();

//...

// JSX
<h1>{router.query.id}</h1>
```

```javascript
// Creating dynamic links
<Link href="/p/[id]" as={`/p/${props.id}`}>
  <a>{props.id}</a>
</Link>
```

Fetching Data for Pages - https://nextjs.org/learn/basics/fetching-data-for-pages

```javascript
// Fetching API data from remote
import fetch from "isomorphic-unfetch";

//...

// Using static getInitialProps to make API fetch
Index.getInitialProps = async function() {
  const res = await fetch("https://api.tvmaze.com/search/shows?q=batman");
  const data = await res.json();

  console.log(`Show data fetched. Count: ${data.length}`);

  return {
    shows: data.map(entry => entry.show)
  };
};

//...

// Inside JSX
{props.shows.map(show => (
  <li key={show.id}>
    <Link href="/p/[id]" as="/p/${show.id}">
      <a>{show.name}</a>
    </Link>
  </li>
))}
```

Styling Components - https://nextjs.org/learn/basics/styling-components

```javascript
// Inside JSX
<Layout>
  <h1>Title of Blog</h1>
  
  {//...}
  
  <style jsx>
  {`
    h1 {
      color: green;
    }
  `}
  </style>
</Layout>

// styled-jsx will not be applied for nested components
```

```javascript
// global attribute to apply styles even for nested components
<style jsx global>{`
    h1,
    a {
        font-family: "Arial";
    }
`}</style>
```

Deploying Nextjs App - https://nextjs.org/learn/basics/deploying-a-nextjs-app

Export into a Static HTML App - https://nextjs.org/learn/excel/static-html-export

```javascript
// File: next.config.js
module.exports = {
  exportPathMap: function() {
    return {
      "/": { page: "/" } // Exporting only index.js
    };
  }
};

// File: package.json
//...
"scripts": {
  "export": "next export"
}
//...

// export command creates html files in /out directory
```

Use Next.js with TypeScript - https://nextjs.org/learn/excel/typescript

Lazy Loading Modules - https://nextjs.org/learn/excel/lazy-loading-modules
