## RoR: simple appointments management system

**Requirements** 

This is a simple appointments management system. It should have a web interface for customers and ability to integrate it through the REST JSON API with the 3rd party applications.

Here is a short list of specs we would like to be implemented. Everything what isn’t outlined here is up to you. Feel free to add anything necessary by your opinion.

* As a user I can register in the system (please put a few lines why you have chosen this implementation approach). 

* As a user I can see a list of my upcoming and past appointments.

* As a user I can create new appointment and with as many reminders as I need. 

* As a user in the web interface I can see a list of submitted appointments through the API and confirm or cancel them.

_​Key specs for objects(​remember, everything else is up to you)_ 

* Appointment has several statuses (pending/confirmed/canceled). 

* Let’s assume that appointment has a one hour length and can’t be overlapped by another one.

* Reminder has status (reminded or not), time to raise remind before appointment.

* Please add any other restrictions you think are fitable to system objects and don’t forget to describe a reason.

_​API_

* As a guest, if I know user API key, I can post request to create appointment on a specific date with defined reminder.

* As a quest, if I know user API key, I can receive the list of user appointments and filter it by date (let’s keep it simple, can specify only one day in params and receive appointments exactly during this day). 

* As a system I should be able to monitor API usage and store general statistics per each user. Please store type of request and its time.

* As a system I should be able to send reminders for appointments in the specified time.

**Technical notes**

* For each chosen technology like DB, Scheduling, Stats Collector, API responses builder try to describe what options are in general and why the option you have chosen is the best one here.

* The code quality should we perfect as well as timing of delivering this task.

* The code should be covered with unit, functional and integration tests (please use RSpec+Capybara). 

* Front-end can be pretty very simple. The source code of application should be uploaded on GitHub in the end.