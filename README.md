# Lightstreamer - Basic Chat Demo - HTML Client #
<!-- START DESCRIPTION lightstreamer-example-chat-client-javascript -->

The Lightstreamer Basic Chat Demo is a very simple chat application based on Lightstreamer.

This project includes a simple web client front-end example for the [Lightstreamer - Basic Chat Demo - Java Adapter](https://github.com/Lightstreamer/Lightstreamer-example-Chat-adapter-java).

## Live Demo

[![screenshot](screen_chat_large.png)](https://demos.lightstreamer.com/ChatDemo/)

### [![](http://demos.lightstreamer.com/site/img/play.png) View live demo](https://demos.lightstreamer.com/ChatDemo/)

## Details

This <b>Basic Chat Demo</b> implements an extremely simple chat application, where all the users connected to the page can exchange messages. Each message reports the originating IP address, together with the user-agent string of the originating client, instead of leveraging a nickname.
Launch multiple instances of the demo, possibly on different machines, to appreciate the message broadcast capability.
The front-end code can be considered a reference example of item subscriptions in DISTINCT mode.

*Note: When you publish a value, your IP address is publicly displayed.*

The demo includes the following client-side functionalities:
* A [Subscription](https://lightstreamer.com/api/ls-web-client/latest/Subscription.html) containing 1 item, subscribed to in <b>DISTINCT</b> mode feeding a [DynaGrid](https://lightstreamer.com/api/ls-web-client/latest/DynaGrid.html).
* The chat messages are sent to the Lightstreamer Server using the [LightstreamerClient.sendMessage](https://lightstreamer.com/api/ls-web-client/latest/LightstreamerClient.html#sendMessage) utility.

<!-- END DESCRIPTION lightstreamer-example-chat-client-javascript -->

## Install
If you want to install a version of this demo pointing to your local Lightstreamer Server, follow these steps:
* As prerequisite, the [Basic Chat Demo - Java Adapter](https://github.com/Lightstreamer/Lightstreamer-example-Chat-adapter-java) has to be deployed on your local Lightstreamer Server instance. Please check out that project and follow the installation instructions provided with it.
* Download this project.
* Get the `lightstreamer.min.js` file from [npm](https://www.npmjs.com/package/lightstreamer-client-web) or [unpkg](https://unpkg.com/lightstreamer-client-web/lightstreamer.min.js) and put it in the `src/js` folder.
  Alternatively, you can generate a customized lightstreamer.min.js library containing only the classes you actually use;
  see the build instructions on the [GitHub page](https://github.com/Lightstreamer/Lightstreamer-lib-client-javascript#building).
  In that case, be sure to include the LightstreamerClient, Subscription, DynaGrid, ConnectionSharing, and StatusWidget modules.
* Get the `require.js` file form [requirejs.org](http://requirejs.org/docs/download.html) and put it in the `src/js` folder.
* Deploy this demo on the Lightstreamer Server (used as Web server) or in any external Web Server. If you choose the former, please note that in the `<LS_HOME>/pages/demos/` folder, there may be already a `ChatDemo` folder. If this is not your case, please create the folders `<LS_HOME>/pages/demos/ChatDemo` and copy here the contents of the `/src` folder of this project.
The client demo configuration assumes that Lightstreamer Server, Lightstreamer Adapters, and this client are launched on the same machine. If you need to target a different Lightstreamer server, please search in `js/lsClient.js` this line:<BR/> `var lsClient = new LightstreamerClient(protocolToUse+"//localhost:"+portToUse,"CHAT");`<BR/> and change it accordingly.
* Open your browser and point it to: [http://localhost:8080/demos/ChatDemo/](http://localhost:8080/demos/ChatDemo/)

## See Also

### Lightstreamer Adapters Needed by This Client
<!-- START RELATED_ENTRIES -->

* [Lightstreamer - Basic Chat Demo - Java Adapter](https://github.com/Lightstreamer/Lightstreamer-example-Chat-adapter-java)
* [Lightstreamer - Reusable Metadata Adapters - Java Adapter](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-java)

<!-- END RELATED_ENTRIES -->

### Related Projects

* [Lightstreamer - Basic Messenger Demo - HTML Client](https://github.com/Lightstreamer/Lightstreamer-example-Messenger-client-javascript)

## Lightstreamer Compatibility Notes

- Compatible with Lightstreamer JavaScript Client library version 6.0 or newer (installation instructions for version 8.0 or newer).
