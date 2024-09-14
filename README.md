# VS_Code

```python

import numpy as np
coin = ['heads', 'tails', 'side']

probabilities = [0.49165, 0.49165, 0.0167] #the probability of the coin landing on a side is 0.0167

number_of_throws = 100000

throws = np.random.choice(coin, number_of_throws, p =probabilities)

print(f"heads: {np.sum(throws == 'heads')}")
print(f"tails: {np.sum(throws == 'tails')}")
print(f"side: {np.sum(throws == 'side')}")
unique, counts = np.unique(throws, return_counts=True )
import matplotlib.pyplot as plt
plt.bar(unique, counts)

import matplotlib.pyplot as plt

total_heads_side = np.sum(throws == "heads")
total_tails_side = np.sum(throws == "tails")
total_side = np.sum(throws == "side")

plt.bar(coin, [total_heads_side, total_tails_side, total_side], color="teal")
plt.title("Coin Toss with Side landing")
plt.xlabel("Landing result")
plt.ylabel("Frequency")
plt.show()
```
