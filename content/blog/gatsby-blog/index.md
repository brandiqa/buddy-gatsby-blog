---
title: "Gatsby Release 2.0"
date: "2019-07-22"
---

We’re incredibly pleased to announce the 2nd major release of Gatsby!

Gatsby is a blazing fast modern website and app generator. Thousands of developers use Gatsby to create amazing blogs, apps, marketing and ecommerce sites, documentation, and more!

- Facebook uses Gatsby to power the [React docs and blog!](https://reactjs.org/)
- Nike built their [“Just Do It” campaign site](https://justdoit.nike.com/) with Gatsby to tell the stories of athletes with incredible dreams
- [Airbnb shows off their engineering and data science projects](https://airbnb.io/) on their site built with Gatsby

V2.0.0 is the result of months of hard work by the Gatsby core team and 315 contributors. Thank you!

This release focuses on performance and developer experience. Highlights include:

- Reduced build times by up to 75%
- Shrunk JavaScript client runtime by 31%
- Upgraded Gatsby’s core dependencies to their latest versions: webpack 4, Babel 7, React 16.5

## Rapidly growing ecosystem

We’ve grown a lot in the last year since the Gatsby v1 release.

- We’ve reached 1100 contributors (up from 198)
- Now merging ~90 PRs / week (up from ~50)
- Gatsby was downloaded 4+ million times
- 457 Gatsby plugins have now been published to npm
- 550,000 people visited our website
- 15,500 people starred our GitHub Repo going from 10k to 25.5k stars
- [Several core Gatsby contributors started a company](https://www.gatsbyjs.org/blog/2018-05-24-launching-new-gatsby-company/). We raised \$3.7 million to support Gatsby OSS and create cloud tools to help teams build and deploy amazing Gatsby sites

## What’s new in v2

### Faster site builds

We focused heavily on improving build speeds for v2 and are very pleased to see large build speed improvements across many parts of the build pipeline.

Most sites should see large speed increases, up to 75% reduction.

Improvements include:

- [Reduced memory usage while server rendering pages](https://github.com/gatsbyjs/gatsby/pull/4912#issuecomment-381407967)
- webpack 4 includes many speedups to JavaScript and CSS bundling
- React 16 improved SSR performance by 3-4x
- [My “hulksmash” PR includes many small fixes to refactor slow algorithms](https://github.com/gatsbyjs/gatsby/pull/6226)
- [Use all available cores when server rendering pages](https://github.com/gatsbyjs/gatsby/pull/6417)

There’s still more to be done to improve build performance! Our goal is to help Gatsby scale to sites of any size. More on this in the coming months.

### Shrunk JavaScript client runtime by 31%

We shrunk the core JavaScript shipped with every Gatsby site by 31%! Less JavaScript means faster sites!

Gatsby v1’s core JavaScript was 78.5kb and **v2 is 53.9kb** (both gzipped sizes).

The reductions are largely due to the hard work by libraries we rely on.

The React team decreased their code size by 30% from React 15 to 16 (49.8kb to 34.8kb gzipped)

We switched routers from react-router to @reach/router which brought a ~70% smaller bundle (18.4kb to 6kb gzipped).

### React 16

We upgraded from React 15 to 16. React 16 was a huge release for the React ecosystem with support for fragments, error boundaries, portals, support for custom DOM attributes, improved server-side rendering, and reduced file size.
