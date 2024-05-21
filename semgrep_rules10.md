rules:
id: generic-entropy-assignment
patterns: 
pattern-either: 
	- patterns: $A=“$B”
	- patterns: $A=$B
metavariable-analysis:
	analyzer: entropy
	metavariable: $B
languages: [generic]
message: ”Found a high-entropy assignment to $A”
severity: ERROR
