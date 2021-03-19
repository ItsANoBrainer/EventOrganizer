# Event Organizer by ItsANoBrainer - v1.1.2

![](https://i.imgur.com/4bKaAY8.png)

This program will take an input .CSV data file containing presenters and information and requirements about them, an input .CSV settings file containing settings for the event, an optional seed, and then create an output .CSV file that has all the presenters organized into days, timeslots, and rooms based on them. On an algorithm level, it does the following:
```
- If the presenter has a required day/timeslot/room, it will assign them first.
- Reserves multiple timeslots for presenters that have an presentation thats lasts multiple hourly timeslots
- Randomly assigns remaining presenters, making sure two presentations in the same timeslot do not have the same primary presenter. (Future feature to make this all presenters assigned to that presentation.)
```

## Getting Started

These instructions will show you how to download the application, install it to your computer, and then run/use the application.

### Prerequisites

Currently the only prerequisites are a Windows OS, as the only installation file available is a .EXE. MacOS and Linux versions are readily available for publishing on each version release if wanted.

```
Windows OS [✔]
MacOS [✔]
Linux [✘]
```

### Installing

Download your OS installation file.

Windows OS - [Download](https://github.com/ItsANoBrainer/EventOrganizer/raw/master/EventOrganizerInstaller.exe)

```
For Windows you will only need to download the EventOrganizerInstaller.exe and run it on your computer.
To download, select the download button above.
When ran, you will get a popup saying windows prevented an app from starting. Click "More Info" and then Run anyway. 
After the install finishes, you will get a shortcut on your desktop, as well as be able to search it from the start menu.
```

MacOS - [Download](https://github.com/ItsANoBrainer/EventOrganizer/raw/master/EventOrganizer.dmg)

```
For MacOS you will only need to download the EventOrganizerInstaller.dmg and run it on your computer.
To download, select the download button above.
When ran, drag the EventOrganizer.dmg to your Applications folder. You will get a popup saying "EventOrganizer" is an app downloaded from the internet. You will need to allow the install. Go to the search menu and type "Security & Privacy". Under the general tab at the bottom it will say "EventOrganizer" was blocked. Click the Open Anyway button.
```

Linux - Available by Request

```
For Linux you will only need to download the Linux installer above and run it on your computer.
When available, you can do so from the download button above.
```

### How to Use Event Organizer

1. Select the input .CSV data file.
2. Select the input .CSV settings file.
3. (Optional) Type in a seed to use. You can include a string of characters to make the program always create the same assignments. Example: Setting the seed to "Duck" before creating will always make the assignments the same for anyone using the program with the seed "Duck".
4. Click create to create and choose where to save the output .CSV file.

#### Getting the .CSV files
Getting the .CSV files from a Google Doc:
```
1. Navigate to the desired google sheet
2. Select File > Download > Comma-separated values (.CSV)
```
This will create a .CSV for the current sheet. 

#### .CSV File Requirements

The .CSV input files have the following required column headers.

##### Presenter Data .CSV File

```
-P1 First Name
-P1 Last Name
-Title
-Audience
-Type
-Required Day
-Required Time
-Length
-Required Room
```
##### Event Settings .CSV File

```
-Friday Timeslots
-Friday Room Names
-Saturday Timeslots
-Saturday Room Names
```

### Updating

Currently, to update the program, just download the latest installer version, and run it. This will update the application on your computer for you.
In the future there will be an automatic process to check for and install a new version automatically when you start the program.

### Uninstalling

You can easily uninstall the program from your machine at any time. Here is how to do so on any operating system.

Windows OS

```
1. Navigate to your start menu and type 'Add or Remove Programs'.
2. Search or find 'Event Organizer' in the list and select it.
3. Click uninstall and wait a few seconds for the application to dissapear from the list.
```

MacOS

```
1. Navigate to the Finder and go to Applications.
2. Find EventOranizer and control+click.
3. Click Move to Trash
```

Linux

```
```

## Built With

Here are some of the frameworks and libraries used to create this application. Some are missing and will be added when possible.

* [Electron](https://www.npmjs.com/package/electron) - Framework used to write cross-platform desktop applications using JavaScript
* [Bootstrap/Popper](https://www.npmjs.com/package/bootstrap) - Sleek, intuitive, and powerful front-end framework for faster and easier web development.
* [jQuery](https://www.npmjs.com/package/jquery) - Feature-rich Javascript Library.
* [Moment](https://www.npmjs.com/package/moment) - A lightweight JavaScript date library for parsing, validating, manipulating, and formatting dates.
* [Papaparse](https://www.npmjs.com/package/papaparse) - Javascript CSV Parsing Library.
* [Seedrandom](https://www.npmjs.com/package/seedrandom) - Javascript seeded random number generator.
* [Glob](https://www.npmjs.com/package/glob) - Assist in parsing .CSV files, as well as saving them.

## Contributing

If you wish to contribute to further devlopment, please contact me via email with any comments, questions, concerns, or improvments.

## Versioning

I use [Semantic Versioning](http://semver.org/) for versioning.

### Future Features

Here are some of the future features that I hope to add and work on for this application.

```
- Multiple Presenters - Add support for checking multiple presenters instead of just the primary in the same timeslot so not to assign two sessions with the same people during the same timeslot. 
- Auto Updating - Client will check for a newer update on startup, and every 10 minutes thereafter. If it finds one, it will prompt the user and auto-install the newest version if allowed.
- Issue Dialogue Popup - A popup after clicking the create button that alerts you if there were any issues assigning presenters, and how many. Also mentioning to check the status log tab for more information. This popup will have a "download anyway" or "cancel" button.
- Icon Update - Change the application icon to a white/brighter color instead of the dark gray so it can be seen on darker backgrounds.
- Data Settings Tab Change - Turn the Data Settings tab into an Input Data tab used for verifying/viewing both input presenter data and input settings data
```

### Changelog

v1.1.3
```
- Added support for up to 6 total presenters for an event. It will make sure none of those 6 are in the same timeslot.
- Reformated output file:
  - Shows all presenters that did not get assigned a timeslot.
  - Shows all presenter info from the original data csv as well as the timeslot information
```

v1.0.3
```
- Intial Release
```

## Authors

* **ItsANoBrainer** - *Application Developer* - [ItsANoBrainer](https://github.com/ItsANoBrainer)

## License

This project is licensed under the [ISC License](https://opensource.org/licenses/ISC). 
By using this program you abide that this program is created and soley owned by Christopher Usiak.
Christopher Usiak has the right to change any License or Ownership at any time.

## Acknowledgments

* This program was intially created for use by [MITESOL](http://mitesol.org/) - Michigan Teachers of English to Speakers of Other Languages  
