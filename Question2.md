**What problems / warnings are there with code?**

1. `isSelected` prop is being passed as an `integer` value to the `SingleListItem` component. It should be a boolean value, but it's currently being used as the selected index. To fix this, change `selectedIndex` to `selectedIndex === index`.

![List Component](https://i.ibb.co/dGgHW0R/App-js-1.png)


2.The `PropTypes.array()` method is being used instead of `PropTypes.arrayOf()`. To fix this, change `PropTypes.array()` to `PropTypes.arrayOf()`.
![List Component](https://i.ibb.co/4JTDtDX/App-js-2.png)

3. The default prop value for the `items` prop should be an empty array instead of null. To fix this, change `WrappedListComponent.defaultProps = { items: null }` to `WrappedListComponent.defaultProps = { items: [] }`.
![List Component](https://i.ibb.co/BLbT9P1/App-js-3.png)

4.The `setSelectedIndex` state setter function is incorrectly used in the `selectedIndex` state declaration, which causes an error when trying to set the initial state. Instead of assigning the function to the state variable, it should be used to set the `initial state` in the useState hook. To fix this, change `const [selectedIndex, setSelectedIndex] = useState(setSelectedIndex);` to `const [selectedIndex, setSelectedIndex] = useState(0);`.
![List Component](https://i.ibb.co/9vryJsb/App-js-4.png)

5.The onClick event handler in the WrappedSingleListItem component should be wrapped in an arrow function to prevent it from being called immediately on render. Instead of onClick={onClickHandler(index)}, it should be onClick={() => onClickHandler(index)}.
![List Component](https://i.ibb.co/p2jpRbG/App-js-5.png)

