# LEETCODE-Arrays-2275
### Key Concepts:
1. **Bitwise AND Operation**: 
   - The expression `(num & (1 << i)) != 0` checks if the `i`-th bit of `num` is set (i.e., equals 1). 
   - `1 << i` is a bit-shift operation that produces a number with only the `i`-th bit set to 1.

2. **Iterate Over Bits**:
   - The loop `for (int i = 0; i < 24; i++)` iterates over the 24 least significant bits of each number in the `candidates` array (assuming integers have significant bits within this range).

3. **Count Occurrences of Set Bits**:
   - For each bit position `i`, the code counts how many numbers in `candidates` have their `i`-th bit set to 1.

4. **Find Maximum Count**:
   - The `result` variable stores the maximum number of candidates that share a set bit in any position.

---

### Example Walkthrough:
For `candidates = [8, 3, 5]`:

- Binary representations:
  - `8` → `1000`
  - `3` → `0011`
  - `5` → `0101`

- Iterating over each bit (from 0 to 23):
  - At `i = 0` (1st bit): `3` and `5` → `count_x = 2`
  - At `i = 1` (2nd bit): `3` → `count_x = 1`
  - At `i = 3` (4th bit): `8` → `count_x = 1`
  - Other bit positions: `count_x = 0`.

The largest count for a common bit across all numbers is `2`.

Thus, the result is `2`.

---

### Performance:
- **Time Complexity**: \(O(n \times 24)\), where \(n\) is the size of the `candidates` array.
- **Space Complexity**: \(O(1)\), since only a few variables are used.
