| Operator   | Description  |
|------------|--------------|
| `stringEquals`  | Case-sensitive string comparison. Boolean or number values are converted into a string before comparison. |
| `stringMatch`  | Case-sensitive string match is performed between the pattern and the target string by using either an asterisk (`*`), question mark (`?`), both, or none (same as literal value). An asterisk (`*`) represents any sequence of zero or more characters in the string, and a question mark (`?`) represents any single character. You can also express an asterisk `*` and question mark `?` as a literal value by enclosing each within two sets of curly brackets `{{}}`. |
| `stringExists`  |  Boolean where `true` indicates that the string must be present and can be empty. `false` indicates that the string must not be present. |
| `stringEqualsAnyOf` | Case-sensitive exact string matching any of the strings in an array of strings. Limit of 10 values. |
| `stringMatchAnyOf` | Case-sensitive string matching any of the strings in an array of strings. The string values can include either an asterisk (`*`), question mark (`?`), both, or none (same as literal value). An asterisk (`*`) represents any sequence of zero or more characters in the string, and a question mark (`?`) represents any single character. You can also express an asterisk `*` and question mark `?` as a literal value by enclosing each within two sets of curly brackets `{{}}`. Limit of 10 values. |
{: caption="The string comparison operators available for conditions in access policies." caption-side="top"}
