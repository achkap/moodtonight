# ΙΟΝΙΟ ΠΑΝΕΠΙΣΤΗΜΙΟ 


# ΤΜΗΜΑ ΠΛΗΡΟΦΟΡΙΚΗΣ 



# ΜΑΘΗΜΑ
## Κινητά και Κοινωνικά Μέσα
 
Επιβλέπων καθηγητής: Χωριανόπουλος Κωνσταντίνος 


# Τίτλος
## Sentiment Analysis on Twitter

Αχιλλέας Καπετάνιος
ΑΜ: Π2015201


Αποθετήριο Κώδικα εφαρμογής στο Github: [https://github.com/achkap/twitter-stream-globe](https://github.com/achkap/twitter-stream-globe)


Η εφαρμογή στο Heroku: [Moodonight](https://moodtonight.herokuapp.com/)


## Σύνοψη

Η εργασία είχε ως σκοπό την παρέμβαση στον κώδικα μιας εφαρμογής που μετρούσε τα συναισθήματα των tweets ανά τον κόσμο. Η εφαρμογή
ψάχνει μέσα στο σώμα των tweets για συγκεκριμένες λέξεις που είναι μέσα σε ένα αρχείο [https://github.com/ioniodi/twitter-stream-globe/blob/master/AFINN-translateToGreek165.txt](https://github.com/ioniodi/twitter-stream-globe/blob/master/AFINN-translateToGreek165.txt) με συγκεκριμένη βαθμολογία η κάθε μία, ανάλογα με το αν είναι θετικό ή αρνητικό το συναίσθημα. Ανάλογα με τη βαθμολογία του, το κάθε tweet έπαιρνε κι ένα συγκεκριμένο χρώμα -κόκκινο αν ήταν αρνητικό και κίτρινο αν ήταν θετικό- και το αποτέλεσμα εμφανιζόταν σε μία τρισδιάστατη υδρόγειο, από την οποία έφευγαν ακτίνες με το ανάλογο χρώμα. Μπορεί κάποιος να δει την εφαρμογή [εδώ](https://stark-lake-93710.herokuapp.com/) και το αποθετήριό της [εδώ](https://github.com/ioniodi/twitter-stream-globe).

## Εισαγωγή
Στην εργασία αυτή με τις οδηγίες των παραδοτέων έγιναν δίαφορες παρεμβάσεις στην εφαρμογή που θα αναλυθούν πιο κάτω. Σε όλες τις περιπτώσεις έπρεπε να πειραχτεί ο κώδικας της εφαρμογής, και κυρίως τα αρχεία javascripts. Έπρεπε να προστεθούν αρχεία - φωτογραφίες- προκειμένου να αλλάξει η υφή της υδρογείου καθώς και να αλλάξει και το αρχείο κειμένου που περιείχε μέσα τις λέξεις ώστε να μπουν μέσα και ελληνικές λέξεις.

## Εργαλεία
Τα εργαλεία που χρησιμοποιήθηκαν ήταν πρώτα και κύρια το Github. Εκεί ήταν γραμμένος ο κώδικας της εφαρμογής καθώς κι εκεί ήταν και η πλατφόρμα επικοινωνίας για το μάθημα. Στη συνέχεια αφού φτιαχτηκε μία νέα εφαρμογή στο Twitter Apps και πάρθηκαν τα tokens και τα keys (για να επικοινωνούν οι διάφορες πλατφόρμες μεταξύ τους), καθώς και τα tokens και τα keys από το PubNub (πλατφόρμα για έλεγχο πρόσβασης και εξουσιοδότησης) και όλα αυτά μπήκαν στο Heroku, ένα online εργαλείο για τη δημιουργία εφαρμογών με πάρα πολλές δυνατότητες, και κυρίως σύνδεση με το Github , όπου εκεί θα υπήρχε και ο κώδικας της εφαρμογής μας.



## Παραδοτέο 1
### Παρεμβάσεις στα χρώματα:

Οι παρεμβάσεις στα χρώματα που θα γίνουν είναι:

Έντονα αρνητικό συναίσθημα : Κόκκινο

Αρνητικό συναίσθημα : Πορτοκαλί

Θετικό συναίσθημα : Κίτρινο

Έντονα θετικό συναίσθημα : Πράσινο


### Λέξεις που θα μεταφραστούν: 
kidnap, kill, kind, kindness, kiss, lack, lame, laugh, lawsuit, lawsuits, 
leave, lethal, limits, loss, love, luck, lunatic, macabre, madness, jerk
hysteria, idiocy, insomnia, insult, irony, ironic, honor, gun, grave, comic


## Παραδοτέο 2

### Διευθυνση εφαρμογής

Σαν διεύθυνση της εφαρμογής έχει μπει το branch όπου είναι ενσωματωμένα όλα τα επιτυχημένα commits.

[https://moodtonight.herokuapp.com/](https://moodtonight.herokuapp.com/)


#### Αλλαγές στον κώδικα της εφαρμογής

Κάθε αλλαγή στον κώδικα έγινε σε διαφορετικό branch του forked αποθετηρίου, που φέρει και το ανάλογο όνομα. Προστέθηκε επίσης ένα branch όπου περιλαμβάνει αθροιστικά όλα τα commits που είναι επιτυχημένα (All-Succesful-Commits). Το master branch είναι καθαρό και χωρίς αλλαγές. Για να λειτουργεί η εφαρμογή μέσω του heroku (προσθήκη keys, tokens του Twitter και του PubNub) δε χρειαζόταν να προστεθούν στο αρχείο tweet-publisher/index.js μια και η είσοδός τους γινόταν κατευθείαν στο heroku.

Τα χρώματα αλλάχτηκαν και διαβαθμίστηκαν όπως δηλώθηκε στο Παραδοτέο 1. Δηλαδή

Έντονα αρνητικό συναίσθημα : Κόκκινο

Αρνητικό συναίσθημα : Πορτοκαλί

Θετικό συναίσθημα : Κίτρινο

Έντονα θετικό συναίσθημα : Πράσινο

Εκτός από την αλλαγή χρώματος στις ακτίνες που φεύγουν από την υδρόγειο, έγινε αλλαγή και στην αριστερή στήλη με τη ροή των tweets, όπου κι εκεί μπήκαν τα ίδια χρώματα, με την ίδια διαβάθμιση. Το ίδιο δεν κρίθηκε σκόπιμο να γίνει στο Tweet Sentiment στη δεξιά στήλη μια και οι τιμές που παίρνει δεν ξεπερνάνε το +-0,8. Η διαβάθμιση στα χρώματα έγινε με βάση την τιμή των λέξεων από το αντίστοιχο αρχείο.

#### Αλλαγη TweetBeacon.js για την αλλαγή χρωμάτων των ακτίνων και διαβάθμισή τους. Η διαβάθμιση έγινε για:

Tweet Sentiment <= -2  -- Έντονα αρνητικό συναίσθημα

-2 < Tweet Sentiment < 0  -- Αρνητικό συναίσθημα

0 < Tweet Sentiment < 2  -- Θετικό συναίσθημα

Tweet Sentiment >= 2  -- Έντονα θετικό συναίσθημα

Η τιμές αυτές λήφθηκαν με βάση το αρχείο AFINN-translateToGreek165.txt και με δεδομένο ότι ο ανώτερος βαθμός βαρύτητας λέξης είναι 5 και ο μικρότερος -5.

[https://github.com/achkap/twitter-stream-globe/blob/Changing-Beam-Colors/public/javascripts/TweetBeacon.js](https://github.com/achkap/twitter-stream-globe/blob/Changing-Beam-Colors/public/javascripts/TweetBeacon.js)

Στις εικόνες φαίνονται και τα πέντε χρώματα (συν το άσπρο που είναι το ουδέτερο tweet) των ακτίνων.



![Screenshot1](screenshot1.jpg)


![Screenshot2](screenshot2.jpg)

#### Αλλαγή αρχείων TweetHud.js, css και scss για αλλαγή χρωμάτων και προσθήκη διαβαθμίσεων χρωμάτων στην αριστερή στήλη με τα tweets. Η διαβάθμιση χρωμάτων ακολουθεί τη λογική διαβάθμισης χρωμάτων των ακτίνων. 

[https://github.com/achkap/twitter-stream-globe/blob/changing-left-column-colors/public/stylesheets/style.css](https://github.com/achkap/twitter-stream-globe/blob/changing-left-column-colors/public/stylesheets/style.css)

[https://github.com/achkap/twitter-stream-globe/blob/changing-left-column-colors/public/stylesheets/style.scss](https://github.com/achkap/twitter-stream-globe/blob/changing-left-column-colors/public/stylesheets/style.scss)

[https://github.com/achkap/twitter-stream-globe/blob/changing-left-column-colors/public/javascripts/TweetHud.js](https://github.com/achkap/twitter-stream-globe/blob/changing-left-column-colors/public/javascripts/TweetHud.js)


Στην εικόνα φαίνονται και τα τέσσερα χρώματα  της ροής των tweets.



![Screenshot3](screenshot3.jpg)




### Λέξεις που μεταφράστηκαν: 
kidnap=απαγάγω, απαγωγή, kill=σκοτώνω, θάνατος, kind=ευγενικό, kindness=ευγένεια, kiss=φιλί, lack=έλλειψη, lame=ξενέρωτο, laugh=γελάω, γέλιο, lawsuit=μήνυση, lawsuits=μηνύσεις, 
leave=εγκαταλείπω, αφήνω, lethal=θανατηφόρο, limits=όρια, loss=απώλεια, love=αγάπη, luck=τύχη, lunatic=παράφρονας, macabre=μακάβριο, madness=τρέλα, jerk=κόπανος
hysteria=υστερία, idiocy=ηλιθιότητα, insomnia=αϋπνία, insult=προσβολή, προσβάλω, irony=ειρωνεία, ironic=ειρωνικός, honor=τιμή, gun=όπλο, grave=τάφος, comic=κόμικς

[https://github.com/achkap/twitter-stream-globe/blob/add-greek-translate/AFINN-translateToGreek165.txt](https://github.com/achkap/twitter-stream-globe/blob/add-greek-translate/AFINN-translateToGreek165.txt)


## Παραδοτέο 3

Κι εδώ οι αλλαγές έγιναν σε διαφορετικό κλαδί αν και όλες αφορούν το ίδιο αρχείο: το /public/javascripts/TwitterStreamGlobe.js.

Όλα τα επιτυχημένα commits έχουν προστεθεί σε ειδικό κλαδί του αποθετηρίου [All-succesful-commits](https://github.com/achkap/twitter-stream-globe/tree/All-succesful-commits).

#### Οι αλλαγές στον κώδικα έχουν επισημανθεί σαν σχόλια στο αρχείο του forked αποθετηρίου, στο κλαδί All-succesful-commits. 


Για να μπορέσω να αλλάξω την υφή της υδρογείου έπρεπε να προσθέσω εικόνες στο φάκελο

[https://github.com/achkap/twitter-stream-globe/tree/changing-earth-visualisation/public/images](https://github.com/achkap/twitter-stream-globe/tree/changing-earth-visualisation/public/images)

Οι εικόνες που προστέθηκαν είναι της υδρογείου μέρα και νύχτα.
Έγιναν και οι ανάλογες αλλαγές στο αρχείο TwitterStreamGlobe.js ώστε να διαβάζει και να φορτώνει τις καινούριες εικόνες.

[https://github.com/achkap/twitter-stream-globe/blob/changing-earth-visualisation/public/javascripts/TwitterStreamGlobe.js](https://github.com/achkap/twitter-stream-globe/blob/changing-earth-visualisation/public/javascripts/TwitterStreamGlobe.js)

Επίσης αλλάχτηκε η ταχύτητα περιστροφής της υδρογείου (πιο γρήγορη)

[https://github.com/achkap/twitter-stream-globe/blob/change-earth-speed/public/javascripts/TwitterStreamGlobe.js](https://github.com/achkap/twitter-stream-globe/blob/change-earth-speed/public/javascripts/TwitterStreamGlobe.js)


καθώς και η φορά περιστροφής. 

[https://github.com/achkap/twitter-stream-globe/blob/change-earth-spin/public/javascripts/TwitterStreamGlobe.js](https://github.com/achkap/twitter-stream-globe/blob/change-earth-spin/public/javascripts/TwitterStreamGlobe.js)

Έγινε αλλαγή και στο μέγεθος της υδρογείου, μόνο που η αλλαγή είναι μικρή μια και μια αρκετά μεγαλύτερη ή αρκετα μικρότερη υδρόγειος δε φαίνεται καλά όταν τρέχει η εφαρμογή.

[https://github.com/achkap/twitter-stream-globe/blob/change-earth-size/public/javascripts/TwitterStreamGlobe.js](https://github.com/achkap/twitter-stream-globe/blob/change-earth-size/public/javascripts/TwitterStreamGlobe.js)

Τέλος έγινε και ο περιορισμός στην προέλευση των tweets στις Η.Π.Α. (μια και τα  περισσότερα tweets προέρχονται από εκεί και η οπτικοποίηση θα ήταν καλύτερη). Η αλλαγή περιοχής μπορεί να γίνει εύκολα αλλάζοντας απλά τις συντεταγμένες στο κατάλληλο σημείο του κώδικα. 

[https://github.com/achkap/twitter-stream-globe/blob/limit-tweet-region/public/javascripts/TwitterStreamGlobe.js](https://github.com/achkap/twitter-stream-globe/blob/limit-tweet-region/public/javascripts/TwitterStreamGlobe.js)


Έγινε ακόμα και η αλλαγή της υφής της υδρογείου ανάλογα με την ώρα της ημέρας. Έτσι όταν η ώρα είναι από τις 07:00 - 19:00 τότε η εικόνα της Γης είναι αυτή που τη δείχνει μέρα, ενώ τις υπόλοιπες ώρες είναι αυτή που τη δείχνει νύχτα.


[https://github.com/achkap/twitter-stream-globe/blob/daynight/public/javascripts/TwitterStreamGlobe.js](https://github.com/achkap/twitter-stream-globe/blob/daynight/public/javascripts/TwitterStreamGlobe.js)


## Παραδοτέο 4
Η αποθήκευση σε σέρβερ δεν κατέστη δυνατό να πραγματοποιηθεί. Η έλλειψη γνώσεων πάνω στο θέμα αυτό δεν επέτρεψαν την υλοιποίηση της παραπάνω οδηγίας.
Η απεικόνιση σε χάρτη 2D έγινε εν μέρει. Ο χάρτης της Γης άλλαξε από σφαίρα σε επίπεδο αλλά το να φεύγουν οι ακτίνες ακριβώς όπως πρέπει, ήταν δύσκολο να γίνει. Όλες οι αλλαγές έγιναν πάνω στο αρχείο 

[https://github.com/achkap/twitter-stream-globe/blob/change-earth-2d/public/javascripts/TwitterStreamGlobe.js](https://github.com/achkap/twitter-stream-globe/blob/change-earth-2d/public/javascripts/TwitterStreamGlobe.js) 

και οι αλλαγές φαίνονται σαν σχόλια στον κώδικα. 

Το αποτέλεσμα φαίνεται στην παρακάτω εικόνα.

![Screenshot4](screenshot4.jpg)

## Συμπεράσματα

Η εργασία αυτή ήταν ένα πολύ καλό παράδειγμα για το πώς δουλεύει το Github. Οι παρεμβάσεις στον κώδικα κάποιου άλλου που έχει κάνει την εφαρμογή και η δυνατότητα συνεννόησης-συνεργασίας δύο (ή και περισσότερων) ανθρώπων, αγνώστων μεταξύ τους για τη βελτίωση κάποιου έργου, κώδικα, προγράματος, δίνει την ευκαιρία σε πολλούς ανθρώπους να συμμετέχουν, αλλά δείχνει και το δρόμο που πρέπει να ακολουθούν όλοι όσοι σκέφτονται να προγραμματίσουν. Ο κλειστος και απαγορευμένος κώδικας έχει πολύ περιορισμένες δυνατότητες σε αντίθεση με τον ανοιχτό, όπου η συνεργασία πολλών ανθρώπων, μπορεί να βελτιώσει εντυπωσιακά και ταχύτατα έναν κώδικα. Δεν είναι τυχαίο ότι και οι διάφορες διανομές Linux και οι διάφορες ομάδες που αναπτύσσουν custom ROM στο Android έχουν τη βάση τους στο Github προκειμένου όλο και περισσότεροι άνθρωποι να συνεισφέρουν στα πρότζεκτ αυτά.

Από την άλλη οι παρεμβάσεις στον κώδικα της εφαρμογής -σύμφωνα με τις οδηγίες- ξεκάθαρα βελτιώνουν την εφαρμογή και μάλιστα, με τη μετάφραση των λέξεων, μπορεί να αξιοποιηθεί μελετώντας και τα ελληνικά tweets. 

Οι παρεμβάσεις στον κώδικα απαιτούσαν τη γενική γνώση προγραμματισμού εκτός από τις τελευταίες που απαιτούσαν την γνώση javascripts καθώς και τη δημιουργία σέρβερ που δυστυχώς δεν υπήρχαν και γι' αυτό δεν υλοποιήθηκαν.


### Βίντεο παρουσίασης εφαρμογής
Έχει προστεθεί κι ένα βίντεο το οποίο δείχνει την αρχική έκδοση της εφαρμογής και την εφαρμογή όπως έχει γίνει μετά από όλα τα επιτυχημένα commits. 

[Youtube Video](https://youtu.be/Baq7xVFOM0E)




## Bonus

### Σελίδα Τελικής Αναφοράς
[https://achkap.github.io/moodtonight/](https://achkap.github.io/moodtonight/)

### Bonus A - Links for merged commits

[https://github.com/pibook/pibookgr/pull/137](https://github.com/pibook/pibookgr/pull/137)

[https://github.com/pibook/pibookgr/pull/136](https://github.com/pibook/pibookgr/pull/136)

[https://github.com/pibook/pibookgr/pull/134](https://github.com/pibook/pibookgr/pull/134)

[https://github.com/pibook/pibookgr/pull/132](https://github.com/pibook/pibookgr/pull/132)

[https://github.com/pibook/pibookgr/pull/156](https://github.com/pibook/pibookgr/pull/156) (unmerged)

### Bonus C - Link for case study merged commit
[https://github.com/pibook/pibookgr/pull/155](https://github.com/pibook/pibookgr/pull/155) (unmerged)
