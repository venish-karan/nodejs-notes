# Events Module

**TERMS**
- Event listener registration using on method on events module like events.on()
- Event emitter registration using emit method on events module like events.emit()

1. The events module allows us to work with events in Node.js
2. An event is an action or an occurrence that has happened in our application that we can respond to
3. Using the events module, we can dispatch our own custom events and respond to
those custom events in a non-blocking manner.
4. If console.log() is present after the event listener and event emitter, console.log() will be printed 1st as event is not blocking
   the main thread of node.

# Events Module - Scenario
1. Let's say you're feeling hungry and head out to Dominos to have pizza
2. At the counter, you place your order for a pizza
3. When you place the order, the line cook sees the order on the screen and bakes
the pizza for you

**_Order being placed is the event_**
**_Baking a pizza is a response to that event_**

```
const EventEmitter = require("node:events");

const emitter = new EventEmitter();

emitter.on("order-pizza", (size, topping) => {
    console.log(`Order received! Baking a ${size} pizza with ${topping}`);
});

//emitter.emit(event name, event arguments...)
emitter.emit("order-pizza", "large", "mushrooms");
```
