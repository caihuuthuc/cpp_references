# cpp_references

## STL

### STL Iterator
| Iterator Category | Ability | Providers |
|  ---| --- | --- |
| Output iterator | Writes forward | Ostream, inserter |
| Input iterator | Reads forward once | Istream |
| Forward iterator | Reads forward | Forward list, unordered containers |
| Bidirectional iterator | Reads forward and backward | List, set, multiset, map, multimap |
| Random-access iterator  | Reads with random access | Array, vector, deque, string, C-style array |

#### Output iterator
| Expression | Effect |
| --- | --- |
| `*iter = val` | Writes val to where the iterator refers |
| `++iter` | Steps forward (returns new position) |
| `iter++` | Steps forward (returns old position) |
| `TYPE(iter)` | Copies iterator (copy constructor) |
 
 #### Input iterator
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

#### Birectional iterator
| Expression | Effect |
| --- | --- |
| `--iter` | Steps backward (returns new position) |
| `iter--` | Steps backward (returns old position) |

#### Random access iterator
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

### STL Algorithm
| Name Effect Page | 
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
