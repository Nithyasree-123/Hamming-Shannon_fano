# HUFFMAN-SHANNON_FANO 

## AIM: 

Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.

## TOOLS REQUIRED: 
Python with NumPy and SciPy libraries, Google Colab.

## PROGRAM: 
```
# Huffman and Shannon-Fano Coding
import numpy as np
import math 

L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples: "))

for i in range(n): 
    pr = float(input(f"Enter the probability of sample {i + 1}: "))  
    p.append(pr)

for j in range(n): 
    l = float(input(f"Enter the length of sample {j + 1}: "))  
    lk.append(l)

# Average Codeword Length
for k in range(n):
    Avg1 = p[k] * lk[k]
    L += Avg1

# Entropy Calculation
for k in range(n):
    e = p[k] * math.log(1 / p[k], 2)
    hs += e
hs = round(hs, 3)

# Efficiency Calculation
eff = round(hs / L, 3)

# Redundancy Calculation
red = round(1 - eff, 3)

# Variance Calculation
var = 0
for k in range(n):
    var1 = p[k] * (lk[k] - L) ** 2
    var += var1
var = round(var, 3)

print(f"Average Codeword Length: {L}")
print(f"Entropy: {hs}")
print(f"Efficiency: {eff}")
print(f"Redundancy: {red}")
print(f"Variance: {var}")

```
## CALCULATION: 

![image 1](https://github.com/user-attachments/assets/2ec3b5f6-4000-47c4-a69b-ade32e5c0eaf)

![image 2](https://github.com/user-attachments/assets/cc58d7c6-10e4-4c9b-943b-02a374e0d3b4)

![image 3](https://github.com/user-attachments/assets/811cbd65-93b3-41a3-974b-1d3a16c98ed8)

## OUTPUT:

<img width="468" height="454" alt="image" src="https://github.com/user-attachments/assets/8520adb5-808a-48cc-b22e-5c40a55293b2" />

## RESULTS: 
 The Huffman and Shannon-Fano coding techniques have been successfully applied to the given source. The average codeword length, entropy, variance, redundancy, and efficiency have been computed.
