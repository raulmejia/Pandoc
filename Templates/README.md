# Generate the .md from your .odt
first: go to the proper folder
cd /Pandoc/Templates/odt_2_pdf/Results
pandoc --extract-media ./MyMediaFolder ../data/Example.odt -o Example.md

# Generate the pdf 
pandoc --pdf-engine=xelatex Example.md -o Example.pdf
