# Hogwarts Spell & Potion Manager

An application designed for magic item management and properties view, such as spells and potions.

## Technologies

### Front-end:
- HTML
- CSS
- Vanilla JavaScript

#### **NOTE:**
In the front-end version of the application, types are being used in Greek (“Ξόρκι” / “Φίλτρο”).

In the back-end version of the application, equivalent types in English are being used (“Spell” / “Potion”).

### Back-end/Database Management:
- Node.js
- ExpressJS
- MongoDB Atlas
- Mongoose
- Postman (for API Testing)

## App Structure

App structure is based on MVC architecture.

- **Models:** Set schema
- **Controllers:** App logic
- **Routes:** Manage routes/endpoints
- **Config:** Connect to MongoDB (MongoDB Atlas)
- **Data:** JSON file, equipped with data
- **Server:** App launch

## App execution steps

For best performance, executing the app through Visual Studio Code and MongoDB Atlas is highly preferred.

### 1. Open a new Terminal window inside your code editor (ie. Visual Studio Code), switched to the directory where app elements exist.

Συνιστάται η χρήση Command Prompt (cmd), για πλήρη συμβατότητα με το Node.js

### 2. Μετάβαση στο φάκελο του project

Πληκτρολογούμε την εντολή:

        cd magic-api

εντός του τερματικού, για να μεταβούμε στο φάκελο του project στο οποίο περιέχονται οι υποφάκελοι και τα αντίστοιχα αρχεία.

### 3. Δημιουργία αρχείου .env στον φάκελο του project

Δημιουργούμε ένα αρχείο στο βασικό φάκελο του project `(magic-api)`, το οποίο θα περιέχει τα στοιχεία που απαιτούνται για τη ρύθμιση παραμέτρων στο κομμάτι της συνδεσιμότητας.

Το αρχείο, περιέχει τη θύρα (PORT) και το Uniform Resource Indicator (URI) της MongoDB, για τη σύνδεση στη βάση δεδομένων.

- #### Uniform Resource Indicator: συνήθως περιέχει το username και password του διαχειριστή της βάσης δεδομένων, για τη σύνδεση στη βάση είτε τοπικά, ή online, κάνοντας χρήση της πλατφόρμας MongoDB Atlas

### 4. Εγκατάσταση εξαρτήσεων

Πριν την εκτέλεση της εφαρμογής, καλό (και προτιμότερο) θα ήταν να εγκατασταθούν κάποιες εξαρτήσεις (dependencies). Οι εξαρτήσεις αυτές, παρέχονται από το framework Node.js, συμβάλλουν στην καλύτερη λειτουργία της εφαρμογής και την υποστήριξη μέσω πακέτων.

Για την εγκατάσταση των εξαρτήσεων, πληκτρολογούμε την εντολή:

    npm install express mongoose dotenv

εντός του τερματικού.

### **ΣΗΜΑΝΤΙΚΟ:** Προηγείται η ολοκλήρωση του βήματος 2 (μετάβαση στον φάκελο του project μέσω εντολής τερματικού) για να πραγματοποιηθεί η εγκατάσταση των εξαρτήσεων εντός του φακέλου magic-api!!!

### Εξαρτήσεις που χρησιμοποιήθηκαν:
- dotenv (πρόσβαση σε μεταβλητές περιβάλλοντος)
- express (το κύριο framework στο οποίο εγκαταστάθηκε η εφαρμογή)
- mongoose (πρόσβαση στη βάση δεδομένων μέσω MongoDB, είτε τοπικά ή μέσω Atlas)

Έπειτα από την ολοκλήρωση της εγκατάστασης των εξαρτήσεων που απαιτούνται, δημιουργούναι αυτόματα:
- package.json
- package-lock.json
- φάκελος node_modules (περιέχει τις λειτουργίες του Node.js)

### 5. Δημιουργία αρχείου server.js

Το αρχείο server.js αποτελεί τον κύριο σκελετό εκτέλεσης της εφαρμογής.

Σε αυτό το αρχείο:
- επιτυγχάνεται η σύνδεση με τη βάση δεδομένων
- αποθηκεύεται το middleware `(ExpressJS)`
- δηλώνονται οι διαδρομές των περιεχομένων του φακέλου, πχ αρχεία που ανήκουν στους υποφακέλους
- εκκινείται ο server

### 6. Εκκίνηση server

Κατόπιν ολοκλήρωσης των παραπάνω βημάτων, πληκτρολογούμε την εντολή:

    npm start

