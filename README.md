# Hogwarts Spell & Potion Manager

An application designed for magic item management, such as spells and potions, and viewing of their equivalent properties.

## Τechnologies

### Frontend:
- HTML
- CSS
- Vanilla JavaScript

## App structure

The application has been implemented using HTML, CSS and Vanilla JavaScript in one global file (`hogwarts_2mon.html`).
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

The application is client-side and does not require a server to operate fully.

### 1. Άνοιγμα αρχείου

Ανοίγουμε το αρχείο hogwarts_2mon.html σε έναν browser `(πχ. Google Chrome, Mozilla Firefox etc)`.

### 2. Χρήση εφαρμογής

Η χρήση της εφαρμογής επιτυγχάνεται από τα παρακάτω βήματα:

- Συμπληρώνουμε όλα τα πεδία της φόρμας για την προσθήκη νέου αντικειμένου
- Κάνουμε κλικ στο κουμπί "Προσθήκη" έτσι ώστε να προστεθεί το αντικείμενο
- Το αντικείμενο εμφανίζεται στη λίστα

#### Σημείωση: Μετά την εισαγωγή τους, τα δεδομένα αποθηκεύονται προσωρινά στη μνήμη (array) και χάνονται με ανανέωση της σελίδας.

## Λειτουργίες Χρήστη

Για κάθε αντικείμενο στη λίστα:

- **Αλλαγή Κατάστασης:** εναλλάσσει την κατάσταση (πχ Μη μαθημένο -> Μαθημένο)
- **Αναβάθμιση Δύναμης:** αυξάνει τη δύναμη κατά +5 μέχρι το μέγιστο όριο (100)
- **Διαγραφή Αντικειμένου:** αφαιρεί το αντικείμενο από τη λίστα

## Συμβουλές Χρήσης

Για βέλτιστη εμπειρία:

- Ανοίξτε τα Developer Tools (`F12`) για προβολή μηνυμάτων στην κονσόλα (debugging)
- Ελέγξτε πιθανά σφάλματα κατά την εισαγωγή δεδομένων
