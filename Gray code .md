vector<int> grayCode(int n) {
        if(n == 0) return {0};
        vector<int> ret = {0, 1};
        
        for(int i=2; i<=n; i++)
            for(int j=ret.size()-1; j>=0; j--)
                ret.push_back(ret[j]+(1<<i-1));
        
        return ret;
}
