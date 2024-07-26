# Express.js Snippets for VS Code

This VS Code extension provides a collection of snippets for quickly setting up Express.js applications and routes. These snippets cover basic setup, HTTP methods, middleware, and more advanced configurations.

## Installation

1. **Open VS Code.**
2. **Go to Extensions**: You can do this by clicking on the Extensions view icon on the Sidebar or pressing `Ctrl+Shift+X`.
3. **Search for "Express.js Snippets"** and click **Install**.

## Available Snippets

### Basic Express.js Setup

- **`!express`**: Creates a basic Express.js server setup.

  ```javascript
  import express from 'express';

  const app = express();
  const port = ${1:3000};

  app.get('/', (req, res) => {
      res.send('Hello World!');
  });

  app.listen(port, () => {
      console.log(`Server running on port ${port}`);
  });
  ```

### HTTP Methods

- **`!eget`**: Defines a GET route.

  ```javascript
  app.get('${1:/path}', (req, res) => {
      ${2:res.send('GET request to the homepage');}
  });
  ```

- **`!epost`**: Defines a POST route.

  ```javascript
  app.post('${1:/path}', (req, res) => {
      ${2:res.send('POST request to the homepage');}
  });
  ```

- **`!eput`**: Defines a PUT route.

  ```javascript
  app.put('${1:/path}', (req, res) => {
      ${2:res.send('PUT request to the homepage');}
  });
  ```

- **`!edelete`**: Defines a DELETE route.

  ```javascript
  app.delete('${1:/path}', (req, res) => {
      ${2:res.send('DELETE request to the homepage');}
  });
  ```

- **`!epatch`**: Defines a PATCH route.

  ```javascript
  app.patch('${1:/path}', (req, res) => {
      ${2:res.send('PATCH request to the homepage');}
  });
  ```

- **`!eoptions`**: Defines an OPTIONS route.

  ```javascript
  app.options('${1:/path}', (req, res) => {
      ${2:res.send('OPTIONS request to the homepage');}
  });
  ```

- **`!ehead`**: Defines a HEAD route.
  ```javascript
  app.head('${1:/path}', (req, res) => {
      ${2:res.send('HEAD request to the homepage');}
  });
  ```

### Middleware and Route Use

- **`!emiddleware`**: Adds a middleware for logging request methods.

  ```javascript
  app.use((req, res, next) => {
    console.log("${1:Request Type}:", req.method);
    next();
  });
  ```

- **`!eruse`**: Declares a middleware route.
  ```javascript
  app.use("${1:/}", "${2:}");
  ```

### Express Router

- **`!routeget1`**: Creates a router with a GET route.

  ```javascript
  import { Router } from 'express';

  const router = Router();

  router.route('${1:/path}').get((req, res) => {
      ${2:res.send('GET request');}
  });

  export default router;
  ```

- **`!routepost1`**: Creates a router with a POST route.

  ```javascript
  import { Router } from 'express';

  const router = Router();

  router.route('${1:/path}').post((req, res) => {
      ${2:res.send('POST request');}
  });

  export default router;
  ```

- **`!routeput1`**: Creates a router with a PUT route.

  ```javascript
  import { Router } from 'express';

  const router = Router();

  router.route('${1:/path}').put((req, res) => {
      ${2:res.send('PUT request');}
  });

  export default router;
  ```

- **`!routedelete1`**: Creates a router with a DELETE route.

  ```javascript
  import { Router } from 'express';

  const router = Router();

  router.route('${1:/path}').delete((req, res) => {
      ${2:res.send('DELETE request');}
  });

  export default router;
  ```

- **`!routepatch1`**: Creates a router with a PATCH route.

  ```javascript
  import { Router } from 'express';

  const router = Router();

  router.route('${1:/path}').patch((req, res) => {
      ${2:res.send('PATCH request');}
  });

  export default router;
  ```

