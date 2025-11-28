# Method
```
internal class Program
{
    private static void Main(string[] args)
    {
        Random juhuarv = new Random();
        Console.WriteLine("Kas sa tahad münti visata, või täringut veeretada?");
        string kasutajaValik = Console.ReadLine();
        if (kasutajaValik == "münti")
        {
            Console.WriteLine(Münt(juhuarv));
        }
        else if (kasutajaValik == "täringut")
        {
            Console.WriteLine(Täring(juhuarv));
        }
        else
        {
            Console.WriteLine("Ei tea sellist vastust");
        }
        // NewMessage(); ...
    }

    private string Täring(Random juhuarv)
    {
        // tee uuus täringuvise ja tagasta juhuarv abil tulemus kasutajale
        //int täringuvise = juhuarv.Next(1,6);
        return juhuarv.Next(1,6);
    }

    static string Münt(Random thing)
    { 
        int mündivise = thing.Next(1,2);
        if (mündivise == 1)
        {
            return "kull";
        }
        else if (mündivise == 2)
        {
            return "kiri";
        }
        return "serv";
    }
}
