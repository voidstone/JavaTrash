
public class BTS {

    Node root;

    public void addNode(int key, String name) {

        Node newNode = new Node(key, name);

        if (root == null) {
            root = newNode;
        } else {
            Node focusNode = root;

            Node parent;

            while (true) {
                parent = focusNode;

                if (key < focusNode.key) {
                    focusNode = focusNode.leftChild;

                    if (focusNode == null) {

                        parent.leftChild = newNode;
                        return;
                    }
                } else {
                    focusNode = focusNode.rightChild;

                    if (focusNode == null) {

                        parent.rightChild = newNode;
                        return;
                    }
                }
            }
        }

    }

    public void inOrderTraverseTree(Node focusNode) {
        if (focusNode != null) {
            inOrderTraverseTree(focusNode.leftChild);
            System.out.println(focusNode);

            inOrderTraverseTree(focusNode.rightChild);
        }
    }

    public void preOrderTraverseTree(Node focusNode) {
        if (focusNode != null) {
            System.out.println(focusNode);
            preOrderTraverseTree(focusNode.leftChild);
            preOrderTraverseTree(focusNode.rightChild);
        }
    }

    public void postOrderTraverseTree(Node focusNode) {
        if (focusNode != null) {
            postOrderTraverseTree(focusNode.leftChild);
            postOrderTraverseTree(focusNode.rightChild);
            System.out.println(focusNode);

        }
    }

    public Node findNode(int key) {
        Node focusNode = root;
        int deep = 0;

        while (focusNode.key != key) {
            if(key < focusNode.key) {
                deep++;
                focusNode = focusNode.leftChild;

            } else {
                deep++;
                focusNode = focusNode.rightChild;
            }

            if(focusNode ==null)
                return null;
        }
        System.out.print(deep);
        return focusNode;
    }

    public static void main(String[] args) {

        BTS theTree = new BTS();


        theTree.addNode(50, "Boss");
        theTree.addNode(25, "V P");
        theTree.addNode(15, "O M");
        theTree.addNode(30, "Secretary");
        theTree.addNode(75, "Sales manager");
        theTree.addNode(85, "Salesman");

        theTree.postOrderTraverseTree(theTree.root);

        System.out.println("Search for 30");

        System.out.println(theTree.findNode(75));


    }
}

class Node {
    int key;
    String name;

    Node leftChild;
    Node rightChild;

    Node(int key, String name) {
        this.key = key;
        this.name = name;
    }

    public String toString() {
        return name + " has a key " + key;
    }
}
