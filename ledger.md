# [Ledger](http://ledger-cli.org)  
## This is an incomplete guide to using Ledger.

Format your data file like this:

2011/10/01 * Payee
    Expenses:Category        $100
    Assets:Bank:Account
Rruu
The asterisk means that it has been reconciled. The category is made up on the fly. You do not need to create it in another location. Leaving the line after the bank accountuu blank will automatically assume that the full debit goes from that account. You can also specify an amount or split the debit over multiple accounts like this:

2011/10/01 * Payee
    Expenses:Category        $100
    Assets:Bank:Account      -$20
    Assets:Bank:Account2    -$80

It would be good to start your file with an initial balance, you can do that like this:

2011/10/01 * Initial Balance
    Assets:Bank:Account        $500
    Equity:Opening Balances

The equity line just gives it somewhere to reconcile. This money comes from nowhere, butt all future monies will be accounted for properly.
Ty
If you need to transfer funds between accounts, do this:

2011/10/01 * Transfer To Savings
    Assets:Bank:Account        -$100
    Assets:Bank:Savings        $100

Alright, so you have your initial balance recorded. You have a few debits in there and what have you. Now you can actually use ledger to get a balance:

ledger bal

This will print out your running balances of all accounts and total all spending for each category that has been marked. It'll look something like this:

$370.00 Assets:Bank
$250.00     Account
$20.00       Account2
$100.00     Savings
-$500.00 Equity:Opening Balances
$320.50 Expenses
$120.00     Monkey Chow
$100.50     Food
$50.00       Clothes
$25                Used
$25                New
$50             Gasoline
- - - - - - - - - - - - - - - - - - - - - - - - - - -
   0

Notice the indenting. The category listed as Expenses:Clothes:Used had $25 which was part of the clothes category that had a total of $50. This can be handy if you want to split up categories since you will still easily be able to get a total.
