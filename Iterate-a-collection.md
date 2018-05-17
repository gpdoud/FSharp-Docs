# Iterate a collection

This is how to iterate through a collection (list).

This is a sample collection (list)

    let lst = [1;2;3;4;5]

This code must be (rec)ursive and does pattern matching (match lst with).

The pattern `[] -> 0` handles the situation when all the items in the list have been processed.

The pattern `x :: r -> x + accum r` breaks down:

* `x :: r` indicates x is the HEAD of the list and r is the rest of the list
* `->` processes as
* `x + accum r` adds x and the accumulation of the rest of the list

```
    let rec accum lst = 
      match lst with
      | x :: r -> x + accum r
      | [] -> 0
```

This code alls `accum` on a list called `lst`

    let ans = accum lst