---
title: Getting started
description: Get started with the Cartify SDK with a step-by-step guide
category: Getting started
position: 0
---

This documentation will walk you through how to:

- Set up a cartify-sdk account.
- Install Cartify SDK into your project.
- Create a cartify-sdk instance to use through your project.

---

## Account setup

Before installing cartify-sdk SDK, you will first need to create a cartify-sdk Account to get your API credentials.

1. Sign up for a cartify-sdk Account [here](#/signup).
2. Navigate to the developer section under settings [here](#/settings/developer).
3. Obtain your generated [public](/docs/sdk/concepts#public-keys) and [secret keys](/docs/sdk/concepts#secret-keys).

---

## Installation

### Prerequisites

The only requirement for using cartify-sdk SDK is to have Node.js (version 16 or higher) installed on your machine.

### Install the SDK with a package manager

If you're using npm or yarn, then adding the cartify-sdk SDK to your project is really simple. Once you've created a
directory for your project, navigate into your project's root folder in your terminal `cd your-project-folder`, and type
the following:

```bash
npm install cartify-sdk
# or
yarn add cartify-sdk
```

<div class="highlight highlight--note">
    <span>Note</span>
    <p>Note that examples provided using the cartify-sdk SDK are using the latest version - available on <a href="https://www.npmjs.com/package/cartify-sdk">npm</a>.</p>
</div>

### Instantiate cartify-sdk with your API key

We're almost ready to go! We need to create a new cartify-sdk instance and give it our [public
key](/docs/sdk/concepts#scope) (you can get your API keys from [cartify-sdk Dashboard > Settings >
Developer](#/settings/developer)).

<div class="highlight highlight--info">
    <span>Tip</span>
    <p>For more information on API keys authentication, read more on <a href="/docs/sdk/concepts#authentication">how we authenticate cartify-sdk core endpoints</a>.</p>
</div>

```js
// Import the cartify-sdk module
import Cartify from 'cartify-sdk';

// Create a cartify-sdk instance
const cartify = new Cartify('{public_api_key}');
```

<div class="highlight highlight--note">
    <span>Note</span>
    <p>We've built in a console debugger into the cartify-sdk SDK to help with debugging during development. To enable the debugger you can include the second argument <code>true</code> when you create your cartify-sdk instance like so: <code>const cartify-sdk = new cartify-sdk('{public_api_key}', true);</code>. Note that a test API key has to be provided as the first argument for the console to show messages - it won't work with a live key.</p>
</div>

Awesome, you have set up your cartify-sdk Account, installed the cartify-sdk SDK and created your first cartify-sdk instance! You
now have access to the `cartify-sdk` object in your application to build out a truly unique frontend presentation layer!

---

### Next steps

Browse through the rest of our documentation to explore all the features of cartify-sdk SDK - [listing
products](/docs/sdk/products#list-products), [add products to cart](/docs/sdk/cart#add-to-cart), or [capture an
order](/docs/sdk/checkout#capture-order). Note that all requests made using the cartify-sdk SDK will have responses that
are returned asynchronously in a promise. Alternatively, if you want to dive more into reading a high-level overview of
cartify-sdk SDK and its features, read more [here](/product/features).

<div class="highlight highlight--warn">
    <span>Important</span>
    <p>Please note that for all the following SDK documentation on  <b>Products</b>, <b>Cart</b>, and <b>Checkout</b>, we import <code>cartify-sdk</code> in every example using cartify-sdk SDK for the sake of brevity. In practice, you would follow the example of creating and exporting out your cartify-sdk client in a file such as <code>/lib/cartify-sdk SDK</code>.</p>
</div>

---
