
# socket.io-parser

[![Build Status](https://github.com/socketio/socket.io-devalue-parser/workflows/CI/badge.svg)](https://github.com/socketio/socket.io-devalue-parser/actions)

A fork of the default socket.io encoder and decoder, which uses
[devalue](https://github.com/Rich-Harris/devalue) over the vanilla
[JSON](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON) object,
for stringifying and parsing JavaScript objects.
This offers many improvements over the default parser, such as support for
dates, maps, sets, regular expressions, `undefined`, custom classes and more.
Check out [devalue](https://github.com/Rich-Harris/devalue) for details.

## Usage

### Server

```js
import * as parser from "@socket.io/devalue-parser";
import { Server } from "socket.io";

const io = new Server({
  parser
});
```

### Client

```js
import * as parser from "@socket.io/devalue-parser";
import { io } from "socket.io-client";

const socket = io({
  parser
});
```

## License

[MIT](LICENSE)
