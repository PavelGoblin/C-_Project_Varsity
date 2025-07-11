Garage Manager – ASP.NET Web Forms Project.
This project is an updated version of the GarageManager website, adapted to meet modern development standards and ensure compatibility with current systems. It serves as a comprehensive Garage Management System, facilitating the management of customers, vehicles, and service records.


Overview
The Garage Manager is a web-based application developed using ASP.NET Web Forms. It provides functionalities to manage customer information, vehicle details, and service histories, making it suitable for small to medium-sized garage businesses.



Features
Customer Management: Add, update, and delete customer records.
Vehicle Tracking: Maintain detailed information about customer vehicles.
Service Records: Log and manage service history for each vehicle.
Responsive Design: Utilizes Bootstrap for a mobile-friendly interface.
Database Integration: Employs Entity Framework for data operations.



Technologies Used
Frontend: HTML, CSS, Bootstrap, JavaScript, jQuery
Backend: C#, ASP.NET Web Forms
Database: SQL Server with Entity Framework
Development Environment: Visual Studio



Getting Started
Prerequisites
Visual Studio 2019 or later
SQL Server
.NET Framework 4.7.2 or higher







Installation
1.Clone the repository:
git clone https://github.com/PavelGoblin/C-_Project_Varsity.git

2.Open the solution:
Navigate to the cloned directory.
Open GarageManager.sln with Visual Studio.

3.Restore NuGet packages:
In Visual Studio, go to Tools > NuGet Package Manager > Package Manager Console.
Run the following command to apply migrations and update the database:
update-database

4.Run the application:
Press F5 or click on the Start button to build and run the project.









Screenshots
Here include screenshots of the application's interface  to showcase its features:
![Screenshot 2025-05-15 212753](https://github.com/user-attachments/assets/dd7ec132-f11c-4199-a814-34d3baa1982b)





About the Developer
Name: Ibrahim Pavel
University: Bangladesh Open University
Department: Computer Science and Engineering (CSE)
Project Type: Web-based Application
Semester: 5th/3rd year 1st semester






Developer Experience:
While working on this project, I gained valuable hands-on experience with the ASP.NET Web Forms framework and overall system development.
Some parts of the project were quite challenging — especially understanding the page lifecycle in Web Forms and configuring proper communication between layers in a multi-tier architecture. Getting the Entity Framework to work correctly with the SQL Server database also took some trial and error, particularly with managing relationships between customer and vehicle entities.
On the other hand, designing the frontend interface using Bootstrap/tailwind and Web Forms controls felt more intuitive. Creating the forms for adding and updating customers or vehicles was relatively easier once I understood how to use the built-in controls effectively.
Debugging was a major learning opportunity. I faced several issues related to data not being saved correctly or forms not updating as expected, which taught me how to trace logic flow, use breakpoints efficiently, and solve real-life issues systematically.

This project significantly improved my understanding of:

- Implementing multi-layered architecture in ASP.NET Web Forms.
- Managing scripts and lifecycle events on different pages.
- Creating data-driven interfaces using WebForms controls.
- Performing CRUD operations using Entity Framework.
- Structuring real-world web applications from scratch.

Overall, this project helped reinforce core software development concepts and strengthened my confidence in handling both frontend and backend responsibilities in a full-stack C# environment.






Notes
This project was created for learning and academic purposes. Feel free to modify and use it for similar educational tasks.



Folder-wise Explanation

1.App_Start

* এই ফোল্ডারে সাধারণত শুরুতে রান হওয়া কোড থাকে।
* যেমনঃ RouteConfig.cs, BundleConfig.cs ইত্যাদি – অ্যাপের Routing বা Resource bundling এখানে কনফিগার হয়।

2. Content

* CSS, custom stylesheets, site-wide ডিজাইন ফাইল থাকে।
* উদাহরণঃ `Site.css` – আপনার ওয়েবসাইটের রঙ, ফন্ট, লে-আউট ইত্যাদি।

3.Images

* ওয়েবসাইটে ব্যবহৃত সকল ছবি এখানে থাকে।
* যেমনঃ লোগো, ব্যানার, ব্যাকগ্রাউন্ড ইত্যাদি।

 4. Migrations

* Entity Framework Code First ব্যবহার করলে database এর ইতিহাস (migrations) এখানে রাখা হয়।
* Example: Add-Migration, Update-Database কমান্ড এর কাজের রেকর্ড।

5. Models

* সকল Data Model (class) এখানে থাকে।
* যেমনঃ `Customer.cs`, `Vehicle.cs`, `Service.cs` ইত্যাদি ক্লাস – ডেটার স্ট্রাকচার ব্যাখ্যা করে।

6. Pages

* সম্ভবত আপনার কাস্টম ইউআই পেইজগুলো এখানে আছে (যদি থাকে) – যেমনঃ নতুন পেইজ ডিজাইন, report page, user dashboard ইত্যাদি।

7.Properties

* `AssemblyInfo.cs` ইত্যাদি ফাইল থাকে যা প্রজেক্টের metadata সংরক্ষণ করে (version, author ইত্যাদি)।

8.Repositories

* ডেটাবেইস অপারেশনের জন্য repository pattern ব্যবহার করা হয়েছে।
* যেমনঃ `ICustomerRepository`, `CustomerRepository` ইত্যাদি – এতে CRUD method (Create, Read, Update, Delete) থাকে।

9. Scripts

* JavaScript ফাইল থাকে (site.js, validation.js, jQuery ইত্যাদি)।
* ক্লায়েন্ট-সাইড লজিক বা ইন্টারঅ্যাকশন নিয়ন্ত্রণ করে।

---

📄 File-wise Explanation (Main Web Pages and Configurations)

  1)   About.aspx / Default.aspx

