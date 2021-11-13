# Nordea-homebank
Nordea to Homebank CVS converter

Converts exported CVS files from Nordea Bank (beta), into Homebank format.

[Homebank](http://homebank.free.fr) is a open source account manager.

## Requirements

  Perl :)
  
## Perl dependencies

Switch

## Usage:

```
  $ nordea-homebank <exported_file.csv> > homebank.csv
```

## Categories
You can edit the categories hash in the script, to suit your own needs.  The script
will then try to match keywords you enter, to the description field in the cvs, and
auto select the category.  Just look at your exported file, and fill in as needed. 
This saves you a lot of time manually inputting categories.  Make sure they exist
in homebank before importing. 

```
%categories = 
   (  "Expenses:Dining"  => qw[ cafe restaurant mcdonalds egon burger ],
      "Bills:Electric"   => qw{ electric hafslund fortum energi ],
      "Mycategory:Subcat => qw{ keyword, keyword, name, whatever, } 
   );

```

## Tags

Tags are left blank.
