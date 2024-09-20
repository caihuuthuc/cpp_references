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
| *iter | Provides access to the actual element |
| iter->member |Provides access to a member of the actual element |
| ++iter |Steps forward (returns new position) |
| iter++ | Steps forward (returns old position) |
| iter1 == iter2 | Returns whether two iterators are equal |
| iter1 != iter2 | Returns whether two iterators are not equal |
| TYPE() | Creates iterator (default constructor) |
| TYPE(iter) | Copies iterator (copy constructor) |
| iter1 = iter2 | Assigns an iterator |

#### Birectional iterator
| Expression | Effect |
| --- | --- |
| --iter | Steps backward (returns new position) |
| iter-- | Steps backward (returns old position) |

#### Random access iterator
| Expression   | Effect |
| ---          | --- |
| iter[n]      | Provides access to the element that has index n |
| iter+=n      | Steps n elements forward (or backward, if n is negative) |
| iter-=n      | Steps n elements backward (or forward, if n is negative) |
| iter+n       | Returns the iterator of the nth next element |
| n+iter       | Returns the iterator of the nth next element |
| iter-n       | Returns the iterator of the nth previous element |
| iter1-iter2  | Returns the distance between iter1 and iter2 |
| iter1<iter2  | Returns whether iter1 is before iter2 |
| iter1>iter2  | Returns whether iter1 is after iter2 |
| iter1<=iter2 | Returns whether iter1 is not after iter2 |
| iter1>=iter2 | Returns whether iter1 is not before iter2 |
