# Running

Sortier can be run through either the API or a CLI

## CLI

Sortier by default will write all files in place. To do so run:

```bash
sortier "[glob syntax]"
```

Don't forget the quotes around the globs! The quotes make sure that Prettier expands the globs rather than your shell, for cross-platform usage. The glob syntax from the glob module is used.

When the CLI is executed, it will use cosmiconfig to load a configuration file for sortier or, if one is not found, run with the default settings.

## API

Sortier also has an API you can run via code:

```typescript
import { formatText } from "sortier/format-text";

formatText("json", `{ "b": "2", "c": "3", "a": "1"}`, {
  logLevel: "diagnostic",
});
```

The first argument is the file you wish to format. The second argument is a JSON object of options of which more details can be found in later sections.
