# Welcome PHP Vegas!!!

Today we are going to be crafting a basic appliation inside of laravel. We will be making use of a few different pieces of laravel, and my hope is that if you follow this, you will know enough about this awesome framework to go out and create the next master piece of the open web!

# What Are We Working With?

This is a simple test application which is a brand-new instance of the laravel 5.2 framework. We will be crafting a simple auth system, a couple of migrations, an artisan command and a nitty gritty ui to display what we have made.

Lets get started!

# Generating Auth

First things first. Go ahead and clone down this repository. Before we go any further, go ahead and change directory into your new project. From there run the following command.

	php artisan serve

This is going to start up a web server for our application and it will get you looking at a screen. This is going to do nothing right now. All you'll see is some nice clean text to look at.

For right now kill that process by pressing

	ctrl+c

and issue the following command

	cp .env.example .env
	php artisan key:generate

Then open up your new file inside of your text editor. From there go ahead and setup the variables inside of the file. For right now, just focus on getting your DB connection set so we can run some migrations.

Once we have the DB hooked up, go ahead and issue the following commands.

	php artisan make:auth
	php artisan migrate

What the first commands does, is genenrate a basic scaffolding for an authentication system, and the migrations that go along with it. The second command takes those migrations and runs them, creating the table inside of the database.

After these have been executed and complete with no issues, execute the following command.

	php artisan serve

This will start up the server again, this time with your environment file loaded, and you'll be placed inside of your new auth ready application!

Step 1 Complete!

# Setting Up The Build Process