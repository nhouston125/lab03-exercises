Find All Duplicates

Find All Duplicates

def find_duplicates_nested_loop(l: list) -> list:
    duplicates = []
    for i in range(len(l)):
        for j in range(i + 1, len(l)):
            if l[i] == l[j] and l[i] not in duplicates:
                duplicates.append(l[i])
    return duplicates
