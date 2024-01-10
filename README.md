<h1 align="center">fivem-js</h1>

This is a fork of d0p3t/fivem-js maintained by BetterLife.GG to keep the project up to date for our use.

Functionality of this wrapper is **based on the FiveM C# wrapper** - [link](https://github.com/citizenfx/fivem/tree/master/code/client/clrcore/External). It's a feature-rich set of helper classes, objects, and functions to help you develop your project faster.

## Features

- One dependency [@citizenfx/client](https://www.npmjs.com/package/@citizenfx/client)
- Abstracts common used FiveM practices
- Entity management through class objects (i.e. `Vehicle` and `Ped` entities)
- UI elements such as `scaleforms` and loading `prompts`
- Audio, Blips, Cameras and more...

In other words, whatever the FiveM C# wrapper can do, this package can as well and more!

## Download & Install

`npm i @betterlife-gg/fivem-js`

https://www.npmjs.com/package/@betterlife-gg/fivem-js

### Typescript

```typescript
import * as Cfx from '@betterlife-gg/fivem-js';

RegisterCommand(
  'adder',
  async (source: number, args: string[]) => {
    const vehicle = await Cfx.World.createVehicle(
      new Cfx.Model('adder'),
      new Cfx.Vector3(1, 2, 3),
      4,
    );
    Cfx.Game.PlayerPed.setIntoVehicle(vehicle, Cfx.VehicleSeat.Driver);
  },
  false,
);
```

You can also individually import classes.

```typescript
import { World } from '@betterlife-gg/fivem-js/lib/World';
```

### Javascript

```js
/// <reference path="node_modules/@betterlife-gg/fivem-js/lib/index.d.ts"/>
/// <reference path="node_modules/@citizenfx/client/natives_universal.d.ts"/>

const Cfx = require('fivem-js');

RegisterCommand(
  'adder',
  async (source, args) => {
    const vehicle = await Cfx.World.createVehicle(
      new Cfx.Model('adder'),
      new Cfx.Vector3(1, 2, 3),
      4,
    );
    Cfx.Game.PlayerPed.setIntoVehicle(vehicle, Cfx.VehicleSeat.Driver);
  },
  false,
);
```

You are more than welcome to contribute to this project by submitting a pull request and creating issues.

Please checkout [CONTRIBUTING.md](./CONTRIBUTING.md) for our contributing guidelines.

## License

MIT with customization. See [LICENSE](https://github.com/d0p3t/fivem-js/blob/master/LICENSE)
