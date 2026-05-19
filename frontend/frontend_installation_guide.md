# Hogwarts Spell & Potion Manager

An application designed for magic item management and properties view, such as spells and potions.

## Τechnologies

- HTML
- CSS
- Vanilla JavaScript

## Language
- Greek

## App structure

The application has been implemented using HTML, CSS and Vanilla JavaScript in one global file (`hogwarts_2mon.html`) located in this repository.
No connection to external files, backend services or databases is further required.

## App functionality

This app allows the user to:

- Add a new magical item (spell/potion)
- View all items list
- Delete item
- Toggle status
- Upgrade power by +5, up to the maximum limit (100)

## Fields description

Each magical item consists of the features below:

- Name (must be unique)
- Type (Spell/Potion
- Element (Fire, Ice, Lightning, Earth)
- Power (1-100)
- Rarity (Common, Rare, Epic, Legendary, Wow)
- Description
- State
    - **Spells:** Unlearned/Learned
    - **Potions:** Unbrewed/Brewed

## Execution Steps

The application is client-side and does not require a server to fully operate.

### 1. Open file

Open the `hogwarts_2mon.html` file inside a browser. `(ie. Google Chrome, Mozilla Firefox etc)`.

### 2. Application usage

The following steps show a process on how to use the application.

- Complete all form fields to add a new object
- Click the "Add" button so that object be added
    - Front-end application language is set to Greek by default, the Greek language variation of the "Add" button is "Προσθήκη".
- After adding an object, the object appears on the list.

#### NOTE: After object insertion, data is being temporarily allocated and stored to memory (array). They will be lost after refreshing the page.

## User Operations

For every object on the list:

- **Toggle Status:** toggles status (ie. Unlearned -> Learned)
- **Upgrade Power:** increases power by +5 until maximum limit (100)
- **Delete Object:** removes object from list

## Usage Tips

For a more optimized experience, it is recommended to:

- Open DevTools (`F12`) to view console messages (debugging)
- Check for possible errors when inserting data
