package balancedbrackets;
import java.util.*;


public class BalancedBrackets {
	//function to check if brackets are balanced
	static boolean areBalancedBrackets(String expr) {
		
		//using Stack class
		Stack<Character> stack = new Stack<Character>();
		
		//Traversing the expression
		for(int i=0; i < expr.length(); i++) {
			char x = expr.charAt(i);
			if (x == '(' || x == '[' || x == '{') {
				
				//push the element in the stack
				stack.push(x);
				continue; //correct until here
				
			}
			// If current character is not opening bracket, then it must be closing
			//Thus stack cannot be empty 
			if (stack.isEmpty())
				return false; // correct

			char c;
			switch (x) {
			
			case ')':
			c = stack.pop();
			if (c == '{' || c == '[')
				return false;
			break;
			
			case '}':
			c = stack.pop();
			if (c == '(' || c == '[')
				return false;
			break;
			
			case ']':
				c = stack.pop();
				if (c == '(' || c == '{')
					return false;
				break; //correct
				default:
					return false;
			
		}
		
		
		}
		//Check Empty Stack
		return (stack.isEmpty());
		
	}

	public static void main(String[] args) {
		// 
		String expr = "([[{}]]))";
		
		// function call
		if (areBalancedBrackets(expr)) 
			System.out.println("The entrered String has Balanced Brackets!");
		else
			System.out.println("The entered Strings do not contain Balanced Brackets.");
			

	}

}
