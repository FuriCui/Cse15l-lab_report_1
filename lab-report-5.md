## Less
## `-N`
# 1.
`      1 
      2 
      3 
      4 
      5 A Brief History
      6 In ancient Greek mythology Athens is named following a contest between Athena, goddess of wisdom, and`
At this first example, I typed `less -N Athens-History.txt` to see the texts inside of the file and this option grant me the ability to show the number of the line I am looking at.
# 2.
`      1 
      2 
      3 
      4 
      5 Athens and
      6 The Athenians
      7 M ention the name Athens and almost everyone will have some preconceived ideas about the city. Socrat`
Here is basically the same logic, this time I typed `less -N Athens-Intro.txt` to see what is inside of the Athens-Intro file and saw the number of the line.
## `-p`
# 3.
`Athens and
The Athenians
M ention the name Athens and almost everyone will have some preconceived ideas about the city. Socrates painted a picture with words in the fourth century b.c., Pausanais during the Roman era. In the 20th century, Hollywood added its own slant to the legends, and every school child learns about the gods of the ancient Greek world — of Zeus, Athena, and Apollo.`
This option is useful when we want a word. Since it highlights all the text we required. I typed `less -p "Athens" Athens-Intro.txt` to see the content and it highted all the "Athens" word in the text file.
# 4.
`A Brief History
In ancient Greek mythology Athens is named following a contest between Athena, goddess of wisdom, and Poseidon, god of the sea. Both had their eye on the prize real estate, so it was agreed that whoever could come up with the more useful gift for mortals would win. The half-human, half-serpent king of Athens, Cecrops, acted as arbiter. `
This time I typed `less -p "Athens" Athens-Intro.txt` to highlight all "Athens" in the text file.
## `+N`
# 5.
`Around 1100 b.c. waves of Dorians swept into the area on horseback. Armed with iron spears and shields, they overpowered the Bronze Age weapons of Mycenae and broke down the Peloponnesian bastions. The ensuing “dark age” lasted about three centuries and resulted in large-scale emigrations of Greeks around the Mediterranean.
Athens managed to escape the scourge, but only after 700 b.c. did it take over and lift to unimagined heights the heritage of Mycenae and Crete. Although they warred as often as they united, the citizens of Athens and surrounding city-states on the Attica peninsula, notably Sparta and Thebes, shared a sense of identity. They were all Greeks — they had a common tongue and an evolving pan-Hellenic religion, and at regular intervals they were brought together by the ritual athletic contest of the Olympian, Delphian, and Isthmian games.`
This time I typed `less +10  Athens-History.txt` as u can tell that this option starts from the line of number that substitute N.
# 6.
`As Athens prospered, intense economic and ideological rivalry developed with Athens’ ally during the Persian Wars, Sparta. In 431 b.c. the Peloponnesian War broke out between them resulting in 27 years of debilitating conflict, involving most of the Greek world. Yet literature and art continued to flourish in spite of the incessant fighting, and during this time Athens built two of the loveliest temples on the Acropolis, the Erechtheion and the temple to Athena Nike (see pages 34 and 35).
Finally, Sparta, with naval help from former foe Persia, blockaded what was then the Hellespont (now the Dardanelles Strait), thus cutting off Athens from its crucial supply of grain. Starvation and heavy naval losses proved too much for Athens, and the Spartans claimed total victory. `
This time I typed `less +30  Athens-History.txt` as u can tell that this option starts from the line of number that substitute N.
## `-s`
# 7.
`A Brief History
In ancient Greek mythology Athens is named following a contest between Athena, goddess of wisdom, and Poseido
n, god of the sea. Both had their eye on the prize real estate, so it was agreed that whoever could come up w
ith the more useful gift for mortals would win. The half-human, half-serpent king of Athens, Cecrops, acted a
s arbiter. 
First came Poseidon, who struck the rock of the Acropolis with his mighty trident and brought salt water gush
ing forth. Then it was Athena’s turn. As she struck the rock an olive tree appeared, which proved more useful
 and valuable. Thus she acquired the position of the city’s special protector.`
this time I typed `less -s Athens-History.txt` to merge all the non-consecutive blank line into 1 blank.
# 8.
`Athens and
The Athenians
M ention the name Athens and almost everyone will have some preconceived ideas about the city. Socrates painted a picture with words in the fourth century b.c., Pausanais during the Roman era. In the 20th century, Hollywood added its own slant to the legends, and every school child learns about the gods of the ancient Greek world — of Zeus, Athena, and Apollo.
The most important city in the world during its heyday in the fifth and fourth centuries b.c., the people of Athens were highly sophisticated in their thoughts and actions, their tastes and fashions. This small city set on and around a dramatic hill of rock — the Acropolis — became the cradle of western civilization. From the public meetings held here the concepts of citizenship, democracy, and debate developed. Through their regard`
this time I typed `less -s Athens-History.txt` to merge all the non-consecutive blank line into 1 blank.