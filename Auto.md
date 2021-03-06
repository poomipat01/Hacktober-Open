  
// Given a number N, the task is to check whether the number is Automorphic number or not.
// A number is called Automorphic number if and only if its square ends in the same digits as the number itself.

// Input  : N = 25
// Output : Automorphic
// As 25*25 = 625

// Input : N = 7
 // Output : Not Automorphic
// As 7*7 = 49

 // Input  : N = 6
// Output : Automorphic
// Since 6*6 = 36 

SOLUTION:
class Test { 
    // Function to check Automorphic number 
    static boolean isAutomorphic(int N) 
    { 
        // Store the square 
        int sq = N * N; 

        // Start Comparing digits 
        while (N > 0) { 
            // Return false, if any digit of N doesn't 
            // match with its square's digits from last 
            if (N % 10 != sq % 10) 
                return false; 

            // Reduce N and square 
            N /= 10; 
            sq /= 10; 
        } 

        return true; 
    } 

    // Driver method 
    public static void main(String[] args) 
    { 
        int N = 25; 

        System.out.println(isAutomorphic(N) ? "Automorphic" : "Not Automorphic"); 
    } 
}
