# pick-dom-element

## Usage

Create an instance of the `ElementPicker` class, and call its `start()` method to start picking. Provide an `onHover` or `onClick` callback to get the picked element(s). Call `stop()` to stop picking and remove the overlay from the DOM.

```javascript
import { ElementPicker } from "@riadhossain43/dom-element-picker";

const style = { borderColor: "#0000ff" };
const picker = new ElementPicker({ style });
picker.start({
  onHover: (el) => console.log(`Hover: ${el}`),
  onClick: (el) => {
    picker.stop();
    console.log(`Picked: ${el}`);
  },
});
```

See the [example](example/) directory for a more complete example of how to use the library.
