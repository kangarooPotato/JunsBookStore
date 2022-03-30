*********************************************

Jun's Book Store MVC

Hyun-jun Lee
Student Number : 0770897

2022-03-08
Started the Prohject in VS19
ASP.NET Core MVC web app 2/ individual acct. authentication


*********************************************

2022-03-08

11:17
- Built it
- Created the README
- Test it

11:21 Confirmed the default app works!
11:28 Quickly modified the content of: View/Home/Index.cshtml



2022-03-09

14:21
- add some bootstrap files and modifided _Layout.cshtml, _LoginPartial.cshtml
- now I can see the bootstrap theme that i added. this Minty theme
- i feel fresh :D



2022-03-23

05:24
- I'm trying to work on my MacBook.
- brought a repo and it's working well


05:45
- added dropdown menu and toggle is not working..


05:59
- i dont know WHY....


12:51
- I copied all codes form bootstrap and paste, and it works!
- Let's move on to the next step!!



2022-03-29

11:45
- Due to Mac and Windows compatibility issues, I restarted working on Windows.
- I created a new branch from Drop Down part repo and tried to proceed with the work.


15:39
- EVERYTHING doesn't work............. :(


15:51
- even repo is getting weird. The README that I worked hard on disappeared
- Yes, so I wrote it AAAGGGAAAIIINNN


16:21
- Now is the moment I realized the importance of making comite and push a habit.
- USE BRAIN JUN.


16:57
- reset everything from the dropdown repo again!
- This is the seventh reset. trully


17:01
- I keep messing up the README file(by my mistake), so I'm going to write it down in my notepad, commit it, and then try to rewrite it.


17:09
- IT WORKED
- After modifying HomeController's namespace, I successfully loaded index pages without UI!


17:32
- yeee i got another error
- InvalidOperationException: The layout view '~/Views/Shared/_Layout' could not be located. The following locations were searched: ~/Views/Shared/_Layout


17:34
- i forgot adding ".cshtml" haha.
- now its working!!


18:08
- tried to merge this branch to main, but I failed completely.
- A copy branch that I had made just in case saved my life.


18:15
- added Admin area and remove Data, Models forlder
- Part 1 DONE.


18:34
- migration file name is "20220329223423_AddDefaultIdentityMigration.cs"
- database updated in PM Console.


18:37
- AddCatrgoryToDb successed


18:55
- Added Repository.cs and IRepository.cs


19:31
- error on ICategoryRepository.cs file ICategoryRepository


19:33
- Again, I typed wrong haha.
- and modified ISP_Call.cs file. this one here-> "public interface ISP_Call : IDisposable"


20:47
- done with SP_Call.cs and ISP_Call.cs.. its to hard for me. everytime it shows error and error


20:53
- I REALLY DONT KNOW WHAT'S WORNG
- GOD, THIS USING STAAAATMENTSSSSSS


21:34
- Let's send an e-mail to the professor before it's too late.


21:52
- i just made IUnitOfWork public and worked
- here is the link https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/compiler-messages/cs0311?f1url=%3FappId%3Droslyn%26k%3Dk(CS0311)
- Let's Move on to the Part 2 Category CRUD!!!


23:04
- YOOOOOOOOO NOW I CAN ACCESS TO https://localhost:44302/Admin/Category !!!!!
- but, i can't add category now haha.

23:34
- <i class="fa-duotone fa-pen-line"></i>&nbsp; <- dont know why. but this code is not working.


2022-03-30

00:24
- DataTables warning: table id=tblData - Ajax error. For more information about this error, please see http://datatables.net/tn/7
- i dont even know what taht means
- An unhandled exception occurred while processing the request.
- InvalidOperationException: The model item passed into the ViewDataDictionary is of type 'JunsBooks.Models.Category',
	but this ViewDataDictionary instance requires a model item of type 'System.Int32'.

01:13
- Ajax error.
- I'm garbage