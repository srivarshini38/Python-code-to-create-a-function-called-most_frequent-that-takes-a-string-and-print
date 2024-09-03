# Python-code-to-create-a-function-called-most_frequent-that-takes-a-string-and-print
def most_frequent(string):
    # Convert the string to lowercase to ensure case insensitivity
    string = string.lower()
    
    # Create a dictionary to count the frequency of each letter
    freq_dict = {}
    for char in string:
        if char.isalpha():  # Consider only alphabetic characters
            freq_dict[char] = freq_dict.get(char, 0) + 1
    
    # Sort the dictionary by frequency in descending order
    sorted_freq = sorted(freq_dict.items(), key=lambda item: item[1], reverse=True)
    
    # Print the letters and their frequencies
    for char, freq in sorted_freq:
        print(f"{char} = {freq:02}")

# Example usage:
input_string = input("Please enter a string: ")
most_frequent(input_string)