εντός του τερματικού, για την εκκίνηση του server της εφαρμογής.

Εφόσον όλα έχουν ρυθμιστεί σωστά, θα εμφανιστεί μήνυμα επιτυχούς εκκίνησης στο τερματικό!!

### 7. Επαλήθευση λειτουργίας εφαρμογής (προαιρετικό)

Αφού εκκινηθεί επιτυχώς ο server, μπορούμε να επαληθεύσουμε ότι η εφαρμογή λειτουργεί σωστά. Στον browser, πληκτρολογούμε τη διεύθυνση:

    http://localhost:5000

Εφόσον η εφαρμογή λειτουργεί κανονικά, θα εμφανιστεί το μήνυμα:

    API is working

Επιβεβαιώνεται ότι:
- ο server εκκίνησε επιτυχώς
- η εφαρμογή "ακούει" τη σωστή θύρα (`PORT 5000`)
- η κύρια διαδρομή λειτουργεί

### Σημείωση για MongoDB Atlas

Για την αποφυγή προβλημάτων σύνδεσης με τη βάση δεδομένων, είναι προτιμότερο να επιτρέπεται πρόσβαση από όλες τις διευθύνσεις IP εντός του MongoDB Atlas.


    0.0.0.0/0

Η ρύθμιση αυτή γίνεται από τις ρυθμίσεις δικτύου (Network Access) της πλατφόρμας.

### Αυτή η ρύθμιση προορίζεται μόνο για ανάπτυξη (development) και όχι για περιβάλλον παραγωγής.

### 8. Εισαγωγή δεδομένων στη βάση

Τα δεδομένα περιέχονται σε αρχείο JSON (`magicItems.json`).

Για να αποθηκευτούν στη βάση, παρέχεται το αρχείο `seed.js`.

Σε ένα νέο terminal, χωρίς να "πειράξουμε" το τερματικό στο οποίο εκτελείται ο server της εφαρμογής, πληκτρολογούμε την εντολή:

    node seed.js

Η διαδικασία:
- Διαβάζει τα δεδομένα από το αρχείο JSON
- Διαγράφει τυχόν υπάρχοντα δεδομένα
- Εισάγει τα νέα δεδομένα στη βάση

Μετά την εκτέλεση, εμφανίζεται μήνυμα επιτυχίας: "Data imported!"

Για να δούμε όλα τα magic items στον browser, πληκτρολογούμε τη διεύθυνση:

    http://localhost:5000/api/v1/magic-items

### 9. Λειτουργίες API (CRUD)

Η εφαρμογή υποστηρίζει πλήρεις CRUD λειτουργίες μέσω REST API.

#### Ανάγνωση (GET)
- Επιστροφή όλων των magic items.
- Αναζήτηση κάνοντας χρήση φίλτρων:
    - type
    - rarity
    - status
    - power (min/max)

#### Δημιουργία (POST)
- Προσθήκη νέου magic item στη βάση δεδομένων

#### Ενημέρωση (PUT)
- Τροποποίηση υπάρχοντος magic item βάσει ID

#### Διαγραφή (DELETE)
- Διαγραφή magic item βάσει ID

### 10. Παραδείγματα Αιτημάτων και Αποκρίσεων

Τα παραδείγματα περιλαμβάνονται στο αρχείο `PostmanResults.md` εντός του φακέλου.

### 11. Postman Collection

Για την ευκολότερη αξιολόγηση της εφαρμογής, περιλαμβάνεται εξαγόμενο αρχείο σε JSON μορφή από τη συλλογή όλων των αποτελεσμάτων μέσω του Postman `(Postman Collection)`.

### 12. Bonus Λειτουργίες

Υλοποιήθηκαν επιπλέον endpoints για την εφαρμογή μέσω PATCH requests:
- Toggle Status (PATCH)
    - Αυτόματη αλλαγή κατάστασης
        - Για ξόρκια: "Μη μαθημένο/Unlearned" -> "Μαθημένο/Learned"
        - Για φίλτρα: "Μη παρασκευασμένο/Unbrewed" -> "Παρασκευασμένο/Brewed"
- Increase Power (PATCH)
    - Αύξηση δύναμης κατά +5, μέχρι το μέγιστο όριο (100).

Τα endpoints αυτά μπορούν να χρησιμοποιηθούν μέσω Postman ή οποιουδήποτε client που πραγματοποιεί HTTP requests.
