# inordeertraversal

class Solution {

    void inorder(TreeNode* root , vector<int>& vct){
        if(root==NULL){
            return;

        }

        inorder(root->left , vct);
        vct.push_back(root->val);
        inorder(root->right, vct);
    }
     public:
    vector<int> inorderTraversal(TreeNode* root) {
        vector<int> vct;
        inorder(root, vct);
        return vct;
    }
};
