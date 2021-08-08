# depth_first_traversal
PreOrder, inOrder, PostOrder tree traversal algorithms from conceptual description

```javascript
const preorderTraverse = (node, array) => {
  const left = node.left ? preorderTraverse(node.left) : [];
  const right = node.right ? preorderTraverse(node.right) : [];
  return [node.value].concat(left, right);
};

const inorderTraverse = (node, array) => {
  const left = node.left ? inorderTraverse(node.left) : [];
  const right = node.right ? inorderTraverse(node.right) : [];
  return [].concat(left, node.value, right);
};

const postorderTraverse = (node, array) => {
  const left = node.left ? postorderTraverse(node.left) : [];
  const right = node.right ? postorderTraverse(node.right) : [];
  return [].concat(left, right, node.value);
};

```
