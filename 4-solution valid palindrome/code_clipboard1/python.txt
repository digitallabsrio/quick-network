def is_palindrome(s):
    left = 0
    right = len(s) - 1
    print("The element being pointed by the left index is", s[left], sep = " ")
    print("The element being pointed by the right index is", s[right], sep = " ")
    while left < right:
        print("We check if the two elements are indeed the same, in this case...")
        if s[left] != s[right]:  # If the elements at index l and index r are not equal,
            print("The elements aren't the same, hence we return False")
            return False    # then the symmetry is broken, the string is not a palindrome
        print("They are the same, thus we move the two pointers toward the middle to continue the \nverification process.\n")
        left = left + 1  # Heading towards the right
        right = right - 1  # Heading towards the left
        print("The new element at the left pointer is", s[left], sep = " ")
        print("The new element at the right pointer is", s[right], sep = " ")
    # We reached the middle of the string without finding a mismatch, so it is a palindrome.
    return True


# Driver Code
def main():

    test_cases = ["RACEACAR", "A", "ABCDEFGFEDCBA",
                  "ABC", "ABCBA", "ABBA", "RACEACAR"]
    for i in range(len(test_cases)):
        print("Test Case #", i + 1)
        print("-" * 100)
        print("The input string is '", test_cases[i], "' and the length of the string is ", len(test_cases[i]), ".", sep='')
        print("\nIs it a palindrome?.....", is_palindrome(test_cases[i]))
        print("-" * 100)


if __name__ == '__main__':
    main()