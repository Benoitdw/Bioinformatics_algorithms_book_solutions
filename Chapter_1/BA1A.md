# Compute the Number of Times a Pattern Appears in a Text
This is a really easy algorithm which compute the number of time a pattern appears in a text.
## Pseudocode
```pseudocode
    PatternCount(Text, Pattern)
        count ← 0
        for i ← 0 to |Text| − |Pattern|
            if Text(i, |Pattern|) = Pattern
                count ← count + 1
        return count
```

## Implementation in Rust
```rust
fn pattern_count(text: &str, pattern: &str) -> u32 {
    let mut count : u32 = 0;
    for i in 0..text.len() - pattern.len()+1 {
        if &text[i..i+pattern.len()] == pattern {
            count += 1;
        }
    }
    count
}
```

## More informations
- [Link to the challenge](https://rosalind.info/problems/ba1a/)
- Time test : 
- Complexity: $O(n)$
