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



---------------------------------------------------------------------------------------
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


---------------------------------------------------------------------------------------
2022-04-05

10:52
- I still don't know what the problem is.
- An unhandled exception occurred while processing the request.
InvalidOperationException: The model item passed into the ViewDataDictionary is of type 'JunsBooks.Models.Category', but this ViewDataDictionary instance requires a model item of type 'System.Int32'.
Microsoft.AspNetCore.Mvc.ViewFeatures.ViewDataDictionary.EnsureCompatible(object value)


17:53
- oh god, I found the reason!!!!!!!!!!!!!!!!!!!!!!!!!


17:57
- First, at the top of the file "_CreateAndBackToListButton.cshtml", there was a code called "@modelint"
- This code was also found in the file "_EditAndBackToListButton.cshtml" and was caused by pasting because they were both similar codes.
- 100% my fault.
- This is the first time I felt the 'REAL' tingle.
- and the "AddCategoryToDb" was empty. so i put some code in there
- on PM console, update-database, it works! now i can see the "dbo.Categories" :D


19:20
- Everything works fine.


19:31
- No, it's not


21:17
- I keep forgetting things when I add tables, so I'll put them in Korean first.

1. 모델 프로젝트에 추가하고싶은 테이블 .cs파일로 생성
2. PM 콘솔 켜고 .DataAccess 기본 프로젝트 설정한 후 add-migration +Add뭐시기ToDb로 마이그래이션 추가
3. 비어있을테니 다른 에드뭐시기투디비 보고 복붙한 후 복수형으로 똑같이 바꾸기
4. ApplicationDbContext.cs 파일 가서 public DbSet<뭐시기> 뭐시기복수형 { get; set; } 똑같이 추가하기
5. PM 콘솔에서 update-database 하기
6. Make "~~Repository.cs" and "I~~Repository.cs" in the folders.
7. add interface in the "IUnitOfWork.cs" and add "public I~~Repository ~~ { get; protected set; }" in the "UnitOfWork.cs"
8. make ~~Controller.cs in the 'Areas/Admin/Controller' 똑같이 만들기
9. make ~~folder in the 'Areas/Admin/Views' and put in "index.cshtml" + ~.js and ~~Upsert.cs files
10. add link on the nav bar

21:24
- added "dbo.CoverTypes"

21:37
- error again
- System.NullReferenceException
  HResult=0x80004003
  message=Object reference not set to an instance of an object.
  source=JunsBookStore
  StackTrace:
   at JunsBookStore.Areas.Admin.Controllers.CoverTypeController.GetAll() in C:\Users\JUN\Documents\GitHub\JunsBookStore\JunsBookStore\Areas\Admin\Controllers\CoverTypeController.cs:line 71

- error again
- Request URL: https://localhost:44302/Admin/CoverType/coverUpsert
Request Method: GET
Status Code: 405 
Remote Address: [::1]:44302
Referrer Policy: strict-origin-when-cross-origin
allow: POST
date: Wed, 06 Apr 2022 03:37:27 GMT
server: Microsoft-IIS/10.0
x-powered-by: ASP.NET
:authority: localhost:44302
:method: GET
:path: /Admin/CoverType/coverUpsert
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: en-US,en;q=0.9,ko-KR;q=0.8,ko;q=0.7
cookie: .AspNetCore.Antiforgery.OzeIPsRERUM=CfDJ8JJ8xuuY611EjtKmgVFQzppTluM7I7OP1FEd5cQF72xxOVcETm3D1lAIdVrl6PriIE76o4oQpghllHnN0F2LnTPl0xSWzTEA8MRspAzDdCxm5HzOYruChSpUI24Wv9GjQyLZTTFntNM4rdEDU51UEQ0
referer: https://localhost:44302/Admin/CoverType
sec-ch-ua: " Not A;Brand";v="99", "Chromium";v="100", "Google Chrome";v="100"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: same-origin
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/100.0.4896.60 Safari/537.36

- it's 405 error. maybe there must be a simple way


23:47
- it was upsert code error in the controller file.
- now we can add cover type now!


23:52
- now im adding Product stuff.
- migration timestamp here! 20220406035334_AddProductToDb.cs


2022-04-06

00:17
- add ProductRepository + IPro..cs and product.js
- and i made Product folder in the Areas/Admin/Views but its for morning..
- good ngiht! :D

00:36
- just few more things.
- add some product stuff (index, nav bar, controller, js )

01:25
- System.InvalidOperationException: 'An error was generated for warning 'Microsoft.EntityFrameworkCore.Query.InvalidIncludePathError': Unable to find navigation ' CoverType' specified in string based include path ' CoverType'. This exception can be suppressed or logged by passing event ID 'CoreEventId.InvalidIncludePathError' to the 'ConfigureWarnings' method in 'DbContext.OnConfiguring' or 'AddDbContext'.'
- error again.

08:47
- same error... hmm
- System.InvalidOperationException
  HResult=0x80131509
  Message=An error was generated for warning 'Microsoft.EntityFrameworkCore.Query.InvalidIncludePathError':
  Unable to find navigation ' CoverType' specified in string based include path ' CoverType'.
  This exception can be suppressed or logged by passing event ID 'CoreEventId.InvalidIncludePathError'
  to the 'ConfigureWarnings' method in 'DbContext.OnConfiguring' or 'AddDbContext'.
  Source=Microsoft.EntityFrameworkCore

09:35
- Don'n know why Product Create is not working
- Part 3 fail.
- oh and this is my tiny.cloud link

