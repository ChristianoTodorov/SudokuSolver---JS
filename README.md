# SudokuSolver---JS
Řešitel libovolně zadaného sudoku

*How to use - Czech version*

1. K zadání sudoku si uživatel po spuštění vybere číslo, které rozklikne a poté ho zadá do libovolné pozice.
Pro vymazání čísla se používá tlačítko "Undo". Tlačítko se zmáčkne a poté si uživatel zvolí číslo, které chce vymazat.

2. Po zadání čísel stačí zmáčknout červené tlačítko "solve" ke správnému vyplnění sudoku. 
Pokud sudoku není zadáno správně, tak to stránka uživateli ohlásí a opakující se čísla se zvýrazní.


*How to use - English version*

1. To assign a sudoku puzzle, the user has to choose a number and select it by clicking on it. Then the user chooses a position for this number by clicking on any position.
If the user wants to delete a number, he has to click the button "Undo", then he can click on the number he chooses to delete.

2. When the sudoku has been assigned, the algorithm will complete it after the user clicks the button named "Solve".
In case the sudoku assigned is incorrect, the site will notify the user and the repeating numbers will be highlighted.


Jedná se o heuristický algoritmus pro vyřešení libovolně zadaného sudoku.
Po spuštění se začnou na volné pozice vyplňovat čísla od 1 do 9, která se neopakují ve sloupci, řádku a ani čtverci - tudíž čísla, která by potencionálně mohla být správná.
Poté dojde k situaci, kde není možné vyplnit žádné číslo do volné pozice. 
V takové situaci jsme v tzv. "deadendu", to znamená, že některé číslo není na správné pozici. 
Algoritmus se vrátí o jednu pozici zpět a toto číslo vymění za další potencionálně správné číslo, které je větší než to předchozí. 
Pokud už není možné zapsat žádné číslo na této pozici, protože byla všechna vyzkoušena, ale "deadend" pozice je stále nevyplněna, tak se algooritmus vrátí o další pozici zpět dokud nenajde pozici, kde bylo zapsané číslo špatně zapsané.
Poté se algoritmus posune přes tuto "deadend" pozici a algoritmus pokračuje stejným cyklem dokud nezaplní všechny volné pozice čísly.