* WebForms পেজ, যেগুলো HTML + Server Controls দিয়ে তৈরি।
* `About.aspx` → About Us পেইজ।
* `Default.aspx` → Home page।

2)    .cs and .designer.cs ফাইলসমূহ

* `aspx.cs` → C# কোড (code-behind) যা user interaction হ্যান্ডেল করে।
* `aspx.designer.cs` → অটোমেটিক জেনারেটেড partial class, যা server control গুলোর declaration রাখে।

3)    GarageManager.csproj

* পুরো প্রজেক্টের configuration ফাইল (build info, references, project settings)।

4)   Global.asax / Global.asax.cs

* ওয়েব অ্যাপের Life Cycle events (Start, End, Error) হ্যান্ডেল করে।
* যেমনঃ Application\_Start(), Session\_Start()।

5)  Site.Master / Site.Mobile.Master

* MasterPage ফাইল যা একটি common layout তৈরি করে (header, footer, menu)।
* Desktop ও Mobile view আলাদা MasterPage ব্যবহৃত হচ্ছে।

6)     ViewSwitcher.ascx

* এটি একটি UserControl যা মোবাইল/ডেস্কটপ ভিউ পরিবর্তনের UI দিতে পারে।

7)    Web.config / Web.Debug.config / Web.Release.config

* প্রধান configuration ফাইল (Database connection, app settings, authentication, authorization)।
* `Debug` ও `Release` configuration আলাদা পরিবেশে ব্যবহার হয়।

8)   favicon.ico

* ব্রাউজার ট্যাবে ওয়েবসাইটের আইকন।

9)   libman.json

* Client-side library manager configuration ফাইল।
* Bootstrap/jQuery এর version & source নির্ধারণ করে।

10)   packages.config

* NuGet প্যাকেজের লিস্ট ও version info।

---

সাধারণভাবে এই GarageManager কী ধরনের কাজ করে?

এই প্রজেক্টের নাম এবং স্ট্রাকচার দেখে ধারণা করা যায় এটি একটি "Garage Management System", যেখানে হতে পারে:

Customer info management
Vehicle info tracking
Service records (repair/maintenance)
Reports and Dashboard
Authentication system (optional)

---




