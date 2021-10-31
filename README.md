# Nordea-homebank
Nordea to Homebank CVS converter

Converts exported CVS files from Nordea Bank, into Homebank format.

[Homebank](http://homebank.free.fr)

Requirements

  Perl :)

Usage:

```
  $ nordea-homebank.pl <exported_file.csv> > homebank.csv
```

You can edit the categories hash in the script, to suit your own needs.  The script
will then try to match keywords you enter, to the description field in the cvs, and
auto select the category.  Just look at your exported file, and fill in as needed. 
This saves you a lot of time manually inputting categories.

```
%categories = (  "Expenses:Dining"  => qw[ cafe restaurant mcdonalds egon burger ],
                 "Bills:Electric"   => qw{ electric hafslund fortum energi ],
                 "Mycategory:Subcat => qw{ keyword, keyword, name, whatever, } );

```

