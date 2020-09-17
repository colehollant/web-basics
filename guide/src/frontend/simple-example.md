# Simple example

Here's a super basic example of a page with a button that increments a count and a text input that auto-updates a message with its contents in vanilla js and in vue:

## Vanilla

```html
<body>
  <div>
    <p id="message">Message:</p>
    <input type="text" id="messageInput" oninput="updateMessage()">
    <p id="count">Count: 0</p>
    <button onclick="increment()">Increment</button>
  </div>
  <script>
    let count = 0
    function updateMessage() {
      document.querySelector('#message').innerHTML = `Message: ${document.querySelector('#messageInput').value}`
    }
    function increment(e) {
      count++
      document.querySelector('#count').innerHTML = `Count: ${count}`
    }
  </script>
</body>
```


## Vue

```html
<body>
  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  <div id="app">
    <p>Message: {{message}}</p>
    <input type="text" v-model="message">
    <p>Count: {{count}}</p>
    <button @click="increment">Increment</button>
  </div>
  <script>
    new Vue({
      el: '#app',
      data: {
        message: "this is some message",
        count: 0
      },
      methods: {
        increment() {
          this.count++
        }
      }
    })
  </script>
</body>
```

Of course, everything is ultimately preference, and this example is a bit silly, but hopefully presents some of the basic reasoning behind JS frameworks. We get a nicer source of truth for our data, falling to some object rather than parsing the DOM, and so on...