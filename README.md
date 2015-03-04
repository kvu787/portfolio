Here are some of the things I've built, organized by language:

# boost - asteroid evasion game (Go)

[Github project](https://github.com/kvu787/boost)

A simple game where you avoid asteroids while trying to slip between them. 

![Screen shot of boost](https://raw.githubusercontent.com/kvu787/portfolio/master/images/boost.png)

# Simple programmable robot (C) (work in progress)

A simple Arduino robot. Basic instructions can be loaded into the robot through the breadboard control interface.

![Screen shot of robot](https://raw.githubusercontent.com/kvu787/portfolio/master/images/robot2.png)

# LL1 Parser (Go)

Library to parse LL1 grammars.

[Source](https://bitbucket.org/kvu787/ll1)

# Simple robot (C)

A simple Arduino robot. Each motor can be controlled independently by sending commands over the serial monitor during runtime.

Transistors are used to vary on-off cycles to simulate different current levels for each motor.

[Source](https://bitbucket.org/kvu787/robot)

![Screen shot of robot](https://raw.githubusercontent.com/kvu787/portfolio/master/images/robot.png)

# Go Schedule (Go)

Go Schedule is an open source library to extract data from the UW time schedule and a web application that uses that library.

[GitHub project](https://github.com/kvu787/goschedule/)

![Screen shot of GoSchedule](https://raw.githubusercontent.com/kvu787/portfolio/master/images/goschedule.png)

### Code sample

[Source](https://github.com/kvu787/goschedule/blob/master/lib/database.go)

The following method executes a `SELECT` operation with an arbitrary Go struct and a database connection. 

It uses Go's reflection package to determine the table names and columns to query based on the provided struct.

By facilitating basic object relational mapping, we can easily query the database like this:

	type Turkey struct {
		Intelligence int
		Power string
	}

	db, err := sql.Open("postgres", "user=macdonald dbname=aminals password=chicken sslmode=require")
	if err != nil {
		fmt.Printf("sql.Open err: %v", err)
	}

	turkeyRecords, err := goschedule.Select(db, Turkey{})
	if err != nil {
		fmt.Printf("goschedule.Select err: %v", err)
	}
	
	processTurkeys(turkeyRecords.([]Turkey))

# Unicool (Javascript)

Library to convert to and from commonly used bases and encodings in Unicode.

Runs an interactive Unicode tutorial I made with AngularJS. 

To view the tutorial, pull the [GitHub repo](https://github.com/kvu787/unicool) and open `index.html` in your browser.

### Code sample

[Source](https://github.com/kvu787/unicool/blob/master/unicode.js)

Usage:

	// The many forms of € (unicode character point '20ac')

	// hex to int 
	unicodeConvert('20ac', datatypesEnum.HEX, datatypesEnum.INT) === '8364';
	// int to utf8
	unicodeConvert('8364', datatypesEnum.INT, datatypesEnum.UTF8) === '111000101000001010101100';
	// utf8 to binary
	unicodeConvert('111000101000001010101100', datatypesEnum.UTF8, datatypesEnum.BIN) === '10000010101100';
	// binary to hex
	unicodeConvert('10000010101100;, datatypesEnum.BIN, datatypesEnum.HEX) === '20ac';

# Wingman (C#, ASP.NET)

Project for Microsoft Research. Code is not open source, but the [web app](http://wingman.azurewebsites.net/) can be publicly accessed.

![Screen shot of Wingman](https://raw.githubusercontent.com/kvu787/portfolio/master/images/wingman.png)

# Teens In Public Service (TIPS) Timesheet Manager (Ruby on Rails)

Web application for TIPS interns to submit timesheets and for administrators to approve them. 
Uses MailChimp to send emails and Cucumber for automated testing.
Code is not open source and website is not available to the public.

![Screen shot of TIPS timesheet manager](https://raw.githubusercontent.com/kvu787/portfolio/master/images/tips.png)
