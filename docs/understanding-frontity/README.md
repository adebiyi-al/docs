# 📃 About Frontity

## What is Frontity?

Frontity is a free and open source framework. It enables you to easily build a **React-based frontend** for a [**headless \(or decoupled\) WordPress**](https://www.elegantthemes.com/blog/wordpress/headless-wordpress) site. Your WordPress site serves its data via the [**REST API**](https://developer.wordpress.org/rest-api/), and the frontend that you build with Frontity consumes this data and renders it in the browser as a SPA \(Single Page Application\) which you can configure and style to your liking.

The above approach, as exemplified by Frontity, has many advantages. But in order to build a site in this way without Frontity there are a lot of things that developers need to learn and configure: _bundling_, _transpiling_, _routing_, _server rendering_, _retrieving data from WordPress_, _managing state_, or _managing CSS_, among many others.

Next.js and Gatsby.js are two great React frameworks that can work with WordPress in this way but none of them is exclusively focused on WordPress. Therefore, there’s still some complex configuration and additional tooling that the developer has to do.

Frontity, on the other hand, is an opinionated framework based on React and focused on WordPress. It aims to make everything simpler, even for developers who are not familiar with React:

* **Focused on WordPress**: each part of the framework has been simplified and optimized to be used with WordPress.
* **Opinionated framework**: developers don’t need to figure out or make decisions about what tools to use for things like CSS or State Management.

This means that everything is ready-to-go out of the box, so to speak, so that you can jump straight in and start creating an amazing new site with WordPress and React right away.

## **An alternative rendering engine for WordPress**

Frontity can also be described as an alternative rendering engine for WordPress.

Traditionally WordPress generates HTML using a theme based on **PHP** template files.

When the [**REST API**](https://developer.wordpress.org/rest-api/) was merged into core in WordPress 4.7, developers were no longer limited to the PHP rendering engine. They could query WordPress for the stored content which WordPress then sent in JSON format. The developer could then use it wherever and however they wanted. This opened up a new world of possibilities for web developers.

One of those possibilities is to create frontend sites based on React. That’s where Frontity comes into play.

## **Why WordPress and React?**

As at time of writing \(April 2020\), WordPress powers [35% of all the sites](https://w3techs.com/technologies/details/cm-wordpress) on the internet. Its market share has been growing over the last few years and it shows no sign of slowing down.

![](https://w3techs.com/diagram/history_technology/cm-wordpress)

With the shift to Gutenberg, and as the use of [headless CMS](https://css-tricks.com/what-is-a-headless-cms/) grows, the WordPress community has increasingly started considering React for their projects. Besides this, modern libraries like React are growing in popularity and becoming essential to rich user experiences.

If **WordPress** is great and **React** is too, then why not **combine** the two? Especially if you want to build a CMS-powered site with modern web development tools.

We believe this JavaScript-based approach is gaining traction in the WordPress ecosystem, so there’s no better time to start getting familiar with it.

## **How does Frontity work?**

With Frontity you still use your WordPress dashboard to edit and manage your content in exactly the same way that you are accustomed to. As you make changes content is automatically updated in your Frontity site, just as it is when using a traditional WordPress theme.

Frontity apps require a Node.js server to run on. This runs in tandem with the WordPress site which is now relegated to providing content to the frontend that is based on Frontity.

* Frontity requests content from the WordPress REST-API and uses it to generate the final HTML that is displayed in the browser.
* Frontity is also capable of generating AMP pages using the same React code and CSS.

![](../.gitbook/assets/frontity-architecture%20%282%29%20%281%29.png)

**Why a different Node.js server?**

React is a JavaScript library. In order to generate HTML for site visitors or for Google AMP, the server needs to be able to run JavaScript as well.

> _In theory a PHP server can send an empty HTML file with the JavaScript files included and the visitor will see the page after the JavaScript has loaded. However, this is not a good user experience and it is certainly not recommended if your site needs to be SEO friendly and to rank in search engine listings._

**Frontity** can be hosted either on a regular Node.js server or in a **serverless** environment. That makes it both super cheap and infinitely scalable.

{% hint style="info" %}
We are working on other possible installations, although for the time being this is the one that we most strongly recommend.
{% endhint %}

## **Frontity features**

Frontity and its extensions will help save you a lot of development time and effort, whilst also allowing you to enjoy all of the latest technology trends that come pre-configured for you out of the box. _You can check them out in more detail here:_ [_Frontity Features page_](frontity-features.md)_._

Here are the main ones:

* [Zero setup development](frontity-features.md#zero-setup-development)
* [Lightning-fast loading](frontity-features.md#lightning-fast-loading)
* [Instant in-app navigation](frontity-features.md#instant-in-app-navigation)
* [Google AMP with the same codebase](frontity-features.md#google-amp-support-with-the-same-codebase)
* [Server-side Rendering](frontity-features.md#server-side-rendering)
* [Extensible](frontity-features.md#less-than-greater-than-extensible)
* [Perfect accessibility](frontity-features.md#perfect-accessibility)
* [Battle-tested](frontity-features.md#battle-tested-framework)
* [Serverless and horizontal scaling](frontity-features.md#serverless-and-horizontal-scaling)
* [First class TypeScript support](frontity-features.md#first-class-typescript-support)
* [Support for ES6 in modern browsers](frontity-features.md#support-for-es6-in-modern-browsers)
* [Support for Wordpress.com & WordPress.org](frontity-features.md#support-for-wordpress-com-and-wordpress-org)
* [Support for multiple sites with a single installation](frontity-features.md#support-for-multiple-sites-with-a-single-installation)
* [Code Splitting](frontity-features.md#code-splitting)
* [Smallest React bundle possible](frontity-features.md#smallest-react-bundle-possible)
* [Ready for React Concurrent and Suspense](frontity-features.md#ready-for-react-concurrent-and-suspense)

## **Key differences from GatsbyJS**

Frontity is in a way similar to, and can be compared with, Gatsby.js. However, there are some key differences, i.e. Frontity is:

* **100% focused on WordPress**: this means the number of concepts that you as a developer need to learn are minimal. No complex configuration is necessary to get started, and the queries to the APIs that deliver the content are pre-configured for the things that developers most frequently need.
* **Opinionated**: Frontity has its own state manager and it uses Emotion for the CSS. Thanks to that developers do not need to learn the complexities of such technologies as Redux. At the same time it powers a very flexible extensibility pattern, more similar to that of WordPress itself, rather than that of other JavaScript frameworks.
* **Rendered dynamically**: the HTML does not have to be rebuilt each time the content is edited or new content is published. Our preferred approach is [SPR](https://vercel.com/blog/serverless-pre-rendering), although there are other ways to configure it.
* **Extensible like WordPress**: themes and extensions can be activated and deactivated without code changes.

In addition:

* There is no need to learn GraphQL or the REST API. The data is available to you using Frontity's built-in State Manager.
* Frontity can output HTML suitable for Google AMP with exactly the same React codebase.

If you still have any questions about Frontity, do please join us in our [**community forum**](https://community.frontity.org) and feel free to ask them there. Our growing community of users and developers will be more than happy to help you out.

One of our goals is to build a community of people interested in WordPress and React, so we’d love to meet you and learn about the project \(or projects\) that you're building with Frontity.

