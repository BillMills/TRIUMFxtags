##xInputTable

xInputTable provides a scalable table of input elements, and fires a callback when the table contents change.  TODO: more fine-grained callback definitions, more flexible and elegant attribute setting.

###Use

See `demo.html` for some minimal use.  The following properties should be defined on object creation:

 - `columns`: A comma separated string list of column titles.
 - `types`: A comma separated string list of the `type` attribute to be assigned to each `<input>`, same order as `columns`; `select` is also a valid option.
 - `values`: as `types`, but for the `value` property.
 - `minima`: as `types`, but for the `min` property.
 - `selectOptions`: Comma separated list of names of `option` elements to insert into any `select` element in the table; note only one unique `select` per table is currently supported.
 - `selectValues`: Comma separated list of the `value` attribute to be applied to the corresponding entries in the `selectOptions` list.

In order to enable a callback any time any of the input elements in the table change, assign the desired callback function to your xInputTable's `.changeCallback` property.

Call xInputTable's `.insertRow()` method to insert a new blank row at the bottom of the table.
