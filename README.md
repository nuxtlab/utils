![Banner](https://nuxtlab.net/api/files/github_banner-K00eZM3AJl3ek01AFl7AyG8haViBYN.png)

# Front-End Utilities

Front-End utilities that facilitate add-ons development for FiveM.

## Installation

Using `npm`:

```
npm install @nuxtlab/utils
```

Using `pnpm`:

```
pnpm install @nuxtlab/utils
```

Using `yarn`:

```
yarn add @nuxtlab/utils
```

## Example Uses

You can use the examples in the subsection below to use the tools.

## isEnvBrowser

-   Checks whether the development environment is a browser.

```javascript
isEnvBrowser(): boolean;
```

-   Usage

```javascript
// import

const browser = isEnvBrowser()

console.log(browser) // returns true if the page developed is open in the browser.
```

## fetchNui

-   Allows you to send requests to the client side.

```javascript
fetchNui(eventName: string, data: object): any;
```

-   Usage

```javascript
// import

fetchNui('test', {
    name: 'Mark Edward'
})
    .then((data) => {
        console.log(data) // prints if a return was provided by the game.
    })
    .catch((error) => {
        console.log(error)
    })
```

## useNuiEvent

-   Allows you to listen to nui callbacks.

```javascript
useNuiEvent(handler: (event: { action: string, data?: object }) => void): void;
```

-   Usage

```javascript
// import

useNuiEvent((event) => {
    console.log(event.data) // prints the event data.
})
```

## sendDebugEvent

-   Simulates sending a callback by the client.

```javascript
sendDebugEvent(name: string, data?: object): void;
```

-   Usage

```javascript
// import

sendDebugEvent('test-event', {
    name: 'Mark Edward'
})
```

## Contact Us

Join our [Discord Server](https://discord.gg/fcNrD3XNdv) for updates, support and special discounts!
