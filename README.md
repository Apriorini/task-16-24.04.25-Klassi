class Auto
{
    private string number;
    private int fuelAmount;
    private float fuelConsumption;
    public void info(string nom, float bak, float ras)
    {
        number = nom;
        fuelAmount = (int)bak;
        fuelConsumption = ras;
    }
    public void outinfo()
    {
        Console.WriteLine($"Номер автомобиля: {number}, Бензин(до заправки): {fuelAmount}, Расход: {fuelConsumption}");
    }
    public void zapravka(float top)
    {
        fuelAmount = fuelAmount + (int)top;
    }
    public void outinfo2() // Информация для удобства проверки как вам так и мне)
    {
        Console.WriteLine($"Номер автомобиля: {number}, Бензин(после заправки): {fuelAmount}, Расход: {fuelConsumption}");
    }
    public void voidmove(int km)
    {
        fuelAmount = fuelAmount - (int)((fuelConsumption / 100) * km);
    }
    public void ostatok()
    {
        Console.WriteLine($"Бензин(остаток): {fuelAmount}");
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
