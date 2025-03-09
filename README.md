Find All Duplicates

def find_duplicates_nested_loop(l: list) -> list:
    duplicates = []
    for i in range(len(l)):
        for j in range(i + 1, len(l)):
            if l[i] == l[j] and l[i] not in duplicates:
                duplicates.append(l[i])
    return duplicates

Different Solutions to Solving This Problem

1. Nested Loop Solution
    Follows through two nested loops in order to iterate through the list twice, and then checking with the second loop to determine if the item in the first loop has a duplicate.

    Pros:
    - Simple algorithm, easy to use for smaller lists.
    
    Cons:
    - Poor time complexity, impractical for larger lists due to the many unneeded linear checks that occur.

2. Dictionary / Hash Map Solution
    Uses an empty dictionary with the keys used to represent the integers from the list and the value representing how many times the number appears. Then iterates through the list, adding each integer to the dictionary and increasing the value of repeating ones. After the iteration of the list, identify the duplicates by finding the keys with a value greater than 1.

    Pros:
    - Good time complexity and reduces the unneeded linear checks.

    Cons:
    - More complex to implement.