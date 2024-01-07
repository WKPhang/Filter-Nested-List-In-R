# Filter-Nested-List-In-R
Script for filtering nested list in R

## How To
Create a custom function as below. Important note: this custom function mantains rows with empty element

```
filter_nested_list <- function(nested_list, chars_to_filter) {
  lapply(nested_list, function(sublist) {
    intersect(sublist, chars_to_filter)
  })
}
```

If you intend to remove rows with empty element in the output filtered nested list, you may include the following code:
```
filtered_list <- filtered_list[lengths(filtered_list) > 0]
```
