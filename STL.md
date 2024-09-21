# STL

## STL Iterator
| Iterator Category | Ability | Providers |
|  ---| --- | --- |
| Output iterator | Writes forward | Ostream, inserter |
| Input iterator | Reads forward once | Istream |
| Forward iterator | Reads forward | Forward list, unordered containers |
| Bidirectional iterator | Reads forward and backward | List, set, multiset, map, multimap |
| Random-access iterator  | Reads with random access | Array, vector, deque, string, C-style array |

### Output iterator
| Expression | Effect |
| --- | --- |
| `*iter = val` | Writes val to where the iterator refers |
| `++iter` | Steps forward (returns new position) |
| `iter++` | Steps forward (returns old position) |
| `TYPE(iter)` | Copies iterator (copy constructor) |
 
### Input iterator
| Expression | Effect |
| --- | --- |
| `*iter` | Provides read access to the actual element |
| `iter->member` |Provides read access to a member of the actual element |
| `++iter` | Steps forward (returns new position) |
| `iter++` | Steps forward |
| `iter1 == iter2` | Returns whether two iterators are equal |
| `iter1 != iter2` | Returns whether two iterators are not equal |
| `TYPE(iter)` | Copies iterator (copy constructor) |

#### Forward iterator
| Expression | Effect |
| --- | --- |
| `*iter` | Provides access to the actual element |
| `iter->member` |Provides access to a member of the actual element |
| `++iter` |Steps forward (returns new position) |
| `iter++` | Steps forward (returns old position) |
| `iter1 == iter2` | Returns whether two iterators are equal |
| `iter1 != iter2` | Returns whether two iterators are not equal |
| `TYPE()` | Creates iterator (default constructor) |
| `TYPE(iter)` | Copies iterator (copy constructor) |
| `iter1 = iter2` | Assigns an iterator |

### Birectional iterator
| Expression | Effect |
| --- | --- |
| `--iter` | Steps backward (returns new position) |
| `iter--` | Steps backward (returns old position) |

### Random access iterator
| Expression     | Effect |
| ---            | --- |
| `iter[n]`      | Provides access to the element that has index n |
| `iter+=n`      | Steps n elements forward (or backward, if n is negative) |
| `iter-=n`      | Steps n elements backward (or forward, if n is negative) |
| `iter+n`       | Returns the iterator of the nth next element |
| `n+iter`       | Returns the iterator of the nth next element |
| `iter-n`       | Returns the iterator of the nth previous element |
| `iter1-iter2`  | Returns the distance between iter1 and iter2 |
| `iter1<iter2`  | Returns whether iter1 is before iter2 |
| `iter1>iter2`  | Returns whether iter1 is after iter2 |
| `iter1<=iter2` | Returns whether iter1 is not after iter2 |
| `iter1>=iter2` | Returns whether iter1 is not before iter2 |

## STL Algorithm
### Non-modify algorithms
| Name | Effect | 
| --- | --- |
| `for_each()` | Performs an operation for each element  | 
| `count()` | Returns the number of elements  | 
| `count_if()` | Returns the number of elements that match a criterion  | 
| `min_element()` | Returns the element with the smallest value  | 
| `max_element()` | Returns the element with the largest value  | 
| `minmax_element()` | Returns the elements with the smallest and largest value (since C++11) | 
| `find()` | Searches for the first element with the passed value  | 
| `find_if()` | Searches for the first element that matches a criterion  | 
| `find_if_not()` | Searches for the first element that matches a criterion not (since C++11) | 
| `search_n()` |Searches for the first n consecutive elements with certain properties | 
| `search()` | Searches for the first occurrence of a subrange  | 
| `find_end()` | Searches for the last occurrence of a subrange  | 
| `find_first_of()` | Searches the first of several possible elements  | 
| `adjacent_find()` | Searches for two adjacent elements that are equal (by some criterion) | 
| `equal()` | Returns whether two ranges are equal  | 
| `is_permutation()` | Returns whether two unordered ranges contain equal elements (since C++11) | 
| `mismatch()` | Returns the first elements of two sequences that differ  | 
| `lexicographical..._compare()` | Returns whether a range is lexicographically less than another range | 
| `is_sorted()` | Returns whether the elements in a range are sorted (since C++11) | 
| `is_sorted_until()` | Returns the first unsorted element in a range (since C++11)  | 
| `is_partitioned()` | Returns whether the elements in a range are partitioned in two groups according to a criterion (since C++11) | 
| `partition_point()` | Returns the partitioning element for a range partitioned into elements fulfilling and elements not fulfilling a predicate (since C++11) | 
| `is_heap()` | Returns whether the elements in a range are sorted as a heap (since C++11) | 
| `is_heap_until()` | Returns the first element in a range not sorted as a heap (since C++11) | 
| `all_of()` | Returns whether all elements match a criterion (since C++11)  | 
| `any_of()` | Returns whether at least one element matches a criterion (since C++11) | 
| `none_of()` | Returns whether none of the elements matches a criterion (since C++11) | 

