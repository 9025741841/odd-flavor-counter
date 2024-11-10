# odd-flavor-counter
from collections import deque
from collections import Counter

def first_odd_flavor(n, flavors):
    # Count the occurrences of each flavor
    flavor_counts = Counter(flavors)
    
    # Find the first flavor with an odd count
    for flavor in flavors:
        if flavor_counts[flavor] % 2 != 0:
            return flavor
    
    # If no flavors have an odd count, return "All are even"
    return "All are even"

# Sample Input
n = 8
flavors = ["chocolate", "mint", "caramel", "caramel", "mint", "vanilla", "vanilla", "chocolates"]

# Output the result
print(first_odd_flavor(n, flavors))  # Expected output: "chocolate"


