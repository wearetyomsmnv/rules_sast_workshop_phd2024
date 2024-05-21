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
metavariable-analysis:
	analyzer: entropy
	metavariable: $VALUE
languages: [yaml]
message: ”Found vuln for yaml-files”
severity: WARNING
