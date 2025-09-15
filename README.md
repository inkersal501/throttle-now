## throttle-now

A tiny throttle function for JavaScript.

---

## Install

```bash
npm install throttle-now
```

---

## Usage

```javascript
//es modules import
import throttle from 'throttle-now';
//commonjs import
const throttle = require('throttle-now');

const log = throttle(() => console.log('Throttled!'), 2000);

window.addEventListener('scroll', log);
```

#### `Typescript Usage`
```typescript
const log: () => void = throttle(() => console.log('Throttled!'), 2000);
```

---

## Features
- Limits the execution of a function to at most once per given interval.
- Works in both browser and Node.js environments.
- Lightweight, no dependencies.
---

## Examples
```javascript
const saveInput = throttle(() => console.log('Saving input...'), 1000);

document.getElementById('input').addEventListener('input', saveInput);
//Even if the user types continuously, the saveInput function runs at most once per second.
```