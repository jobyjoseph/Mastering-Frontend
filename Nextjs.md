Getting Started with Nextjs - https://nextjs.org/learn/basics/getting-started

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
