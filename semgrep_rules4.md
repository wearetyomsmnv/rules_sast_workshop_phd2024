rules:
id: eval-use
patterns: 
	pattern: eval(…);
	pattern-not: eval(‘…’);
	pattern-not: eval(f””)
languages: [php]
message: ”Eval detected”
severity: ERROR
