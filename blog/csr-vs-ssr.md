---
path: /posts/blog
date: 2019-12-24T18:36:40.791Z
title: CSR vs SSR
---
After the initial HTML and CSS loads the browser requests the rest of the application which comes in a JS file. While this JS is being loaded and parsed, the page will be blank. The content will be viewable and intractable once the JS file has been parsed.

[![Client Side Rendering Diagram](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/raw/master/content/posts/client-side-rendering-vs-server-side-rendering/csr.png)](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/blob/master/content/posts/client-side-rendering-vs-server-side-rendering/csr.png)

The advantage of Client Side Rendering (CSR) is once the page loads all subsequent navigation within the site will be fast as no more pages needed to be loaded from the server unlike a Multi Page Application.

One disadvantage is the user of the site will have to wait a long time until he/she sees anything meaningful on the screen during the first render. This can take a long time depending of the size of the app, speed of the connection and the power of the device the site os being viewed in (especially in low end mobile devices).

Another disadvantage comes when looking at Search Engine Optimization (SEO). Web crawlers might not parse the JavaScript and load the content, so they might only see an empty page.

JavaScript Single Page Application Frameworks like[React](https://reactjs.org/)and[Angular](https://angular.io/)are client side rendered by default.

## [](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/blob/master/content/posts/client-side-rendering-vs-server-side-rendering/index.mdx#enter-server-side-rendering)Enter Server Side Rendering

We can solve these issues by using Server Side Rendering. SSR is rendering the app to a string (HTML) in the server itself and sending it to the browser. This takes the work of rendering from the client to the server. So when the browser receives the initial HTML file there is content for the user to see unlike a CSR site where the entire JS file needs to be downloaded and parsed before something meaningful can be shown on screen. The site becomes interactive once the JS file has been downloaded and parsed.

[![Server Side Rendering Diagram](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/raw/master/content/posts/client-side-rendering-vs-server-side-rendering/ssr.png)](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/blob/master/content/posts/client-side-rendering-vs-server-side-rendering/ssr.png)

The downside of using just SSR is that it makes navigation within the site slow as each page needs to be rendered and fetched from the server. This also increases the load on the server.

## [](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/blob/master/content/posts/client-side-rendering-vs-server-side-rendering/index.mdx#is-there-a-way-to-use-both-csr-and-ssr-as-needed)Is there a way to use both CSR and SSR as needed?

CSR makes out app faster and more interactive. SSR can speed up the first render of the site and improve SEO. We don't to sacrifice the features of one by going fully with the other. Instead we can use an Universal Web App.

## [](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/blob/master/content/posts/client-side-rendering-vs-server-side-rendering/index.mdx#universal-web-app)Universal Web App

Universal Web Apps combine the best of the both Client Side Rendering and Server Side Rendering. In an Universal Web App, the initial render will be done in the server, and once the page loads client side rendering will take over. This makes sure that we have good SEO, a quick first render and speed when browsing in the app.

There are a couple of frameworks which allow us to build UWAs quickly.

* [Next.js](https://nextjs.org/)- A framework to build Universal Web Apps with[React](https://reactjs.org/)
* [Nuxt.js](https://nuxtjs.org/)- A framework to build Universal Web Apps with[Vue.js](https://vuejs.org/)

## [](https://github.com/akhila-ariyachandra/akhilaariyachandra.com/blob/master/content/posts/client-side-rendering-vs-server-side-rendering/index.mdx#conclusion)Conclusion

I hope you found this useful on learning about Server Side Rendering and Client Side Rendering.😊
