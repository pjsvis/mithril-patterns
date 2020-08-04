## mithril patterns

- [learn mithril blog](http://lhorie.github.io/mithril-blog/index.html)
- use pragma to force jsx to use m

```javascript
/* @jsx m */
```

```js
vnode = m(selector, attributes, children)
```


```javascript
//I just want a div
m("div")

//but it has text
m("div", "Hello world")

//actually, I need to toggle a class on it too
m("div", {class: isActive ? "active" : ""}, "Hello world")
```

- props

```javascript
var name = m.prop("")

//set the value
name("John")

//get the value
console.log(name()) // "John"

// in use
var User = function(data) {
    this.firstName = m.prop(data.firstName)
    this.lastName = m.prop(data.lastName)
}

//automatically convert response objects to User instances
m.request({method: "GET", url: "/users", type: User})

```
