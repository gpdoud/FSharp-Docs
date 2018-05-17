# Iterate a collection

This is how to iterate through a collection (list).

    let lst = [1;2;3;4;5]



    let rec accum lst = 
      match lst with
      | x :: r -> x + accum r
      | [] -> 0

    let ans = accum lst