def generate_uutv(file1, file2, file3):
    # Initialize an empty set to store unique tokens
    uutv = set()

    # Open each file and read its contents
    with open(file1, 'r') as f1, open(file2, 'r') as f2, open(file3, 'r') as f3:
        # Read each line in each file
        for line in f1.readlines() + f2.readlines() + f3.readlines():
            # Split the line into words
            words = line.split()
            # Add each word to the set
            uutv.update(words)

    # Convert the set to a list and return it
    return list(uutv)

# Example usage:
file1 = 'D:\MY COUSES\iinformation retrieval\Text01.txt'
file2 = 'D:\MY COUSES\iinformation retrieval\Text02.txt'
file3 = 'D:\MY COUSES\iinformation retrieval\Text03.txt'

uutv = generate_uutv(file1, file2, file3)
print(uutv)
