# scansion
A beginner friendly python script to scan one or more lines using prosodic.py 

Step-by-step instructions in the form of a python notebook to help new users of prosodic.py

  *  you can modify the metrical constraints for scansion
  *  input one or multiple lines as string
  *  scan from a text file
  *  output results as a dataframe or using prosodic's built in display format
  *  edit the data frame to include only relevant colums

For full documentation and source code, check out https://github.com/quadrismegistus/prosodic

For a web-based version of prosodic.py, check out https://prosodic.dev/

---

Default metrical constraints are for iambic pentameter, emphasizing English poetry's preference for avoiding polysyllabic or "lexical" stress in weak (even) positions. 


constraints={
    'w_peak':3.0,      ## this constraint avoids lexical stress in weak positions
    'w_stress':1.0,
    's_unstress':1.0,
    'unres_across':1.0,
    'unres_within':1.0,
    'pentameter':20.0,    ## set this to zero if you aren't forcing pentameter scansions
}
meter = prosodic.Meter(
    constraints=constraints,
    resolve_optionality=True,
    max_s=1,
    max_w=2,
)
