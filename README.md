# 23620005-mahemud-borgave

# Output 
# -----------------------------------

Flat profile:

Each sample counts as 0.01 seconds.
 no time accumulated

  %   cumulative   self              self     total           
 time   seconds   seconds    calls  Ts/call  Ts/call  name    
  0.00      0.00     0.00       15     0.00     0.00  std::remove_reference<int&>::type&& std::move<int&>(int&)
  0.00      0.00     0.00        5     0.00     0.00  std::enable_if<std::__and_<std::__not_<std::__is_tuple_like<int> >, std::is_move_constructible<int>, std::is_move_assignable<int> >::value, void>::type std::swap<int>(int&, int&)
  0.00      0.00     0.00        4     0.00     0.00  partition(int*, int, int)
  0.00      0.00     0.00        1     0.00     0.00  quickSort(int*, int, int)

			Call graph


granularity: each sample hit covers 2 byte(s) no time propagated

index % time    self  children    called     name
                0.00    0.00      15/15          std::enable_if<std::__and_<std::__not_<std::__is_tuple_like<int> >, std::is_move_constructible<int>, std::is_move_assignable<int> >::value, void>::type std::swap<int>(int&, int&) [9]
[8]      0.0    0.00    0.00      15         std::remove_reference<int&>::type&& std::move<int&>(int&) [8]
-----------------------------------------------
                0.00    0.00       5/5           partition(int*, int, int) [10]
[9]      0.0    0.00    0.00       5         std::enable_if<std::__and_<std::__not_<std::__is_tuple_like<int> >, std::is_move_constructible<int>, std::is_move_assignable<int> >::value, void>::type std::swap<int>(int&, int&) [9]
                0.00    0.00      15/15          std::remove_reference<int&>::type&& std::move<int&>(int&) [8]
-----------------------------------------------
                0.00    0.00       4/4           quickSort(int*, int, int) [11]
[10]     0.0    0.00    0.00       4         partition(int*, int, int) [10]
                0.00    0.00       5/5           std::enable_if<std::__and_<std::__not_<std::__is_tuple_like<int> >, std::is_move_constructible<int>, std::is_move_assignable<int> >::value, void>::type std::swap<int>(int&, int&) [9]
-----------------------------------------------
                                   8             quickSort(int*, int, int) [11]
                0.00    0.00       1/1           main [6]
[11]     0.0    0.00    0.00       1+8       quickSort(int*, int, int) [11]
                0.00    0.00       4/4           partition(int*, int, int) [10]
                                   8             quickSort(int*, int, int) [11]
-----------------------------------------------

Index by function name

  [10] partition(int*, int, int) [8] std::remove_reference<int&>::type&& std::move<int&>(int&)
  [11] quickSort(int*, int, int) [9] std::enable_if<std::__and_<std::__not_<std::__is_tuple_like<int> >, std::is_move_constructible<int>, std::is_move_assignable<int> >::value, void>::type std::swap<int>(int&, int&)
