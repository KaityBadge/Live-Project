# Tech Academy Live-Project

## Introduction
**Role:** Developer

&emsp; This project was developed during a two-week sprint by a collaborative team of developers using ASP.NET MVC and Entity Framework. 
Our goal was to build an interactive website for a theatre and acting company that allows non-technical users to easily manage website content and productions.
<br> 
This application is designed to:
- Provide a user-friendly content management system
- Support subscriber login functionality
- Maintain a wiki of past performances and performers

## Project Overview
We followed an Agile/Scrum methodology
- Daily stand-ups
- Sprint planning sessions
- Sprint retrospectives

&emsp; This process simulated a real-world, organized, and collaborative development environment.
Each team member worked on individual stories. My focus was on the front-end development of the rental history feature, ensuring a clean, 
intuitive user interface for users to review and interact with rental data.

## Core Technologies
- Front-end: HTML, CSS, JavaScript
- ASP.NET MVC
- Entity Framework
- Version Control: Git, GitHub
- Azure DevOps

## User Stories
1. [Create Entity Model](#create-entity-model)
2. [Create & Edit View](#create--edit-view)
3. [Index View](#index-view)
4. [Sorting Rental History](#sorting-rental-history)
##

*Jump To: [Introduction](#introduction), [Project Overview](#project-overview), [Core Technologies](#core-technologies), [User Stories](#user-stories), [Create Entity Model](#create-entity-model), 
[Create & Edit View](#create--edit-view), [Index View](#index-view), [Sorting Rental History](#sorting-rental-history), [Key Skills](#key-skills--lessons-learned)*

### Create Entity Model
&emsp; I was responsible for designing and implementing the RentalHistory entity model to support data persistence within the application. I created and defined a new class called RentalHistory 
in the Models folder to represent the data structure for rental records in the database. Since this project uses a code-first approach with Entity Framework, the database schema was automatically 
generated and kept in sync based on the model I defined. This allowed for a streamlined development process, where changes to the data structure could easily be maintained through code. 
Once the model was created, I used Visual Studio's scaffolding tools to generate the CRUD pages. During this process, I selected and shared the Layout.cshtml file as the layout page to maintain 
visual consistency across the site. 


### Create & Edit View
&emsp; This story was relatively simple however I still ran into some styling challenges for the Create and Edit pages, specifically with overriding Bootstrap classes.
My page layout was as I intended, though Bootstraps default styling gave it a few unexpected adjustments. I resolved this issue by applying my own custom formatting 
in Rent.css that would override specific Bootstrap styles. Additionally, I implemented a bit of front-end logic in Rent.js. This script adds dynamic behavior to the 
RentalDamaged checkbox. When the checkbox is selected, the label for DamagesIncurred will change to display "Damages Incurred"; when the checkbox is unchecked, 
the label will switch to display "Notes". This improved the forms usability by providing context-specific labeling based on user input. 

![Create and Edit CSS GIF](Media/checkbox.gif)

![Create and Edit View JS](Media/CheckBoxLogic.png)

### Index View
&emsp; In this story I fully customized the Index page to show all of the Rental Histories in tabular form. I stylized the table similar to the Create and Edit views 
with a few minor adjustments using Bootstrap components and customized css classes. I used Font-Awesome for the status icons that displayed next to each rental-- 
a green checkmark for undamaged rentals and a red X for the damaged rentals. The rental name is displayed next to the icon using a Bootstrap badge, helping it stand out within the cell. 
I changed the text behavior of DamagesIncurred text by using a text-muted class, to have text greyed out if the rental was not damaged. Finally, I truncated the text with an ellipsis(...) 
if the text was too long and exceeded the width of the cell to prevent it from wrapping to a new line. To add a more visually appealing format, I put a vertical ellipsis on the right 
side of each row which will appear when a user hovers over a row. This vertical ellipsis was completed with a dropdown menu to show Edit, Details, and Delete options.

![Index View GIF](Media/details.gif)


### Sorting Rental History
&emsp; My final story of the sprint consisted of enhancing the usability of the Index page. I implemented dynamic client-side sorting for rental history records using vanilla JavaScript, 
allowing users to filter and sort entries without reloading the page. The sorting method uses data-damaged attributes to filter through damaged or undamaged rentals. I also used 
localeCompare method on the data-title attribute to sort the rentals alphabetically. 

![Sorting Rental History GIF](Media/SortBy.gif)

![Sorting Rental History JS](Media/SortLogic.png)


## Key Skills & Lessons Learned

### Scrum Development
I gained hand-on experience working within a Scrum framework by actively participating in spring planning sessions, daily stand-ups, and retrospectives. Daily stand-ups proved essential for 
team alignment and collaboration. For instance, a teammate and I encountered similar debugging issues in Visual Studio and were able to support each other in resolving them. This experience
taught me the importance of organization, preparedness, and timely communication to improve overall team efficiency. 

### Front-End Development
Using HTML, CSS, and JavaScript, I developed responsive and accessible user interfaces aligned with project requirements and design guidelines. I refined my attention to detail and problem-solving
skills through iterative testing and adjustments to achieve the desired behavior or UI elements. This process required patience, adaptability, and a willingness to learn from trial and error. 

### Version Control
I used Git to manage version control and maintain a clean, collaborative workflow. This included creating and managing feature branches, resolving merge conflicts, and following best practices.
Utilizing Git allowed for efficient collaboration and ensured code integrity throughout the development lifecycle. 

### Problem Solving & Debugging
Debugging was one of the most challenging and rewarding aspects of the project. I often engaged in extensive independent research to troubleshoot issues and identify solutions. Over time, I learned 
to balance self-reliance with collaboration by knowing when to seek guidance from mentors or fellow developers, which greatly improved my problem-solving efficiency.
