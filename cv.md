# Egor Isakovich
![asd](./img/qwe.jpg)<br>

### Links:
[GitHub](https://github.com/losker123) / [Telegram](https://t.me/Losker1) 
/ [Vk](https://vk.com/losker1)

# About me
I am currently a second-year student at the Faculty of Computer Science in Belarus. At this stage of my education, I am drawn towards the field of software development, with a particular interest in utilizing the C# programming language and the WinUI3 framework. While I have yet to gain practical work experience or participate in an internship, I am dedicated to participating in various projects to accumulate valuable hands-on experience.

Alongside my focus on specific technologies and tools, I am also committed to enhancing my logical thinking and problem-solving abilities. I actively involve myself in solving a variety of tasks, as this approach aids in the development of my analytical and solution-oriented skills.

Although I am currently inclined towards software development, I haven't fully decided on the specific direction I wish to pursue within the field. As I continue my studies and gain more exposure to different aspects of computer science, I am keeping an open mind and exploring various possibilities to determine my true passion and specialization.

## My stack of technologies 
 - C# 
 - WinUi 3
 - SQL ( MS SQL Server)
 - C++

## My projects
 - [RaidDesigner:](https://github.com/losker123/RaidDesigner.git)
An application on WinUI 3 that provides an opportunity to study and test your knowledge in the field of RAID technology

## Code example
Usage example Semaphore
```csharp
    static Semaphore semaphore = new Semaphore(0, 3);
   
    for (int i = 1; i <= 5; i++)
    {
        Thread thread = new Thread(DoWork);
        thread.Name = "Поток " + i;
        thread.Start();
    }

    Console.WriteLine("Нажмите Enter для продолжения...");
    Console.ReadLine();

    semaphore.Release(3);

    Console.WriteLine("Нажмите Enter для завершения...");
    Console.ReadLine();
    
    static void DoWork()
    {
        Console.WriteLine(Thread.CurrentThread.Name + " ожидает разрешения.");
        semaphore.WaitOne();

        Console.WriteLine(Thread.CurrentThread.Name + " получил разрешение и выполняет работу.");
        Thread.Sleep(2000);

        Console.WriteLine(Thread.CurrentThread.Name + " завершил работу и освободил разрешение.");
        semaphore.Release();
    }
}
```
