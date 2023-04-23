**What problems / warnings are there with code?**

1. `isSelected` prop is being passed as an `integer` value to the `SingleListItem` component. It should be a boolean value, but it's currently being used as the selected index. To fix this, change `selectedIndex` to `selectedIndex === index`.

![List Component](https://i.ibb.co/dGgHW0R/App-js-1.png)

