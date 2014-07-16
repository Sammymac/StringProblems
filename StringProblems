import java.util.HashMap;

public class StringProblems{

    public static void main(String []args){
        StringProblems hw = new StringProblems();
        System.out.println(hw.makeIntoPalindrome("abcdabc"));
    }
    
    public String makeIntoPalindrome(String temp){
        HashMap<Character, Integer> hm = new HashMap<Character, Integer>();
        char word[] = temp.toCharArray();
        char newWord[] = new char[word.length];
        int oddCount = 0;
        int index=0;
        
        for(int i=0;i<word.length;i++){
            if(hm.containsKey(word[i])){
                hm.put(word[i], hm.get(word[i])+1);
            }
            else{
                hm.put(word[i], 1);
            }
        }
        
        for(Character c : hm.keySet()){     //Check if palindrome possible
            if(hm.get(c) % 2 != 0){
                oddCount++;
            }
        }
        if(oddCount>1){
            System.out.println("FAIL");
        }
        
        for(Character c : hm.keySet()){
            if(hm.get(c) % 2 != 0){
                hm.put(c, hm.get(c)-1);
                newWord[newWord.length/2] = c;
            }
            while(hm.get(c) > 0){
                newWord[index] = c;
                newWord[newWord.length-index-1] = c;
                hm.put(c, hm.get(c)-2);
                index++;
            }
            
        }
        
        String finalString = new String(newWord);
        return finalString;
    }
    
}
