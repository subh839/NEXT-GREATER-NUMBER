# NEXT-GREATER-NUMBER

 vector<long long> nextLargerElement(vector<long long> arr, int n){
     stack<long long> s;
        vector<long long> v(n);
        for(long i=n-1; i>=0; i--){
            while(!s.empty() && arr[i]>s.top()) s.pop();
            v[i] = s.empty() ? -1 : s.top();
            s.push(arr[i]);
        }
        return v;}
        };
