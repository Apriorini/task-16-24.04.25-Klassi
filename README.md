class Auto
{
    private string number;
    private int ostatoktopl;
    private float rashodtopl;
    public void info(string nom, float bak, float ras)
    {
        number = nom;
        ostatoktopl = (int)bak;
        rashodtopl = ras;
    }
    public void outinfo()
    {
        Console.WriteLine($"Номер автомобиля: {number}, Бензин(до заправки): {ostatoktopl}, Расход: {rashodtopl}");
    }
    public void zapravka(float top)
    {
        ostatoktopl = ostatoktopl + (int)top;
    }
    public void outinfo2() // Информация для удобства проверки как вам так и мне)
    {
        Console.WriteLine($"Номер автомобиля: {number}, Бензин(после заправки): {ostatoktopl}, Расход: {rashodtopl}");
    }
    public void voidmove(int km)
    {
        ostatoktopl = ostatoktopl - (int)((rashodtopl / 100) * km);
        Console.WriteLine($"Авто проехало: {km} км");
    }
    public void ostatok()
    {
        Console.WriteLine($"Бензин(остаток): {ostatoktopl}");
    }
}
class Program
{
    static void Main(string[] args)
    {
        Auto car = new Auto();
        car.info("1", 50.5f, 8.0f);
        car.outinfo();
        car.zapravka(5.0f);
        car.outinfo2();
        car.voidmove(500);
        car.ostatok();
    }
}
