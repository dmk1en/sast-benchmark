#Added per-entry:
- vulnerabilities[] → my_verdict, my_explain
- false_positives[] → my_verdict, my_notes

#Tool result stats
##Vulnerabilities bucket (tool says "real", n=53):
┌────────────────┬───────┐
│   My verdict   │ Count │
├────────────────┼───────┤
│ TRUE POSITIVE  │ 40    │
├────────────────┼───────┤
│ FALSE POSITIVE │ 9     │
├────────────────┼───────┤
│ MIXED          │ 4     │
└────────────────┴───────┘

##False-positives bucket (tool says "dismiss", n=38):
┌─────────────────────────────┬───────┐
│         My verdict          │ Count │
├─────────────────────────────┼───────┤
│ FALSE POSITIVE (tool right) │ 24    │
├─────────────────────────────┼───────┤
│ TRUE POSITIVE (tool missed) │ 11    │
├─────────────────────────────┼───────┤
│ MIXED                       │ 3     │
└─────────────────────────────┴───────┘

##Confusion matrix (mixed excluded, n=84)
┌────────────────┬───────────────┬──────────────┐
│                │ Actually vuln │ Actually not │
├────────────────┼───────────────┼──────────────┤
│ Tool flagged   │ TP = 40       │ FP = 9       │
├────────────────┼───────────────┼──────────────┤
│ Tool dismissed │ FN = 11       │ TN = 24      │
└────────────────┴───────────────┴──────────────┘

##Metrics
- Precision = 40/49 = 81.6%
- Recall = 40/51 = 78.4% (was 80.0% — flip added 1 FN)
- F1 = 80.0%
- Accuracy = 64/84 = 76.2%
- Mixed = 7 (excluded)
