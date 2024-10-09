# Overvågning af diskplads

For at teste scriptet i opgave 5 kan du oprette store filer for at fylde diskplads. Du kan bruge PowerShell-kommandoen nedenfor til at oprette en stor dummy-fil:

fsutil file createnew C:\dummy_data\largefile.txt 1000000000

Dette vil oprette en fil på 1 GB. Du kan tilpasse filstørrelsen ved at ændre tallet til det ønskede antal bytes.