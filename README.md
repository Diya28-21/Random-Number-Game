import java.util.*;
class NumberGame
{
	public static void main(String args[])
	{
	 Scanner sc=new Scanner(System.in);
	 Random r=new Random();
	 int score=0;
	 char playagain='y';
	 while(playagain!='n')
	 {
	 	int number = r.nextInt(100)+1;
	 	int attempts=1;
	 	int guess;
	 	int flag = 0;
	 	System.out.println("Guess the Between 1 and 100");
	 	for(int i=1;i<=5;i++)
	 	{
	 		System.out.println("Guess:"+i);
	 		System.out.println("Enter your Guess");
	 		int n=sc.nextInt();
	 		if(n==number)
	 		{
	 			System.out.println("Correct Guess");
	 			score++;
	 			flag=1;
	 			break;
	 		}
	 		else if(n>number)
	 		{
	 			System.out.println("Too High");
	 		}
             else
             {
             	System.out.println("too low");
             }
            

             }
          if(flag==0)
             {
             	System.out.println("You Lost");
             	System.out.println("Carrect Number is="+number);
             	System.out.println("Better Luck next time Game..... Thank You....");

             System.out.println("Play Again('y'/'n')");
            playagain = sc.next().charAt(0);


	 	     }
	 	System.out.println("Final Score="+score);
	 System.out.println("Game Over");   
	 }

	}
}
