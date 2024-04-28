# EventNetworking Example Project

This is an example project for the [EventNetworking](https://github.com/OnuGame/eventnetworking) library.

## How to use

1. Clone the repository
2. Install the dependencies of the client, server and shared library with `npm install` in the respective folders
3. Run the server with `npm run dev` in the server folder
4. Run the client with `npm run dev` in the client folder
5. Open the client in your browser at the address shown in the console

## Use in your own project

For an advanced example on how to use the library in your own project, check out the main repository of the library: [EventNetworking](https://github.com/OnuGame/eventnetworking)

## Known problems using the library with Vite

When you're using Vite as a client and try to install the shared library locally, you might run into problems like `Uncaught SyntaxError: The requested module '...' does not provide an export named 'xyz'`.

To fix this, make sure that the shared library is built before the client and that the client includes it in the `vite.config.js` like this:

```javascript
export default {
  optimizeDeps: {
    include: ["shared"],
  },
};
```
