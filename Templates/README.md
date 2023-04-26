# Generate the .md from your .odt
first: go to the proper folder  
cd /Pandoc/Templates/odt_2_pdf/Results  
pandoc --extract-media ./MyMediaFolder ../data/Example.odt -o Example.md  

# Generate the pdf 
pandoc --pdf-engine=xelatex Example.md -o Example.pdf

install cite proc  apt get install pandoc-citeproc

# Adding references

copy your .md and add your reference for example "@Alex2023Approach"  
cp Example.md Example1.md  
vi Example1.md  

pandoc --pdf-engine=xelatex --bibliography ../../Somereferences.bib Example1.md -o Example_with_references.pdf  

if you edit your "Example1.md" adding a "# Somereferences" they will be listed