- **`!routeoptions1`**: Creates a router with an OPTIONS route.

  ```javascript
  import { Router } from 'express';

  const router = Router();

  router.route('${1:/path}').options((req, res) => {
      ${2:res.send('OPTIONS request');}
  });

  export default router;
  ```

- **`!routehead1`**: Creates a router with a HEAD route.

  ```javascript
  import { Router } from 'express';

  const router = Router();

  router.route('${1:/path}').head((req, res) => {
      ${2:res.send('HEAD request');}
  });

  export default router;
  ```

- **`!routeget2`**: Creates a router with a GET route without the basic controller setup.

  ```javascript
  import { Router } from "express";

  const router = Router();

  router.route("${1:/path}").get("${2:}");

  export default router;
  ```

- **`!routepost2`**: Creates a router with a POST route without the basic controller setup.

  ```javascript
  import { Router } from "express";

  const router = Router();

  router.route("${1:/path}").post("${2:}");

  export default router;
  ```

- **`!routeput2`**: Creates a router with a PUT route without the basic controller setup.

  ```javascript
  import { Router } from "express";

  const router = Router();

  router.route("${1:/path}").put("${2:}");

  export default router;
  ```

- **`!routedelete2`**: Creates a router with a DELETE route without the basic controller setup.

  ```javascript
  import { Router } from "express";

  const router = Router();

  router.route("${1:/path}").delete("${2:}");

  export default router;
  ```

- **`!routepatch2`**: Creates a router with a PATCH route without the basic controller setup.

  ```javascript
  import { Router } from "express";

  const router = Router();

  router.route("${1:/path}").patch("${2:}");

  export default router;
  ```

- **`!routeoptions2`**: Creates a router with an OPTIONS route without the basic controller setup.

  ```javascript
  import { Router } from "express";

  const router = Router();

  router.route("${1:/path}").options("${2:}");

  export default router;
  ```

- **`!routehead2`**: Creates a router with a HEAD route without the basic controller setup.

  ```javascript
  import { Router } from "express";

  const router = Router();

  router.route("${1:/path}").head("${2:}");

  export default router;
  ```

### Express.js Middleware and Full Setup

- **`!emiddleware`**: Adds a middleware for logging request methods.

  ```javascript
  app.use((req, res, next) => {
    console.log("${1:Request Type}:", req.method);
    next();
  });
  ```

- **`!esetup`**: Basic Express.js setup with JSON and URL-encoded body parsers.

  ```javascript
  import express from 'express';

  const app = express();
  const port = ${1:3000};

  app.use(express.json());
  app.use(express.urlencoded({ extended: true }));

  app.get('/', (req, res) => {
      res.send('Hello World!');
  });

  app.listen(port, () => {
      console.log(`Server running on port ${port}`);
  });
  ```

- **`!efullsetup`**: Full Express.js setup with additional middleware.

  ```javascript
  import express from 'express';
  import cookieparser from 'cookie-parser';
  import cors from 'cors';

  const app = express();
  app.use(cookieparser());
  app.use(
    cors({
      origin: process.env.CORS_ORIGIN,
      credentials: true,
    })
  );
  const port = ${1:process.env.PORT || 3000};

  app.use(express.json());
  app.use(express.urlencoded({ extended: true }));

  app.get('/', (req, res) => {
      res.send('Hello World!');
  });

  app.listen(process.env.PORT, () => {
      console.log(`Server running on port ${process.env.PORT}`);
  });
  ```

## Usage

1. **Type the snippet prefix** (e.g., `!express`, `!eget`) in a JavaScript file.
2. **Press `Tab`** to insert the snippet.
3. **Fill in the placeholders** with your specific route paths, request handlers, or configurations.

## Contributing

Feel free to contribute to this extension by submitting issues or pull requests. For more information on how to contribute, please refer to the [contributing guide](CONTRIBUTING.md).

## License

This extension is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Enjoy coding with Express.js and make your development process faster and more efficient with these snippets!
