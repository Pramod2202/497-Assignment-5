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

3: Shortest Path Visiting all Nodes: 
    Algorithm used:
        Initialization:
        Initialize a 2D array dp of size (2^n) x n, where n is the number of nodes.
        Each state in dp is represented by a bitmask, where each bit corresponds to whether a node is visited or not.
        Initialize the base case: set the distance to infinity for all nodes and set the distance to 0 for the starting node.
        Dynamic Programming with Bitmasking:
        Iterate through all possible states (subsets of nodes) using a bitmask.
        For each state, iterate through all nodes.
        If a node is present in the current subset (bitmask), iterate through its neighbors.
        Update the state by including the neighbor node, and update the distance based on the previous state.
        Final State:
        After iterating through all possible states, find the minimum distance among all final states (all nodes visited).
    Time complexity: 
        The time complexity is O(2^n * n^2), where n is the number of nodes in the graph.
        Each state in dp is visited once, and for each state, we iterate through all nodes and their neighbors.
    Space Complexity:
        The space complexity is O(2^n * n).
        The dp array has dimensions (2^n) x n, representing all possible states and nodes.

4: Binary Tree Maximum Path Sum:
    Algorithm used: 
        Recursive Helper Function (max_path_sum_helper):
        The function takes a node as input.
        If the node is None, return 0 (base case).
        Calculate the maximum path sum for the left and right subtrees using recursion.
        Update the max_sum variable by considering the current node and both subtrees.
        Return the maximum path sum that goes through the current node.
        Main Function (maxPathSum):
        Initialize max_sum with negative infinity.
        Call the recursive helper function with the root of the binary tree.
        Return the final max_sum.
    Time complexity:
        The time complexity is O(n), where n is the number of nodes in the binary tree.
        Each node is visited once during the recursive traversal.
    Space Complexity:
        The space complexity is O(h), where h is the height of the binary tree.
        The space is used for the recursive call stack.
        In the worst case, when the tree is skewed, the height h can be equal to n, making the space complexity O(n).

5: Lexicographical NUmbers:
    Algorithm used:
        Initialize an empty list result to store the final result.
        Initialize current to 1.
        Loop from 1 to n, and at each iteration:
        Append current to the result.
        Move to the next lexicographical order:
        If current * 10 is within the range [1, n], set current to current * 10.
        Otherwise, increment current by 1.
        If the last digit of current is 9, keep removing the last digit until a non-9 digit is found, then increment it by 1.
        Return the final result.
    Time complexity:
        The time complexity is O(n), where n is the input integer.
        Each number from 1 to n is processed once.
    Space complexity:
        The space complexity is O(1), as the additional space used is constant regardless of the input size.
        The result list stores the final output, but its size is proportional to n, and it's not considered in the space complexity analysis.
