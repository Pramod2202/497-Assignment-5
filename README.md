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

2: Maximum Absolute Difference in BST:
    Algorithm used: 
        In-order Traversal Function (in_order_traversal):
        Traverse the left subtree recursively.
        Update the minimum difference if applicable by comparing the current node's value with the previously visited node's value.
        Update the previously visited node.
        Traverse the right subtree recursively.
        Minimum Difference Function (getMinimumDifference):
        Initialize variables prev to track the previously visited node and min_diff to store the minimum absolute difference (initialized to positive infinity).
        Call the in_order_traversal function, starting from the root of the BST.
        Return the final min_diff as the result.
    Time Complexity: 
        The time complexity is O(n), where n is the number of nodes in the BST.
        Each node is visited once during the in-order traversal.
    Space Complexity:
        The space complexity is O(h), where h is the height of the BST.
        The space is used for the recursive call stack during in-order traversal.
        In the worst case, when the tree is skewed, the height h can be equal to n, making the space complexity O(n).

        