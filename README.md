# INTRO TO VUE JS

https://cli.vuejs.org/

Create new project

```
vue create my-project
```

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

## Practicing

- Props
- Primitive vs Reference types
- Event (child to parents)
- Events Bus
- Life-cycle hooks

### Life cycle hooks

```javascript
  beforeCreate() {
    alert("Before create!");
  },
  created() {
    alert("Created!");
  },
  beforeMount() {
    alert("Before Mount");
  },
  mounted() {
    alert("Mounted");
  },
  beforeUpdate() {
    alert("Before update");
  },
  updated() {
    alert("updated");
  },
```

- Slots
- Dynamic components

### HTTP request

```
npm install vue-resouce
```
