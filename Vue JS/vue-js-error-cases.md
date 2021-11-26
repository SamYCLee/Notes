# VueJS Error Cases

## Error - Cannot read property '__ob__' of undefined

### _Possible Scenarios_

----

#### **Empty data function**

##### *Issue*

Please check if your components have any empty vue function, if yes, please remove the function that are not using. Here is one of the examples:

``` javascript
  Vue.component("foo", {
    data(){

    },
    ....
  })
```

In the example the vue function //data () {} // is an empty function, if such function exists, the mentioned error will possibly be resulted.

##### *Solution*

- Remove the data function if local state is not needed
- Return an empty object

``` javascript
  Vue.component("foo", {
    data(){
      return {}
    },
    ....
  })
```