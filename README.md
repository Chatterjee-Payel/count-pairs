# count-pairs
class Solution{   
public:
    int getPairsCount(int arr[], int n, int k) {
        // code here
      unordered_map<int,int>mp;
      int count=0;
      for(int i=0;i<n;i++){
          if(mp.contains(k-arr[i]))
          {
              count+=mp.get(k-arr[i]);
          }
          if(!mp.containskey(arr[i]))
          {
              mp.get(arr[i],1);
          }
          else{
              mp.put(arr[i],mp.get(arr[i])+1);
          }
      }
      return count;
};
