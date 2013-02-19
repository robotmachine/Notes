# Ledger Reference
#
# Reconciled Balance:
ledger -C bal
#
# Per month:
ledger -b sep bal  # Start in September
ledger -e sep bal  # End in September
ledger -b sep -e oct bal  # Only show September (Begin: Sep, End: Oct)
#
# Percentage:
ledger -% bal
