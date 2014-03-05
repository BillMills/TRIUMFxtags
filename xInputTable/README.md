##xInputTable

xInputTable provides a scalable table of input elements, and fires a callback when the table contents change.  TODO: more fine-grained callback definitions.

###Use

See `demo.html` for some minimal use.  The following properties should be defined on object creation:

 - `columns`: A comma separated string list of column titles.
 - `types`: A comma separated string list of the `type` attribute to be assigned to each `<input>`, same order as `columns`.
 - `values`: as `types`, but for the `value` property.

In order to enable a callback any time any of the input elements in the table change, assign the desired callback function to your xInputTable's `.changeCallback` property.
