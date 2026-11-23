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

The use of Command Prompt (cmd) is recommended, to support full Node.js compatibility.

### 2. Head to the project folder

Type in the command below:

        cd magic-api

inside the terminal, in order to head to the project folder where sub-folders and files are included.

### 3. Create an .env file inside the project folder

Create a file inside the core project folder `(magic-api)`, which will include the items required for accessibility settings configuration.

The file consists of the port (PORT) and the Uniform Resource Indicator (URI) of MongoDB, in order to connect to the database.

- #### Uniform Resource Indicator: It usually consists of the username and password of the database admin, in order to connect to the database locally or online, using MongoDB Atlas.

### 4. Install Dependencies

Before executing the application, it is best and recommended to install some dependencies. These dependencies are provided by the Node.js framework and support best application functionality and packages.

In order to install dependencies, type in the command below:

    npm install express mongoose dotenv

inside the terminal

### **IMPORTANT:** Step 2 must be completed first (head to the project folder using a command inside the terminal project) in order to install dependencies inside the magic-api folder!!!

### Used Dependencies:
- dotenv (access to environment variables)
- express (main application framework)
- mongoose (database access through MongoDB, locally or using MongoDB Atlas)

After installing required dependencies, the following files are created automatically:
- package.json
- package-lock.json
- node_modules folder (includes Node.js modules)

### 5. Create server.js file

The server.js file is the main application component.

In this file:
- database connected is being achieved
- the `(ExpressJS)` middleware is being stored
- folder content paths are being declared (ie subfolder files)
- server is being launched

### 6. Server Launch

After completing the steps above, type the following command:

    npm start

inside the terminal, in order to launch the app.

After everything has been set successfully, a message depicting successful launch will show up on the terminal!!

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
