dijkstra algorithm
https://www.geeksforgeeks.org/problems/implementing-dijkstra-set-1-adjacency-matrix/0


/*
class iPair {
    int first, second;

    iPair(int first, int second) {
        this.first = first;
        this.second = second;
    }
}
 

// User function Template for Java
class Solution {
    // Function to find the shortest distance of all the vertices
    // from the source vertex src.
    ArrayList<Integer> dijkstra(ArrayList<ArrayList<iPair>> adj, int src) {
        // Write your code here
            PriorityQueue<iPair> pq = new PriorityQueue<iPair>((x , y) -> x.first - y.first);
            
        ArrayList<Integer> dist = new ArrayList<Integer>();
        for(int i =0;i<adj.size();i++) {
            dist.add(Integer.MAX_VALUE);
        }
        dist.set(src , 0);
        pq.add(new iPair(0 , src));
        while(pq.size() != 0) {
            int distance = pq.peek().first;
            int node = pq.peek().second;
            pq.remove();
            
            for(iPair it  : adj.get(node)) {
                int newDistance = distance + it.second;
                int newNode = it.first;
                if(dist.get(newNode) > newDistance) {
                    pq.add(new iPair(newDistance , newNode));
                    dist.set(newNode , newDistance);
                }
            }
            
        }
        for(int i =0;i<adj.size();i++) {
          if( dist.get(i) == Integer.MAX_VALUE) dist.set(i , -1);
        }
        
        return dist;
    }
}
*/
