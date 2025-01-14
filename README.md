//Function that counts a total number of consonant in a given string
public static int CountCons(string text) 
{
    //List of Consonants
    string consonant = "bcdfghjklmnpqrstvwxyz";

    int count = 0;

    //for case-sensitive strings
    string lowerText = text.ToLower();

    //Loop through each character in a string
    foreach (char x in lowerText) 
    {
        if (consonant.Contains(x)) 
        {
            count++;
        }
    }
    return count;
}


public static void Main(string[] args)
{
    //Output message to communicate to the user what to do
    Console.WriteLine("Enter a word or a sentence,then the program will help find the number of consonants in that word or string of words");

    //user to input string 
    string input = Console.ReadLine();

    //output the amount of consonants you have in your string
    Console.WriteLine($"\n{CountCons(input)} \nThere are  { CountCons(input)}  Consonants in your string");
}
