# BST Search

```csharp
//Node class definition
public class Node {
    public int key;
    public Node left, right;

    public Node(int item){
        key = item;
        left = right = null;
    }
}
```

```csharp
//Search a BST for given key
//T/C => 0(log N)
public Node search(Node root, int key){
    if( root == null || root.key == key) return root;

    Node curr = root;
    while(curr != null) {
        if( key == curr.key){
            return curr;
        }else if( key < curr.key){
            curr = curr.left;
        }else{
            curr = curr.right
        }
    }
    return null;
}
```
