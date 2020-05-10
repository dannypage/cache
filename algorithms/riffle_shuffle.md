# Riffle Shuffle

## Strictly alternating, one by one.

### Python

```python
left = [1,2,3,4]
right = [5,6,7,8]
combined = []

while len(left) > 0 or len(right) > 0:
    combined.append(left.pop(0))  if left  else None
    combined.append(right.pop(0)) if right else None

print(combined)
# [1, 5, 2, 6, 3, 7, 4, 8]
```

## Realistic card riffle

### Python

```python
import random

left = [1,2,3,4]
right = [5,6,7,8]
combined = []

while len(left) > 0 or len(right) > 0:
    deck = random.choice([left, right])
    combined.append(deck.pop(0)) if deck else None

print(combined)
# [1, 5, 2, 3, 6, 7, 4, 8] - one possible iteration
```
