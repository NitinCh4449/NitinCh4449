ANS 1)-

The output for the given Python code print(["sunday","monday","tuesday","wednesday"][-3:-1]) would be:
['monday', 'tuesday']
This is because the slice [-3:-1] selects elements starting from the third element from the end ("monday") up to, but not including, the first element from the end ("wednesday"). 
So, it will print the list containing "monday" and "tuesday".


ANS 2)-

Maximum value will be : 11
Tree depth value will be: 3

**program to calculate values:-**
class TreeNodeDepth {
    int val;
    TreeNodeDepth l, r;

    public TreeNodeDepth(int val) {
        this.val = val;
        this.l = this.r = null;
    }
}

public class BinaryTree {
    TreeNodeDepth root;

    public BinaryTree() {
        this.root = null;
    }

    public int findMaxValue() {
        return findValue(root);
    }

    private int findValue(TreeNodeDepth node) {
        if (node == null)
            return Integer.MIN_VALUE;

        int max = node.val;
        int leftMax = findValue(node.l);
        int rightMax = findValue(node.r);

        if (leftMax > max)
            max = leftMax;
        if (rightMax > max)
            max = rightMax;

        return max;
    }

    public int calculateDepth() {
        return calculateD(root);
    }

    private int calculateD(TreeNodeDepth node) {
        if (node == null)
            return 0;

        int leftDepth = calculateD(node.l);
        int rightDepth = calculateD(node.r);

        return Math.max(leftDepth, rightDepth) + 1;
    }

    public static void main(String[] args) {
        BinaryTree tree = new BinaryTree();
        tree.root = new TreeNodeDepth(5);
        tree.root.l = new TreeNodeDepth(3);
        tree.root.r = new TreeNodeDepth(2);
        tree.root.l.l = new TreeNodeDepth(10);
        tree.root.l.r = new TreeNodeDepth(11);

        System.out.println("Max value: " + tree.findMaxValue());
        System.out.println("Tree depth: " + tree.calculateDepth());
    }
}



ANS 3)- 
sting="$180,240/y"

**Below program to convert string into integer:**

public class ABC {
    public static void main(String[] args) {
        String str = "$180,240/y";
        int result = stringtoint(str);
        System.out.println("Converted integer: " + result);
    }
    
    public static int stringtoint(String str) {
        StringBuilder numericString = new StringBuilder();
        for (char c : str.toCharArray()) {
            if (Character.isDigit(c)) {
                numericString.append(c);
            }
        }
        return Integer.parseInt(numericString.toString());
    }
}

we are crateing StringBuilder to store only the numeric characters encountered while iterating over the input string. 
It checks each character, and if it's a digit, it appends it to the StringBuilder. Finally,
it converts the StringBuilder to a string and parses it to an integer using Integer.parseInt() used for string and parses it to an integer  

