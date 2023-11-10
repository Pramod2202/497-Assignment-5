# Assignment-5
1: Remove Invalid Parenthesis:
    Algorithm used: 
        is_valid Function:
        This function checks if a given expression is valid by counting the number of open and close parentheses.
        removeInvalidParentheses Function:
        Initialize an empty list result to store valid expressions.
        Initialize an empty set visited to keep track of visited expressions to avoid duplicates.
        Initialize a boolean variable found to track whether a valid expression has been found.
        Perform a breadth-first search (BFS) using a queue:
        Enqueue the initial expression s.
        Mark s as visited.
        While the queue is not empty:
            Dequeue the current expression current.
            If current is valid, add it to the result and set found to True.
            If found is True, skip further exploration.
            Generate all possible expressions by removing one parenthesis at a time.
            Enqueue the newly generated expressions if they are not visited.
        Return the list of valid expressions result.
    Time Complexity:
        Let n be the length of the input string s.
        In the worst case, all possible combinations of removing parentheses are explored.
        Each expression is processed once in BFS, and for each expression, all possible next expressions are generated.
        The time complexity is O(2^n), where n is the length of the input string.        
    Space Complexity:
        The space complexity is also O(2^n)