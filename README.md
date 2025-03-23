FINONACCIGENERATOR CODE

def fibonacci_generator(n):
    """
    Generate the first n numbers in the Fibonacci sequence.
    
    Args:
        n (int): Number of Fibonacci numbers to generate
        
    Returns:
        list: First n Fibonacci numbers
    """
    # Handle edge cases
    if n <= 0:
        return []
    if n == 1:
        return [0]
    
    # Initialize the sequence with the first two numbers
    fib_sequence = [0, 1]
    
    # Generate the remaining numbers
    for i in range(2, n):
        # Each number is the sum of the two preceding numbers
        next_number = fib_sequence[i-1] + fib_sequence[i-2]
        fib_sequence.append(next_number)
    
    return fib_sequence

# Example usage
if __name__ == "__main__":
    num_terms = 20
    result = fibonacci_generator(num_terms)
    print(f"First {num_terms} Fibonacci numbers: {result}")
    
    # Print the sequence with indices
    for i, num in enumerate(result):
        print(f"F({i}) = {num}")