<script src="https://cdn.tiny.cloud/1/bws62ht2ocrfai3tnan7ogir4tpy26jmeondamxxv5gi4bg0/tinymce/5/tinymce.min.js" referrerpolicy="origin"></script>

-------

2022-04-12

11:22
- same error

System.InvalidOperationException
  HResult=0x80131509
  Message=An error was generated for warning 'Microsoft.EntityFrameworkCore.Query.InvalidIncludePathError': Unable to find navigation ' CoverType' specified in string based include path ' CoverType'. This exception can be suppressed or logged by passing event ID 'CoreEventId.InvalidIncludePathError' to the 'ConfigureWarnings' method in 'DbContext.OnConfiguring' or 'AddDbContext'.

Error	CS1520	Method must have a return type	JunsBooks.DataAccess	C:\Users\W0770897\Documents\GitHub\JunsBookStore\JunsBooks.DataAccess\Repository\CoverTypeRepository.cs	15	Active

and if i trying to keep running this code

ajax error comes out
http://datatables.net/tn/7


11:29
- in the Areas\Admin\Controllers file "var allObj = _unitOfWork.Product.GetAll(includeProperties: "Category,CoverType");"
there was a space between "Category, CoverType"); <-like this.. and i remove it
- now it works!

11:32
- ajax error!
- DataTables warning: table id=tblData - Requested unknown parameter 'price' for row 0, column 2. For more information about this error, please see http://datatables.net/tn/4

11:39
- if i ignore the error and keep running it shows up

- Microsoft.EntityFrameworkCore.DbUpdateException
  HResult=0x80131500
  Message=An error occurred while updating the entries. See the inner exception for details.
  Source=Microsoft.EntityFrameworkCore.Relational
  This exception was originally thrown at this call stack:
    [External Code]

Inner Exception 1:
SqlException: The INSERT statement conflicted with the FOREIGN KEY constraint "FK_Products_CoverTypes_CategoryId". The conflict occurred in database "aspnet-JunsBookStore", table "dbo.CoverTypes", column 'Id'.
The statement has been terminated.

-----
2022-04-19


16:53

- The same error kept appearing, so I deleted all of the databases and recreated them.
- I re-created dbo.Product by changing the FOREIGN KEY code because it seems like a problem connecting the FOREIGN KEY between CoverType and Product.

- Everything works better than I thought.

- Various kinds of items can be put into categories and cover types.

- The problem is that the generated data has an ID number that is sometimes skipped. The bigger problem is that the ID starts at 1001 once.

- I erased all the databases and restarted them, so there's no problem, but I'm not sure when this will happen again.

- But if I update database again, ID starts from 1, so I understand that there is no big problem with the code :D


5:12

- Remove the dummy link from the navigation and leave it in a clean layout

- Time to make product and show to home page


5:28

- namesapce of the ProductComtroller.cs was JunsBookS'o'tore.Areas.Admin.Controllers
- Sotore? oh my english.....

19:19

- cant add my img on the db.. is this upsert problem??? i dont think so...


19:47

- nope it's controller problem!

- I wrote a code to add A to the database. its in the ProductController

19:51

- I made a list of Categories/Genres.

- The cover types are hardcover, softcover, and no cover.

- and the books

--- Categories ----

Action and Adventure
Classics
Comic Book or Graphic Novel
Cookbooks
Detective and Mystery
Fantasy
History
Historical Fiction
Horror
Literary Fiction
Transdisciplinary non-fiction
Poetry	
Romance
SF

--- Cover Types ---

Hard Cover
Soft Cover
No Cover

--- Book list ---

Title : It Ends with Us
ISBN : 9781501110368
Author : Colleen Hoover
In this “brave and heartbreaking novel that digs its claws into you and doesn’t let go, long after you’ve finished it” (Anna Todd, New York Times bestselling author) from the #1 New York Times bestselling author of All Your Perfects, a workaholic with a too-good-to-be-true romance can’t stop thinking about her first love.
Price : $11.99
Category : Romance


Where the Crawdads Sing
9786057879134
Delia Owens
For years, rumors of the “Marsh Girl” haunted Barkley Cove, a quiet fishing village. Kya Clark is barefoot and wild; unfit for polite society. So in late 1969, when the popular Chase Andrews is found dead, locals immediately suspect her.
$19.99
Literary fiction


The Seven Husbands of Evelyn Hugo
9788416517275
Taylor Jenkins Reid
Aging and reclusive Hollywood movie icon Evelyn Hugo is finally ready to tell the truth about her glamorous and scandalous life. But when she chooses unknown magazine reporter Monique Grant for the job, no one is more astounded than Monique herself. Why her? Why now?
$14.99
Historical fiction


1984 (nineteen eighty-four)
9780140817744
George Orwell
Among the seminal texts of the 20th century, Nineteen Eighty-Four is a rare work that grows more haunting as its futuristic purgatory becomes more real. Published in 1949, the book offers political satirist George Orwell's nightmarish vision of a totalitarian, bureaucratic world and one poor stiff's attempt to find individuality. The brilliance of the novel is Orwell's prescience of modern life—the ubiquity of television, the distortion of the language—and his ability to construct such a thorough version of hell. Required reading for students since it was published, it ranks among the most terrifying novels ever written.
$12.79
SF


Guns, Germs, and Steel: The Fates of Human Societies
9780393317558
Jared Diamond
"Diamond has written a book of remarkable scope ... one of the most important and readable works on the human past published in recent years." Winner of the Pulitzer Prize and a national bestseller: the global account of the rise of civilization that is also a stunning refutation of ideas of human development based on race.
$19.99
Transdisciplinary non-fiction

20:50

- done!