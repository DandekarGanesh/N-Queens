class Solution {
    static List<List<String>> ans;
    static int n;
    public List<List<String>> solveNQueens(int n) {
        ans = new ArrayList<>();
        this.n = n;
        char grid[][] = new char[n][n];

        for(char i[]: grid) {
            Arrays.fill(i, '.');
        }

        solve(grid, 0);
        return ans;
    }



    void solve(char grid[][], int i) {
        if(i == n) {
            add(grid);
            return;
        }


        for(int j=0; j<n; j++) {
            if(isPossible(grid, i, j)) {
                grid[i][j] = 'Q';
                solve(grid, i+1);
                grid[i][j] = '.';
            }
        } 
    }



    boolean isPossible(char grid[][], int  row, int col) {
        int i = row;
        int j = col;

        // top
        for(int k=row-1; k>=0; k--) {
            if(grid[k][col] == 'Q') return false;
        }

        // left top
        while(i >=0 && j>= 0) {
            if(grid[i--][j--] == 'Q') return false;
        }


        // right top
        while(row >= 0 && col < n) {
            if(grid[row--][col++] == 'Q') return false;
        }

        return true;
    }


    void add(char grid[][]) {
        List<String> List = new ArrayList<>();

        for(int i=0; i<n; i++) {
            StringBuilder sb = new StringBuilder();
            for(int j=0; j<n; j++) {
                sb.append(grid[i][j]);
            }

            List.add(sb.toString());
        }

        ans.add(List);
    }

}
