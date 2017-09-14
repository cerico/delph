# Delph - A WebComponents Router

## TLDR / Install

```
npm install delph
```

## Examples

```
cd examples/one
npm run dev
```


## Dependencies

none!

## How to use

### Import

```
import { Delph } from 'delph'
```


### Instantiate

```
constructor(){
      const page = window.location.pathname.substr(1) || ''
      const main = document.getElementById('main')
      this.delph = new Delph(routes, main, page)
    }
```


Delph takes in a Routes object, an element to append to, and the current url

### Sample Routes

```
const routes = {
    about:   AboutComponent,
    '' : DefaultComponent
}
```

### Sample Component

```
export class DefaultComponent extends HTMLElement {
    
  connectedCallback() {
    this.render();
  }
    
  render() {
    this.innerHTML = (`i am the homepage`)
  }
}
    
customElements.define('default-component', DefaultComponent);
```





