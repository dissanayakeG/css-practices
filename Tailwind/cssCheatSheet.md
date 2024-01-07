GRID
====
display: grid;
grid-template-columns: auto auto; // 2 columns in raw
gap: 20px; //gap around an item
grid:  100px 100px / auto auto auto auto; //2 rows with 100px size + 4 columns with auto size. 
                                          //This will override grid-template-columns if defined
                                          
grid-area: 1 / 1 / span 2 / span 3;  // Row Start / Column Start / Row Span / Column Span : this should apply for specific item in a grid


