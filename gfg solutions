class Solution {
  public:
    vector<vector<int>> insertInterval(vector<vector<int>> &intervals,
                                       vector<int> &newInterval) {
        // code here
        int n = intervals.size(), f = 0;
        vector<vector<int>> ans;
        for(int i = 0; i < n; i++) {
            if(!f && intervals[i][0] > newInterval[0]) {
                ans.push_back(newInterval);
                f = 1;
            }
            if(!ans.empty() && ans.back()[1] >= intervals[i][0]) 
            ans.back()[1] = max(ans.back()[1], intervals[i][1]);
            else ans.push_back(intervals[i]);
            
            if(!ans.empty() && ans.back()[1] >= newInterval[0]) {
                ans.back()[1] = max(ans.back()[1], newInterval[1]);
                f = 1;
            }
            
        }
        if(f == 0) ans.push_back(newInterval);
        return ans;
    }
};
