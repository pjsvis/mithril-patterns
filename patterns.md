## mithril patterns

- [learn mithril blog](http://lhorie.github.io/mithril-blog/index.html)
- use pragma to force jsx to use m

```javascript
/* @jsx m */
```

```javascript
//I just want a div
m("div")

//but it has text
m("div", "Hello world")

//actually, I need to toggle a class on it too
m("div", {class: isActive ? "active" : ""}, "Hello world")
```
