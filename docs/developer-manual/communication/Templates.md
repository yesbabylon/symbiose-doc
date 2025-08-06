# Templates

### TemplateParts – Arbitrary Variable Injection

In *arbitrary variable mode*, a `TemplatePart` contains placeholders written in a predefined syntax, for example:

```
{{ partner.name }}
{{ invoice_total }}
```

Whenever a `TemplatePart` is updated, the system automatically scans its `value` using a regular expression to detect all placeholders matching the pattern `{{ variable_path }}`.

These variable references are stored in the `variables` field of the part, in array/JSON format.

At render time, you must provide an object or associative array (`$data`) that contains all the required variables.
 The engine resolves each placeholder by traversing `$data` according to the dot‑notation path:

- If `$data` is an array: `$data['partner']['name']`
- If `$data` is an object: `$data->partner->name`

If **any** variable listed in `variables` is missing or cannot be resolved, the render process will throw an `Exception` and the template will **not** be rendered.
 This strict validation ensures that no incomplete or partially filled template is sent or generated.

**Summary of workflow:**

1. Author writes a template with placeholders.
2. On save/update, the system extracts placeholders and updates the `variables` list.
3. On render, an object/map with matching fields is injected.
4. All variables must be resolvable, or the process fails.