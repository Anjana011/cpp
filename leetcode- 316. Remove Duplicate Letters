class Solution {
public:
    string removeDuplicateLetters(string s) {
        stack<char>st;
        map<char,bool>vis;
        map<char,int>last;
        int n=s.size();
        for(int i=0;i<n;i++){
            last[s[i]]=i;
        }
        for(int i=0;i<n;i++)if(!vis[s[i]]){
            while(!st.empty() && st.top()>s[i]){
                if(last[st.top()]>i) vis[st.top()]=0,st.pop();
                else break;
            }
            st.push(s[i]);
            vis[s[i]]=1;
        }
        string ans="";
        while(!st.empty()){
            ans+=st.top();
            st.pop();
        }
        reverse(ans.begin(),ans.end());
        return ans;
    }
};