### Modify algorithms
| Name | Effect|
| --- | --- |
| `for_each()` | Performs an operation for each element |
| `copy()` | Copies a range starting with the first element |
| `copy_if()` | Copies elements that match a criterion (since C++11) |
| `copy_n()` | Copies n elements (since C++11) |
| `copy_backward()` | Copies a range starting with the last element |
| `move()` | Moves elements of a range starting with the first element (since C++11)|
| `move_backward()` | Moves elements of a range starting with the last element (since C++11)|
| `transform()` | Modifies (and copies) elements; combines elements of two ranges |
| `merge()` | Merges two ranges |
| `swap_ranges()` | Swaps elements of two ranges |
| `fill()` | Replaces each element with a given value |
| `fill_n()` | Replaces n elements with a given value |
| `generate()` | Replaces each element with the result of an operation |
| `generate_n()` | Replaces n elements with the result of an operation |
| `iota()` | Replaces each element with a sequence of incremented values (since C++11)|
| `replace()` | Replaces elements that have a special value with another value|
| `replace_if()` | Replaces elements that match a criterion with another value|
| `replace_copy()` | Replaces elements that have a special value while copying the whole range|
| `replace_copy_if()` | Replaces elements that match a criterion while copying the whole range|

### Removing algorithms
| Name | Effect|
| --- | --- |
| `remove()` | Removes elements with a given value  |
| `remove_if()` | Removes elements that match a given criterion  |
| `remove_copy()` | Copies elements that do not match a given value  |
| `remove_copy_if()` | Copies elements that do not match a given criterion  |
| `unique()` | Removes adjacent duplicates (elements that are equal to their predecessor) |
| `unique_copy()` | Copies elements while removing adjacent duplicates  |

### Mutating algorithms
| Name | Effect|
| --- | --- |
| `reverse()` | Reverses the order of the elements  |
| `reverse_copy()` | Copies the elements while reversing their order  |
| `rotate()` | Rotates the order of the elements  |
| `rotate_copy()` | Copies the elements while rotating their order  |
| `next_permutation()` | Permutates the order of the elements  |
| `prev_permutation()` | Permutates the order of the elements  |
| `shuffle()` | Brings the elements into a random order (since C++)  |
| `random_shuffle()` | Brings the elements into a random order  |
| `partition()` | Changes the order of the elements so that elements that match a criterion are at the front |
| `stable_partition()` | Same as partition() but preserves the relative order of matching and nonmatching elements |
| `partition_copy()` | Copies the elements while changing the order so that elements that match a criterion are at the front |

### Sorting algorithms
| Name | Effect|
| --- | --- |
| `sort()` | Sorts all elements  |
| `stable_sort()` | Sorts while preserving order of equal elements  |
| `partial_sort()` | Sorts until the first n elements are correct  |
| `partial_sort_copy()` | Copies elements in sorted order  |
| `nth_element()` | Sorts according to the nth position  |
| `partition()` | Changes the order of the elements so that elements that match a criterion are at the beginning |
| `stable_partition()` | Same as partition() but preserves the relative order of matching and nonmatching elements |
| `partition_copy()` | Copies the elements while changing the order so that elements that match a criterion are at the beginning |
| `make_heap()` | Converts a range into a heap  |
| `push_heap()` | Adds an element to a heap  |
| `pop_heap()` | Removes an element from a heap  |
| `sort_heap()` | Sorts the heap (it is no longer a heap after the call)  |

Algorithms Checking for Sortings:
| Name | Effect|
| --- | --- |
| `is_sorted()` | Returns whether the elements in a range are sorted (since C++11) |
| `is_sorted_until()` | Returns the first unsorted element in a range (since C++11) |
| `is_partitioned()` | Returns whether the elements in a range are partitioned in two groups according to a criterion (since C++11) |
| `partition_point()` | Returns the partitioning element for a range partitioned into elements fulfilling and elements not fulfilling a predicate (since C++11) |
| `is_heap()` | Returns whether the elements in a range are sorted as a heap (since C++11) |
| `is_heap_until()` | Returns the first element in a range not sorted as a heap (since C++11) |

### Sorted-Range Algorithms
| Name | Effect|
| --- | --- |
| `binary_search()` | Returns whether the range contains an element  |
| `includes()` | Returns whether each element of a range is also an element of another range |
| `lower_bound()` | Finds the first element greater than or equal to a given value |
| `upper_bound()` | Finds the first element greater than a given value  |
| `equal_range()` | Returns the range of elements equal to a given value |
| `merge()` | Merges the elements of two ranges  |
| `set_union()` | Processes the sorted union of two ranges  |
| `set_intersection()` | Processes the sorted intersection of two ranges  |
| `set_difference()` | Processes a sorted range that contains all elements of a range that are not part of another range |
| `set_symmetric_difference()` | Processes a sorted range that contains all elements that are in exactly one of two ranges |
| `inplace_merge()` | Merges two consecutive sorted ranges  |
| `partition_point()` | Returns the partitioning element for a range partitioned into elements fulfilling and elements not fulfilling a predicate (since C++11) |

### Numeric Algorithms
| Name | Effect|
| --- | --- |
| `accumulate()` | Combines all element values (processes sum, product, and so forth) |
| `inner_product()` | Combines all elements of two ranges |
| `adjacent_difference()` | Combines each element with its predecessor |
| `partial_sum()` | Combines each element with all its predecessors |
