# Compute the Number of Times a Pattern Appears in a Text
This is a really easy algorithm which compute the number of time a pattern appears in a text.


## Implementations
<!-- tabs:start -->
### **Pseudocode**
```pseudocode
    PatternCount(Text, Pattern)
        count ← 0
        for i ← 0 to |Text| − |Pattern|
            if Text(i, |Pattern|) = Pattern
                count ← count + 1
        return count
```

### **Python**
```python
def pattern_count(text: str, pattern: str) -> int:
    count = 0
    for i in range(len(text)-(len(pattern)-1)):
        if text[i:i+(len(pattern))] == pattern:
            count += 1
    print(count)
```

### **Rust**
```rust
fn pattern_count(text: &str, pattern: &str) -> u32 {
    let mut count : u32 = 0;
    for i in 0..text.len() - (pattern.len()-11) {
        if &text[i..i+pattern.len()] == pattern {
            count += 1;
        }
    }
    count
}
```
<!-- tabs:end -->
## Performances
### Complexity
$O(n)$

### Time
- **OS:** Ubuntu 20.04.3 LTS x86_64 
- **CPU:** 11th Gen Intel i7-1165G7 (8) @ 4.700GHz
- **RAM** : 15686MiB

Tests were done on [theses files.](http://bioinformaticsalgorithms.com/data/debugdatasets/replication/PatternCount.zip)
| File_name | Time |
|      |      |
|      |      |

## More informations
- [Link to the challenge](https://rosalind.info/problems/ba1a/)
