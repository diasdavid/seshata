**seshata** - Create your interactive API
============
[![Gitter chat](https://badges.gitter.im/diasdavid/seshata.png)](https://gitter.im/diasdavid/seshata)
[![](https://david-dm.org/diasdavid/seshata.png)](https://david-dm.org/diasdavid/seshata)
[![devDependency Status](https://david-dm.org/diasdavid/seshata/dev-status.png)](https://david-dm.org/diasdavid/seshata#info=devDependencies)

**seshata** is a new way to document your API, without documenting anything at all! Just let your users try it, live! 


#### It's simple, first you define all your API calls available

![](https://i.cloudup.com/36dV5tgoeP-3000x3000.png)

#### Second, when a user clicks on a specific API call, he gets a live answer

![](https://i.cloudup.com/eABDXnuXf0-3000x3000.png)

#### No more mockups, no more non-updated documentation (well, sort of, I'm sure there is a 'lil' more to go to find the panacea of documentation :))


### How to use

Map your api in a `api-map.json` file:

```javascript
{
 "title": "my API docs",
 "api-calls": [
    {
      "id": "route-user",
      "method": "GET",
      "data-route": "/api/user",
      "simple-route": "/api/user",
      "data-target": "route-user",
      "data-body": {},
      "data-truncate": "20"
    },
    ...
```
full example [here](https://github.com/diasdavid/seshata/blob/master/seshata-playground/api-map.json)

Download the module by

```bash
$ git clone git@github.com:diasdavid/seshata.git
$ cd seshats
$ npm link
```

or(once it is on NPM)
```bash
$ npm install -g seshata
```

After this, all you need to gen your API Docs is:
```bash
$ seshata gen <api-map.json> [<output-folder>]
```

### Want to try it out first?

```bash
$ git clone git@github.com:diasdavid/seshata.git
$ cd seshata/seshata-playground
$ seshata gen api-map.json
$ npm install
$ node index.js
# open your browser in localhost:8080
```

### Why **seshata**?

![Seshata](http://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Seshat.svg/200px-Seshat.svg.png)

"In Egyptian mythology, Seshata (also spelled Safkhet, Sesat, Seshet, Sesheta, and Seshata) was the Ancient Egyptian goddess of wisdom, knowledge, and writing."

Source: [Wikipedia](http://en.wikipedia.org/wiki/Seshat)

### Acknowledgements

The original idea for seshata is from [Pedro Teixeira](https://github.com/pgte), he was the one having the vision and suggested me to do it :) Thank you Pedro! Also, it was inspired by the [sls-sample-app-coobook](https://github.com/strongloop/sls-sample-app-cookbook), which uses this interactive technique 
