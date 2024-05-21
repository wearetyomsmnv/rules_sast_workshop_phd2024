rules:
id: secrets-in-config-file
patterns: 
	- pattern: |
	$KEY:$VALUE
	- pattern-inside: |
	data: …
	- pattern-inside: |
	kind: Secret
	…
metavariable-regex:
	metavariable: $VALUE
	regex: (?i)^[aA-zZ0-9+/]+={0,2}$
metavariable-analysis:
	analyzer: entropy
	metavariable: $VALUE
languages: [yaml]
message: ”Found vuln for yaml-files”
severity: WARNING