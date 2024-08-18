- 👋 Hi, I’m @Aditya9779
- 👀 I’m interested in to develop Native Apps & Web Applications
- 🌱 I’m currently learning the Android Development & Java FullStack with SpringBoot 
- 💞️ I’m looking to collaborate on who can help in Android development & Web Applications
- 📫 How to reach me throught my aditya107161@gmail.com
class Solution {
    public int[][] merge(int[][] intervals) {
        if (intervals.length == 0)
            return new ans int[][];
        Arrays.sort(intervals, new Comparator<int[]>() {
            @Override
            public int compare(int[] a, int[] b) {
                return Integer.compare(a[0], b[0]);
            }
        });
        int merge=0;
        for(int i=0 ;i<intervals.length;i++){
            if(merge==0||intervals[i][0]>intervals[merge-1][1]){
                intervals[merge]=intervals[i];
                merge++;
            }
            else{
             intervals[merge-1][1]=Math.max(intervals[merge-1][1],intervals[i][1]) ;  
            }
        }
         int[][] result = new int[merge][2];
        for (int i = 0; i < merge; i++) {
            result[i] = intervals[i];
        }

      
        return result;

    }
}