SCREENSHOT:
1.
![WhatsApp Image 2025-07-11 at 1 53 17 AM](https://github.com/user-attachments/assets/72dda45c-49d7-4994-80eb-b28570dbbc04)
2.
![WhatsApp Image 2025-07-11 at 1 53 18 AM](https://github.com/user-attachments/assets/62e3ecb3-7fbb-448c-a9b4-d4d9468b1d69)
3.
![WhatsApp Image 2025-07-11 at 1 53 19 AM](https://github.com/user-attachments/assets/fad812a9-be82-4aa6-9881-7a7df500c6de)
4.
![WhatsApp Image 2025-07-11 at 1 53 20 AM](https://github.com/user-attachments/assets/e5363004-83ef-4549-b570-42592d52c699)
5.
![WhatsApp Image 2025-07-11 at 1 53 20 AM (1)](https://github.com/user-attachments/assets/d4368128-f158-47aa-b53f-7f0f85cdb49f)
6.
![WhatsApp Image 2025-07-11 at 1 53 21 AM](https://github.com/user-attachments/assets/e9b83c30-da42-4257-8b43-b02615d4a2fa)
7.
![WhatsApp Image 2025-07-11 at 1 53 21 AM (1)](https://github.com/user-attachments/assets/14e8ebde-8944-410e-aaf9-0f93f6063a42)
8.
![WhatsApp Image 2025-07-11 at 1 53 22 AM](https://github.com/user-attachments/assets/aaddcda3-b30b-47ad-b833-6b414e350fd0)
9.
![WhatsApp Image 2025-07-11 at 1 53 23 AM](https://github.com/user-attachments/assets/d30b047f-03e9-4aa6-b6e4-ad48ceb5baf3)
10.
![WhatsApp Image 2025-07-11 at 1 53 23 AM (1)](https://github.com/user-attachments/assets/5c067bdd-1438-417a-a26d-40d628d90c47)
11.
![WhatsApp Image 2025-07-11 at 1 53 23 AM (2)](https://github.com/user-attachments/assets/154230cd-dcfc-4616-9473-043eb3b8db0b)
12.
![WhatsApp Image 2025-07-11 at 1 53 25 AM](https://github.com/user-attachments/assets/bb7b5e8b-d184-4f52-9f1e-da5515039317)
13.
![WhatsApp Image 2025-07-11 at 1 53 25 AM (1)](https://github.com/user-attachments/assets/eadb853e-81d3-4165-8b5f-3f0b9dc0db32)
14.
![WhatsApp Image 2025-07-11 at 1 53 26 AM](https://github.com/user-attachments/assets/3c64b69f-c8b8-41ab-91cb-cb8edc7a92ce)
15.
![WhatsApp Image 2025-07-11 at 1 53 26 AM (1)](https://github.com/user-attachments/assets/4d0f7cd4-3d80-4e1e-a0b9-6e4e77b86891)
16.
![WhatsApp Image 2025-07-11 at 1 53 26 AM (2)](https://github.com/user-attachments/assets/9ac9d3ea-af4a-49ec-9e33-e66d5c060eef)
17.
![WhatsApp Image 2025-07-11 at 1 53 27 AM](https://github.com/user-attachments/assets/3e7fdfb0-ba3a-4a81-96f2-826f918beb64)
18.
![WhatsApp Image 2025-07-11 at 1 53 27 AM (1)](https://github.com/user-attachments/assets/24bed401-e61a-4402-93cc-e40dac089a88)
19.
![WhatsApp Image 2025-07-11 at 1 53 27 AM (2)](https://github.com/user-attachments/assets/c5665f83-9384-4d3e-a416-672aa54cc8c2)
20.
![WhatsApp Image 2025-07-11 at 1 53 28 AM](https://github.com/user-attachments/assets/862b1d68-c2ae-4d2d-a33a-2f6b2a46452b)
21.
![WhatsApp Image 2025-07-11 at 1 53 28 AM (1)](https://github.com/user-attachments/assets/97443363-9081-4c95-81c3-d5b6eceb50d0)
22.
![WhatsApp Image 2025-07-11 at 1 53 29 AM](https://github.com/user-attachments/assets/377e0398-5826-4cda-8577-6ea2e3ab18ff)






























